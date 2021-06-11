---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Obtiene el valor de la propiedad de cuenta especificada.
ms.openlocfilehash: d24df8cfa9d54bee4614c1f31e12268748b8c986
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433741"
---
# <a name="iolkaccountgetprop"></a><span data-ttu-id="919dc-103">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="919dc-103">IOlkAccount::GetProp</span></span>

<span data-ttu-id="919dc-104">Obtiene el valor de la propiedad de cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="919dc-104">Gets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="919dc-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="919dc-105">Quick info</span></span>

<span data-ttu-id="919dc-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="919dc-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="919dc-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="919dc-107">Parameters</span></span>

<span data-ttu-id="919dc-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="919dc-108">_dwProp_</span></span>
  
> <span data-ttu-id="919dc-109">[in] Etiqueta de propiedad de la propiedad account que se debe obtener.</span><span class="sxs-lookup"><span data-stu-id="919dc-109">[in] The property tag of the account property to get.</span></span>
    
<span data-ttu-id="919dc-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="919dc-110">_pVar_</span></span>
  
> <span data-ttu-id="919dc-111">[salida] Valor de la propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="919dc-111">[out] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="919dc-112">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="919dc-112">Return values</span></span>

|<span data-ttu-id="919dc-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="919dc-113">**HRESULT**</span></span>|<span data-ttu-id="919dc-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="919dc-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="919dc-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="919dc-115">S_OK</span></span>  <br/> |<span data-ttu-id="919dc-116">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="919dc-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="919dc-117">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="919dc-117">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="919dc-118">La propiedad no se encuentra para la cuenta determinada.</span><span class="sxs-lookup"><span data-stu-id="919dc-118">The property is not found for the given account.</span></span>  <br/> |
|<span data-ttu-id="919dc-119">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="919dc-119">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="919dc-120">Se ha especificado una etiqueta de propiedad no válida.</span><span class="sxs-lookup"><span data-stu-id="919dc-120">An invalid property tag has been specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="919dc-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="919dc-121">Remarks</span></span>

<span data-ttu-id="919dc-122">Después de que este método devuelva, si el valor de la propiedad account es un tipo binario o de cadena, debe liberar  *pVar*  mediante [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span><span class="sxs-lookup"><span data-stu-id="919dc-122">After this method returns, if the value of the account property is a binary or string type, you must free  *pVar*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="919dc-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="919dc-123">See also</span></span>

- [<span data-ttu-id="919dc-124">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="919dc-124">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="919dc-125">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="919dc-125">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)  
- [<span data-ttu-id="919dc-126">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="919dc-126">IOlkAccount::SetProp</span></span>](iolkaccount-setprop.md)

