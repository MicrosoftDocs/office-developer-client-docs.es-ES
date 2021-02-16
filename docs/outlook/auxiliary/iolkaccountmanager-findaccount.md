---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Busca una cuenta por valor de propiedad.
ms.openlocfilehash: d09bce88413f85ee3ccc332c3cb88bb545a0ccaf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428805"
---
# <a name="iolkaccountmanagerfindaccount"></a><span data-ttu-id="b89f8-103">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="b89f8-103">IOlkAccountManager::FindAccount</span></span>

<span data-ttu-id="b89f8-104">Busca una cuenta por valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="b89f8-104">Finds an account by property value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b89f8-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b89f8-105">Quick info</span></span>

<span data-ttu-id="b89f8-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="b89f8-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a><span data-ttu-id="b89f8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b89f8-107">Parameters</span></span>

<span data-ttu-id="b89f8-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="b89f8-108">_dwProp_</span></span>
  
> <span data-ttu-id="b89f8-109">[entrada] La propiedad en la que se buscará.</span><span class="sxs-lookup"><span data-stu-id="b89f8-109">[in] The property to search on.</span></span> <span data-ttu-id="b89f8-110">Debe ser [PROP_ACCT_ID](prop_acct_id.md) o [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).</span><span class="sxs-lookup"><span data-stu-id="b89f8-110">Must be [PROP_ACCT_ID](prop_acct_id.md) or [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).</span></span>
    
<span data-ttu-id="b89f8-111">_pVar_</span><span class="sxs-lookup"><span data-stu-id="b89f8-111">_pVar_</span></span>
  
> <span data-ttu-id="b89f8-112">[entrada] Valor que se debe coincidir.</span><span class="sxs-lookup"><span data-stu-id="b89f8-112">[in] The value to match.</span></span>
    
<span data-ttu-id="b89f8-113">_ppAccount_</span><span class="sxs-lookup"><span data-stu-id="b89f8-113">_ppAccount_</span></span>
  
> <span data-ttu-id="b89f8-114">[salida] La cuenta encontrada.</span><span class="sxs-lookup"><span data-stu-id="b89f8-114">[out] The account found.</span></span> <span data-ttu-id="b89f8-115">Este objeto admite una [interfaz IOlkAccount.](iolkaccount.md)</span><span class="sxs-lookup"><span data-stu-id="b89f8-115">This object supports an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b89f8-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="b89f8-116">Return values</span></span>

|<span data-ttu-id="b89f8-117">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="b89f8-117">**HRESULT**</span></span>|<span data-ttu-id="b89f8-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="b89f8-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b89f8-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b89f8-119">S_OK</span></span>  <br/> |<span data-ttu-id="b89f8-120">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="b89f8-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="b89f8-121">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b89f8-121">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="b89f8-122">No se encuentra la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="b89f8-122">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="b89f8-123">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="b89f8-123">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="b89f8-124">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="b89f8-124">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="b89f8-125">E_OLK_PARAM_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="b89f8-125">E_OLK_PARAM_NOT_SUPPORTED</span></span>  <br/> |<span data-ttu-id="b89f8-126">Uno o varios parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="b89f8-126">One or more parameters are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b89f8-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b89f8-127">See also</span></span>

- [<span data-ttu-id="b89f8-128">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="b89f8-128">ACCT_VARIANT</span></span>](acct_variant.md)  
- [<span data-ttu-id="b89f8-129">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="b89f8-129">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="b89f8-130">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="b89f8-130">IOlkAccountHelper</span></span>](iolkaccounthelper.md)

