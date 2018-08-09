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
ms.openlocfilehash: cb93d9ae4e6660c208d74e43bb26be4dbd55f4e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816943"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="7fdc4-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="7fdc4-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="7fdc4-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7fdc4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7fdc4-105">Indica si está habilitado el modo de intercambio en caché para la carpeta **Favoritos de carpetas públicas** y, si esto se aplica mediante una directiva.</span><span class="sxs-lookup"><span data-stu-id="7fdc4-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7fdc4-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="7fdc4-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fdc4-107">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="7fdc4-107">Exported by:</span></span>  <br/> |<span data-ttu-id="7fdc4-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="7fdc4-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="7fdc4-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="7fdc4-109">Called by:</span></span>  <br/> |<span data-ttu-id="7fdc4-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="7fdc4-110">Client</span></span>  <br/> |
|<span data-ttu-id="7fdc4-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="7fdc4-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="7fdc4-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="7fdc4-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="7fdc4-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fdc4-113">Parameters</span></span>

 <span data-ttu-id="7fdc4-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="7fdc4-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="7fdc4-115">[out] **true** si se aplica el valor devuelto por la directiva, **false** si no lo está.</span><span class="sxs-lookup"><span data-stu-id="7fdc4-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="7fdc4-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="7fdc4-116">Return values</span></span>

 <span data-ttu-id="7fdc4-117">**True**</span><span class="sxs-lookup"><span data-stu-id="7fdc4-117">**true**</span></span>
  
- <span data-ttu-id="7fdc4-118">Almacenamiento en caché está habilitado.</span><span class="sxs-lookup"><span data-stu-id="7fdc4-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="7fdc4-119">**False**</span><span class="sxs-lookup"><span data-stu-id="7fdc4-119">**false**</span></span>
  
- <span data-ttu-id="7fdc4-120">Se deshabilita el almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="7fdc4-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7fdc4-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fdc4-121">See also</span></span>



[<span data-ttu-id="7fdc4-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="7fdc4-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

