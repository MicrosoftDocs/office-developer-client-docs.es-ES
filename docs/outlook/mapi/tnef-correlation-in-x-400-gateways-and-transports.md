---
title: Correlación TNEF en puertas de enlace x.400 y transportes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e08f16ff60a282f1be3adf93d858471e38d19957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406377"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a>Correlación TNEF en puertas de enlace x.400 y transportes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las puertas de enlace y los transportes que se conectan a sistemas basados en X.400, usan el valor del atributo X.400 de IM_THIS_IPM y el atributo **TNEF attMessageID** para implementar la correlación TNEF. 
  
El valor del atributo IM_THIS_IPM del mensaje saliente se copia en **attMessageID** en la secuencia TNEF. El IM_THIS_IPM X.400 suele ser una cadena, mientras que el atributo **TNEF attMessageID** es una cadena de dígitos hexadecimales que representa un valor binario. Por lo tanto, cada carácter del atributo IM_THIS_IPM X.400, incluido el carácter nulo de terminación, debe convertirse en una cadena hexadecimal de 2 caracteres que represente el valor ASCII de ese carácter. Por ejemplo, si el IM_THIS_IPM X.400 es la siguiente cadena: 
  
3030322D3030312D305337533A3A3936303631312D3135337303030
  
a continuación, el **valor de attMessageID** sería la siguiente secuencia de dígitos hexadecimales: 
  
33 30 33 30 33 32 32 44
  
33 30 33 30 33 31 32 44
  
33 30 35 33 33 37 35 33
  
33 41 33 41 33 39 33 36
  
33 30 33 36 33 31 33 31
  
32 44 33 31 33 35 33 33
  
33 37 33 30 33 30 00
  
Esta técnica la usa el Microsoft Exchange Server X.400 Connector. Esta técnica debe ser usada por las puertas de enlace X.400 y los transportes que se conectan a Microsoft Exchange Server para maximizar la interoperabilidad.
  
Para mayor compatibilidad con el software de Microsoft futuro y presente, el atributo IM_THIS_IPM X.400 también debe copiarse en la propiedad **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)). Sin embargo, **PR_TNEF_CORRELATION_KEY** es una propiedad binaria, no es necesario traducir a una cadena hexadecimal. 
  

