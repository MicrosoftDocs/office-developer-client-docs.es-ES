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
  
Algunos sistemas de mensajería realizan una comprobación de correlación en cualquier secuencia de formato de encapsulación neutro para el transporte (TNEF) que se adjunta a un mensaje entrante para comprobar que el flujo TNEF realmente pertenece a ese mensaje. Esto implica que se hace coincidir el valor de un campo en el encabezado del mensaje entrante con una copia de ese valor almacenada en alguna propiedad del flujo TNEF. Para esto, se suelen usar valores que son únicos para cada mensaje, como los números de identificador de mensaje. El transporte o la puerta de enlace que creó la secuencia TNEF es responsable de elegir un valor apropiado del encabezado del mensaje y colocar una copia en una propiedad adecuada antes de codificar las propiedades del mensaje saliente en la secuencia TNEF. Las puertas de enlace o los transportes que reciben el mensaje pueden extraer la propiedad de la secuencia TNEF y comprobar que su valor coincida con el valor del campo de encabezado correspondiente en el mensaje entrante.
  
Si los valores no coinciden, la puerta de enlace o el transporte deben descartar la secuencia TNEF y procesar sólo el sobre del mensaje nativo. Estas comprobaciones son prudentes porque los clientes de correo no basados en MAPI pueden adjuntar un archivo que contenga un flujo TNEF de un mensaje antiguo a un reenvío o incluso a un mensaje no relacionado; Si no se activa, un error de este tipo puede provocar la pérdida de texto del mensaje.
  
El valor del campo de encabezado elegido debe ser único para el mensaje. No hay ningún campo de encabezado fijo para todos los sistemas de mensajería, ya que los distintos sistemas de mensajería utilizan distintos campos de encabezado, pero normalmente el sistema de mensajería asigna un identificador único al mensaje que es adecuado para este propósito. Por ejemplo, los sistemas SMTP usan normalmente el encabezado MessageID, mientras que los sistemas X. 400 normalmente usan el atributo IM_THIS_IPM.
  

