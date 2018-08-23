---
title: Sección MapiSvc.inf [Servicios]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 520478061e192f9fec97c6b13edde7833a13a3d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571398"
---
# <a name="mapisvcinf-services-section"></a>Sección MapiSvc.inf [Servicios]

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La sección **[Services]** enumera los servicios de mensaje que se instalan en un equipo. Las entradas de esta sección use el siguiente formato: 
  
 **[Services]**
  
 _nombre de la sección servicio de mensajes_ =  _nombre de servicio de mensajes_
  
El nombre de la sección servicio de mensajes es que una cadena definida por el servicio de mensajes que se vincula esta entrada a una sección correspondiente para el servicio en el resto de mapisvc.inf. El nombre de servicio de mensajes es el nombre del servicio instalado. En la sección siguiente se muestra tres servicios de mensaje: la libreta de direcciones predeterminada, mi propio servicio y el servicio de almacén de mensajes. Estos servicios son ficticios, únicamente con fines de ilustración. Cada implementador del servicio mensaje sería sustituir la entrada adecuada para su servicio de mensajes en esta sección.
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

Cada entrada de esta sección tiene una sección correspondiente de su propio donde se almacena la información para el servicio de mensajes. Por ejemplo, la sección correspondiente de la libreta de direcciones predeterminada se denomina [AB].
  

