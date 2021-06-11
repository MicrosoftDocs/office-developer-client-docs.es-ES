---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5e623c9d40ffd2dd276bd9601676244644bb3402
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417710"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="5237e-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="5237e-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="5237e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5237e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5237e-105">Indica si el modo Exchange caché para la carpeta Favoritos de **carpetas** públicas está habilitado y si se aplica mediante directiva.</span><span class="sxs-lookup"><span data-stu-id="5237e-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="5237e-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="5237e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5237e-107">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="5237e-107">Exported by:</span></span>  <br/> |<span data-ttu-id="5237e-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="5237e-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="5237e-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="5237e-109">Called by:</span></span>  <br/> |<span data-ttu-id="5237e-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="5237e-110">Client</span></span>  <br/> |
|<span data-ttu-id="5237e-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5237e-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="5237e-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="5237e-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="5237e-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="5237e-113">Parameters</span></span>

 <span data-ttu-id="5237e-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="5237e-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="5237e-115">[salida] **true** si la directiva aplica el valor devuelto, **false** si no lo es.</span><span class="sxs-lookup"><span data-stu-id="5237e-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="5237e-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="5237e-116">Return values</span></span>

 <span data-ttu-id="5237e-117">**true**</span><span class="sxs-lookup"><span data-stu-id="5237e-117">**true**</span></span>
  
- <span data-ttu-id="5237e-118">El almacenamiento en caché está habilitado.</span><span class="sxs-lookup"><span data-stu-id="5237e-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="5237e-119">**false**</span><span class="sxs-lookup"><span data-stu-id="5237e-119">**false**</span></span>
  
- <span data-ttu-id="5237e-120">El almacenamiento en caché está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="5237e-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5237e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="5237e-121">See also</span></span>



[<span data-ttu-id="5237e-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="5237e-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

