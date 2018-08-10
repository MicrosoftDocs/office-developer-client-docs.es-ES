---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Modifica el orden de la categoría especificada de cuentas.
ms.openlocfilehash: fcb27404471c9b551320027b0ed6979926ad3d58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816226"
---
# <a name="iolkaccountmanagersetorder"></a><span data-ttu-id="64ce6-103">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="64ce6-103">IOlkAccountManager::SetOrder</span></span>

<span data-ttu-id="64ce6-104">Modifica el orden de la categoría especificada de cuentas.</span><span class="sxs-lookup"><span data-stu-id="64ce6-104">Modifies the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="64ce6-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="64ce6-105">Quick info</span></span>

<span data-ttu-id="64ce6-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="64ce6-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a><span data-ttu-id="64ce6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64ce6-107">Parameters</span></span>

<span data-ttu-id="64ce6-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="64ce6-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="64ce6-109">[entrada] El identificador de clase de categoría para la que se va a establecer el orden.</span><span class="sxs-lookup"><span data-stu-id="64ce6-109">[in] The category class ID for which to set the order.</span></span> <span data-ttu-id="64ce6-110">El valor debe ser uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="64ce6-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="64ce6-111">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="64ce6-111">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="64ce6-112">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="64ce6-112">CLSID_OlkStore</span></span>
    
<span data-ttu-id="64ce6-113">_cAccts_</span><span class="sxs-lookup"><span data-stu-id="64ce6-113">_cAccts_</span></span>
  
> <span data-ttu-id="64ce6-114">[entrada] El número de cuentas.</span><span class="sxs-lookup"><span data-stu-id="64ce6-114">[in] The number of accounts.</span></span>
    
<span data-ttu-id="64ce6-115">_rgAccts_</span><span class="sxs-lookup"><span data-stu-id="64ce6-115">_rgAccts_</span></span>
  
> <span data-ttu-id="64ce6-116">[entrada] Una matriz de identificadores de cuenta.</span><span class="sxs-lookup"><span data-stu-id="64ce6-116">[in] An array of account IDs.</span></span> <span data-ttu-id="64ce6-117">El tamaño de la matriz es _cAccts_.</span><span class="sxs-lookup"><span data-stu-id="64ce6-117">The size of the array is  _cAccts_.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="64ce6-118">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="64ce6-118">Return values</span></span>

|<span data-ttu-id="64ce6-119">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="64ce6-119">**HRESULT**</span></span>|<span data-ttu-id="64ce6-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="64ce6-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="64ce6-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="64ce6-121">S_OK</span></span>  <br/> |<span data-ttu-id="64ce6-122">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="64ce6-122">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="64ce6-123">E_ACCT_WRONG_SORT_ORDER</span><span class="sxs-lookup"><span data-stu-id="64ce6-123">E_ACCT_WRONG_SORT_ORDER</span></span>  <br/> |<span data-ttu-id="64ce6-124">El nuevo criterio de ordenación tiene un número diferente de las cuentas que el criterio de ordenación anterior.</span><span class="sxs-lookup"><span data-stu-id="64ce6-124">The new sort order has a different number of accounts than the old sort order.</span></span>  <br/> |
|<span data-ttu-id="64ce6-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="64ce6-125">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="64ce6-126">Uno o más argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="64ce6-126">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="64ce6-127">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="64ce6-127">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="64ce6-128">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="64ce6-128">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64ce6-129">Notas</span><span class="sxs-lookup"><span data-stu-id="64ce6-129">Remarks</span></span>

<span data-ttu-id="64ce6-130">El autor de la llamada asigna memoria para el puntero de matriz _prgAccts_ así como para la matriz en qué momentos _prgAccts_ .</span><span class="sxs-lookup"><span data-stu-id="64ce6-130">The caller allocates memory for the array pointer  _prgAccts_ as well as for the array at which  _prgAccts_ points.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64ce6-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="64ce6-131">See also</span></span>

- [<span data-ttu-id="64ce6-132">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="64ce6-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="64ce6-133">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="64ce6-133">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)
