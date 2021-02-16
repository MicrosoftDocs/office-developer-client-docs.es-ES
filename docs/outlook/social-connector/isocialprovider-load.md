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
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285766"
---
# <a name="isocialproviderload"></a><span data-ttu-id="1ec4a-103">ISocialProvider::Load</span><span class="sxs-lookup"><span data-stu-id="1ec4a-103">ISocialProvider::Load</span></span>

<span data-ttu-id="1ec4a-104">Inicializa el proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="1ec4a-104">Initializes the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a><span data-ttu-id="1ec4a-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ec4a-105">Parameters</span></span>

<span data-ttu-id="1ec4a-106">_socialProviderInterfaceVersion_</span><span class="sxs-lookup"><span data-stu-id="1ec4a-106">_socialProviderInterfaceVersion_</span></span>
  
> <span data-ttu-id="1ec4a-107">[entrada] La versión de las interfaces del proveedor de OSC esperada por el OSC.</span><span class="sxs-lookup"><span data-stu-id="1ec4a-107">[in] The version of the OSC provider interfaces expected by the OSC.</span></span>
    
<span data-ttu-id="1ec4a-108">_languageTag_</span><span class="sxs-lookup"><span data-stu-id="1ec4a-108">_languageTag_</span></span>
  
> <span data-ttu-id="1ec4a-109">[entrada] La etiqueta de idioma del Grupo de trabajo de ingeniería de Internet (IETF), definida por [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) y [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), que representa el idioma actual de la interfaz de usuario de Outlook.</span><span class="sxs-lookup"><span data-stu-id="1ec4a-109">[in] The Internet Engineering Task Force (IETF) language tag, defined by [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), that represents the current Outlook user-interface language.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ec4a-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ec4a-110">Remarks</span></span>

<span data-ttu-id="1ec4a-111">El formato de versión del parámetro  _socialProviderInterfaceVersion_ es  _X_. _xxxx_, donde  _X_ es la versión principal y  _xxxx_ es la versión secundaria del OSC.</span><span class="sxs-lookup"><span data-stu-id="1ec4a-111">The version format for the  _socialProviderInterfaceVersion_ parameter is  _X_. _xxxx_, where  _X_ is the major version and  _xxxx_ is the minor version of the OSC.</span></span> <span data-ttu-id="1ec4a-112">Para Office 2013, compruebe que la versión principal sea 15.</span><span class="sxs-lookup"><span data-stu-id="1ec4a-112">For Office 2013, check for the major version being 15.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ec4a-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ec4a-113">See also</span></span>

- [<span data-ttu-id="1ec4a-114">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1ec4a-114">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

