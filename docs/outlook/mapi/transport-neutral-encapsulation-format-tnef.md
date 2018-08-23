---
title: Formato de encapsulamiento neutro para el transporte (TNEF)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: 'Última modificación: 12 de marzo de 2013'
ms.openlocfilehash: 440c27b019b91ec8c2c02e37850d2768a273559b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591936"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a>Formato de encapsulamiento neutro para el transporte (TNEF)

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
TNEF es un formato para convertir un conjunto de propiedades MAPI, un mensaje MAPI: en una secuencia de datos en serie. Las funciones TNEF se usan principalmente los proveedores de transporte que necesitan para codificar las propiedades de mensaje MAPI para la transmisión a través de un sistema de mensajería que no es compatible con esas propiedades directamente. Por ejemplo, un transporte basado en SMTP utiliza TNEF para codificar propiedades como **PR_SENT_REPRESENTING_NAME de MAPI** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), que no tienen directos representaciones en la estructura de un mensaje SMTP.
  
La implementación de TNEF define varios atributos específicos de TNEF, cada uno de los cuales corresponde a una propiedad determinada de MAPI. Estos atributos se utilizan para codificar sus respectivas propiedades MAPI en la secuencia TNEF. Además, se define un atributo especial que se pueden utilizar para encapsular cualquier propiedad MAPI que no tiene un atributo específico correspondiente a ella. La razón estos atributos están definidos, en lugar de usar simplemente una uniforme codificación para todas las propiedades MAPI (método) — es permitir la compatibilidad con versiones anteriores con el software compatible con MAPI que está utilizando la codificación TNEF.
  
En el resto de esta sección se describe la estructura y la sintaxis de una secuencia TNEF, la asignación entre las propiedades MAPI y atributos TNEF y consideraciones importantes para ciertos atributos TNEF.
  

