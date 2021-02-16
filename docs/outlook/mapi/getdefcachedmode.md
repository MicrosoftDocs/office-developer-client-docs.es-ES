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
# <a name="getdefcachedmode"></a><span data-ttu-id="d282d-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="d282d-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="d282d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d282d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d282d-105">Indica si el modo caché de Exchange para el almacén de Exchange privado está habilitado y si esto se aplica mediante la directiva.</span><span class="sxs-lookup"><span data-stu-id="d282d-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d282d-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="d282d-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d282d-107">Exportado por:</span><span class="sxs-lookup"><span data-stu-id="d282d-107">Exported by:</span></span>  <br/> |<span data-ttu-id="d282d-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="d282d-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="d282d-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d282d-109">Called by:</span></span>  <br/> |<span data-ttu-id="d282d-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="d282d-110">Client</span></span>  <br/> |
|<span data-ttu-id="d282d-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d282d-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="d282d-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="d282d-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="d282d-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d282d-113">Parameters</span></span>

 <span data-ttu-id="d282d-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="d282d-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="d282d-115">[salida] **true** si la directiva aplica el valor devuelto, **false** si no lo es.</span><span class="sxs-lookup"><span data-stu-id="d282d-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="d282d-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="d282d-116">Return values</span></span>

 <span data-ttu-id="d282d-117">**true**</span><span class="sxs-lookup"><span data-stu-id="d282d-117">**true**</span></span>
  
- <span data-ttu-id="d282d-118">El almacenamiento en caché está habilitado.</span><span class="sxs-lookup"><span data-stu-id="d282d-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="d282d-119">**false**</span><span class="sxs-lookup"><span data-stu-id="d282d-119">**false**</span></span>
  
- <span data-ttu-id="d282d-120">El almacenamiento en caché está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="d282d-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d282d-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d282d-121">See also</span></span>



[<span data-ttu-id="d282d-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="d282d-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

