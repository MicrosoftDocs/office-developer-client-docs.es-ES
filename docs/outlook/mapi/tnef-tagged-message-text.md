---
title: TNEF-Tagged texto del mensaje
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
# <a name="tnef-tagged-message-text"></a>TNEF-Tagged texto del mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
TNEF usa el texto del mensaje etiquetado para resolver las posiciones de datos adjuntos en el mensaje primario. Para ello, se agrega un titular en el texto del mensaje en la posición de los datos adjuntos. Este titular del lugar, o etiqueta de datos adjuntos, describe los datos adjuntos de tal manera que TNEF sepa cómo resolver los datos adjuntos y su posición. Las etiquetas tienen el siguiente formato:
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 **\< El \> título del** objeto **\< y el nombre \> de** archivo son variables que contienen valores que se toman de los datos adjuntos en sí. En los casos en los que estos valores no están disponibles, TNEF tiene el título predeterminado en función del tipo de datos adjuntos. 
  
La **\< variable \> KeyNum** contiene la representación textual de la clave de datos adjuntos asignada a los datos adjuntos por TNEF. El valor base de la clave se pasa a la [llamada OpenTnefStreamEx.](opentnefstreamex.md) El valor base no debe ser cero y no debe ser el mismo para todas las llamadas a **OpenTnefStreamEx**. Debería bastar con usar números pseudo aleatorios en función del tiempo del sistema de cualquier generador de números aleatorios que la biblioteca de tiempo de ejecución proporciona, siempre y cuando se garantice que nunca sean cero.
  
La variable **\< Transport \> Name** contiene el nombre de secuencia pasado a la llamada [OpenTnefStreamEx](opentnefstreamex.md) o el valor de la propiedad **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
  
> [!NOTE]
> La **PR_ATTACH_TRANSPORT_NAME** y la variable **\< Transport Name \>** de una etiqueta de texto de mensaje no tienen nada que ver con el nombre del proveedor de transporte que está implementando. Estos elementos representan el nombre de un archivo adjunto para el proveedor de transporte y el sistema de mensajería. 
  
El texto del mensaje se etiqueta cuando un proveedor de transporte solicita un texto de mensaje etiquetado llamando al método [ITnef::OpenTaggedBody.](itnef-opentaggedbody.md) Al leer desde la secuencia de texto etiquetada, TNEF reemplaza el carácter único que estaba en el texto del mensaje en el índice proporcionado en la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) por la etiqueta adecuada. Al escribir en la secuencia de texto etiquetada, TNEF comprueba los datos entrantes en busca de etiquetas, busca los datos adjuntos asociados y reemplaza la etiqueta por un solo carácter de espacio.
  
Tenga en cuenta que, al usar texto de mensaje etiquetado, un proveedor de transporte puede conservar el posicionamiento de los datos adjuntos independientemente de la mayoría de los cambios realizados en el texto del mensaje por los sistemas de mensajería.
  

