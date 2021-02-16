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
ms.openlocfilehash: a7906a9a5e953332dba5c4776c63bb433a937a5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435323"
---
# <a name="mapisvcinf-default-services-section"></a>Sección MapiSvc.inf [Servicios predeterminados]

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La **sección [Servicios predeterminados]** enumera todos los servicios de mensajes seleccionados como servicios de mensajes predeterminados. Estos servicios de mensajes predeterminados son un subconjunto de los servicios de mensaje enumerados en la **sección [Servicios].** Cuando un programa de configuración de perfil crea un perfil predeterminado, los servicios de mensajes de esta sección se incluyen automáticamente. 
  
Las entradas usan el mismo formato que las entradas de la sección **[Servicios],** como se muestra a continuación: 
  
 **[Servicios predeterminados]**
  
 _nombre de la sección de servicio de mensajes_  =   _nombre del servicio de mensajes_
  
Las siguientes entradas se incluirían en la sección **[Servicios predeterminados]** para mapisvc.inf que se muestra en la ilustración anterior: 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


