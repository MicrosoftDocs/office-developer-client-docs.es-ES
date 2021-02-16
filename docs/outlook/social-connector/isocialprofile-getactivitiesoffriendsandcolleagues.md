---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Este método ha quedado en desuso en Outlook Social Connector 2013.
ms.openlocfilehash: c02cf0e8a6d2da3f9fb7704c92e10e0409042393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406895"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a>ISocialProfile::GetActivitiesOfFriendsAndColleagues

Este método ha quedado obsoleto en Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a>Comentarios

A partir de Outlook Social Connector 2013, el OSC solo admite la sincronización a petición de actividades y no la sincronización híbrida o en caché de las actividades. El OSC omite la configuración **cacheActivities** en el XML de funcionalidades y ya no llama a este método. Para admitir la búsqueda de actividades dinámicas, implemente [el método ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) Establezca **getActivities** y **dynamicActivitiesLookupEx** como **true**, lo que pedirá al OSC que llame a **ISocialSession2::GetActivitiesEx** en su lugar. 
  
Para obtener más información sobre cómo el OSC obtiene actividades de amigos, consulta Sincronizar amigos [y actividades.](synchronizing-friends-and-activities.md) 
  
## <a name="see-also"></a>Consulte también

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

