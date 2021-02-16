---
title: Correlación TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: 'Última modificación: 12 de marzo de 2013'
ms.openlocfilehash: 8d601bb2bbc65e21c5bc83179cc29e53ddd33876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410374"
---
# <a name="tnef-correlation"></a>Correlación TNEF

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Algunos sistemas de mensajería realizan una comprobación de correlación en cualquier secuencia de formato de encapsulamiento de Transport-Neutral (TNEF) adjunta a un mensaje entrante para comprobar que la secuencia TNEF pertenece de hecho a ese mensaje. Esto implica hacer coincidir el valor de algún campo en el encabezado del mensaje entrante con una copia de ese valor almacenada en alguna propiedad de la secuencia TNEF. Normalmente se usan valores que son presumiblemente únicos para cada mensaje, como los números de id. de mensaje. El transporte o la puerta de enlace que creó la secuencia TNEF es responsable de elegir un valor adecuado del encabezado del mensaje y colocar una copia en una propiedad adecuada antes de codificar las propiedades del mensaje saliente en la secuencia TNEF. Las puertas de enlace o los transportes que reciben el mensaje pueden extraer esa propiedad de la secuencia TNEF y comprobar que su valor coincide con el valor del campo de encabezado correspondiente en el mensaje entrante.
  
Si los valores no coinciden, la puerta de enlace o el transporte deben descartar la secuencia TNEF y procesar solo el sobre del mensaje nativo. Estas comprobaciones son prudentes porque los clientes de correo no basados en MAPI pueden adjuntar un archivo que contiene una secuencia TNEF de un mensaje antiguo a un reenvío o incluso un mensaje no relacionado; si no se comprueba, este error puede provocar la pérdida del texto del mensaje.
  
El valor del campo de encabezado elegido debe ser único para el mensaje. No hay ningún campo de encabezado fijo para todos los sistemas de mensajería porque diferentes sistemas de mensajería usan campos de encabezado diferentes, pero normalmente el sistema de mensajería asigna un identificador único al mensaje que es adecuado para este propósito. Por ejemplo, los sistemas SMTP suelen usar el encabezado MessageID, mientras que los sistemas X.400 suelen usar el IM_THIS_IPM principal.
  

