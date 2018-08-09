---
title: Texto del mensaje etiquetado con TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bedfc0457b0de8287a4e7bc8bdf8fb57404e4fa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820870"
---
# <a name="tnef-tagged-message-text"></a>Texto del mensaje etiquetado con TNEF

  
  
**Hace referencia a**: Outlook 
  
Texto del mensaje con etiqueta se usa en TNEF para resolver las posiciones de los datos adjuntos en el mensaje primario. Esto se realiza mediante la adición de un marcador de posición en el texto del mensaje en la posición de los datos adjuntos. Este marcador de posición o etiqueta de datos adjuntos, se describe los datos adjuntos de forma que TNEF sabe cómo resolver los datos adjuntos y su posición. Las etiquetas tienen el formato de la siguiente manera:
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 ** \<Objeto título\> ** y ** \<nombre de archivo\> ** son variables que contiene los valores que se toman de los datos adjuntos del propio. En los casos en que estos valores no están disponibles, el título es el predeterminado por TNEF en función del tipo de datos adjuntos. 
  
La ** \<KeyNum\> ** variable contiene la representación textual de la clave de datos adjuntos que se ha asignado a los datos adjuntos TNEF. El valor de base de la clave se pasa a la llamada de [OpenTnefStreamEx](opentnefstreamex.md) . El valor de base no debe ser cero y no debe ser el mismo para todas las llamadas a **OpenTnefStreamEx**. Debe ser suficiente para usar números aleatorios ficticio según la hora del sistema desde cualquier generador de números aleatorios que proporciona la biblioteca de tiempo de ejecución, siempre y cuando se garantiza que nunca son cero.
  
La ** \<nombre del transporte\> ** variable contiene el nombre de secuencia pasado a la llamada [OpenTnefStreamEx](opentnefstreamex.md) o el valor de la propiedad **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
  
> [!NOTE]
> La propiedad **PR_ATTACH_TRANSPORT_NAME** y el ** \<nombre del transporte\> ** variable en una etiqueta de texto del mensaje no tienen nada que ver con el nombre del proveedor de transporte que va a implementar. Estos elementos representan el nombre de datos adjuntos para el proveedor de transporte y el sistema de mensajería. 
  
El texto del mensaje está etiquetado cuando un proveedor de transporte solicita un mensaje con etiqueta de texto llamando al método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) . Al leer de la secuencia de texto con etiqueta, TNEF reemplaza el carácter único que se encontraba en el texto del mensaje en el índice proporcionado en la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) con la etiqueta adecuada. Al escribir en la secuencia de texto con etiqueta, TNEF comprueba los datos entrantes para las etiquetas, los datos adjuntos asociados no encuentra y reemplaza la etiqueta con un único carácter de espacio.
  
Tenga en cuenta que, mediante el uso de texto del mensaje con etiqueta, un proveedor de transporte puede conservar la colocación de los datos adjuntos, independientemente de la mayoría de los cambios realizado en el texto del mensaje por sistemas de mensajería.
  

