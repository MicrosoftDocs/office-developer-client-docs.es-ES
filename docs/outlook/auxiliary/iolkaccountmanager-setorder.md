---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Modifica el orden de la categoría de cuentas especificada.
ms.openlocfilehash: 29dfe4fd1bda9e323481297167361650c3b3a173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422862"
---
# <a name="iolkaccountmanagersetorder"></a><span data-ttu-id="ec8b1-103">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="ec8b1-103">IOlkAccountManager::SetOrder</span></span>

<span data-ttu-id="ec8b1-104">Modifica el orden de la categoría de cuentas especificada.</span><span class="sxs-lookup"><span data-stu-id="ec8b1-104">Modifies the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ec8b1-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="ec8b1-105">Quick info</span></span>

<span data-ttu-id="ec8b1-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="ec8b1-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a><span data-ttu-id="ec8b1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec8b1-107">Parameters</span></span>

<span data-ttu-id="ec8b1-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="ec8b1-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="ec8b1-109">[entrada] Identificador de clase de categoría para el que se va a establecer el orden.</span><span class="sxs-lookup"><span data-stu-id="ec8b1-109">[in] The category class ID for which to set the order.</span></span> <span data-ttu-id="ec8b1-110">El valor debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="ec8b1-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="ec8b1-111">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="ec8b1-111">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="ec8b1-112">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="ec8b1-112">CLSID_OlkStore</span></span>
    
<span data-ttu-id="ec8b1-113">_cAccts_</span><span class="sxs-lookup"><span data-stu-id="ec8b1-113">_cAccts_</span></span>
  
> <span data-ttu-id="ec8b1-114">[entrada] El número de cuentas.</span><span class="sxs-lookup"><span data-stu-id="ec8b1-114">[in] The number of accounts.</span></span>
    
<span data-ttu-id="ec8b1-115">_rgAccts_</span><span class="sxs-lookup"><span data-stu-id="ec8b1-115">_rgAccts_</span></span>
  
> <span data-ttu-id="ec8b1-116">[entrada] Una matriz de los IDs de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="ec8b1-116">[in] An array of account IDs.</span></span> <span data-ttu-id="ec8b1-117">El tamaño de la matriz  _es cAccts_.</span><span class="sxs-lookup"><span data-stu-id="ec8b1-117">The size of the array is  _cAccts_.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ec8b1-118">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="ec8b1-118">Return values</span></span>

|<span data-ttu-id="ec8b1-119">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="ec8b1-119">**HRESULT**</span></span>|<span data-ttu-id="ec8b1-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="ec8b1-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ec8b1-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec8b1-121">S_OK</span></span>  <br/> |<span data-ttu-id="ec8b1-122">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="ec8b1-122">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="ec8b1-123">E_ACCT_WRONG_SORT_ORDER</span><span class="sxs-lookup"><span data-stu-id="ec8b1-123">E_ACCT_WRONG_SORT_ORDER</span></span>  <br/> |<span data-ttu-id="ec8b1-124">El nuevo criterio de ordenación tiene un número diferente de cuentas que el criterio de ordenación anterior.</span><span class="sxs-lookup"><span data-stu-id="ec8b1-124">The new sort order has a different number of accounts than the old sort order.</span></span>  <br/> |
|<span data-ttu-id="ec8b1-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ec8b1-125">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ec8b1-126">Uno o más argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="ec8b1-126">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="ec8b1-127">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ec8b1-127">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="ec8b1-128">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="ec8b1-128">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec8b1-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ec8b1-129">Remarks</span></span>

<span data-ttu-id="ec8b1-130">El llamador asigna memoria para el puntero de matriz _prgAccts,_ así como para la matriz a la que _apunta prgAccts._</span><span class="sxs-lookup"><span data-stu-id="ec8b1-130">The caller allocates memory for the array pointer  _prgAccts_ as well as for the array at which  _prgAccts_ points.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ec8b1-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ec8b1-131">See also</span></span>

- [<span data-ttu-id="ec8b1-132">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="ec8b1-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="ec8b1-133">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="ec8b1-133">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

