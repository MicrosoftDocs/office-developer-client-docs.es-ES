---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Notifica al cliente de los cambios realizados en la cuenta especificada.
ms.openlocfilehash: ea4cab8cb8571cf5f34637c08935c78c657e5503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816243"
---
# <a name="iolkaccountnotifynotify"></a><span data-ttu-id="fbbe8-103">IOlkAccountNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="fbbe8-103">IOlkAccountNotify::Notify</span></span>

<span data-ttu-id="fbbe8-104">Notifica al cliente de los cambios realizados en la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="fbbe8-104">Notifies the client of changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fbbe8-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="fbbe8-105">Quick info</span></span>

<span data-ttu-id="fbbe8-106">Vea [IOlkAccountNotify](iolkaccountnotify.md).</span><span class="sxs-lookup"><span data-stu-id="fbbe8-106">See [IOlkAccountNotify](iolkaccountnotify.md).</span></span>
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="fbbe8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fbbe8-107">Parameters</span></span>

<span data-ttu-id="fbbe8-108">_dwNotify_</span><span class="sxs-lookup"><span data-stu-id="fbbe8-108">_dwNotify_</span></span>
  
> <span data-ttu-id="fbbe8-109">[entrada] El tipo de notificación.</span><span class="sxs-lookup"><span data-stu-id="fbbe8-109">[in] The type of notification.</span></span> <span data-ttu-id="fbbe8-110">El valor debe ser uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="fbbe8-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="fbbe8-111">NOTIFY_ACCT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="fbbe8-111">NOTIFY_ACCT_CHANGED</span></span> 
    
   - <span data-ttu-id="fbbe8-112">NOTIFY_ACCT_CREATED</span><span class="sxs-lookup"><span data-stu-id="fbbe8-112">NOTIFY_ACCT_CREATED</span></span> 
    
   - <span data-ttu-id="fbbe8-113">NOTIFY_ACCT_DELETED</span><span class="sxs-lookup"><span data-stu-id="fbbe8-113">NOTIFY_ACCT_DELETED</span></span>
    
   - <span data-ttu-id="fbbe8-114">NOTIFY_ACCT_ORDER_CHANGED</span><span class="sxs-lookup"><span data-stu-id="fbbe8-114">NOTIFY_ACCT_ORDER_CHANGED</span></span> 
    
   - <span data-ttu-id="fbbe8-115">NOTIFY_ACCT_PREDELETED</span><span class="sxs-lookup"><span data-stu-id="fbbe8-115">NOTIFY_ACCT_PREDELETED</span></span> 
    
 <span data-ttu-id="fbbe8-116">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="fbbe8-116">_dwAcctID_</span></span>
  
> <span data-ttu-id="fbbe8-117">[entrada] El identificador de cuenta de la cuenta que se ha creado, modificado, eliminado o eliminado previamente.</span><span class="sxs-lookup"><span data-stu-id="fbbe8-117">[in] The account ID of the account that has been created, changed, deleted, or pre-deleted.</span></span>
    
 <span data-ttu-id="fbbe8-118">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="fbbe8-118">_dwFlags_</span></span>
  
>  <span data-ttu-id="fbbe8-119">[entrada] No se usa.</span><span class="sxs-lookup"><span data-stu-id="fbbe8-119">[in] Not used.</span></span> <span data-ttu-id="fbbe8-120">OLK_ACCOUNT_NO_FLAGS es el único valor admitido.</span><span class="sxs-lookup"><span data-stu-id="fbbe8-120">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="fbbe8-121">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="fbbe8-121">Return values</span></span>

<span data-ttu-id="fbbe8-122">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="fbbe8-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fbbe8-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbbe8-123">See also</span></span>

- [<span data-ttu-id="fbbe8-124">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="fbbe8-124">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="fbbe8-125">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="fbbe8-125">IOlkAccountManager</span></span>](iolkaccountmanager.md)

