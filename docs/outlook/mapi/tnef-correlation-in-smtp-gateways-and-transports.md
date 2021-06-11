---
title: Correlación de TNEF en puertas de enlace SMTP y transportes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0a685e081d319c43daa583d95d163677e81f2480
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413671"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>Correlación de TNEF en puertas de enlace SMTP y transportes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las puertas de enlace y los transportes que se conectan a sistemas basados en Internet, los que usan SMTP, usan el valor del encabezado SMTP MessageID y la propiedad **PR_TNEF_CORRELATION_KEY** para implementar la correlación TNEF. 
  
El valor del encabezado MessageID del mensaje saliente debe copiarse en la propiedad **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) y codificarse en el atributo [attMAPIProps](attmapiprops.md) de la secuencia TNEF. Tenga en **cuenta PR_TNEF_CORRELATION_KEY** es una propiedad binaria, mientras que MessageID es una cadena; el terminador nulo debe incluirse en la copia y en la comparación. 
  
Esta técnica la usa todo el software de Microsoft que conecta sistemas de mensajería basados en MAPI a Internet, como Microsoft Exchange Server. Esta técnica debe ser usada por las puertas de enlace SMTP y los transportes que se conectan a sistemas que admiten clientes MAPI para maximizar la interoperabilidad.
  

