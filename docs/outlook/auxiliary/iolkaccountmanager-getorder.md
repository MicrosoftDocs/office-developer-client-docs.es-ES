---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Obtiene el orden de la categoría de cuentas especificada.
ms.openlocfilehash: 3eb6dd96caa43f81eba86a389c938ef90c9533b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424626"
---
# <a name="iolkaccountmanagergetorder"></a><span data-ttu-id="9e0c7-103">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="9e0c7-103">IOlkAccountManager::GetOrder</span></span>

<span data-ttu-id="9e0c7-104">Obtiene el orden de la categoría de cuentas especificada.</span><span class="sxs-lookup"><span data-stu-id="9e0c7-104">Gets the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9e0c7-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="9e0c7-105">Quick info</span></span>

<span data-ttu-id="9e0c7-106">Consulta [IOlkAccountManager](iolkaccountmanager.md)</span><span class="sxs-lookup"><span data-stu-id="9e0c7-106">See [IOlkAccountManager](iolkaccountmanager.md)</span></span>
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a><span data-ttu-id="9e0c7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e0c7-107">Parameters</span></span>

<span data-ttu-id="9e0c7-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="9e0c7-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="9e0c7-109">[entrada] Identificador de clase de categoría para el que se va a obtener el pedido.</span><span class="sxs-lookup"><span data-stu-id="9e0c7-109">[in] The category class ID for which to get the order.</span></span> <span data-ttu-id="9e0c7-110">El valor debe ser uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="9e0c7-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="9e0c7-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="9e0c7-111">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="9e0c7-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="9e0c7-112">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="9e0c7-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="9e0c7-113">CLSID_OlkStore</span></span>
    
<span data-ttu-id="9e0c7-114">_pcAccts_</span><span class="sxs-lookup"><span data-stu-id="9e0c7-114">_pcAccts_</span></span>
  
>  <span data-ttu-id="9e0c7-115">[salida] El número de cuentas.</span><span class="sxs-lookup"><span data-stu-id="9e0c7-115">[out] The number of accounts.</span></span> 
    
<span data-ttu-id="9e0c7-116">_prgAccts_</span><span class="sxs-lookup"><span data-stu-id="9e0c7-116">_prgAccts_</span></span>
  
> <span data-ttu-id="9e0c7-117">[salida] Puntero a una matriz de cuentas.</span><span class="sxs-lookup"><span data-stu-id="9e0c7-117">[out] A pointer to an array of accounts.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="9e0c7-118">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="9e0c7-118">Return values</span></span>

|<span data-ttu-id="9e0c7-119">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="9e0c7-119">**HRESULT**</span></span>|<span data-ttu-id="9e0c7-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="9e0c7-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9e0c7-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e0c7-121">S_OK</span></span>  <br/> |<span data-ttu-id="9e0c7-122">La llamada se ha realiza correctamente</span><span class="sxs-lookup"><span data-stu-id="9e0c7-122">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="9e0c7-123">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="9e0c7-123">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="9e0c7-124">Uno o más argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="9e0c7-124">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="9e0c7-125">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="9e0c7-125">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="9e0c7-126">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="9e0c7-126">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e0c7-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9e0c7-127">Remarks</span></span>

<span data-ttu-id="9e0c7-128">Antes de llamar a este método, el llamador asigna solo un puntero de matriz *prgAccts,* pero no memoria para la matriz a la que *apunta prgAccts.*</span><span class="sxs-lookup"><span data-stu-id="9e0c7-128">Before calling this method, the caller allocates only an array pointer  *prgAccts*  but no memory for the array at which  *prgAccts*  points.</span></span> <span data-ttu-id="9e0c7-129">Después de que este método devuelve, el llamador debe usar [IOlkAccountManager::FreeMemory para](iolkaccountmanager-freememory.md) liberar la memoria asignada para  *prgAccts*  .</span><span class="sxs-lookup"><span data-stu-id="9e0c7-129">After this method returns, the caller must use [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) to release the memory allocated for  *prgAccts*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e0c7-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9e0c7-130">See also</span></span>

- [<span data-ttu-id="9e0c7-131">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="9e0c7-131">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="9e0c7-132">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="9e0c7-132">IOlkAccountManager::SetOrder</span></span>](iolkaccountmanager-setorder.md)

