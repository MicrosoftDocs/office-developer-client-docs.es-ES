---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Obtiene la información de tipo y las categorías de la cuenta especificada.
ms.openlocfilehash: 85f27d1d5f47a372090b208821b52656a56559ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816153"
---
# <a name="iolkaccountgetaccountinfo"></a><span data-ttu-id="ceeb4-103">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="ceeb4-103">IOlkAccount::GetAccountInfo</span></span>

<span data-ttu-id="ceeb4-104">Obtiene la información de tipo y las categorías de la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="ceeb4-104">Gets the type and categories information for the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ceeb4-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="ceeb4-105">Quick info</span></span>

<span data-ttu-id="ceeb4-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="ceeb4-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a><span data-ttu-id="ceeb4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ceeb4-107">Parameters</span></span>

<span data-ttu-id="ceeb4-108">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="ceeb4-108">_pclsidType_</span></span>
  
> <span data-ttu-id="ceeb4-109">[out] El identificador de clase para el tipo de cuenta.</span><span class="sxs-lookup"><span data-stu-id="ceeb4-109">[out] The class identifier for the account type.</span></span> <span data-ttu-id="ceeb4-110">El valor debe ser uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="ceeb4-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="ceeb4-111">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="ceeb4-111">CLSID_OlkPOP3Account</span></span> 
    
   - <span data-ttu-id="ceeb4-112">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="ceeb4-112">CLSID_OlkIMAP4Account</span></span> 
    
   - <span data-ttu-id="ceeb4-113">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="ceeb4-113">CLSID_OlkMAPIAccount</span></span> 
    
   - <span data-ttu-id="ceeb4-114">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="ceeb4-114">CLSID_OlkHotmailAccount</span></span> 
    
   - <span data-ttu-id="ceeb4-115">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="ceeb4-115">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="ceeb4-116">_pcCategories_</span><span class="sxs-lookup"><span data-stu-id="ceeb4-116">_pcCategories_</span></span>
  
> <span data-ttu-id="ceeb4-117">[out] El número de categorías en _prgclsidCategory_.</span><span class="sxs-lookup"><span data-stu-id="ceeb4-117">[out] The number of categories in  _prgclsidCategory_.</span></span>
    
<span data-ttu-id="ceeb4-118">_prgclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="ceeb4-118">_prgclsidCategory_</span></span>
  
> <span data-ttu-id="ceeb4-119">[out] Una matriz de categorías a las que está asociada esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="ceeb4-119">[out] An array of categories that this account is associated with.</span></span> <span data-ttu-id="ceeb4-120">La matriz es de tamaño \* _pcCategories_.</span><span class="sxs-lookup"><span data-stu-id="ceeb4-120">The array is of size \* _pcCategories_.</span></span> <span data-ttu-id="ceeb4-121">El valor de cada categoría de la matriz debe ser uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="ceeb4-121">The value of each category in the array must be one of the following:</span></span>
    
   - <span data-ttu-id="ceeb4-122">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="ceeb4-122">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="ceeb4-123">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="ceeb4-123">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="ceeb4-124">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="ceeb4-124">CLSID_OlkStore</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ceeb4-125">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="ceeb4-125">Return values</span></span>

<span data-ttu-id="ceeb4-126">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="ceeb4-126">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ceeb4-127">Notas</span><span class="sxs-lookup"><span data-stu-id="ceeb4-127">Remarks</span></span>

<span data-ttu-id="ceeb4-128">Después de que devuelve este método, debe liberar *prgclsidCategory* mediante [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span><span class="sxs-lookup"><span data-stu-id="ceeb4-128">After this method returns, you must free  *prgclsidCategory*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
<span data-ttu-id="ceeb4-129">**IOlkAccount::GetAccountInfo** no es compatible con la categoría de la libreta de direcciones para una cuenta de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ceeb4-129">**IOlkAccount::GetAccountInfo** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="ceeb4-130">Si la cuenta es un intercambio cuenta (*pclsidType* es **CLSID_OlkMAPIAccount** ) y la cuenta implementa la libreta de direcciones, llamada **IOlkAccount::GetAccountInfo** no devolverá **CLSID_OlkAddressBook** como una categoría en * prgclsidCategory* .</span><span class="sxs-lookup"><span data-stu-id="ceeb4-130">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and the account implements the address book, calling **IOlkAccount::GetAccountInfo** will not return **CLSID_OlkAddressBook** as a category in  *prgclsidCategory*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ceeb4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ceeb4-131">See also</span></span>

- [<span data-ttu-id="ceeb4-132">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="ceeb4-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="ceeb4-133">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="ceeb4-133">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)

