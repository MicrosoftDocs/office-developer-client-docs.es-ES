---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Devuelve una matriz de cadenas que especifican las direcciones URL de sitio para el proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: a2b2e0397c7c67476ac8067a53e2acbd4eddf270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821096"
---
# <a name="isocialproviderdefaultsiteurls"></a><span data-ttu-id="259ea-103">ISocialProvider::DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="259ea-103">ISocialProvider::DefaultSiteUrls</span></span>

<span data-ttu-id="259ea-104">Devuelve una matriz de cadenas que especifican las direcciones URL de sitio para el proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="259ea-104">Returns an array of strings that specify site URLs for the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a><span data-ttu-id="259ea-105">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="259ea-105">Property value</span></span>

<span data-ttu-id="259ea-106">Un puntero a una estructura que especifica una matriz de cadenas que representan direcciones URL de sitio para el proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="259ea-106">A pointer to a structure that specifies an array of strings that represent site URLs for the OSC provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="259ea-107">Notas</span><span class="sxs-lookup"><span data-stu-id="259ea-107">Remarks</span></span>

<span data-ttu-id="259ea-108">Un proveedor puede admitir varias direcciones URL de sitio.</span><span class="sxs-lookup"><span data-stu-id="259ea-108">A provider can support multiple site URLs.</span></span> <span data-ttu-id="259ea-109">El OSC establece la propiedad [ISocialSession::SiteUrl](isocialsession-siteurl.md) para informar al proveedor de la dirección URL de sitio seleccionado.</span><span class="sxs-lookup"><span data-stu-id="259ea-109">The OSC sets the [ISocialSession::SiteUrl](isocialsession-siteurl.md) property to inform the provider of the selected site URL.</span></span> 
  
<span data-ttu-id="259ea-110">El OSC utiliza el primer elemento de la matriz como la dirección URL del sitio de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="259ea-110">The OSC uses the first element of the array as the default site URL.</span></span> <span data-ttu-id="259ea-111">Un proveedor puede devolver elementos adicionales en la matriz de dirección URL del sitio, pero el OSC no las usa.</span><span class="sxs-lookup"><span data-stu-id="259ea-111">A provider can return additional elements in the site URL array, but the OSC does not use them.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="259ea-112">Ver también</span><span class="sxs-lookup"><span data-stu-id="259ea-112">See also</span></span>

- [<span data-ttu-id="259ea-113">ISocialProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="259ea-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

