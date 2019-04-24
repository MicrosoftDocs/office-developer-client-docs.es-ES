---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Establece el valor de la propiedad de la cuenta especificada.
ms.openlocfilehash: 94134cee7886177ab840a6caff7d70d65bf9d4cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322256"
---
# <a name="iolkaccountsetprop"></a><span data-ttu-id="0b0a9-103">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="0b0a9-103">IOlkAccount::SetProp</span></span>

<span data-ttu-id="0b0a9-104">Establece el valor de la propiedad de la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="0b0a9-104">Sets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0b0a9-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="0b0a9-105">Quick info</span></span>

<span data-ttu-id="0b0a9-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="0b0a9-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="0b0a9-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="0b0a9-107">Parameters</span></span>

<span data-ttu-id="0b0a9-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="0b0a9-108">_dwProp_</span></span>
  
> <span data-ttu-id="0b0a9-109">a La etiqueta de propiedad de la propiedad de cuenta que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="0b0a9-109">[in] The property tag of the account property to set.</span></span>
    
<span data-ttu-id="0b0a9-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="0b0a9-110">_pVar_</span></span>
  
> <span data-ttu-id="0b0a9-111">a Valor de la propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="0b0a9-111">[in] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="0b0a9-112">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="0b0a9-112">Return values</span></span>

|<span data-ttu-id="0b0a9-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="0b0a9-113">**HRESULT**</span></span>|<span data-ttu-id="0b0a9-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="0b0a9-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0b0a9-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="0b0a9-115">S_OK</span></span>  <br/> |<span data-ttu-id="0b0a9-116">La llamada al método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0b0a9-116">The method call was successful.</span></span>  <br/> |
|<span data-ttu-id="0b0a9-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0b0a9-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="0b0a9-118">Se ha especificado una etiqueta de propiedad no válida.</span><span class="sxs-lookup"><span data-stu-id="0b0a9-118">An invalid property tag was specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b0a9-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b0a9-119">Remarks</span></span>

<span data-ttu-id="0b0a9-120">Use [IOlkAccount:: SaveChanges](iolkaccount-savechanges.md) para guardar los cambios en el valor de las propiedades de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="0b0a9-120">Use [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save changes to the value of account properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b0a9-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b0a9-121">See also</span></span>

- [<span data-ttu-id="0b0a9-122">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="0b0a9-122">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="0b0a9-123">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="0b0a9-123">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

