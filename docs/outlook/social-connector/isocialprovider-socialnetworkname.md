---
title: ISocialProviderSocialNetworkName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: Devuelve una cadena que representa el nombre de la red social.
ms.openlocfilehash: 5a6240fa6e609eec8498456fe56c83a761fadab0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406881"
---
# <a name="isocialprovidersocialnetworkname"></a><span data-ttu-id="aacaf-103">ISocialProvider::SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="aacaf-103">ISocialProvider::SocialNetworkName</span></span>

<span data-ttu-id="aacaf-104">Devuelve una cadena que representa el nombre de la red social.</span><span class="sxs-lookup"><span data-stu-id="aacaf-104">Returns a string that represents the social network name.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a><span data-ttu-id="aacaf-105">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="aacaf-105">Property value</span></span>

<span data-ttu-id="aacaf-106">Cadena que contiene el nombre de la red social.</span><span class="sxs-lookup"><span data-stu-id="aacaf-106">A string that contains the social network name.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aacaf-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aacaf-107">Remarks</span></span>

<span data-ttu-id="aacaf-108">Los proveedores de Outlook Social Connector (OSC) deben localiza el nombre de la red social.</span><span class="sxs-lookup"><span data-stu-id="aacaf-108">Outlook Social Connector (OSC) providers should localize the social network name.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aacaf-109">Vea también</span><span class="sxs-lookup"><span data-stu-id="aacaf-109">See also</span></span>

- [<span data-ttu-id="aacaf-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aacaf-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

