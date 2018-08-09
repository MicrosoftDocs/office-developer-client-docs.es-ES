---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Inicializa el proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 172595db8d9467f22a80c8caf0e3444250826aaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821108"
---
# <a name="isocialproviderload"></a><span data-ttu-id="43dea-103">ISocialProvider::Load</span><span class="sxs-lookup"><span data-stu-id="43dea-103">ISocialProvider::Load</span></span>

<span data-ttu-id="43dea-104">Inicializa el proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="43dea-104">Initializes the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a><span data-ttu-id="43dea-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43dea-105">Parameters</span></span>

<span data-ttu-id="43dea-106">_socialProviderInterfaceVersion_</span><span class="sxs-lookup"><span data-stu-id="43dea-106">_socialProviderInterfaceVersion_</span></span>
  
> <span data-ttu-id="43dea-107">[entrada] La versión de las interfaces de proveedor OSC esperado por el OSC.</span><span class="sxs-lookup"><span data-stu-id="43dea-107">[in] The version of the OSC provider interfaces expected by the OSC.</span></span>
    
<span data-ttu-id="43dea-108">_languageTag_</span><span class="sxs-lookup"><span data-stu-id="43dea-108">_languageTag_</span></span>
  
> <span data-ttu-id="43dea-109">[entrada] La etiqueta de idioma de ingeniería de Internet (IETF), definida por [[RFC4646]](http://www.ietf.org/rfc/rfc4646.txt) y [[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt), que representa el idioma de interfaz de usuario de Outlook actual.</span><span class="sxs-lookup"><span data-stu-id="43dea-109">[in] The Internet Engineering Task Force (IETF) language tag, defined by [[RFC4646]](http://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt), that represents the current Outlook user-interface language.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43dea-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43dea-110">Remarks</span></span>

<span data-ttu-id="43dea-111">El formato de versión para el parámetro _socialProviderInterfaceVersion_ es _X_. _xxxx_, donde _X_ es la versión principal y _xxxx_ es la versión secundaria de la OSC.</span><span class="sxs-lookup"><span data-stu-id="43dea-111">The version format for the  _socialProviderInterfaceVersion_ parameter is  _X_. _xxxx_, where  _X_ is the major version and  _xxxx_ is the minor version of the OSC.</span></span> <span data-ttu-id="43dea-112">Para Office 2013, compruebe si la versión principal que se va a 15.</span><span class="sxs-lookup"><span data-stu-id="43dea-112">For Office 2013, check for the major version being 15.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="43dea-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="43dea-113">See also</span></span>

- [<span data-ttu-id="43dea-114">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="43dea-114">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

