---
title: Responsabilidades de la asignación de puerta de enlace
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: ad5f4e896b748dc0d7495c428af093af57bc7cdd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816899"
---
# <a name="gateway-mapping-responsibilities"></a>Responsabilidades de la asignación de puerta de enlace

**Se aplica a**: Outlook 
  
Cuando una puerta de enlace compatible con MAPI recibe un mensaje que contiene propiedades con nombre en uno de los conjuntos de propiedades especiales designados para contener propiedades pueda asignar la puerta de enlace, la puerta de enlace debe asignar todas las propiedades del protocolo del sistema de mensajería de destino. Aunque MAPI, se recomienda que las puertas de enlace controlan con nombre de todas las propiedades en los conjuntos de propiedades especiales, las puertas de enlace se espera que controlen sólo dos: dirección y tipo de dirección de correo electrónico. Debido a que la dirección de correo electrónico y las propiedades de tipo de dirección afectan directamente a la transmisión de mensajes, es fundamental que las puertas de enlace compatible con la asignación de estas dos propiedades. Debido a que las claves de búsqueda se componen de tipo de dirección y la dirección de un usuario, también se deben traducir si es posible.
  
No se esperan que los identificadores de entrada se controlarán con frecuencia. Para habilitar la asignación de un identificador de entrada que se origina en un sistema de mensajería a un identificador de entrada que se puede usar por otro sistema de mensajería, la puerta de enlace debe ser capaz de utilizar el formato de ambos sistemas. Debido a que la mayoría de las puertas de enlace no son conscientes de formatos de identificador de entrada, la traducción de los identificadores de entrada es poco habitual.
  
Otra propiedad pueda asignar que no se espera que se debe traducir con frecuencia es el nombre para mostrar. Las puertas de enlace deben almacenar los nombres para mostrar y transmitirlos, pero no necesariamente traducir a ellos. 
  

