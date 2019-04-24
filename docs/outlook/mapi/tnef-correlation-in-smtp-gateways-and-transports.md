---
title: Correlación TNEF en puertas de enlace SMTP y transportes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0a685e081d319c43daa583d95d163677e81f2480
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339693"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>Correlación TNEF en puertas de enlace SMTP y transportes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Puertas de enlace y transportes que se conectan a sistemas basados en Internet, los que usan SMTP, usan el valor del encabezado SMTP MessageID y la propiedad **PR_TNEF_CORRELATION_KEY** para implementar la correlación de TNEF. 
  
El valor del encabezado MessageID del mensaje saliente debe copiarse en la propiedad **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) y codificarse en el atributo [attMAPIProps](attmapiprops.md) de la secuencia TNEF. Tenga en cuenta que **PR_TNEF_CORRELATION_KEY** es una propiedad binaria, mientras que el MessageID es una cadena; el terminador null debe incluirse en la copia y en la comparación. 
  
Esta técnica se usa en todo el software de Microsoft que conecta sistemas de mensajería basados en MAPI a Internet, como Microsoft Exchange Server. Esta técnica debe usarse en todas las puertas de enlace SMTP y los transportes que se conectan a los sistemas que admiten clientes MAPI con el fin de maximizar la interoperabilidad.
  

