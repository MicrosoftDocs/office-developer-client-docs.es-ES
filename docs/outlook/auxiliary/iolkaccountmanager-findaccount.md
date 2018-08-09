---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Busca una cuenta por valor de la propiedad.
ms.openlocfilehash: a7d016ab7e265e547b33940c16f96979bd5fa87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816223"
---
# <a name="iolkaccountmanagerfindaccount"></a><span data-ttu-id="c9eed-103">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="c9eed-103">IOlkAccountManager::FindAccount</span></span>

<span data-ttu-id="c9eed-104">Busca una cuenta por valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c9eed-104">Finds an account by property value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c9eed-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="c9eed-105">Quick info</span></span>

<span data-ttu-id="c9eed-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="c9eed-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a><span data-ttu-id="c9eed-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9eed-107">Parameters</span></span>

<span data-ttu-id="c9eed-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="c9eed-108">_dwProp_</span></span>
  
> <span data-ttu-id="c9eed-109">[entrada] La propiedad para buscar en.</span><span class="sxs-lookup"><span data-stu-id="c9eed-109">[in] The property to search on.</span></span> <span data-ttu-id="c9eed-110">Debe ser [PROP_ACCT_ID](prop_acct_id.md) o [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).</span><span class="sxs-lookup"><span data-stu-id="c9eed-110">Must be [PROP_ACCT_ID](prop_acct_id.md) or [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).</span></span>
    
<span data-ttu-id="c9eed-111">_pVar_</span><span class="sxs-lookup"><span data-stu-id="c9eed-111">_pVar_</span></span>
  
> <span data-ttu-id="c9eed-112">[entrada] Para que coincida con el valor.</span><span class="sxs-lookup"><span data-stu-id="c9eed-112">[in] The value to match.</span></span>
    
<span data-ttu-id="c9eed-113">_ppAccount_</span><span class="sxs-lookup"><span data-stu-id="c9eed-113">_ppAccount_</span></span>
  
> <span data-ttu-id="c9eed-114">[out] La cuenta que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="c9eed-114">[out] The account found.</span></span> <span data-ttu-id="c9eed-115">Este objeto es compatible con una interfaz [IOlkAccount](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="c9eed-115">This object supports an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="c9eed-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="c9eed-116">Return values</span></span>

|<span data-ttu-id="c9eed-117">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="c9eed-117">**HRESULT**</span></span>|<span data-ttu-id="c9eed-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="c9eed-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c9eed-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9eed-119">S_OK</span></span>  <br/> |<span data-ttu-id="c9eed-120">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="c9eed-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="c9eed-121">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c9eed-121">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="c9eed-122">No se encuentra la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="c9eed-122">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="c9eed-123">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="c9eed-123">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="c9eed-124">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="c9eed-124">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="c9eed-125">E_OLK_PARAM_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="c9eed-125">E_OLK_PARAM_NOT_SUPPORTED</span></span>  <br/> |<span data-ttu-id="c9eed-126">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="c9eed-126">One or more parameters are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9eed-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9eed-127">See also</span></span>

- [<span data-ttu-id="c9eed-128">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="c9eed-128">ACCT_VARIANT</span></span>](acct_variant.md)  
- [<span data-ttu-id="c9eed-129">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="c9eed-129">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="c9eed-130">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="c9eed-130">IOlkAccountHelper</span></span>](iolkaccounthelper.md)

