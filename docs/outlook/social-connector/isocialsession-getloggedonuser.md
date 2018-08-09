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
# <a name="isocialsessiongetloggedonuser"></a><span data-ttu-id="88427-103">ISocialSession::GetLoggedOnUser</span><span class="sxs-lookup"><span data-stu-id="88427-103">ISocialSession::GetLoggedOnUser</span></span>

<span data-ttu-id="88427-104">Obtiene una interfaz [ISocialProfile](isocialprofileisocialperson.md) que representa al usuario que ha iniciado la sesión.</span><span class="sxs-lookup"><span data-stu-id="88427-104">Gets an [ISocialProfile](isocialprofileisocialperson.md) interface that represents the logged-on user.</span></span> 
  
```cpp
HRESULT _stdcall GetLoggedOnUser([out, retval] ISocialProfile** result);
```

## <a name="parameters"></a><span data-ttu-id="88427-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88427-105">Parameters</span></span>

<span data-ttu-id="88427-106">_resultado_</span><span class="sxs-lookup"><span data-stu-id="88427-106">_result_</span></span>
  
> <span data-ttu-id="88427-107">[out] Una interfaz **ISocialProfile** .</span><span class="sxs-lookup"><span data-stu-id="88427-107">[out] An **ISocialProfile** interface.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="88427-108">Vea también</span><span class="sxs-lookup"><span data-stu-id="88427-108">See also</span></span>

- [<span data-ttu-id="88427-109">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="88427-109">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

