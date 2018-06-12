---
title: Creación de datos adjuntos del mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: eef42a8c7d19af313316bea68624ac67fb1ab4e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816620"
---
# <a name="creating-a-message-attachment"></a>Creación de datos adjuntos del mensaje
  
**Se aplica a**: Outlook 
  
Datos adjuntos del mensaje son algunos datos adicionales, como un archivo, otro mensaje o un objeto OLE, que se puede enviar o guardar junto con un mensaje. Cada dato adjunto tiene una colección de propiedades que lo identifica y describe su tipo y cómo se presenta. Al igual que los destinatarios, datos adjuntos de mensajes sólo pueden tener acceso a través del mensaje al que pertenecen. Por lo tanto, para que los datos adjuntos que se pueda usar, su mensaje debe estar abierto.
  
## <a name="create-a-message-attachment"></a>Crear datos adjuntos del mensaje
  
1. Llamar al método [IMessage::CreateAttach](imessage-createattach.md) del mensaje y pase NULL como el identificador de interfaz. **CreateAttach** devuelve un número que identifica de forma exclusiva el nuevo dato adjunto dentro del mensaje. El número de datos adjuntos se almacena en la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) y es válido sólo mientras está abierto el mensaje que contiene los datos adjuntos.
    
2. Llame a [IMAPIProp::SetProps](imapiprop-setprops.md) para establecer **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) para indicar cómo tener acceso a los datos adjuntos. Se requiere **PR_ATTACH_METHOD** . Establézcala en: 
    
   - ATTACH_BY_VALUE si los datos adjuntos son datos binarios.
    
   - ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE o ATTACH_BY_REF_ONLY si los datos adjuntos están un archivo.
    
   - ATTACH_EMBEDDED_MSG si los datos adjuntos son un mensaje.
    
   - ATTACH_OLE si los datos adjuntos están un objeto OLE.
    
3. Establezca la propiedad de datos datos adjuntos adecuado:
    
   - **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) para los datos binarios y objetos OLE 1.
    
   - **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) para los archivos.
    
   - **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) para los mensajes y objetos OLE 2.
    
4. Establecer **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) para contener la representación gráfica de los datos adjuntos de archivo o datos adjuntos binarios. No se establece para los objetos OLE, que almacenan la información de representación internamente, o para mensajes adjuntos. 
    
5. Establecer **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) para indicar dónde se deben mostrar los datos adjuntos. **PR_RENDERING_POSITION** se aplica sólo a los clientes que establezca la propiedad **PR_BODY** . Si solo admite **PR_RTF_COMPRESSED**, coloque la siguiente información de marcador de posición en la secuencia comprimida:
    
   `\objattph`

   Para establecer **PR_RENDERING_POSITION**, asigne a un número que representa un desplazamiento ordinal en caracteres, con el primer carácter de **PR_BODY** que se va a 0, si necesita saber dónde en el mensaje se procesa los datos adjuntos o 0xFFFFFFFF, si no lo hace representar datos adjuntos dentro de **PR_BODY**.
    
6. Establecer **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) para indicar el nombre corto del archivo para un archivo adjunto y **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) para indicar el nombre del archivo como compatibles en una plataforma que controla el formato de nombre de archivo largo. Ambas propiedades son opcionales. Sin embargo, si se establece **PR_ATTACH_LONG_FILENAME**, también establece **PR_ATTACH_FILENAME**. 
    
7. Establecer **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) para indicar el nombre de los datos adjuntos que pueden aparecer en un cuadro de diálogo. PR_DISPLAY_NAME es opcional. 
    
## <a name="set-prattachdatabin"></a>Establecer PR_ATTACH_DATA_BIN
  
1. Llame a [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir la propiedad con la interfaz **IStream** . 
    
2. Si un archivo contiene los datos y está abierto o si necesita control explícito con respecto al tamaño del búfer, llame a **IStream::Write** en un bucle para colocar los datos en la secuencia. 
    
3. Otra opción consiste en llamar a **OpenStreamOnFile** para crear una secuencia para tener acceso al archivo de datos y, a continuación, llame al método esta secuencia **IStream:: CopyTo** para copiar los datos en la secuencia devuelta por **OpenProperty**.
    
4. Llamar al método **IStream:: Commit** de la nueva secuencia. 
    
## <a name="set-prattachdataobj"></a>Establecer PR_ATTACH_DATA_OBJ
  
1. Llame a **IMAPIProp::OpenProperty** para abrir la propiedad con la interfaz **IStreamDocfile** para crear una secuencia que funciona con almacenamiento estructurado. **IStreamDocfile** se implementa mediante los proveedores de almacén de mensajes para ofrecer a los clientes un método de mayor rendimiento para almacenar y recuperar almacenamiento estructurado. La interfaz de **IStreamDocfile** es el mismo que **IStream**, pero se garantiza que el contenido de la secuencia se con formato de almacenamiento estructurado. Si esta llamada se realiza correctamente, cree la secuencia con los mismos pasos que se describen para la configuración de **PR_ATTACH_DATA_BIN**.
    
2. Si se produce un error en **OpenProperty** : 
    
   1. Llamar a **OpenProperty** nuevo que pedía **IStorage**. 
      
   2. Llamar a **StgOpenStorage** para abrir el objeto OLE y devolver un objeto de almacenamiento. 
      
   3. Llamar al método **IStorage** del objeto de almacenamiento devuelto para copiar en el objeto de almacenamiento devuelto desde **OpenProperty**.
      
   4. Llamar al método **IStorage::Commit** del objeto de almacenamiento nuevo. 
    
## <a name="set-prattachpathname"></a>Establecer PR_ATTACH_PATHNAME
  
1. Asignar una estructura [SPropValue](spropvalue.md) , estableciendo el miembro de **ulPropTag** a **PR_ATTACH_PATHNAME** y el miembro **Value.LPSZ** a la cadena de caracteres representa el nombre de archivo. 
    
2. Llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) de los datos adjuntos. 
    
> [!NOTE]
> Si su plataforma admite nombres largos de archivo, establezca **PR_ATTACH_PATHNAME** y **PR_ATTACH_LONG_PATHNAME**. Puede que sea necesario realizar un sistema operativo llamada para recuperar el nombre de archivo corto. 
  
## <a name="see-also"></a>Ver también

- [Datos adjuntos de MAPI](mapi-attachments.md)

