---
title: Sección MapiSvc.inf [servicios predeterminados]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 5d860135d846df8ef1ea0784d7430c71ad0fe64e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818280"
---
# <a name="mapisvcinf-default-services-section"></a>Sección MapiSvc.inf [servicios predeterminados]

  
  
**Se aplica a**: Outlook 
  
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


