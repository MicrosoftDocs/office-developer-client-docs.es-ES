---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Libera memoria asignada por la interfaz IOlkAccountManager.
ms.openlocfilehash: 85ba4d0d47eb5c879fa562e3147860533ef59f23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816218"
---
# <a name="iolkaccountmanagerfreememory"></a><span data-ttu-id="6ee73-103">IOlkAccountManager::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="6ee73-103">IOlkAccountManager::FreeMemory</span></span>

<span data-ttu-id="6ee73-104">Libera memoria asignada por la interfaz [IOlkAccountManager](iolkaccountmanager.md) .</span><span class="sxs-lookup"><span data-stu-id="6ee73-104">Frees memory allocated by the [IOlkAccountManager](iolkaccountmanager.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="6ee73-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="6ee73-105">Quick info</span></span>

<span data-ttu-id="6ee73-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="6ee73-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a><span data-ttu-id="6ee73-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ee73-107">Parameters</span></span>

<span data-ttu-id="6ee73-108">_PV_</span><span class="sxs-lookup"><span data-stu-id="6ee73-108">_pv_</span></span>
  
> <span data-ttu-id="6ee73-109">[entrada] Un puntero a la memoria para liberar.</span><span class="sxs-lookup"><span data-stu-id="6ee73-109">[in] A pointer to the memory to free.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="6ee73-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="6ee73-110">Return values</span></span>

<span data-ttu-id="6ee73-111">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="6ee73-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6ee73-112">Notas</span><span class="sxs-lookup"><span data-stu-id="6ee73-112">Remarks</span></span>

<span data-ttu-id="6ee73-113">Use este método para liberar memoria asignada por [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span><span class="sxs-lookup"><span data-stu-id="6ee73-113">Use this method to release memory allocated by [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6ee73-114">Ver también</span><span class="sxs-lookup"><span data-stu-id="6ee73-114">See also</span></span>

- [<span data-ttu-id="6ee73-115">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="6ee73-115">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

