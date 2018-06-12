---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Este método ha quedado obsoleto en Outlook Social Connector 2013.
ms.openlocfilehash: af952b6d57325e1b52093fcf655e6fdc271ca34f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821094"
---
# <a name="isocialpersongetactivities"></a>ISocialPerson::GetActivities

Este método ha quedado obsoleto en Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a>Notas

Inicio en Outlook Social Connector 2013, el OSC admite la sincronización de sólo a petición de actividades y no en caché o sincronización híbrido de actividades. El OSC pasa por alto la configuración de **cacheActivities** en el XML de las capacidades y no llama a este método. Para admitir la búsqueda de actividades dinámico, implemente el método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Establezca **cacheActivities** como **false**, **getActivities** y **dynamicActivitiesLookupEx** como **true**, que se le pedirá el OSC para llamar a **ISocialSession2::GetActivitiesEx** en su lugar. 
  
Para obtener más información acerca de cómo el OSC Obtiene las actividades de amigos, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Ver también

- [ISocialPerson: IUnknown](isocialpersoniunknown.md)

