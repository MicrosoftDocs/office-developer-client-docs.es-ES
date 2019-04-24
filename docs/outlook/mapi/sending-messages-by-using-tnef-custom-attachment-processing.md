---
title: Enviar mensajes mediante el procesamiento de datos adJuntos personalizado TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: f9d154b26319f5ed72b1abd6aeef307d07a63bda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339700"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a>Enviar mensajes mediante el procesamiento de datos adJuntos personalizado TNEF

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para personalizar el procesamiento de datos adjuntos al enviar un mensaje:
  
1. Obtenga un objeto TNEF pasando una interfaz **IStream** y un mensaje a la función [OpenTnefStreamEx](opentnefstreamex.md) . 
    
2. Obtenga una lista de todas las propiedades definidas para el mensaje llamando al método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) . 
    
3. Use los métodos [IMAPIProp](imapipropiunknown.md) para excluir todas las propiedades admitidas por el sistema de mensajería. En el momento adecuado, escriba esas propiedades en el sistema de mensajería en el formato que requiera el sistema de mensajería. 
    
4. Llame al método [ITnef:: AddProps](itnef-addprops.md) para agregar solo las propiedades del mensaje (es decir, ninguna de las propiedades de los datos adjuntos) estableciendo la marca TNEF_PROP_MESSAGE_ONLY. 
    
5. Llamar a [ITnef:: AddProps](itnef-addprops.md) con estos elementos: el indicador TNEF_PROP_EXCLUDE, una matriz de etiquetas de propiedad que contiene los **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) o **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) y un identificador de datos adjuntos que especifica los datos adjuntos que se van a procesar.
    
6. Use el método [ITnef:: SetProps](itnef-setprops.md) para agregar la etiqueta de propiedad **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) con una cadena única que identifica los datos adjuntos al sistema de mensajería si los datos adjuntos tienen un nombre de archivo que el no es compatible con el sistema de mensajería. Por ejemplo, varios datos adjuntos con el mismo nombre de archivo original o un nombre de archivo que no es un nombre de archivo válido para el sistema de mensajería. Esta cadena se utilizará con un número de clave al escribir las etiquetas de datos adjuntos en el texto del mensaje etiquetado para asociar datos adjuntos a sus datos. Para obtener más información, vea [el texto del mensaje con etiqueta TNEF](tnef-tagged-message-text.md).
    
7. Repita las llamadas **AddProps** y **SetProps** para cada dato adjunto. 
    
8. Llame al método [ITnef:: Finish](itnef-finish.md) para codificar el mensaje en la secuencia TNEF después de que se hayan agregado todas las propiedades solicitadas. 
    
9. Para obtener el texto del mensaje etiquetado, llame al método [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) . Este texto etiquetado se lee usando métodos de la interfaz **IStream** , codificados con el modelo de datos adjuntos del sistema de mensajería y se escribe en el sistema de mensajería. 
    
10. Llame al método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberar el objeto [ITnef](itnefiunknown.md) . 
    
11. Escriba los datos adjuntos restantes en el sistema de mensajería a través del modelo de datos adjuntos del sistema de mensajería.
    
El proveedor de transporte debe usar el procedimiento descrito anteriormente para procesar los datos adjuntos. Si esto no es posible, el proveedor de transporte debe seguir estos pasos para el procesamiento de datos adjuntos personalizados:
  
1. El proveedor de transporte garantiza que las propiedades **PR_ATTACH_TRANSPORT_NAME** de todos los datos adjuntos contengan valores únicos que son identificadores de datos adjuntos válidos para el sistema de mensajería. 
    
2. A continuación, el proveedor de transporte usa una sola llamada a **ITnef:: AddProps** para cada dato adjunto, pasando la marca TNEF_PROP_CONTAINED. 
    

