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
ms.openlocfilehash: 19031f6c02f3e8e925adfc8d2affa43fb6532fee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818285"
---
# <a name="mapisvcinf-services-section"></a>Sección MapiSvc.inf [Servicios]

  
  
**Hace referencia a**: Outlook 
  
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
  

