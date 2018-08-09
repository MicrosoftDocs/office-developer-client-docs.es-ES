---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Este método ha quedado obsoleto en Outlook Social Connector 2013.
ms.openlocfilehash: 54b5cd6d681aa1e8008eade024ef57783bf18ead
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821132"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a>ISocialProfile::GetActivitiesOfFriendsAndColleagues

Este método ha quedado obsoleto en Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a>Comentarios

Inicio en Outlook Social Connector 2013, el OSC admite la sincronización de sólo a petición de actividades y no en caché o sincronización híbrido de actividades. El OSC pasa por alto la configuración de **cacheActivities** en el XML de las capacidades y ya no se llama a este método. Para admitir la búsqueda de actividades dinámico, implemente el método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Establecer **getActivities** y **dynamicActivitiesLookupEx** como **true**, que se le pedirá el OSC para llamar a **ISocialSession2::GetActivitiesEx** en su lugar. 
  
Para obtener más información acerca de cómo el OSC Obtiene las actividades de amigos, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Vea también

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

