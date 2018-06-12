---
title: Correlación de TNEF en las puertas de enlace SMTP y los transportes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: ec1d826ee2b3b46685a2c03dfaf45d2843869cc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820867"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>Correlación de TNEF en las puertas de enlace SMTP y los transportes

  
  
**Se aplica a**: Outlook 
  
Las puertas de enlace y los transportes que se conectan a internet sistemas basados en, aquellos que usan SMTP, use el valor de encabezado de SMTP MessageID y la propiedad **PR_TNEF_CORRELATION_KEY** para implementar la correlación de TNEF. 
  
El valor del encabezado del mensaje saliente MessageID debe se copia a la propiedad **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) y codificado en el atributo [attMAPIProps](attmapiprops.md) de la secuencia TNEF. Tenga en cuenta que **PR_TNEF_CORRELATION_KEY** es una propiedad binaria, mientras que el identificador del mensaje es una cadena; el terminador nulo se debe incluir en la copia y en la comparación. 
  
Esta técnica se usa en todo el software de Microsoft que se conecta a sistemas de mensajería basado en MAPI a Internet, como Microsoft Exchange Server. Las puertas de enlace SMTP y los transportes que se conectan a los sistemas que admiten los clientes MAPI para maximizar la interoperabilidad debe usar esta técnica.
  

