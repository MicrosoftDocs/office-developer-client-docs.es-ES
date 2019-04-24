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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342801"
---
# <a name="gateway-mapping-responsibilities"></a>Responsabilidades de la asignación de puerta de enlace

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando una puerta de enlace compatible con MAPI recibe un mensaje que contiene propiedades con nombre en uno de los conjuntos de propiedades especiales designados para contener propiedades asignables a la puerta de enlace, la puerta de enlace debe asignar todas las propiedades al protocolo del sistema de mensajería de destino. Aunque MAPI recomienda que las puertas de enlace controlen todas las propiedades con nombre en los conjuntos de propiedades especiales, se espera que las puertas de enlace controlen sólo dos: la dirección de correo electrónico y el tipo de dirección. Debido a que las propiedades de dirección de correo electrónico y tipo de dirección afectan directamente a la transmisión de mensajes, es fundamental que las puertas de enlace admitan la asignación de estas dos propiedades. Como las claves de búsqueda constan de la dirección y el tipo de dirección de un usuario, también deben traducirse si es posible.
  
No se espera que los identificadores de entrada se traten con frecuencia. Para habilitar la asignación de un identificador de entrada que se origina en un sistema de mensajería a un identificador de entrada que puede ser utilizado por otro sistema de mensajería, la puerta de enlace debe ser capaz de usar el formato de ambos sistemas. Como la mayoría de las puertas de enlace no conocen los formatos de identificador de entrada, la conversión de los identificadores de entrada es poco frecuente.
  
Otra propiedad asignable que no se espera que se traduzca con frecuencia es el nombre para mostrar. Las puertas de enlace deben almacenar los nombres para mostrar y transmitirlos, pero no necesariamente traducirlos. 
  

