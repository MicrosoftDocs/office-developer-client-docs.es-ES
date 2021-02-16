---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Libera la memoria asignada por la interfaz IOlkAccountManager.
ms.openlocfilehash: 3e680e1e26d6c9b12c2dd4a7d48df4dbeae14154
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408491"
---
# <a name="iolkaccountmanagerfreememory"></a><span data-ttu-id="c13af-103">IOlkAccountManager::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="c13af-103">IOlkAccountManager::FreeMemory</span></span>

<span data-ttu-id="c13af-104">Libera la memoria asignada por la [interfaz IOlkAccountManager.](iolkaccountmanager.md)</span><span class="sxs-lookup"><span data-stu-id="c13af-104">Frees memory allocated by the [IOlkAccountManager](iolkaccountmanager.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c13af-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="c13af-105">Quick info</span></span>

<span data-ttu-id="c13af-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="c13af-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a><span data-ttu-id="c13af-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c13af-107">Parameters</span></span>

<span data-ttu-id="c13af-108">_pv_</span><span class="sxs-lookup"><span data-stu-id="c13af-108">_pv_</span></span>
  
> <span data-ttu-id="c13af-109">[entrada] Puntero a la memoria que se liberará.</span><span class="sxs-lookup"><span data-stu-id="c13af-109">[in] A pointer to the memory to free.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="c13af-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="c13af-110">Return values</span></span>

<span data-ttu-id="c13af-111">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="c13af-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c13af-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c13af-112">Remarks</span></span>

<span data-ttu-id="c13af-113">Use este método para liberar memoria asignada por [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span><span class="sxs-lookup"><span data-stu-id="c13af-113">Use this method to release memory allocated by [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c13af-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c13af-114">See also</span></span>

- [<span data-ttu-id="c13af-115">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="c13af-115">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

