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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412747"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="327dc-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="327dc-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="327dc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="327dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="327dc-105">Indica si el modo caché de Exchange del almacén privado de Exchange está habilitado y si lo exige la Directiva.</span><span class="sxs-lookup"><span data-stu-id="327dc-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="327dc-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="327dc-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="327dc-107">ExPortado por:</span><span class="sxs-lookup"><span data-stu-id="327dc-107">Exported by:</span></span>  <br/> |<span data-ttu-id="327dc-108">MSMAPI32. dll</span><span class="sxs-lookup"><span data-stu-id="327dc-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="327dc-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="327dc-109">Called by:</span></span>  <br/> |<span data-ttu-id="327dc-110">Client</span><span class="sxs-lookup"><span data-stu-id="327dc-110">Client</span></span>  <br/> |
|<span data-ttu-id="327dc-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="327dc-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="327dc-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="327dc-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="327dc-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="327dc-113">Parameters</span></span>

 <span data-ttu-id="327dc-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="327dc-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="327dc-115">contempla **true** si la Directiva aplica el valor devuelto, **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="327dc-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="327dc-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="327dc-116">Return values</span></span>

 <span data-ttu-id="327dc-117">**caso**</span><span class="sxs-lookup"><span data-stu-id="327dc-117">**true**</span></span>
  
- <span data-ttu-id="327dc-118">El almacenamiento en caché está habilitado.</span><span class="sxs-lookup"><span data-stu-id="327dc-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="327dc-119">**false**</span><span class="sxs-lookup"><span data-stu-id="327dc-119">**false**</span></span>
  
- <span data-ttu-id="327dc-120">El almacenamiento en caché está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="327dc-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="327dc-121">Ver también</span><span class="sxs-lookup"><span data-stu-id="327dc-121">See also</span></span>



[<span data-ttu-id="327dc-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="327dc-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

