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
ms.openlocfilehash: 2b4d4cd790870a024cac6f2ed9952d18a970235a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419922"
---
# <a name="tnef-tagged-message-text"></a>Texto del mensaje etiquetado con TNEF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
TNEF utiliza el texto del mensaje etiquetado para resolver las posiciones de los datos adjuntos en el mensaje principal. Esto se realiza agregando un marcador de posición en el texto del mensaje en la posición de los datos adjuntos. Este marcador de posición, o etiqueta de datos adjuntos, describe los datos adjuntos de tal manera que TNEF sabe cómo resolver los datos adjuntos y su posición. Las etiquetas tienen el siguiente formato:
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 **El título\> del objeto y el nombre de archivo son variables que contienen valores de los datos adjuntos en sí. \<** ** \<\> ** En los casos en los que estos valores no están disponibles, el título es el predeterminado en formato TNEF en función del tipo de datos adjuntos. 
  
La ** \<variable\> KeyNum** contiene la representación textual de la clave de datos adjuntos asignada a los datos adjuntos por TNEF. El valor base de la clave se pasa a la llamada [OpenTnefStreamEx](opentnefstreamex.md) . El valor base no debe ser cero y no debe ser el mismo para cada llamada a **OpenTnefStreamEx**. Debe bastar con usar números pseudoaleatorios en función de la hora del sistema, desde cualquier generador de números aleatorios que proporcione la biblioteca en tiempo de ejecución, siempre que se garantice que nunca son cero.
  
La ** \<variable de\> nombre de transporte** contiene el nombre de la secuencia que se ha pasado a la llamada [OpenTnefStreamEx](opentnefstreamex.md) o el valor de la propiedad **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
  
> [!NOTE]
> La propiedad **PR_ATTACH_TRANSPORT_NAME** y la ** \<variable de\> nombre de transporte** de una etiqueta de texto de mensaje no tienen nada que saber con el nombre del proveedor de transporte que se está implementando. Estos elementos representan el nombre de los datos adjuntos del proveedor de transporte y el sistema de mensajería. 
  
El texto del mensaje se etiqueta cuando un proveedor de transporte solicita el texto del mensaje etiquetado llamando al método [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) . Al leer de la secuencia de texto etiquetada, TNEF reemplaza el carácter único que estaba en el texto del mensaje en el índice proporcionado en la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) con la etiqueta adecuada. Al escribir en la secuencia de texto etiquetada, TNEF comprueba las etiquetas de los datos entrantes, busca los datos adjuntos asociados y reemplaza la etiqueta con un solo carácter de espacio.
  
Tenga en cuenta que, al usar el texto del mensaje etiquetado, un proveedor de transporte puede conservar la posición de los datos adjuntos independientemente de la mayoría de los cambios realizados en el texto del mensaje por sistemas de mensajería.
  

