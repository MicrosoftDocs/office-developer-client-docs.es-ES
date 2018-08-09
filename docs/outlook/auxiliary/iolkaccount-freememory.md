---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Libera memoria asignada por la interfaz IOlkAccount.
ms.openlocfilehash: ce3046db29cb2cac7d7ee72a3e4e9125346a4ac4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816162"
---
# <a name="iolkaccountfreememory"></a><span data-ttu-id="ea45f-103">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="ea45f-103">IOlkAccount::FreeMemory</span></span>

<span data-ttu-id="ea45f-104">Libera memoria asignada por la interfaz [IOlkAccount](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="ea45f-104">Frees memory allocated by the [IOlkAccount](iolkaccount.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="ea45f-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="ea45f-105">Quick info</span></span>

<span data-ttu-id="ea45f-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="ea45f-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a><span data-ttu-id="ea45f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea45f-107">Parameters</span></span>

<span data-ttu-id="ea45f-108">_PV_</span><span class="sxs-lookup"><span data-stu-id="ea45f-108">_pv_</span></span>
  
> <span data-ttu-id="ea45f-109">[entrada] Un puntero a la memoria que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="ea45f-109">[in] A pointer to memory to be freed.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ea45f-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="ea45f-110">Return values</span></span>

<span data-ttu-id="ea45f-111">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="ea45f-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ea45f-112">Notas</span><span class="sxs-lookup"><span data-stu-id="ea45f-112">Remarks</span></span>

<span data-ttu-id="ea45f-113">Use este método para liberar memoria asignada por [IOlkAccount::GetProp](iolkaccount-getprop.md) (si el valor de la propiedad de la cuenta especificada es un tipo de archivo binario o cadena) y [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).</span><span class="sxs-lookup"><span data-stu-id="ea45f-113">Use this method to free memory allocated by [IOlkAccount::GetProp](iolkaccount-getprop.md) (if the value of the specified account property is a binary or string type) and [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ea45f-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea45f-114">See also</span></span>

- [<span data-ttu-id="ea45f-115">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="ea45f-115">IOlkAccount::GetAccountInfo</span></span>](iolkaccount-getaccountinfo.md)  
- [<span data-ttu-id="ea45f-116">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="ea45f-116">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

