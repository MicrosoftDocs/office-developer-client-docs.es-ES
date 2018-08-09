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
ms.openlocfilehash: 7595fac4346a537eed86550432f56a761c27c0ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816944"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="a49a9-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="a49a9-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="a49a9-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a49a9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a49a9-105">Indica si está habilitado el modo de intercambio en caché para el almacén de Exchange privado y, si esto se aplica mediante una directiva.</span><span class="sxs-lookup"><span data-stu-id="a49a9-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a49a9-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="a49a9-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a49a9-107">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="a49a9-107">Exported by:</span></span>  <br/> |<span data-ttu-id="a49a9-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="a49a9-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="a49a9-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a49a9-109">Called by:</span></span>  <br/> |<span data-ttu-id="a49a9-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="a49a9-110">Client</span></span>  <br/> |
|<span data-ttu-id="a49a9-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="a49a9-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="a49a9-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="a49a9-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="a49a9-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a49a9-113">Parameters</span></span>

 <span data-ttu-id="a49a9-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="a49a9-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="a49a9-115">[out] **true** si se aplica el valor devuelto por la directiva, **false** si no lo está.</span><span class="sxs-lookup"><span data-stu-id="a49a9-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a49a9-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="a49a9-116">Return values</span></span>

 <span data-ttu-id="a49a9-117">**True**</span><span class="sxs-lookup"><span data-stu-id="a49a9-117">**true**</span></span>
  
- <span data-ttu-id="a49a9-118">Almacenamiento en caché está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a49a9-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="a49a9-119">**False**</span><span class="sxs-lookup"><span data-stu-id="a49a9-119">**false**</span></span>
  
- <span data-ttu-id="a49a9-120">Se deshabilita el almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="a49a9-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a49a9-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a49a9-121">See also</span></span>



[<span data-ttu-id="a49a9-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="a49a9-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

