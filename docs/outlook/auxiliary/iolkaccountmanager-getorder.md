---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Obtiene el orden de la categoría especificada de cuentas.
ms.openlocfilehash: d05e354e25d49a51b3d3f8f053c2b39dc37b333f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816230"
---
# <a name="iolkaccountmanagergetorder"></a><span data-ttu-id="e6b36-103">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="e6b36-103">IOlkAccountManager::GetOrder</span></span>

<span data-ttu-id="e6b36-104">Obtiene el orden de la categoría especificada de cuentas.</span><span class="sxs-lookup"><span data-stu-id="e6b36-104">Gets the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e6b36-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="e6b36-105">Quick info</span></span>

<span data-ttu-id="e6b36-106">Vea [IOlkAccountManager](iolkaccountmanager.md)</span><span class="sxs-lookup"><span data-stu-id="e6b36-106">See [IOlkAccountManager](iolkaccountmanager.md)</span></span>
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a><span data-ttu-id="e6b36-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6b36-107">Parameters</span></span>

<span data-ttu-id="e6b36-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="e6b36-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="e6b36-109">[entrada] El identificador de clase de categoría para la que se va a obtener el orden.</span><span class="sxs-lookup"><span data-stu-id="e6b36-109">[in] The category class ID for which to get the order.</span></span> <span data-ttu-id="e6b36-110">El valor debe ser uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="e6b36-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="e6b36-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="e6b36-111">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="e6b36-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="e6b36-112">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="e6b36-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="e6b36-113">CLSID_OlkStore</span></span>
    
<span data-ttu-id="e6b36-114">_pcAccts_</span><span class="sxs-lookup"><span data-stu-id="e6b36-114">_pcAccts_</span></span>
  
>  <span data-ttu-id="e6b36-115">[out] El número de cuentas.</span><span class="sxs-lookup"><span data-stu-id="e6b36-115">[out] The number of accounts.</span></span> 
    
<span data-ttu-id="e6b36-116">_prgAccts_</span><span class="sxs-lookup"><span data-stu-id="e6b36-116">_prgAccts_</span></span>
  
> <span data-ttu-id="e6b36-117">[out] Un puntero a una matriz de las cuentas.</span><span class="sxs-lookup"><span data-stu-id="e6b36-117">[out] A pointer to an array of accounts.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="e6b36-118">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="e6b36-118">Return values</span></span>

|<span data-ttu-id="e6b36-119">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="e6b36-119">**HRESULT**</span></span>|<span data-ttu-id="e6b36-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="e6b36-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6b36-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6b36-121">S_OK</span></span>  <br/> |<span data-ttu-id="e6b36-122">La llamada se ha realizado correctamente</span><span class="sxs-lookup"><span data-stu-id="e6b36-122">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="e6b36-123">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e6b36-123">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e6b36-124">Uno o más argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="e6b36-124">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="e6b36-125">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e6b36-125">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="e6b36-126">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="e6b36-126">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6b36-127">Notas</span><span class="sxs-lookup"><span data-stu-id="e6b36-127">Remarks</span></span>

<span data-ttu-id="e6b36-128">Antes de llamar a este método, el autor de la llamada asigna sólo de puntero de matriz *prgAccts* pero no hay memoria para la matriz en qué momentos *prgAccts* .</span><span class="sxs-lookup"><span data-stu-id="e6b36-128">Before calling this method, the caller allocates only an array pointer  *prgAccts*  but no memory for the array at which  *prgAccts*  points.</span></span> <span data-ttu-id="e6b36-129">Después de que devuelve este método, el autor de la llamada debe usar [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) para liberar la memoria asignada para *prgAccts* .</span><span class="sxs-lookup"><span data-stu-id="e6b36-129">After this method returns, the caller must use [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) to release the memory allocated for  *prgAccts*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6b36-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6b36-130">See also</span></span>

- [<span data-ttu-id="e6b36-131">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="e6b36-131">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="e6b36-132">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="e6b36-132">IOlkAccountManager::SetOrder</span></span>](iolkaccountmanager-setorder.md)

