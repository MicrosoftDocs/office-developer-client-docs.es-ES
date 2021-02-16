---
title: Crear un archivo adjunto de mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2bdba3574c962c825f45cd098efa1cba6e21a4ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405999"
---
# <a name="creating-a-message-attachment"></a>Crear un archivo adjunto de mensaje
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los datos adjuntos de un mensaje son algunos datos adicionales, como un archivo, otro mensaje o un objeto OLE, que puede enviar o guardar junto con un mensaje. Cada dato adjunto tiene una colección de propiedades que lo identifica y describe su tipo y cómo se representa. Al igual que los destinatarios, solo se puede tener acceso a los datos adjuntos de los mensajes a través del mensaje al que pertenecen. Por lo tanto, para que se puedan usar datos adjuntos, su mensaje debe estar abierto.
  
## <a name="create-a-message-attachment"></a>Crear datos adjuntos de un mensaje
  
1. Llama al método [IMessage::CreateAttach](imessage-createattach.md) del mensaje y pasa NULL como identificador de interfaz. **CreateAttach devuelve** un número que identifica de forma exclusiva los nuevos datos adjuntos dentro del mensaje. El número de datos adjuntos se almacena en la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) y solo es válido mientras el mensaje que contiene los datos adjuntos esté abierto.
    
2. Llame [a IMAPIProp::SetProps](imapiprop-setprops.md) para establecer **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) para indicar cómo obtener acceso a los datos adjuntos. **PR_ATTACH_METHOD** es necesario. Estacórlo en: 
    
   - ATTACH_BY_VALUE si los datos adjuntos son datos binarios.
    
   - ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE o ATTACH_BY_REF_ONLY si los datos adjuntos son un archivo.
    
   - ATTACH_EMBEDDED_MSG si los datos adjuntos son un mensaje.
    
   - ATTACH_OLE si los datos adjuntos son un objeto OLE.
    
3. Establezca la propiedad de datos adjuntos apropiada:
    
   - **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) para datos binarios y objetos OLE 1.
    
   - **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) para los archivos.
    
   - **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) para mensajes y objetos OLE 2.
    
4. Establezca **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) para contener la representación gráfica de los datos adjuntos de archivos o datos adjuntos binarios. No lo establezca para objetos OLE, que almacenan la información de representación internamente o para mensajes adjuntos. 
    
5. Establezca **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) para indicar dónde deben mostrarse los datos adjuntos. **PR_RENDERING_POSITION** se aplica solo a los clientes que establecen la **PR_BODY** propiedad. Si solo admite la **PR_RTF_COMPRESSED**, coloque la siguiente información de marcador de posición en la secuencia comprimida:
    
   `\objattph`

   Para establecer PR_RENDERING_POSITION **,** asigne un número que represente un desplazamiento ordinal en caracteres, con el primer carácter de **PR_BODY** en 0, si necesita saber dónde se representan los datos adjuntos en el mensaje o 0xFFFFFFFF, si no representa datos adjuntos dentro de **PR_BODY**.
    
6. Establezca **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) para indicar el nombre corto del archivo para un archivo adjunto y **PR \_ ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) para indicar el nombre del archivo tal como se admite en una plataforma que controla el formato de nombre de archivo largo. Ambas propiedades son opcionales. Sin embargo, si establece **PR_ATTACH_LONG_FILENAME**, también establecer **PR_ATTACH_FILENAME**. 
    
7. Establezca **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) para indicar el nombre de los datos adjuntos que pueden aparecer en un cuadro de diálogo. PR_DISPLAY_NAME es opcional. 
    
## <a name="set-pr_attach_data_bin"></a>Establecer PR_ATTACH_DATA_BIN
  
1. Llame [a IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir la propiedad con la **interfaz IStream.** 
    
2. Si un archivo contiene los datos y está abierto o si necesitas un control explícito sobre el tamaño del búfer, llama a **IStream::Write** en un bucle para colocar los datos en la secuencia. 
    
3. Otra opción es llamar a **OpenStreamOnFile** para crear una secuencia para tener acceso al archivo de datos y, a continuación, llamar al método **IStream::CopyTo** de esta secuencia para copiar los datos en la secuencia devuelta por **OpenProperty**.
    
4. Llama al método **IStream::Commit** de la nueva secuencia. 
    
## <a name="set-pr_attach_data_obj"></a>Establecer PR_ATTACH_DATA_OBJ
  
1. Llame **a IMAPIProp::OpenProperty** para abrir la propiedad con la interfaz **IStreamDocfile** para crear una secuencia que funcione con almacenamiento estructurado. Los proveedores de almacén de mensajes implementan **IStreamDocfile** para proporcionar a los clientes una forma de mayor rendimiento de almacenar y recuperar almacenamiento estructurado. La **interfaz IStreamDocfile** es la misma que **IStream,** pero se garantiza que el contenido de la secuencia tenga el formato de almacenamiento estructurado. Si esta llamada se realiza correctamente, cree la secuencia con los mismos pasos descritos para establecer **PR_ATTACH_DATA_BIN**.
    
2. Si **se produce un error en OpenProperty:** 
    
   1. Vuelva **a llamar a OpenProperty** **solicitando IStorage**. 
      
   2. Llame **a StgOpenStorage** para abrir el objeto OLE y devolver un objeto de almacenamiento. 
      
   3. Llame al método **IStorage::CopyTo** del objeto de almacenamiento devuelto para copiar al objeto de almacenamiento devuelto desde **OpenProperty**.
      
   4. Llame al método **IStorage::Commit** del nuevo objeto de almacenamiento. 
    
## <a name="set-pr_attach_pathname"></a>Establecer PR_ATTACH_PATHNAME
  
1. Asigna una [estructura SPropValue,](spropvalue.md) estableciendo el miembro **ulPropTag** en **PR_ATTACH_PATHNAME** y el miembro **Value.LPSZ** en la cadena de caracteres que representa el nombre de archivo. 
    
2. Llame al método [IMAPIProp::SetProps](imapiprop-setprops.md) de los datos adjuntos. 
    
> [!NOTE]
> Si su plataforma admite nombres de archivo largos, establezca **PR_ATTACH_PATHNAME** y **PR_ATTACH_LONG_PATHNAME**. Puede que sea necesario realizar una llamada al sistema operativo para recuperar el nombre de archivo corto. 
  
## <a name="see-also"></a>Consulte también

- [Datos adjuntos mapi](mapi-attachments.md)

