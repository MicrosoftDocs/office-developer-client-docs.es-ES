---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Confirma los cambios en el objeto de cuenta escribiendo en el almacén del registro.
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322263"
---
# <a name="iolkaccountsavechanges"></a><span data-ttu-id="0ce07-103">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="0ce07-103">IOlkAccount::SaveChanges</span></span>

<span data-ttu-id="0ce07-104">Confirma los cambios en el objeto de cuenta escribiendo en el almacén del registro.</span><span class="sxs-lookup"><span data-stu-id="0ce07-104">Commits changes to the account object by writing to the registry store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0ce07-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="0ce07-105">Quick info</span></span>

<span data-ttu-id="0ce07-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="0ce07-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="0ce07-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="0ce07-107">Parameters</span></span>

<span data-ttu-id="0ce07-108">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="0ce07-108">_dwFlags_</span></span>
  
> <span data-ttu-id="0ce07-109">[entrada] Marcadores para modificar el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="0ce07-109">[in] Flags to modify behavior.</span></span> <span data-ttu-id="0ce07-110">OLK_ACCOUNT_NO_FLAGS es el único valor admitido.</span><span class="sxs-lookup"><span data-stu-id="0ce07-110">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="0ce07-111">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="0ce07-111">Return values</span></span>

|<span data-ttu-id="0ce07-112">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="0ce07-112">**HRESULT**</span></span>|<span data-ttu-id="0ce07-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="0ce07-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ce07-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ce07-114">S_OK</span></span>  <br/> |<span data-ttu-id="0ce07-115">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0ce07-115">The method was successful.</span></span>  <br/> |
|<span data-ttu-id="0ce07-116">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0ce07-116">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="0ce07-117">No se encuentra la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="0ce07-117">Cannot find the specified account.</span></span>  <br/> |
|<span data-ttu-id="0ce07-118">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="0ce07-118">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="0ce07-119">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="0ce07-119">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ce07-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0ce07-120">Remarks</span></span>

<span data-ttu-id="0ce07-121">Después de cambiar el valor de las propiedades de cuenta mediante [IOlkAccount:: SetProp](iolkaccount-setprop.md), use **IOlkAccount:: SaveChanges** para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="0ce07-121">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0ce07-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ce07-122">See also</span></span>

- [<span data-ttu-id="0ce07-123">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="0ce07-123">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="0ce07-124">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="0ce07-124">IOlkAccountManager::SaveChanges</span></span>](iolkaccountmanager-savechanges.md)

