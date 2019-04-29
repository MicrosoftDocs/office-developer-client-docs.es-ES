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
  
Los datos adjuntos de un mensaje son datos adicionales, como un archivo, otro mensaje o un objeto OLE, que puede enviar o guardar junto con un mensaje. Cada archivo adjunto tiene una colección de propiedades que lo identifican y describen su tipo y cómo se representa. Al igual que los destinatarios, solo se puede tener acceso a los datos adjuntos de los mensajes a través del mensaje al que pertenecen. Por lo tanto, para que los datos adjuntos se puedan usar, el mensaje debe estar abierto.
  
## <a name="create-a-message-attachment"></a>Crear un dato adjunto de mensaje
  
1. Llame al método [IMessage:: CreateAttach](imessage-createattach.md) del mensaje y pase NULL como identificador de la interfaz. **CreateAttach** devuelve un número que identifica de forma única los nuevos datos adjuntos en el mensaje. El número de datos adjuntos se almacena en la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) y solo es válido mientras el mensaje que contiene los datos adjuntos esté abierto.
    
2. Llame a [IMAPIProp:: SetProps](imapiprop-setprops.md) para establecer **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) para indicar cómo tener acceso a los datos adjuntos. Se requiere **PR_ATTACH_METHOD** . Establézcalo en: 
    
   - ATTACH_BY_VALUE si los datos adjuntos son datos binarios.
    
   - ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE o ATTACH_BY_REF_ONLY si los datos adjuntos son un archivo.
    
   - ATTACH_EMBEDDED_MSG si los datos adjuntos son un mensaje.
    
   - ATTACH_OLE si los datos adjuntos son un objeto OLE.
    
3. Establezca la propiedad de datos adjuntos adecuada:
    
   - **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) para datos binarios y objetos OLE 1.
    
   - **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) para los archivos.
    
   - **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) para mensajes y objetos OLE 2.
    
4. Establezca **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) para que contenga la representación gráfica de los datos adjuntos de archivos o datos adjuntos binarios. No la establezca para objetos OLE, que almacenan la información de representación de forma interna o para mensajes adjuntos. 
    
5. Establezca **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) para indicar dónde se deben mostrar los datos adjuntos. **PR_RENDERING_POSITION** solo se aplica a los clientes que establecen la propiedad **PR_BODY** . Si solo admite **PR_RTF_COMPRESSED**, incluya la siguiente información de marcador de posición en la secuencia comprimida:
    
   `\objattph`

   Para establecer **PR_RENDERING_POSITION**, asigne un número que represente un desplazamiento ordinal en caracteres, donde el primer carácter de **PR_BODY** sea 0, si necesita saber en qué lugar del mensaje se representa el archivo adjunto, o 0xFFFFFFFF, si no lo hace representar datos adjuntos dentro de **PR_BODY**.
    
6. Establecer **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) para indicar el nombre corto del archivo para un archivo adjunto y **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) para indicar el nombre del archivo como compatible en una plataforma que controla el formato de nombre de archivo largo. Ambas propiedades son opcionales. Sin embargo, si establece **PR_ATTACH_LONG_FILENAME**, también establece **PR_ATTACH_FILENAME**. 
    
7. Establezca **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) para indicar el nombre de los datos adjuntos que pueden aparecer en un cuadro de diálogo. PR_DISPLAY_NAME es opcional. 
    
## <a name="set-prattachdatabin"></a>Establecer PR_ATTACH_DATA_BIN
  
1. Llame a [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para abrir la propiedad con la interfaz **IStream** . 
    
2. Si un archivo contiene los datos y está abierto o si necesita controlar explícitamente el tamaño del búfer, llame a **IStream:: Write** en un bucle para ubicar los datos en la secuencia. 
    
3. Otra opción es llamar a **OpenStreamOnFile** para crear una secuencia para obtener acceso al archivo de datos y, a continuación, llamar al método **IStream:: CopyTo** de la secuencia para copiar los datos en la secuencia devuelta por **OpenProperty**.
    
4. Llamar al método **IStream:: commit** de la nueva secuencia. 
    
## <a name="set-prattachdataobj"></a>Establecer PR_ATTACH_DATA_OBJ
  
1. Llame a **IMAPIProp:: OpenProperty** para abrir la propiedad con la interfaz **IStreamDocfile** para crear una secuencia que funcione con el almacenamiento estructurado. **IStreamDocfile** está implementado por los proveedores de almacenamiento de mensajes para proporcionar a los clientes una forma de mayor rendimiento para almacenar y recuperar almacenamiento estructurado. La interfaz **IStreamDocfile** es la misma que **IStream**, pero se garantiza que el contenido de la secuencia tiene el formato de almacenamiento estructurado. Si la llamada se realiza correctamente, cree la secuencia con los mismos pasos detallados para la configuración **PR_ATTACH_DATA_BIN**.
    
2. Si **OpenProperty** produce un error: 
    
   1. Vuelva a llamar a **OpenProperty** para obtener el **IStorage**. 
      
   2. Llame a **StgOpenStorage** para abrir el objeto OLE y devolver un objeto de almacenamiento. 
      
   3. Llamar al método **IStorage:: CopyTo** del objeto de almacenamiento devuelto para copiarlo en el objeto de almacenamiento devuelto desde **OpenProperty**.
      
   4. Llamar al método **IStorage:: commit** del nuevo objeto de almacenamiento. 
    
## <a name="set-prattachpathname"></a>Establecer PR_ATTACH_PATHNAME
  
1. Asigne una estructura [SPropValue](spropvalue.md) , configure el miembro **ulPropTag** a **PR_ATTACH_PATHNAME** y el miembro **Value. LPSZ** a la cadena de caracteres que representa el nombre de archivo. 
    
2. Llame al método [IMAPIProp:: SetProps](imapiprop-setprops.md) del archivo adjunto. 
    
> [!NOTE]
> Si la plataforma admite nombres de archivo largos, establezca tanto **PR_ATTACH_PATHNAME** como **PR_ATTACH_LONG_PATHNAME**. Puede que sea necesario realizar una llamada de sistema operativo para recuperar el nombre corto del archivo. 
  
## <a name="see-also"></a>Ver también

- [Datos adJuntos MAPI](mapi-attachments.md)

