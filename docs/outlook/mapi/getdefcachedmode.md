---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 7595fac4346a537eed86550432f56a761c27c0ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816944"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="df3ae-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="df3ae-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="df3ae-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df3ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df3ae-105">Indica si está habilitado el modo de intercambio en caché para el almacén de Exchange privado y, si esto se aplica mediante una directiva.</span><span class="sxs-lookup"><span data-stu-id="df3ae-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="df3ae-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="df3ae-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df3ae-107">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="df3ae-107">Exported by:</span></span>  <br/> |<span data-ttu-id="df3ae-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="df3ae-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="df3ae-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="df3ae-109">Called by:</span></span>  <br/> |<span data-ttu-id="df3ae-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="df3ae-110">Client</span></span>  <br/> |
|<span data-ttu-id="df3ae-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="df3ae-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="df3ae-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="df3ae-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="df3ae-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df3ae-113">Parameters</span></span>

 <span data-ttu-id="df3ae-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="df3ae-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="df3ae-115">[out] **true** si se aplica el valor devuelto por la directiva, **false** si no lo está.</span><span class="sxs-lookup"><span data-stu-id="df3ae-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="df3ae-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="df3ae-116">Return values</span></span>

 <span data-ttu-id="df3ae-117">**True**</span><span class="sxs-lookup"><span data-stu-id="df3ae-117">**true**</span></span>
  
- <span data-ttu-id="df3ae-118">Almacenamiento en caché está habilitado.</span><span class="sxs-lookup"><span data-stu-id="df3ae-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="df3ae-119">**False**</span><span class="sxs-lookup"><span data-stu-id="df3ae-119">**false**</span></span>
  
- <span data-ttu-id="df3ae-120">Se deshabilita el almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="df3ae-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df3ae-121">Ver también</span><span class="sxs-lookup"><span data-stu-id="df3ae-121">See also</span></span>



[<span data-ttu-id="df3ae-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="df3ae-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

