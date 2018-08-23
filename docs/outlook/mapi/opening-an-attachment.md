---
title: Abrir un archivo adjunto
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 768528c59d7aa5888c0d0427f86b8be8e1d33669
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579980"
---
# <a name="opening-an-attachment"></a>Abrir un archivo adjunto

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abrir un archivo adjunto implica la visualización de sus datos. Por ejemplo, cuando se abre un archivo adjunto, se muestra el contenido del archivo. Mientras que los mensajes y las carpetas se abren con sus identificadores de entrada, los datos adjuntos se abren utilizando sus números de datos adjuntos: propiedades **PR_ATTACH_NUM** . Para obtener más información, vea **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)). Los números de los datos adjuntos están disponibles a través de la tabla de datos adjuntos de un mensaje.
  
### <a name="to-open-all-attachments-in-a-message"></a>Para abrir todos los datos adjuntos en un mensaje
  
1. Llamar al método [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) del mensaje para obtener acceso a su tabla de datos adjuntos. 
    
2. Llame a [HrQueryAllRows](hrqueryallrows.md) para recuperar todas las filas de la tabla. 
    
3. Para cada fila: 
    
    1. Abra los datos adjuntos, pase el número de datos adjuntos que se representan en la columna **PR_ATTACH_NUM** en una llamada al método **IMessage::OpenAttach** del mensaje. Para obtener más información, vea [IMessage::OpenAttach](imessage-openattach.md). **OpenAttach** devuelve un puntero a una implementación de **IAttach** que proporciona acceso a las propiedades de los datos adjuntos. 
        
    2. Llamar al método **IMAPIProp::GetProps** de los datos adjuntos para recuperar su propiedad **PR_ATTACH_METHOD** . Para obtener más información, vea [IMAPIProp::GetProps](imapiprop-getprops.md) y **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
        
    3. Si se establece **PR_ATTACH_METHOD** en ATTACH_BY_REF_ONLY, llame a **IMAPIProp::GetProps** para recuperar la propiedad **PR_ATTACH_PATHNAME** . Para obtener más información, vea **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).
        
    4. Si **PR\_ATTACH_METHOD** está establecida en ATTACH\_BY_VALUE, llame a **IMAPIProp::OpenProperty** para abrir el **PR\_ATTACH_DATA_BIN** (propiedad) con la interfaz **IStream** . Vea el código de ejemplo, siga este procedimiento. Para obtener más información, vea [IMAPIProp::OpenProperty](imapiprop-openproperty.md) y **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).
        
    5. Si se establece **PR_ATTACH_METHOD** en ATTACH_OLE y los datos adjuntos es un objeto OLE 2: 
        
        1. Llame a **IMAPIProp::OpenProperty** para abrir el **PR\_ATTACH_DATA_OBJ** (propiedad) con la interfaz **IStreamDocfile** . Intenta utilizar esta interfaz porque es una implementación de **IStream** garantizada que funcionen con almacenamiento estructurado con la menor cantidad de sobrecarga. Para obtener más información, vea **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).
            
        2. Si se produce un error en la llamada **OpenProperty** , llame al nuevo para recuperar la propiedad **PR_ATTACH_DATA_BIN** con la interfaz **IStreamDocfile** . 
            
        3. Si se produce un error en esta segunda llamada **OpenProperty** , vuelva a intentar llamar **OpenProperty** para recuperar **PR_ATTACH_DATA_OBJ**. Sin embargo, en lugar de especificar **IStreamDocfile**, especificar la interfaz **IStorage** . 
    
4. Si se establece **PR_ATTACH_METHOD** en ATTACH_EMBEDDED_MSG, no es extraño que el valor de **PR_ATTACH_DATA_OBJ** para que contenga un error. Esto es debido a que usted y el implementador de la tabla no tienen forma está de acuerdo en el tipo de objeto que se va a devolver. Para recuperar un puntero al mensaje adjunto, abra los datos adjuntos con **IMessage::OpenAttach**. A continuación, tener acceso a los datos adjuntos mediante una llamada a su método **IMAPIProp::OpenProperty** . Para obtener más información, vea [IMessage::OpenAttach](imessage-openattach.md) y [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Puede solicitar que los datos adjuntos se abren en modo de sólo lectura o de lectura y escritura. Sólo lectura es el modo predeterminado y muchos de los proveedores de almacén de mensajes abrir todos los datos adjuntos en este modo, independientemente de los clientes que solicitan. Pase el indicador MAPI_BEST_ACCESS para solicitar que el proveedor de almacenamiento de mensaje conceder el mayor nivel de acceso puede y, a continuación, recuperar la propiedad **PR_ACCESS_LEVEL** de los datos adjuntos abiertos para determinar el nivel de acceso que realmente se ha concedido. Para obtener más información, vea **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
En el ejemplo siguiente se muestra cómo abrir los datos en un documento adjunto **PR\_ATTACH_DATA_BIN** (propiedad). Asigna punteros a dos secuencias: uno para el archivo y otro para los datos adjuntos. La función **OpenStreamOnFile** abre la secuencia de archivo en modo de sólo lectura. La llamada al método de **IMAPIProp::OpenProperty** de los datos adjuntos, abre la secuencia de datos adjuntos en el modo de lectura y escritura. Para obtener más información, vea **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md)y [IMAPIProp::OpenProperty](imapiprop-openproperty.md). El código, a continuación, copia de la secuencia de archivo en la secuencia de datos adjuntos y libera ambas secuencias.
  
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


