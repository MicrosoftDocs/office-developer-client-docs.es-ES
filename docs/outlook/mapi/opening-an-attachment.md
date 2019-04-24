---
title: Abrir datos adjuntos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 39da1e02622d81cd12a2d4673b827d49bf418128
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326176"
---
# <a name="opening-an-attachment"></a>Abrir datos adjuntos

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La apertura de datos adjuntos implica mostrar sus datos. Por ejemplo, cuando se abre un archivo adjunto, se muestra el contenido del archivo. Mientras que los mensajes y las carpetas se abren mediante sus identificadores de entrada, los datos adjuntos se abren con sus números de datos adjuntos: propiedades de **PR_ATTACH_NUM** . Para obtener más información, vea **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)). Los números de datos adJuntos están disponibles en la tabla de datos adjuntos del mensaje.
  
### <a name="to-open-all-attachments-in-a-message"></a>Para abrir todos los datos adjuntos en un mensaje
  
1. Llame al método [IMessage:: GetAttachmentTable](imessage-getattachmenttable.md) del mensaje para obtener acceso a su tabla de datos adjuntos. 
    
2. Llame a [HrQueryAllRows](hrqueryallrows.md) para recuperar todas las filas de la tabla. 
    
3. Para cada fila: 
    
    1. Abra el archivo adjunto pasando el número de archivo adjunto representado en la columna **PR_ATTACH_NUM** en una llamada al método **IMessage:: OpenAttach** del mensaje. Para obtener más información, vea [IMessage:: OpenAttach](imessage-openattach.md). **OpenAttach** devuelve un puntero a una implementación de **IAttach** que proporciona acceso a las propiedades de datos adjuntos. 
        
    2. Llame al método **IMAPIProp:: GetProps** del adjunto para recuperar su propiedad **PR_ATTACH_METHOD** . Para obtener más información, vea [IMAPIProp:: GetProps](imapiprop-getprops.md) y **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
        
    3. Si **PR_ATTACH_METHOD** se establece en ATTACH_BY_REF_ONLY, llame a **IMAPIProp:: GetProps** para recuperar la propiedad **PR_ATTACH_PATHNAME** . Para obtener más información, vea **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).
        
    4. Si **el\_ATTACH_METHOD de PR** está configurado\_para adjuntar BY_VALUE, llame a **IMAPIProp:: OpenProperty** para abrir la propiedad **\_PR ATTACH_DATA_BIN** con la interfaz **IStream** . Vea el código de ejemplo que sigue a este procedimiento. Para obtener más información, vea [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) y **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).
        
    5. Si **PR_ATTACH_METHOD** se establece en ATTACH_OLE y Attachment es un objeto OLE 2: 
        
        1. Llame a **IMAPIProp:: OpenProperty** para abrir la propiedad **\_PR ATTACH_DATA_OBJ** con la interfaz **IStreamDocfile** . Intente usar esta interfaz porque es una implementación de **IStream** garantizada para trabajar con almacenamiento estructurado con la menor cantidad de sobrecarga. Para obtener más información, vea **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).
            
        2. Si se produce un error en la llamada a **OpenProperty** , llámela de nuevo para recuperar la propiedad **PR_ATTACH_DATA_BIN** con la interfaz **IStreamDocfile** . 
            
        3. Si se produce un error en la segunda llamada a **OpenProperty** , intente llamar de nuevo a **OpenProperty** para recuperar **PR_ATTACH_DATA_OBJ**. Sin embargo, en lugar de especificar **IStreamDocfile**, especifique la interfaz **IStorage** . 
    
4. Si **PR_ATTACH_METHOD** se establece en ATTACH_EMBEDDED_MSG, no es raro que el valor de **PR_ATTACH_DATA_OBJ** contenga un error. Esto se debe a que usted y el implementador de tablas no tienen forma de acordar el tipo de objeto que se va a devolver. Para recuperar un puntero al mensaje adjunto, abra el archivo adjunto con **IMessage:: OpenAttach**. A continuación, obtenga acceso a los datos adjuntos llamando a su método **IMAPIProp:: OpenProperty** . Para obtener más información, vea [IMessage:: OpenAttach](imessage-openattach.md) y [IMAPIProp:: OpenProperty](imapiprop-openproperty.md).
    
Puede solicitar que se abran los datos adjuntos en modo de lectura y escritura o de solo lectura. Read-Only es el modo predeterminado y muchos proveedores de almacenamiento de mensajes abren todos los datos adjuntos en este modo, independientemente de lo que los clientes soliciten. Pase la marca MAPI_BEST_ACCESS para solicitar que el proveedor de almacén de mensajes conceda el máximo nivel de acceso que pueda y, a continuación, recupere la propiedad **PR_ACCESS_LEVEL** de los datos adjuntos para determinar el nivel de acceso que se ha concedido realmente. Para obtener más información, vea **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
En el siguiente ejemplo, se muestra cómo abrir los datos en la **propiedad\_PR ATTACH_DATA_BIN** de datos adjuntos. Asigna punteros a dos secuencias: una para el archivo y otra para los datos adjuntos. La función **OpenStreamOnFile** abre la secuencia de archivo en modo de solo lectura. La llamada al método **IMAPIProp:: OpenProperty** de Attachment abre la secuencia de datos adjuntos en modo de lectura y escritura. Para obtener más información, vea **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md)y [IMAPIProp:: OpenProperty](imapiprop-openproperty.md). A continuación, el código copia desde la secuencia de archivo a la secuencia de datos adjuntos y libera ambas secuencias.
  
```cpp
LPSTREAM pStreamFile, pStreamAtt;
HRESULT hr;
hr = OpenStreamOnFile (MAPIAllocateBuffer, MAPIFreeBuffer,
                       STGM_READ, "myfile.doc", NULL, &pStreamFile);
if (HR_SUCCEEDED(hr))
{
    // Open the destination stream in the attachment object
    hr = pAttach->OpenProperty (PR_ATTACH_DATA_BIN,
                                &IID_IStream,
                                0,
                                MAPI_MODIFY | MAPI_CREATE,
                                (LPUNKNOWN *)&pStreamAtt);
    if (HR_SUCCEEDED(hr))
    {
        STATSTG StatInfo;
        pStreamFile->Stat (&StatInfo, STATFLAG_NONAME);
        hResult = pStreamFile->CopyTo (pStreamAtt, StatInfo.cbSize,
                                       NULL, NULL);
        pStreamAtt->Release();
    }
    pStreamFile->Release();
}
```


