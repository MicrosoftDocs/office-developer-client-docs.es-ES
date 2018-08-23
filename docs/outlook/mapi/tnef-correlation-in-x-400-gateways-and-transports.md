---
title: Correlación TNEF de puertas de enlace X.400 y transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 297fff3482a4b7aea391c3e1869cd127cc49cad2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566820"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a>Correlación TNEF de puertas de enlace X.400 y transporte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las puertas de enlace y los transportes que se conectan a sistemas basados en X.400, use el valor del atributo IM_THIS_IPM X.400 y el atributo TNEF **attMessageID** para implementar la correlación de TNEF. 
  
El valor del atributo IM_THIS_IPM del mensaje saliente se copia a **attMessageID** en la secuencia TNEF. El atributo IM_THIS_IPM X.400 normalmente es una cadena, mientras que el atributo TNEF **attMessageID** es una cadena de dígitos hexadecimales que representa un valor binario. Por lo tanto, cada carácter en el atributo IM_THIS_IPM X.400, incluido el carácter null final, se debe convertir en una cadena hexadecimal 2 caracteres que representa el valor ASCII del carácter. Por ejemplo, si el atributo IM_THIS_IPM X.400 es la cadena siguiente: 
  
3030322D3030312D305337533A3A3936303631312D313533373030
  
a continuación, el valor de **attMessageID** sería la siguiente secuencia de dígitos hexadecimales: 
  
33 30 33 30 33 32 32 44
  
33 30 33 30 33 31 32 44
  
33 30 35 33 33 37 35 33
  
33 41 33 41 33 39 33 36
  
33 30 33 36 33 31 33 31
  
32 44 33 31 33 35 33 33
  
33 37 33 30 33 30 00
  
Esta técnica se usa en el conector de X.400 de Microsoft Exchange Server. Las puertas de enlace X.400 y los transportes que se conectan a Microsoft Exchange Server para maximizar la interoperabilidad debe usar esta técnica.
  
Para mayor compatibilidad con el software de Microsoft futuro, así como está presente, el atributo IM_THIS_IPM X.400 también se debe copiar en la propiedad **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)). Sin embargo, puesto que **PR_TNEF_CORRELATION_KEY** es una propiedad binaria, es necesaria ninguna traducción en una cadena hexadecimal. 
  

