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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385833"
---
# <a name="isocialproviderload"></a><span data-ttu-id="d5724-103">ISocialProvider::Load</span><span class="sxs-lookup"><span data-stu-id="d5724-103">ISocialProvider::Load</span></span>

<span data-ttu-id="d5724-104">Inicializa el proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="d5724-104">Initializes the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a><span data-ttu-id="d5724-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5724-105">Parameters</span></span>

<span data-ttu-id="d5724-106">_socialProviderInterfaceVersion_</span><span class="sxs-lookup"><span data-stu-id="d5724-106">_socialProviderInterfaceVersion_</span></span>
  
> <span data-ttu-id="d5724-107">[entrada] La versión de las interfaces de proveedor OSC esperado por el OSC.</span><span class="sxs-lookup"><span data-stu-id="d5724-107">[in] The version of the OSC provider interfaces expected by the OSC.</span></span>
    
<span data-ttu-id="d5724-108">_languageTag_</span><span class="sxs-lookup"><span data-stu-id="d5724-108">_languageTag_</span></span>
  
> <span data-ttu-id="d5724-109">[entrada] La etiqueta de idioma de ingeniería de Internet (IETF), definida por [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) y [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), que representa el idioma de interfaz de usuario de Outlook actual.</span><span class="sxs-lookup"><span data-stu-id="d5724-109">[in] The Internet Engineering Task Force (IETF) language tag, defined by [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), that represents the current Outlook user-interface language.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5724-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5724-110">Remarks</span></span>

<span data-ttu-id="d5724-111">El formato de versión para el parámetro _socialProviderInterfaceVersion_ es _X_. _xxxx_, donde _X_ es la versión principal y _xxxx_ es la versión secundaria de la OSC.</span><span class="sxs-lookup"><span data-stu-id="d5724-111">The version format for the  _socialProviderInterfaceVersion_ parameter is  _X_. _xxxx_, where  _X_ is the major version and  _xxxx_ is the minor version of the OSC.</span></span> <span data-ttu-id="d5724-112">Para Office 2013, compruebe si la versión principal que se va a 15.</span><span class="sxs-lookup"><span data-stu-id="d5724-112">For Office 2013, check for the major version being 15.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d5724-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5724-113">See also</span></span>

- [<span data-ttu-id="d5724-114">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5724-114">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

