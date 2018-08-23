---
title: Sección MapiSvc.inf [Servicios predeterminados]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a7270bce12f6d91dbb5632f739f4644df866924d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573148"
---
# <a name="mapisvcinf-default-services-section"></a>Sección MapiSvc.inf [Servicios predeterminados]

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La sección **[Services predeterminado]** enumera todos los servicios de mensaje que se han seleccionado como servicios de mensajes de forma predeterminada. Estos servicios de mensaje predeterminada son un subconjunto de los servicios de mensaje que aparecen en la sección **[Services]** . Cuando un programa de configuración de perfil crea un perfil de forma predeterminada, los servicios de mensaje en esta sección se incluyen automáticamente. 
  
Las entradas de utilizan el mismo formato como entradas de la sección **[Services]** , como se muestra a continuación: 
  
 **[Servicios predeterminados]**
  
 _nombre de la sección servicio de mensajes_ =  _nombre de servicio de mensajes_
  
Las siguientes entradas se incluirá en la sección **[Services predeterminado]** para el mapisvc.inf que se muestra en la ilustración anterior: 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


