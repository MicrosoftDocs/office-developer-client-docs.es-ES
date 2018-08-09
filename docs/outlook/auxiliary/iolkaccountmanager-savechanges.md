---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Guarda los cambios realizados a la cuenta especificada.
ms.openlocfilehash: 87b513659b632e88697fb63d1aeccccb77ed9fd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816238"
---
# <a name="iolkaccountmanagersavechanges"></a><span data-ttu-id="8fa4c-103">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="8fa4c-103">IOlkAccountManager::SaveChanges</span></span>

<span data-ttu-id="8fa4c-104">Guarda los cambios realizados a la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="8fa4c-104">Saves changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8fa4c-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="8fa4c-105">Quick info</span></span>

<span data-ttu-id="8fa4c-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="8fa4c-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="8fa4c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8fa4c-107">Parameters</span></span>

<span data-ttu-id="8fa4c-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="8fa4c-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="8fa4c-109">[entrada] El identificador de cuenta para guardar.</span><span class="sxs-lookup"><span data-stu-id="8fa4c-109">[in] The account ID to save.</span></span> 
    
<span data-ttu-id="8fa4c-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="8fa4c-110">_dwFlags_</span></span>
  
> <span data-ttu-id="8fa4c-111">[entrada] Marcadores para modificar el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="8fa4c-111">[in] Flags to modify behavior.</span></span> <span data-ttu-id="8fa4c-112">OLK_ACCOUNT_NO_FLAGS es el único valor admitido.</span><span class="sxs-lookup"><span data-stu-id="8fa4c-112">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="8fa4c-113">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="8fa4c-113">Return values</span></span>

|<span data-ttu-id="8fa4c-114">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="8fa4c-114">**HRESULT**</span></span>|<span data-ttu-id="8fa4c-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="8fa4c-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8fa4c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8fa4c-116">S_OK</span></span>  <br/> |<span data-ttu-id="8fa4c-117">La llamada se ha realizado correctamente</span><span class="sxs-lookup"><span data-stu-id="8fa4c-117">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="8fa4c-118">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8fa4c-118">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="8fa4c-119">No se encuentra la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="8fa4c-119">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="8fa4c-120">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8fa4c-120">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="8fa4c-121">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="8fa4c-121">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8fa4c-122">Notas</span><span class="sxs-lookup"><span data-stu-id="8fa4c-122">Remarks</span></span>

<span data-ttu-id="8fa4c-123">Después de cambiar el valor de las propiedades de cuenta mediante el uso de [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccountManager::SaveChanges** o [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) para guardar estos cambios.</span><span class="sxs-lookup"><span data-stu-id="8fa4c-123">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccountManager::SaveChanges** or [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8fa4c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fa4c-124">See also</span></span>

- [<span data-ttu-id="8fa4c-125">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="8fa4c-125">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="8fa4c-126">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="8fa4c-126">IOlkAccount::SaveChanges</span></span>](iolkaccount-savechanges.md)

