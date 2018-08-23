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
ms.openlocfilehash: 91a56acf4afc7453496fa89becd905184101c910
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591397"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="19212-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="19212-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="19212-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19212-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19212-105">Indica si está habilitado el modo de intercambio en caché para el almacén de Exchange privado y, si esto se aplica mediante una directiva.</span><span class="sxs-lookup"><span data-stu-id="19212-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="19212-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="19212-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19212-107">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="19212-107">Exported by:</span></span>  <br/> |<span data-ttu-id="19212-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="19212-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="19212-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="19212-109">Called by:</span></span>  <br/> |<span data-ttu-id="19212-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="19212-110">Client</span></span>  <br/> |
|<span data-ttu-id="19212-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="19212-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="19212-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="19212-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="19212-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19212-113">Parameters</span></span>

 <span data-ttu-id="19212-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="19212-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="19212-115">[out] **true** si se aplica el valor devuelto por la directiva, **false** si no lo está.</span><span class="sxs-lookup"><span data-stu-id="19212-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="19212-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="19212-116">Return values</span></span>

 <span data-ttu-id="19212-117">**True**</span><span class="sxs-lookup"><span data-stu-id="19212-117">**true**</span></span>
  
- <span data-ttu-id="19212-118">Almacenamiento en caché está habilitado.</span><span class="sxs-lookup"><span data-stu-id="19212-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="19212-119">**False**</span><span class="sxs-lookup"><span data-stu-id="19212-119">**false**</span></span>
  
- <span data-ttu-id="19212-120">Se deshabilita el almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="19212-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19212-121">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="19212-121">See also</span></span>



[<span data-ttu-id="19212-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="19212-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

