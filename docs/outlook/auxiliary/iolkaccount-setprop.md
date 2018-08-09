---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Establece el valor de la propiedad de cuenta especificado.
ms.openlocfilehash: 2bb8a323f5f3399b9eac1cfdf9ac18faddfdb259
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816187"
---
# <a name="iolkaccountsetprop"></a><span data-ttu-id="ac0c7-103">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="ac0c7-103">IOlkAccount::SetProp</span></span>

<span data-ttu-id="ac0c7-104">Establece el valor de la propiedad de cuenta especificado.</span><span class="sxs-lookup"><span data-stu-id="ac0c7-104">Sets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ac0c7-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="ac0c7-105">Quick info</span></span>

<span data-ttu-id="ac0c7-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="ac0c7-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="ac0c7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac0c7-107">Parameters</span></span>

<span data-ttu-id="ac0c7-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="ac0c7-108">_dwProp_</span></span>
  
> <span data-ttu-id="ac0c7-109">[entrada] La etiqueta de propiedad de la propiedad de cuenta para establecer.</span><span class="sxs-lookup"><span data-stu-id="ac0c7-109">[in] The property tag of the account property to set.</span></span>
    
<span data-ttu-id="ac0c7-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="ac0c7-110">_pVar_</span></span>
  
> <span data-ttu-id="ac0c7-111">[entrada] El valor de la propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="ac0c7-111">[in] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ac0c7-112">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="ac0c7-112">Return values</span></span>

|<span data-ttu-id="ac0c7-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="ac0c7-113">**HRESULT**</span></span>|<span data-ttu-id="ac0c7-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="ac0c7-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ac0c7-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac0c7-115">S_OK</span></span>  <br/> |<span data-ttu-id="ac0c7-116">La llamada al método fue correcta.</span><span class="sxs-lookup"><span data-stu-id="ac0c7-116">The method call was successful.</span></span>  <br/> |
|<span data-ttu-id="ac0c7-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ac0c7-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ac0c7-118">Se ha especificado una etiqueta de propiedad no válido.</span><span class="sxs-lookup"><span data-stu-id="ac0c7-118">An invalid property tag was specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac0c7-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ac0c7-119">Remarks</span></span>

<span data-ttu-id="ac0c7-120">Use [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) para guardar los cambios en el valor de las propiedades de cuenta.</span><span class="sxs-lookup"><span data-stu-id="ac0c7-120">Use [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save changes to the value of account properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ac0c7-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac0c7-121">See also</span></span>

- [<span data-ttu-id="ac0c7-122">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="ac0c7-122">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="ac0c7-123">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="ac0c7-123">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

