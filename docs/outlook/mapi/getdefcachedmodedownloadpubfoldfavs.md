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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299891"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="7d598-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="7d598-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="7d598-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d598-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d598-105">Indica si está habilitado el modo caché de Exchange para la carpeta favoritos de la **carpeta pública** y si lo exige la Directiva.</span><span class="sxs-lookup"><span data-stu-id="7d598-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7d598-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="7d598-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d598-107">ExPortado por:</span><span class="sxs-lookup"><span data-stu-id="7d598-107">Exported by:</span></span>  <br/> |<span data-ttu-id="7d598-108">MSMAPI32. dll</span><span class="sxs-lookup"><span data-stu-id="7d598-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="7d598-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="7d598-109">Called by:</span></span>  <br/> |<span data-ttu-id="7d598-110">Client</span><span class="sxs-lookup"><span data-stu-id="7d598-110">Client</span></span>  <br/> |
|<span data-ttu-id="7d598-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="7d598-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="7d598-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="7d598-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="7d598-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="7d598-113">Parameters</span></span>

 <span data-ttu-id="7d598-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="7d598-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="7d598-115">contempla **true** si la Directiva aplica el valor devuelto, **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7d598-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="7d598-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="7d598-116">Return values</span></span>

 <span data-ttu-id="7d598-117">**true**</span><span class="sxs-lookup"><span data-stu-id="7d598-117">**true**</span></span>
  
- <span data-ttu-id="7d598-118">El almacenamiento en caché está habilitado.</span><span class="sxs-lookup"><span data-stu-id="7d598-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="7d598-119">**false**</span><span class="sxs-lookup"><span data-stu-id="7d598-119">**false**</span></span>
  
- <span data-ttu-id="7d598-120">El almacenamiento en caché está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="7d598-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d598-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d598-121">See also</span></span>



[<span data-ttu-id="7d598-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="7d598-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

