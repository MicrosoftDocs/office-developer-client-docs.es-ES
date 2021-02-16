---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Este método ha quedado obsoleto en OSC 1.1.
ms.openlocfilehash: 29a7cdc9895dcfa2bd926d95dbd2089b7a5dc778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439299"
---
# <a name="isocialsessiongetactivities"></a>ISocialSession::GetActivities

Este método ha quedado obsoleto en OSC 1.1.
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a>Comentarios

A partir de OSC 1.1, el OSC ya no llama **a GetActivities**. El OSC omite el valor **de dynamicActivitiesLookup**. Para admitir la búsqueda de actividades dinámicas, implemente [el método ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) Establezca **cacheActivities** como **false** y **getActivities** y **dynamicActivitiesLookupEx** como **true**, lo que pedirá al OSC que llame a **ISocialSession2::GetActivitiesEx** en su lugar. 
  
## <a name="see-also"></a>Consulte también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

