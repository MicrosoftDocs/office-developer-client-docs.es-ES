---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8e8a6ac07e14af52337b6e280fa58274df453c65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299709"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="8ed24-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="8ed24-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="8ed24-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ed24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ed24-105">Indica si el modo caché de Exchange del almacén privado de Exchange está habilitado y si lo exige la Directiva.</span><span class="sxs-lookup"><span data-stu-id="8ed24-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8ed24-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="8ed24-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ed24-107">ExPortado por:</span><span class="sxs-lookup"><span data-stu-id="8ed24-107">Exported by:</span></span>  <br/> |<span data-ttu-id="8ed24-108">MSMAPI32. dll</span><span class="sxs-lookup"><span data-stu-id="8ed24-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="8ed24-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="8ed24-109">Called by:</span></span>  <br/> |<span data-ttu-id="8ed24-110">Client</span><span class="sxs-lookup"><span data-stu-id="8ed24-110">Client</span></span>  <br/> |
|<span data-ttu-id="8ed24-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="8ed24-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="8ed24-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="8ed24-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="8ed24-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="8ed24-113">Parameters</span></span>

 <span data-ttu-id="8ed24-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="8ed24-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="8ed24-115">contempla **true** si la Directiva aplica el valor devuelto, **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8ed24-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="8ed24-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="8ed24-116">Return values</span></span>

 <span data-ttu-id="8ed24-117">**true**</span><span class="sxs-lookup"><span data-stu-id="8ed24-117">**true**</span></span>
  
- <span data-ttu-id="8ed24-118">El almacenamiento en caché está habilitado.</span><span class="sxs-lookup"><span data-stu-id="8ed24-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="8ed24-119">**false**</span><span class="sxs-lookup"><span data-stu-id="8ed24-119">**false**</span></span>
  
- <span data-ttu-id="8ed24-120">El almacenamiento en caché está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8ed24-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ed24-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ed24-121">See also</span></span>



[<span data-ttu-id="8ed24-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="8ed24-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

