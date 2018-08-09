---
title: IOlkAccountManagerEnumerateAccounts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: Obtiene un enumerador para las cuentas de la categoría específica o tipo.
ms.openlocfilehash: f9b332c0bbc90b1a8f5f944492448055f23c0668
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816225"
---
# <a name="iolkaccountmanagerenumerateaccounts"></a><span data-ttu-id="b8d95-103">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="b8d95-103">IOlkAccountManager::EnumerateAccounts</span></span>

<span data-ttu-id="b8d95-104">Obtiene un enumerador para las cuentas de la categoría específica o tipo.</span><span class="sxs-lookup"><span data-stu-id="b8d95-104">Gets an enumerator for the accounts of the specific category or type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b8d95-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b8d95-105">Quick info</span></span>

<span data-ttu-id="b8d95-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="b8d95-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::EnumerateAccounts (  
    const CLSID *pclsidCategory, 
    const CLSID *pclsidType, 
    DWORD dwFlags, 
    IOlkEnum **ppEnum 
);

```

## <a name="parameters"></a><span data-ttu-id="b8d95-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8d95-107">Parameters</span></span>

<span data-ttu-id="b8d95-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="b8d95-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="b8d95-p101">[entrada] El identificador de clase de la categoría para enumerar. El valor debe ser uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="b8d95-p101">[in] The class identifier of the category to enumerate. The value must be one of the following:</span></span>
    
   - <span data-ttu-id="b8d95-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="b8d95-111">CLSID_OlkMail</span></span> 
    
   -  <span data-ttu-id="b8d95-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="b8d95-112">CLSID_OlkAddressBook</span></span> 
    
   - <span data-ttu-id="b8d95-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="b8d95-113">CLSID_OlkStore</span></span> 
    
<span data-ttu-id="b8d95-114">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="b8d95-114">_pclsidType_</span></span>
  
> <span data-ttu-id="b8d95-p102">[entrada] El identificador de clase del tipo de cuenta para enumerar. El valor debe ser uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="b8d95-p102">[in] The class identifier of the account type to enumerate. The value must be one of the following:</span></span>
    
   - <span data-ttu-id="b8d95-117">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="b8d95-117">CLSID_OlkPOP3Account</span></span>
    
   - <span data-ttu-id="b8d95-118">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="b8d95-118">CLSID_OlkIMAP4Account</span></span>
    
   - <span data-ttu-id="b8d95-119">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="b8d95-119">CLSID_OlkMAPIAccount</span></span>
    
   - <span data-ttu-id="b8d95-120">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="b8d95-120">CLSID_OlkHotmailAccount</span></span>
    
   - <span data-ttu-id="b8d95-121">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="b8d95-121">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="b8d95-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="b8d95-122">_dwFlags_</span></span>
  
> <span data-ttu-id="b8d95-p103">[entrada] Marcadores para modificar el comportamiento. El único valor admitido es OLK_ACCOUNT_NO_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="b8d95-p103">[in] Flags to modify behavior. The only supported value is OLK_ACCOUNT_NO_FLAGS.</span></span>
    
<span data-ttu-id="b8d95-125">_ppEnum_</span><span class="sxs-lookup"><span data-stu-id="b8d95-125">_ppEnum_</span></span>
  
> <span data-ttu-id="b8d95-126">[out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface.</span><span class="sxs-lookup"><span data-stu-id="b8d95-126">[out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b8d95-127">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="b8d95-127">Return values</span></span>

|<span data-ttu-id="b8d95-128">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="b8d95-128">**HRESULT**</span></span>|<span data-ttu-id="b8d95-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="b8d95-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b8d95-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="b8d95-130">S_OK</span></span>  <br/> |<span data-ttu-id="b8d95-131">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="b8d95-131">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="b8d95-132">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="b8d95-132">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="b8d95-133">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="b8d95-133">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8d95-134">Notas</span><span class="sxs-lookup"><span data-stu-id="b8d95-134">Remarks</span></span>

<span data-ttu-id="b8d95-p104">Especificar NULL para la categoría, devuelve un enumerador de todas las cuentas del tipo especificado. De forma similar, si se especifica NULL para el tipo de, devuelve un enumerador de todas las cuentas de la categoría especificada.</span><span class="sxs-lookup"><span data-stu-id="b8d95-p104">Specifying NULL for category returns an enumerator of all accounts of the specified type. Similarly, specifying NULL for type returns an enumerator of all accounts of the specified category.</span></span>
  
 <span data-ttu-id="b8d95-137">**IOlkAccountManager::EnumerateAccounts** no es compatible con la categoría de la libreta de direcciones para una cuenta de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b8d95-137">**IOlkAccountManager::EnumerateAccounts** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="b8d95-138">Si la cuenta es una cuenta de Exchange (*pclsidType* es **CLSID_OlkMAPIAccount** ), y está intentando enumerar las cuentas que implementan la libreta de direcciones (*prgclsidCategory* es **CLSID_OlkAddressBook** ), al llamar a ** IOlkAccountManager::EnumerateAccounts** no devolverá la cuenta de Exchange en el enumerador de cuentas *ppEnum* .</span><span class="sxs-lookup"><span data-stu-id="b8d95-138">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and you are trying to enumerate accounts that implement the address book (*prgclsidCategory*  is **CLSID_OlkAddressBook** ), calling **IOlkAccountManager::EnumerateAccounts** will not return the Exchange account in the accounts enumerator  *ppEnum*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b8d95-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8d95-139">See also</span></span>

- [<span data-ttu-id="b8d95-140">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="b8d95-140">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="b8d95-141">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="b8d95-141">IOlkEnum</span></span>](iolkenum.md)

