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
ms.openlocfilehash: fc96799ada773cc7260e156d3e2ab8423b73884b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407875"
---
# <a name="isocialprovidersocialnetworkguid"></a><span data-ttu-id="0cde3-103">ISocialProvider::SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="0cde3-103">ISocialProvider::SocialNetworkGuid</span></span>

<span data-ttu-id="0cde3-104">Devuelve un GUID que representa un identificador único para la red social.</span><span class="sxs-lookup"><span data-stu-id="0cde3-104">Returns a GUID that represents a unique identifier for the social network.</span></span>
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a><span data-ttu-id="0cde3-105">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0cde3-105">Property value</span></span>

<span data-ttu-id="0cde3-106">Puntero a un valor GUID que representa un identificador único para la red social.</span><span class="sxs-lookup"><span data-stu-id="0cde3-106">A pointer to a GUID value that represents a unique identifier for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0cde3-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0cde3-107">Remarks</span></span>

<span data-ttu-id="0cde3-108">El GUID debe ser inmutable y no debe cambiar incluso si cambia la versión del proveedor.</span><span class="sxs-lookup"><span data-stu-id="0cde3-108">The GUID must be immutable and must not change even if the provider version changes.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0cde3-109">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cde3-109">See also</span></span>

- [<span data-ttu-id="0cde3-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0cde3-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

