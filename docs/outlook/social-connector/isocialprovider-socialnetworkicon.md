---
title: ISocialProviderSocialNetworkIcon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: Devuelve una matriz de bytes que representa el icono para la red social.
ms.openlocfilehash: b86a2d1c14c444ba79db495a3795dc61b1fe3660
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821236"
---
# <a name="isocialprovidersocialnetworkicon"></a><span data-ttu-id="dc974-103">ISocialProvider::SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="dc974-103">ISocialProvider::SocialNetworkIcon</span></span>

<span data-ttu-id="dc974-104">Devuelve una matriz de bytes que representa el icono para la red social.</span><span class="sxs-lookup"><span data-stu-id="dc974-104">Returns an array of bytes that represents the icon for the social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a><span data-ttu-id="dc974-105">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="dc974-105">Property value</span></span>

<span data-ttu-id="dc974-106">Un puntero a una estructura que especifica una matriz de bytes que contiene el icono para la red social.</span><span class="sxs-lookup"><span data-stu-id="dc974-106">A pointer to a structure that specifies an array of bytes that contains the icon for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc974-107">Notas</span><span class="sxs-lookup"><span data-stu-id="dc974-107">Remarks</span></span>

<span data-ttu-id="dc974-108">Los recursos de imagen admitidos son .bmp, .jpeg y .png formatos.</span><span class="sxs-lookup"><span data-stu-id="dc974-108">The supported picture resources are .bmp, .jpeg, and .png formats.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dc974-109">Ver también</span><span class="sxs-lookup"><span data-stu-id="dc974-109">See also</span></span>

- [<span data-ttu-id="dc974-110">ISocialProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dc974-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

