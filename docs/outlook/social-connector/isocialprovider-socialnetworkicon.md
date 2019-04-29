---
title: ISocialProviderSocialNetworkIcon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: Devuelve una matriz de bytes que representa el icono de la red social.
ms.openlocfilehash: c63d9996d4478c8ce7e46210aae34791bcfe9222
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438690"
---
# <a name="isocialprovidersocialnetworkicon"></a><span data-ttu-id="2df9f-103">ISocialProvider::SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="2df9f-103">ISocialProvider::SocialNetworkIcon</span></span>

<span data-ttu-id="2df9f-104">Devuelve una matriz de bytes que representa el icono de la red social.</span><span class="sxs-lookup"><span data-stu-id="2df9f-104">Returns an array of bytes that represents the icon for the social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a><span data-ttu-id="2df9f-105">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2df9f-105">Property value</span></span>

<span data-ttu-id="2df9f-106">Un puntero a una estructura que especifica una matriz de bytes que contiene el icono para la red social.</span><span class="sxs-lookup"><span data-stu-id="2df9f-106">A pointer to a structure that specifies an array of bytes that contains the icon for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2df9f-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2df9f-107">Remarks</span></span>

<span data-ttu-id="2df9f-108">Los recursos de imágenes compatibles son formatos. bmp,. JPEG y. png.</span><span class="sxs-lookup"><span data-stu-id="2df9f-108">The supported picture resources are .bmp, .jpeg, and .png formats.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2df9f-109">Vea también</span><span class="sxs-lookup"><span data-stu-id="2df9f-109">See also</span></span>

- [<span data-ttu-id="2df9f-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2df9f-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

