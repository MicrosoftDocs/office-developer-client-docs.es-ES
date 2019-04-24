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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322060"
---
# <a name="iolkaccountmanagerfreememory"></a><span data-ttu-id="14977-103">IOlkAccountManager::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="14977-103">IOlkAccountManager::FreeMemory</span></span>

<span data-ttu-id="14977-104">Libera la memoria asignada por la interfaz [IOlkAccountManager](iolkaccountmanager.md) .</span><span class="sxs-lookup"><span data-stu-id="14977-104">Frees memory allocated by the [IOlkAccountManager](iolkaccountmanager.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="14977-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="14977-105">Quick info</span></span>

<span data-ttu-id="14977-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="14977-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a><span data-ttu-id="14977-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="14977-107">Parameters</span></span>

<span data-ttu-id="14977-108">_argumento_</span><span class="sxs-lookup"><span data-stu-id="14977-108">_pv_</span></span>
  
> <span data-ttu-id="14977-109">a Un puntero a la memoria que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="14977-109">[in] A pointer to the memory to free.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="14977-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="14977-110">Return values</span></span>

<span data-ttu-id="14977-111">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="14977-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="14977-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="14977-112">Remarks</span></span>

<span data-ttu-id="14977-113">Use este método para liberar la memoria asignada por [IOlkAccountManager:: GetOrder](iolkaccountmanager-getorder.md).</span><span class="sxs-lookup"><span data-stu-id="14977-113">Use this method to release memory allocated by [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="14977-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="14977-114">See also</span></span>

- [<span data-ttu-id="14977-115">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="14977-115">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

