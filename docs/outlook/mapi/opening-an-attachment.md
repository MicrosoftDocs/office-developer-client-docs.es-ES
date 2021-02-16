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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430626"
---
# <a name="opening-an-attachment"></a>Abrir datos adjuntos

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La apertura de datos adjuntos implica mostrar sus datos. Por ejemplo, cuando se abre un archivo adjunto, se muestra el contenido del archivo. Mientras que los mensajes y carpetas se abren con sus identificadores de entrada, los datos adjuntos se abren con sus números de datos **adjuntos, PR_ATTACH_NUM** propiedades. Para obtener más información, **vea PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)). Los números de datos adjuntos están disponibles a través de la tabla de datos adjuntos de un mensaje.
  
### <a name="to-open-all-attachments-in-a-message"></a>Para abrir todos los datos adjuntos de un mensaje
  
1. Llame al método [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) del mensaje para obtener acceso a su tabla de datos adjuntos. 
    
2. Llame [a HrQueryAllRows](hrqueryallrows.md) para recuperar todas las filas de la tabla. 
    
3. Para cada fila: 
    
    1. Abra los datos adjuntos pasando el número de datos adjuntos representado en **la columna PR_ATTACH_NUM** en una llamada al método **IMessage::OpenAttach del** mensaje. Para obtener más información, [vea IMessage::OpenAttach](imessage-openattach.md). **OpenAttach devuelve** un puntero a una **implementación de IAttach** que proporciona acceso a las propiedades de datos adjuntos. 
        
    2. Llame al método **IMAPIProp::GetProps** de los datos adjuntos para recuperar **su PR_ATTACH_METHOD** datos adjuntos. Para obtener más información, [vea IMAPIProp::GetProps](imapiprop-getprops.md) **y PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
        
    3. Si **PR_ATTACH_METHOD** se establece en ATTACH_BY_REF_ONLY, llame a **IMAPIProp::GetProps** para recuperar la **PR_ATTACH_PATHNAME** propiedad. Para obtener más información, **vea PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).
        
    4. Si **PR \_ ATTACH_METHOD** está establecido en ATTACH BY_VALUE, llame a \_ **IMAPIProp::OpenProperty** para abrir la propiedad **PR \_ ATTACH_DATA_BIN** con la **interfaz IStream.** Vea el código de ejemplo que sigue a este procedimiento. Para obtener más información, [vea IMAPIProp::OpenProperty](imapiprop-openproperty.md) **y PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).
        
    5. Si **PR_ATTACH_METHOD** se establece en ATTACH_OLE datos adjuntos es un objeto OLE 2: 
        
        1. Llame **a IMAPIProp::OpenProperty** para abrir la propiedad **PR \_ ATTACH_DATA_OBJ** con la **interfaz IStreamDocfile.** Intenta usar esta interfaz porque es una implementación de **IStream** que garantiza que funcione con almacenamiento estructurado con la menor cantidad de sobrecarga. Para obtener más información, **vea PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).
            
        2. Si se produce un error en la llamada de **OpenProperty,** llámela de nuevo para recuperar **PR_ATTACH_DATA_BIN** propiedad con la **interfaz IStreamDocfile.** 
            
        3. Si se produce un error en esta segunda llamada de **OpenProperty,** vuelva a llamar **a OpenProperty** para recuperar **PR_ATTACH_DATA_OBJ**. Sin embargo, en lugar de especificar **IStreamDocfile**, especifique la **interfaz IStorage.** 
    
4. Si **PR_ATTACH_METHOD** se establece en ATTACH_EMBEDDED_MSG, no es inusual que el valor de **PR_ATTACH_DATA_OBJ** contenga un error. Esto se debe a que usted y el implementador de tabla no tienen forma de ponerse de acuerdo sobre el tipo de objeto que se va a devolver. Para recuperar un puntero al mensaje adjunto, abra los datos adjuntos con **IMessage::OpenAttach**. A continuación, obtenga acceso a los datos adjuntos llamando a su **método IMAPIProp::OpenProperty.** Para obtener más información, [vea IMessage::OpenAttach](imessage-openattach.md) e [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Puede solicitar que los datos adjuntos se abran en modo de lectura y escritura o de solo lectura. Solo lectura es el modo predeterminado y muchos proveedores de al almacenamiento de mensajes abren todos los datos adjuntos en este modo independientemente de lo que soliciten los clientes. Pase la marca MAPI_BEST_ACCESS para solicitar que el proveedor del almacén de mensajes conceda el máximo nivel de acceso posible y, a continuación, recupere la propiedad **PR_ACCESS_LEVEL** de los datos adjuntos abiertos para determinar el nivel de acceso que se concedió realmente. Para obtener más información, **vea PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
En el ejemplo siguiente se muestra cómo abrir los datos en la propiedad **PR \_ ATTACH_DATA_BIN** datos adjuntos. Asigna punteros a dos secuencias: una para el archivo y otra para los datos adjuntos. La **función OpenStreamOnFile** abre la secuencia de archivos en modo de solo lectura. La llamada al método **IMAPIProp::OpenProperty** de los datos adjuntos abre la secuencia de datos adjuntos en modo de lectura y escritura. Para obtener más información, **vea PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md)e [IMAPIProp::OpenProperty](imapiprop-openproperty.md). A continuación, el código copia desde la secuencia de archivos a la secuencia de datos adjuntos y libera ambas secuencias.
  
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


