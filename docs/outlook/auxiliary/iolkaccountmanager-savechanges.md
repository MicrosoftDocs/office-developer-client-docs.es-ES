---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Guarda los cambios realizados en la cuenta especificada.
ms.openlocfilehash: dbb1dffa1725e96bd2ab635341718ce53738b864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429610"
---
# <a name="iolkaccountmanagersavechanges"></a><span data-ttu-id="b75ba-103">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="b75ba-103">IOlkAccountManager::SaveChanges</span></span>

<span data-ttu-id="b75ba-104">Guarda los cambios realizados en la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="b75ba-104">Saves changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b75ba-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b75ba-105">Quick info</span></span>

<span data-ttu-id="b75ba-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="b75ba-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="b75ba-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="b75ba-107">Parameters</span></span>

<span data-ttu-id="b75ba-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="b75ba-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="b75ba-109">a IDENTIFICADOR de cuenta que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="b75ba-109">[in] The account ID to save.</span></span> 
    
<span data-ttu-id="b75ba-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="b75ba-110">_dwFlags_</span></span>
  
> <span data-ttu-id="b75ba-111">[entrada] Marcadores para modificar el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="b75ba-111">[in] Flags to modify behavior.</span></span> <span data-ttu-id="b75ba-112">OLK_ACCOUNT_NO_FLAGS es el único valor admitido.</span><span class="sxs-lookup"><span data-stu-id="b75ba-112">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="b75ba-113">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="b75ba-113">Return values</span></span>

|<span data-ttu-id="b75ba-114">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="b75ba-114">**HRESULT**</span></span>|<span data-ttu-id="b75ba-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="b75ba-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b75ba-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b75ba-116">S_OK</span></span>  <br/> |<span data-ttu-id="b75ba-117">La llamada se realizó correctamente</span><span class="sxs-lookup"><span data-stu-id="b75ba-117">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="b75ba-118">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b75ba-118">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="b75ba-119">No se encuentra la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="b75ba-119">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="b75ba-120">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="b75ba-120">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="b75ba-121">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="b75ba-121">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b75ba-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b75ba-122">Remarks</span></span>

<span data-ttu-id="b75ba-123">Después de cambiar el valor de las propiedades de cuenta mediante [IOlkAccount:: SetProp](iolkaccount-setprop.md), use **IOlkAccountManager:: SaveChanges** o [IOlkAccount:: SaveChanges](iolkaccount-savechanges.md) para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="b75ba-123">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccountManager::SaveChanges** or [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b75ba-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="b75ba-124">See also</span></span>

- [<span data-ttu-id="b75ba-125">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="b75ba-125">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="b75ba-126">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="b75ba-126">IOlkAccount::SaveChanges</span></span>](iolkaccount-savechanges.md)

