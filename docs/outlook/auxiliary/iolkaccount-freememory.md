---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Libera la memoria asignada por la interfaz IOlkAccount.
ms.openlocfilehash: a7f763ba4fc260a517f8b7df4d3791f4a8fd23b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321339"
---
# <a name="iolkaccountfreememory"></a><span data-ttu-id="40948-103">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="40948-103">IOlkAccount::FreeMemory</span></span>

<span data-ttu-id="40948-104">Libera la memoria asignada por la interfaz [IOlkAccount](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="40948-104">Frees memory allocated by the [IOlkAccount](iolkaccount.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="40948-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="40948-105">Quick info</span></span>

<span data-ttu-id="40948-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="40948-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a><span data-ttu-id="40948-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="40948-107">Parameters</span></span>

<span data-ttu-id="40948-108">_argumento_</span><span class="sxs-lookup"><span data-stu-id="40948-108">_pv_</span></span>
  
> <span data-ttu-id="40948-109">a Puntero a la memoria que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="40948-109">[in] A pointer to memory to be freed.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="40948-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="40948-110">Return values</span></span>

<span data-ttu-id="40948-111">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="40948-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="40948-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40948-112">Remarks</span></span>

<span data-ttu-id="40948-113">Use este método para liberar la memoria asignada por [IOlkAccount:: GetProp](iolkaccount-getprop.md) (si el valor de la propiedad Account especificada es un tipo binary o String) y [IOlkAccount:: GetAccountInfo](iolkaccount-getaccountinfo.md).</span><span class="sxs-lookup"><span data-stu-id="40948-113">Use this method to free memory allocated by [IOlkAccount::GetProp](iolkaccount-getprop.md) (if the value of the specified account property is a binary or string type) and [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="40948-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="40948-114">See also</span></span>

- [<span data-ttu-id="40948-115">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="40948-115">IOlkAccount::GetAccountInfo</span></span>](iolkaccount-getaccountinfo.md)  
- [<span data-ttu-id="40948-116">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="40948-116">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

