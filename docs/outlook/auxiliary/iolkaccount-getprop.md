---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Obtiene el valor de la propiedad de cuenta especificado.
ms.openlocfilehash: 2c0756f416a209d37eff2209a82c298837f85f3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816170"
---
# <a name="iolkaccountgetprop"></a><span data-ttu-id="9b17e-103">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="9b17e-103">IOlkAccount::GetProp</span></span>

<span data-ttu-id="9b17e-104">Obtiene el valor de la propiedad de cuenta especificado.</span><span class="sxs-lookup"><span data-stu-id="9b17e-104">Gets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9b17e-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="9b17e-105">Quick info</span></span>

<span data-ttu-id="9b17e-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="9b17e-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="9b17e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b17e-107">Parameters</span></span>

<span data-ttu-id="9b17e-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="9b17e-108">_dwProp_</span></span>
  
> <span data-ttu-id="9b17e-109">[entrada] La etiqueta de propiedad de la propiedad cuenta que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="9b17e-109">[in] The property tag of the account property to get.</span></span>
    
<span data-ttu-id="9b17e-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="9b17e-110">_pVar_</span></span>
  
> <span data-ttu-id="9b17e-111">[out] El valor de la propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="9b17e-111">[out] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="9b17e-112">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="9b17e-112">Return values</span></span>

|<span data-ttu-id="9b17e-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="9b17e-113">**HRESULT**</span></span>|<span data-ttu-id="9b17e-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="9b17e-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b17e-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b17e-115">S_OK</span></span>  <br/> |<span data-ttu-id="9b17e-116">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="9b17e-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="9b17e-117">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9b17e-117">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="9b17e-118">No se encontró la propiedad para la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="9b17e-118">The property is not found for the given account.</span></span>  <br/> |
|<span data-ttu-id="9b17e-119">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="9b17e-119">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="9b17e-120">Se ha especificado una etiqueta de propiedad no válido.</span><span class="sxs-lookup"><span data-stu-id="9b17e-120">An invalid property tag has been specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b17e-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9b17e-121">Remarks</span></span>

<span data-ttu-id="9b17e-122">Después de que este método devuelve, si el valor de la propiedad de cuenta es un tipo de archivo binario o cadena, debe liberar *pVar* mediante [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span><span class="sxs-lookup"><span data-stu-id="9b17e-122">After this method returns, if the value of the account property is a binary or string type, you must free  *pVar*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9b17e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b17e-123">See also</span></span>

- [<span data-ttu-id="9b17e-124">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="9b17e-124">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="9b17e-125">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="9b17e-125">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)  
- [<span data-ttu-id="9b17e-126">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="9b17e-126">IOlkAccount::SetProp</span></span>](iolkaccount-setprop.md)

