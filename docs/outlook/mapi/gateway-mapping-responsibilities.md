---
title: Responsabilidades de la asignación de puerta de enlace
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 214d24bb0b0af525d5e2588c556c37cf720364a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422757"
---
# <a name="gateway-mapping-responsibilities"></a>Responsabilidades de la asignación de puerta de enlace

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando una puerta de enlace compatible con MAPI recibe un mensaje que contiene propiedades con nombre en uno de los conjuntos de propiedades especiales designados para contener propiedades asignables a la puerta de enlace, la puerta de enlace debe asignar todas las propiedades al protocolo del sistema de mensajería de destino. Aunque MAPI recomienda que las puertas de enlace controle todas las propiedades con nombre en los conjuntos de propiedades especiales, se espera que las puertas de enlace controle solo dos: dirección de correo electrónico y tipo de dirección. Dado que las propiedades de dirección de correo electrónico y tipo de dirección afectan directamente a la transmisión de mensajes, es fundamental que las puertas de enlace admitan la asignación de estas dos propiedades. Dado que las claves de búsqueda constan del tipo de dirección y la dirección de un usuario, también deben traducirse si es posible.
  
No se espera que los identificadores de entrada se controle con frecuencia. Para habilitar la asignación de un identificador de entrada que se origina en un sistema de mensajería a un identificador de entrada que otro sistema de mensajería pueda usar, la puerta de enlace debe poder usar el formato de ambos sistemas. Dado que la mayoría de las puertas de enlace no conocen los formatos de identificador de entrada, la traducción de identificadores de entrada es poco común.
  
Otra propiedad asignable que no se espera que se traduzca con frecuencia es el nombre para mostrar. Las puertas de enlace deben almacenar nombres para mostrar y transmitirlos, pero no traducirlos necesariamente. 
  

