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
ms.openlocfilehash: d902039fa1081e30947ddd8f70ead9ae7acec06a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428693"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a>Formato de encapsulamiento neutro para el transporte (TNEF)

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
TNEF es un formato para convertir un conjunto de propiedades MAPI (un mensaje MAPI) en una secuencia de datos de serie. Las funciones TNEF las usan principalmente los proveedores de transporte que necesitan codificar las propiedades de los mensajes MAPI para su transmisión a través de un sistema de mensajería que no admite esas propiedades directamente. Por ejemplo, un transporte basado en SMTP usa TNEF para codificar propiedades como **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), que no tienen representaciones directas en la estructura de un mensaje SMTP.
  
La implementación de TNEF define varios atributos específicos de TNEF, cada uno de los cuales corresponde a una propiedad MAPI determinada. Estos atributos se usan para codificar sus respectivas propiedades MAPI en la secuencia TNEF. Además, se define un atributo especial que se puede usar para encapsular cualquier propiedad MAPI que no tenga un atributo específico correspondiente. La razón por la que se definen estos atributos, en lugar de simplemente usar un método de codificación uniforme para todas las propiedades MAPI, es habilitar la compatibilidad con versiones anteriores con software no compatible con MAPI que usa TNEF.
  
En el resto de esta sección se describe la estructura y la sintaxis de una secuencia TNEF, la asignación entre propiedades MAPI y atributos TNEF y consideraciones importantes para determinados atributos TNEF.
  

