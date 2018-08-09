---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Confirma los cambios realizados en el objeto de cuenta mediante la escritura en el almacén del registro.
ms.openlocfilehash: ebff8af8af8a7512b577b36a2c31f76f3297a19d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816168"
---
# <a name="iolkaccountsavechanges"></a><span data-ttu-id="4362e-103">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="4362e-103">IOlkAccount::SaveChanges</span></span>

<span data-ttu-id="4362e-104">Confirma los cambios realizados en el objeto de cuenta mediante la escritura en el almacén del registro.</span><span class="sxs-lookup"><span data-stu-id="4362e-104">Commits changes to the account object by writing to the registry store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4362e-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="4362e-105">Quick info</span></span>

<span data-ttu-id="4362e-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="4362e-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="4362e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4362e-107">Parameters</span></span>

<span data-ttu-id="4362e-108">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="4362e-108">_dwFlags_</span></span>
  
> <span data-ttu-id="4362e-109">[entrada] Marcadores para modificar el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="4362e-109">[in] Flags to modify behavior.</span></span> <span data-ttu-id="4362e-110">OLK_ACCOUNT_NO_FLAGS es el único valor admitido.</span><span class="sxs-lookup"><span data-stu-id="4362e-110">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="4362e-111">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="4362e-111">Return values</span></span>

|<span data-ttu-id="4362e-112">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="4362e-112">**HRESULT**</span></span>|<span data-ttu-id="4362e-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="4362e-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4362e-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="4362e-114">S_OK</span></span>  <br/> |<span data-ttu-id="4362e-115">El método era correcto.</span><span class="sxs-lookup"><span data-stu-id="4362e-115">The method was successful.</span></span>  <br/> |
|<span data-ttu-id="4362e-116">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="4362e-116">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="4362e-117">No se encuentra la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="4362e-117">Cannot find the specified account.</span></span>  <br/> |
|<span data-ttu-id="4362e-118">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="4362e-118">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="4362e-119">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="4362e-119">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4362e-120">Notas</span><span class="sxs-lookup"><span data-stu-id="4362e-120">Remarks</span></span>

<span data-ttu-id="4362e-121">Después de cambiar el valor de las propiedades de cuenta mediante el uso de [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** para guardar estos cambios.</span><span class="sxs-lookup"><span data-stu-id="4362e-121">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4362e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="4362e-122">See also</span></span>

- [<span data-ttu-id="4362e-123">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="4362e-123">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="4362e-124">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="4362e-124">IOlkAccountManager::SaveChanges</span></span>](iolkaccountmanager-savechanges.md)

