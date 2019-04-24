---
title: Sección MapiSvc. inf [servicios preDeterminados]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a7906a9a5e953332dba5c4776c63bb433a937a5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270073"
---
# <a name="mapisvcinf-default-services-section"></a>Sección MapiSvc. inf [servicios preDeterminados]

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La sección **[default Services]** muestra todos los servicios de mensajes que están seleccionados como los servicios de mensajes predeterminados. Estos servicios de mensajes predeterminados son un subconjunto de los servicios de mensajes que se enumeran en la sección **[Services]** . Cuando un programa de configuración de perfiles crea un perfil predeterminado, los servicios de mensajes de esta sección se incluyen automáticamente. 
  
Las entradas usan el mismo formato que las entradas de la sección **[Services]** , como se muestra a continuación: 
  
 **[Servicios preDeterminados]**
  
 _nombre de sección de servicio de mensajes_ =  _nombre del servicio de mensajes_
  
Las siguientes entradas se incluirán en la sección **[default Services]** del archivo MAPISVC. inf que se muestra en la ilustración anterior: 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


