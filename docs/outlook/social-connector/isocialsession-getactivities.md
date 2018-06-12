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
ms.openlocfilehash: dc5fe25e4c4f83717309d407963d0046aa6063ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821115"
---
# <a name="isocialsessiongetactivities"></a>ISocialSession::GetActivities

Este método ha quedado obsoleto en OSC 1.1.
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a>Notas

A partir de OSC 1.1, el OSC ya no llama a **GetActivities**. El OSC ignora el valor de **dynamicActivitiesLookup**. Para admitir la búsqueda de actividades dinámico, implemente el método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Establezca **cacheActivities** como **false**y **getActivities** y **dynamicActivitiesLookupEx** como **true**, que se le pedirá el OSC para llamar a **ISocialSession2::GetActivitiesEx** en su lugar. 
  
## <a name="see-also"></a>Ver también

- [ISocialSession: IUnknown](isocialsessioniunknown.md)

