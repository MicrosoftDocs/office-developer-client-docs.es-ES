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
ms.openlocfilehash: ced6f2c6540e04a0bb4945ff98c4fda520322f03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581730"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="e6593-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="e6593-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="e6593-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6593-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6593-105">Indica si está habilitado el modo de intercambio en caché para la carpeta **Favoritos de carpetas públicas** y, si esto se aplica mediante una directiva.</span><span class="sxs-lookup"><span data-stu-id="e6593-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e6593-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="e6593-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6593-107">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="e6593-107">Exported by:</span></span>  <br/> |<span data-ttu-id="e6593-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="e6593-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="e6593-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e6593-109">Called by:</span></span>  <br/> |<span data-ttu-id="e6593-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="e6593-110">Client</span></span>  <br/> |
|<span data-ttu-id="e6593-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="e6593-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="e6593-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="e6593-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="e6593-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6593-113">Parameters</span></span>

 <span data-ttu-id="e6593-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="e6593-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="e6593-115">[out] **true** si se aplica el valor devuelto por la directiva, **false** si no lo está.</span><span class="sxs-lookup"><span data-stu-id="e6593-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="e6593-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="e6593-116">Return values</span></span>

 <span data-ttu-id="e6593-117">**True**</span><span class="sxs-lookup"><span data-stu-id="e6593-117">**true**</span></span>
  
- <span data-ttu-id="e6593-118">Almacenamiento en caché está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e6593-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="e6593-119">**False**</span><span class="sxs-lookup"><span data-stu-id="e6593-119">**false**</span></span>
  
- <span data-ttu-id="e6593-120">Se deshabilita el almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="e6593-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e6593-121">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e6593-121">See also</span></span>



[<span data-ttu-id="e6593-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="e6593-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

