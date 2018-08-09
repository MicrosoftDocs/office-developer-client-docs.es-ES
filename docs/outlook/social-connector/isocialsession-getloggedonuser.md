---
title: ISocialSessionGetLoggedOnUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bd6bdaf6-52d5-4308-9c3d-869f6e1a6608
description: Obtiene una interfaz ISocialProfile que representa al usuario que ha iniciado la sesión.
ms.openlocfilehash: 05e645fa62441b8c9001cf3ec043add36b8593dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821238"
---
# <a name="isocialsessiongetloggedonuser"></a>ISocialSession::GetLoggedOnUser

Obtiene una interfaz [ISocialProfile](isocialprofileisocialperson.md) que representa al usuario que ha iniciado la sesión. 
  
```cpp
HRESULT _stdcall GetLoggedOnUser([out, retval] ISocialProfile** result);
```

## <a name="parameters"></a>Parámetros

_resultado_
  
> [out] Una interfaz **ISocialProfile** . 
    
## <a name="see-also"></a>Vea también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

