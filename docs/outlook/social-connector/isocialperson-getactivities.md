---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Este método está en desuso en Outlook Social Connector 2013.
ms.openlocfilehash: abad4fc2a3e3aaea8a7097ac7e6f56b0aadae299
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286167"
---
# <a name="isocialpersongetactivities"></a>ISocialPerson::GetActivities

Este método está en desuso en Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a>Comentarios

A partir de Outlook Social Connector 2013, el OSC admite sólo la sincronización a petición de actividades y no la sincronización híbrida o la caché de actividades. El OSC omite la configuración **cacheActivities** en el XML de capacidades y no llama a este método. Para admitir la búsqueda de actividades dinámicas, implemente el método [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) . Establezca **cacheActivities** como **false**, **getActivities** y **dynamicActivitiesLookupEx** como **true**, lo que pedirá al OSC que llame a **ISocialSession2:: GetActivitiesEx** en su lugar. 
  
Para obtener más información sobre cómo el OSC obtiene las actividades de amigos, consulte [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Vea también

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

