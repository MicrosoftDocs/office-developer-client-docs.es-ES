---
title: Correlación de TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: 'Última modificación: 12 de marzo de 2013'
ms.openlocfilehash: b8b30dcc2fcf0c8e75004e36b6fd9f4f4583e304
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820868"
---
# <a name="tnef-correlation"></a>Correlación de TNEF

 
  
**Se aplica a**: Outlook 
  
Algunos sistemas de mensajería realizan una comprobación de correlación en cualquier secuencia de formato de encapsulación neutro para el transporte (TNEF) que se adjunta a un mensaje entrante para comprobar que la secuencia TNEF en realidad pertenecen a ese mensaje. Esto implica que coincidan con el valor de algún campo en el encabezado del mensaje entrante con una copia de ese valor almacenado en alguna propiedad en la secuencia TNEF. Los valores que son supuestamente únicos para cada mensaje, como los números de identificador de mensaje, se suelen usar para esto. El transporte o la puerta de enlace que se creó la secuencia TNEF es responsable de elegir un valor apropiado en el encabezado del mensaje y coloca una copia en una propiedad adecuada antes de la codificación de propiedades de los mensajes salientes en la secuencia de TNEF. Las puertas de enlace o los transportes que reciben el mensaje, a continuación, pueden extraer dicha propiedad de la secuencia TNEF y compruebe que su valor coincide con el valor del campo de encabezado correspondiente en el mensaje entrante.
  
Si los valores no coinciden, la puerta de enlace o transporte debe descartar la secuencia TNEF y proceso sólo el sobre del mensaje nativo. Estos controles son prudentes debido a que los clientes de correo basado en MAPI no pueden adjuntar un archivo que contiene una secuencia de TNEF de los mensajes antiguos a una transferencia o incluso un mensaje sin relacionar; Si no está activado, este tipo de error puede causar la pérdida de texto del mensaje.
  
El valor del campo de encabezado elegido debe ser único para el mensaje. No hay ningún campo de encabezado fija para todos los sistemas de mensajería debido a que los sistemas de mensajería distintos usar los campos de encabezado diferentes, pero normalmente, el sistema de mensajería asigna un identificador único para el mensaje que es adecuado para este propósito. Por ejemplo, sistemas de SMTP normalmente utilizan el encabezado MessageID, mientras sistemas X.400 normalmente usa el atributo IM_THIS_IPM.
  

