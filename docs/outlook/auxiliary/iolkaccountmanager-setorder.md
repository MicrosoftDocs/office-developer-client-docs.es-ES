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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322046"
---
# <a name="iolkaccountmanagersetorder"></a><span data-ttu-id="868b5-103">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="868b5-103">IOlkAccountManager::SetOrder</span></span>

<span data-ttu-id="868b5-104">Modifica el orden de la categoría de cuentas especificada.</span><span class="sxs-lookup"><span data-stu-id="868b5-104">Modifies the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="868b5-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="868b5-105">Quick info</span></span>

<span data-ttu-id="868b5-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="868b5-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a><span data-ttu-id="868b5-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="868b5-107">Parameters</span></span>

<span data-ttu-id="868b5-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="868b5-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="868b5-109">a IDENTIFICADOR de clase de categoría para el que se va a establecer el orden.</span><span class="sxs-lookup"><span data-stu-id="868b5-109">[in] The category class ID for which to set the order.</span></span> <span data-ttu-id="868b5-110">El valor debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="868b5-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="868b5-111">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="868b5-111">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="868b5-112">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="868b5-112">CLSID_OlkStore</span></span>
    
<span data-ttu-id="868b5-113">_cAccts_</span><span class="sxs-lookup"><span data-stu-id="868b5-113">_cAccts_</span></span>
  
> <span data-ttu-id="868b5-114">a El número de cuentas.</span><span class="sxs-lookup"><span data-stu-id="868b5-114">[in] The number of accounts.</span></span>
    
<span data-ttu-id="868b5-115">_rgAccts_</span><span class="sxs-lookup"><span data-stu-id="868b5-115">_rgAccts_</span></span>
  
> <span data-ttu-id="868b5-116">a Una matriz de identificadores de cuenta.</span><span class="sxs-lookup"><span data-stu-id="868b5-116">[in] An array of account IDs.</span></span> <span data-ttu-id="868b5-117">El tamaño de la matriz es _cAccts_.</span><span class="sxs-lookup"><span data-stu-id="868b5-117">The size of the array is  _cAccts_.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="868b5-118">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="868b5-118">Return values</span></span>

|<span data-ttu-id="868b5-119">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="868b5-119">**HRESULT**</span></span>|<span data-ttu-id="868b5-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="868b5-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="868b5-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="868b5-121">S_OK</span></span>  <br/> |<span data-ttu-id="868b5-122">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="868b5-122">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="868b5-123">E_ACCT_WRONG_SORT_ORDER</span><span class="sxs-lookup"><span data-stu-id="868b5-123">E_ACCT_WRONG_SORT_ORDER</span></span>  <br/> |<span data-ttu-id="868b5-124">El nuevo criterio de ordenación tiene un número de cuentas distinto del criterio de ordenación anterior.</span><span class="sxs-lookup"><span data-stu-id="868b5-124">The new sort order has a different number of accounts than the old sort order.</span></span>  <br/> |
|<span data-ttu-id="868b5-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="868b5-125">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="868b5-126">Uno o más argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="868b5-126">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="868b5-127">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="868b5-127">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="868b5-128">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="868b5-128">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="868b5-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="868b5-129">Remarks</span></span>

<span data-ttu-id="868b5-130">El autor de la llamada asigna memoria para el puntero de matriz _prgAccts_ , así como para la matriz en la que apunta _prgAccts_ .</span><span class="sxs-lookup"><span data-stu-id="868b5-130">The caller allocates memory for the array pointer  _prgAccts_ as well as for the array at which  _prgAccts_ points.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="868b5-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="868b5-131">See also</span></span>

- [<span data-ttu-id="868b5-132">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="868b5-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="868b5-133">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="868b5-133">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

