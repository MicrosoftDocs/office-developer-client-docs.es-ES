---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Devuelve una matriz de cadenas que especifican las direcciones URL del sitio para el proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 34d779d5eb42b81a14c5236685104e9ef4fe36f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285859"
---
# <a name="isocialproviderdefaultsiteurls"></a><span data-ttu-id="d0db7-103">ISocialProvider::DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="d0db7-103">ISocialProvider::DefaultSiteUrls</span></span>

<span data-ttu-id="d0db7-104">Devuelve una matriz de cadenas que especifican las direcciones URL del sitio para el proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="d0db7-104">Returns an array of strings that specify site URLs for the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a><span data-ttu-id="d0db7-105">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d0db7-105">Property value</span></span>

<span data-ttu-id="d0db7-106">Un puntero a una estructura que especifica una matriz de cadenas que representan las direcciones URL del sitio para el proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="d0db7-106">A pointer to a structure that specifies an array of strings that represent site URLs for the OSC provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d0db7-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d0db7-107">Remarks</span></span>

<span data-ttu-id="d0db7-108">Un proveedor puede admitir varias direcciones URL de sitio.</span><span class="sxs-lookup"><span data-stu-id="d0db7-108">A provider can support multiple site URLs.</span></span> <span data-ttu-id="d0db7-109">El OSC establece la propiedad [ISocialSession:: siteUrl](isocialsession-siteurl.md) para informar al proveedor de la dirección URL del sitio seleccionado.</span><span class="sxs-lookup"><span data-stu-id="d0db7-109">The OSC sets the [ISocialSession::SiteUrl](isocialsession-siteurl.md) property to inform the provider of the selected site URL.</span></span> 
  
<span data-ttu-id="d0db7-110">El OSC utiliza el primer elemento de la matriz como dirección URL predeterminada del sitio.</span><span class="sxs-lookup"><span data-stu-id="d0db7-110">The OSC uses the first element of the array as the default site URL.</span></span> <span data-ttu-id="d0db7-111">Un proveedor puede devolver elementos adicionales en la matriz de dirección URL del sitio, pero el OSC no las usa.</span><span class="sxs-lookup"><span data-stu-id="d0db7-111">A provider can return additional elements in the site URL array, but the OSC does not use them.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d0db7-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0db7-112">See also</span></span>

- [<span data-ttu-id="d0db7-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d0db7-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

