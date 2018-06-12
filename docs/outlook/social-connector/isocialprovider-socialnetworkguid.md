---
title: ISocialProviderSocialNetworkGuid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3c07f71d-b906-4a7f-b20a-4a7f558dbf11
description: Devuelve un GUID que representa un identificador único para la red social.
ms.openlocfilehash: 5ff10d51fab03c3bca3eead52848088f2cd80bba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821125"
---
# <a name="isocialprovidersocialnetworkguid"></a><span data-ttu-id="c6542-103">ISocialProvider::SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="c6542-103">ISocialProvider::SocialNetworkGuid</span></span>

<span data-ttu-id="c6542-104">Devuelve un GUID que representa un identificador único para la red social.</span><span class="sxs-lookup"><span data-stu-id="c6542-104">Returns a GUID that represents a unique identifier for the social network.</span></span>
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a><span data-ttu-id="c6542-105">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c6542-105">Property value</span></span>

<span data-ttu-id="c6542-106">Un puntero a un valor GUID que representa un identificador único para la red social.</span><span class="sxs-lookup"><span data-stu-id="c6542-106">A pointer to a GUID value that represents a unique identifier for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c6542-107">Notas</span><span class="sxs-lookup"><span data-stu-id="c6542-107">Remarks</span></span>

<span data-ttu-id="c6542-108">El GUID debe ser inmutable y no debe cambiar incluso si cambia la versión del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c6542-108">The GUID must be immutable and must not change even if the provider version changes.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c6542-109">Ver también</span><span class="sxs-lookup"><span data-stu-id="c6542-109">See also</span></span>

- [<span data-ttu-id="c6542-110">ISocialProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6542-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

