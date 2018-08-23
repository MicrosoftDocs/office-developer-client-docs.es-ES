---
title: Enviar mensajes a través del procesamiento de datos adjuntos personalizado TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 0c7cdf754b2a4b38516b1ac06074fdba9d2227f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577747"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a>Enviar mensajes a través del procesamiento de datos adjuntos personalizado TNEF

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para personalizar el procesamiento de datos adjuntos al enviar un mensaje:
  
1. Obtener un objeto TNEF pasando una interfaz **IStream** y un mensaje en la función [OpenTnefStreamEx](opentnefstreamex.md) . 
    
2. Para obtener una lista de todas las propiedades definidas para el mensaje llamando al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
    
3. Utilizar los métodos [IMAPIProp](imapipropiunknown.md) para excluir todas las propiedades compatibles con el sistema de mensajería. En un momento adecuado escribir esas propiedades en el sistema de mensajería en el formato requerido por el sistema de mensajería. 
    
4. Llame al método [ITnef::AddProps](itnef-addprops.md) para agregar sólo las propiedades en el mensaje, es decir, ninguna de las propiedades en los datos adjuntos: estableciendo el indicador TNEF_PROP_MESSAGE_ONLY. 
    
5. Llame al método [ITnef::AddProps](itnef-addprops.md) con estos elementos: la marca TNEF_PROP_EXCLUDE, una matriz de etiqueta de propiedad que contiene el **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) o **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) propiedad y un identificador de datos adjuntos que especifica los datos adjuntos que va a procesar.
    
6. Use el método [ITnef::SetProps](itnef-setprops.md) para agregar la etiqueta de propiedad de **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) con una cadena única que identifica el sistema de mensajería de los datos adjuntos, si los datos adjuntos tienen un nombre de archivo que el no se admite el sistema de mensajería. Por ejemplo, varios datos adjuntos con el mismo nombre de archivo original, o un nombre de archivo que no es un nombre de archivo válido para el sistema de mensajería. Esta cadena se utilizará junto con un número clave al escribir las etiquetas de datos adjuntos en el texto del mensaje con etiqueta para asociar un archivo adjunto a sus datos. Para obtener más información, vea [TNEF-Tagged texto del mensaje](tnef-tagged-message-text.md).
    
7. Repita las llamadas **AddProps** y **SetProps** por cada dato adjunto. 
    
8. Llame al método [ITnef::Finish](itnef-finish.md) para codificar el mensaje en la secuencia TNEF después de que se agregan todas las propiedades solicitadas. 
    
9. Obtener el texto del mensaje con etiqueta llamando al método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) . Este texto etiquetado es de lectura con los métodos de la interfaz **IStream** , codifican mediante el modelo de datos adjuntos del sistema de mensajería y se escriben en el sistema de mensajería. 
    
10. Llame al método [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberar el objeto [ITnef](itnefiunknown.md) . 
    
11. Escribir los datos adjuntos restante para el sistema de mensajería a través del modelo de datos adjuntos del sistema de mensajería.
    
El proveedor de transporte debe utilizar el procedimiento descrito anteriormente para los datos adjuntos de proceso. Si eso no es posible, el proveedor de transporte debe usar los siguientes pasos para el procesamiento de datos adjuntos personalizado:
  
1. El proveedor de transporte se asegura de que las propiedades **PR_ATTACH_TRANSPORT_NAME** de todos los datos adjuntos contienen valores únicos que son identificadores de conexión válida para el sistema de mensajería. 
    
2. El proveedor de transporte, a continuación, usa una sola llamada a **ITnef::AddProps** por cada dato adjunto, pasando el indicador TNEF_PROP_CONTAINED. 
    

