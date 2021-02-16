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
ms.openlocfilehash: e5bf5242ef673976ebda928d6ce4862e3e7dd072
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434784"
---
# <a name="mapisvcinf-services-section"></a>Sección MapiSvc.inf [Servicios]

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En **la sección [Servicios]** se enumeran los servicios de mensajes instalados en un equipo. Las entradas de esta sección tienen el siguiente formato: 
  
 **[Servicios]**
  
 _nombre de la sección de servicio de mensajes_  =   _nombre del servicio de mensajes_
  
El nombre de la sección de servicio de mensajes es una cadena definida por el servicio de mensajes que vincula esta entrada a una sección correspondiente para el servicio en otro lugar de mapisvc.inf. El nombre del servicio de mensajes es el nombre del servicio instalado. En la siguiente sección se muestran tres servicios de mensajes: la libreta de direcciones predeterminada, mi propio servicio y el servicio de almacenamiento de mensajes. Estos servicios son ficticios, solo con fines ilustrativos. Cada implementador del servicio de mensajes sustituiría la entrada adecuada por su servicio de mensajes en esta sección.
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

Cada entrada de esta sección tiene una sección propia correspondiente donde se almacena la información del servicio de mensajes. Por ejemplo, la sección correspondiente de la Libreta de direcciones predeterminada se denomina [AB].
  

