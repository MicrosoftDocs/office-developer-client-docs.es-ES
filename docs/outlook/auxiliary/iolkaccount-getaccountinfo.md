---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Obtiene la información de tipos y categorías de la cuenta especificada.
ms.openlocfilehash: 88021537cc7ff4c55759081e6f3619c2a9f10ea3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318189"
---
# <a name="iolkaccountgetaccountinfo"></a><span data-ttu-id="77c4e-103">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="77c4e-103">IOlkAccount::GetAccountInfo</span></span>

<span data-ttu-id="77c4e-104">Obtiene la información de tipos y categorías de la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="77c4e-104">Gets the type and categories information for the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="77c4e-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="77c4e-105">Quick info</span></span>

<span data-ttu-id="77c4e-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="77c4e-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a><span data-ttu-id="77c4e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="77c4e-107">Parameters</span></span>

<span data-ttu-id="77c4e-108">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="77c4e-108">_pclsidType_</span></span>
  
> <span data-ttu-id="77c4e-109">contempla El identificador de clase para el tipo de cuenta.</span><span class="sxs-lookup"><span data-stu-id="77c4e-109">[out] The class identifier for the account type.</span></span> <span data-ttu-id="77c4e-110">El valor debe ser uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="77c4e-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="77c4e-111">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="77c4e-111">CLSID_OlkPOP3Account</span></span> 
    
   - <span data-ttu-id="77c4e-112">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="77c4e-112">CLSID_OlkIMAP4Account</span></span> 
    
   - <span data-ttu-id="77c4e-113">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="77c4e-113">CLSID_OlkMAPIAccount</span></span> 
    
   - <span data-ttu-id="77c4e-114">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="77c4e-114">CLSID_OlkHotmailAccount</span></span> 
    
   - <span data-ttu-id="77c4e-115">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="77c4e-115">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="77c4e-116">_pcCategories_</span><span class="sxs-lookup"><span data-stu-id="77c4e-116">_pcCategories_</span></span>
  
> <span data-ttu-id="77c4e-117">contempla El número de categorías en _prgclsidCategory_.</span><span class="sxs-lookup"><span data-stu-id="77c4e-117">[out] The number of categories in  _prgclsidCategory_.</span></span>
    
<span data-ttu-id="77c4e-118">_prgclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="77c4e-118">_prgclsidCategory_</span></span>
  
> <span data-ttu-id="77c4e-119">contempla Matriz de categorías a las que está asociada esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="77c4e-119">[out] An array of categories that this account is associated with.</span></span> <span data-ttu-id="77c4e-120">La matriz tiene el tamaño \* _pcCategories_.</span><span class="sxs-lookup"><span data-stu-id="77c4e-120">The array is of size \* _pcCategories_.</span></span> <span data-ttu-id="77c4e-121">El valor de cada categoría de la matriz debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="77c4e-121">The value of each category in the array must be one of the following:</span></span>
    
   - <span data-ttu-id="77c4e-122">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="77c4e-122">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="77c4e-123">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="77c4e-123">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="77c4e-124">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="77c4e-124">CLSID_OlkStore</span></span>
    
## <a name="return-values"></a><span data-ttu-id="77c4e-125">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="77c4e-125">Return values</span></span>

<span data-ttu-id="77c4e-126">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="77c4e-126">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="77c4e-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="77c4e-127">Remarks</span></span>

<span data-ttu-id="77c4e-128">Después de que se devuelva este método, debe liberar *prgclsidCategory* mediante [IOlkAccount:: FreeMemory](iolkaccount-freememory.md).</span><span class="sxs-lookup"><span data-stu-id="77c4e-128">After this method returns, you must free  *prgclsidCategory*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
<span data-ttu-id="77c4e-129">**IOlkAccount:: GetAccountInfo** no admite la categoría de la libreta de direcciones para una cuenta de Exchange.</span><span class="sxs-lookup"><span data-stu-id="77c4e-129">**IOlkAccount::GetAccountInfo** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="77c4e-130">Si la cuenta es una cuenta de Exchange (*pclsidType* es **CLSID_OlkMAPIAccount** ) y la cuenta implementa la libreta de direcciones, al llamar a **IOlkAccount:: GetAccountInfo** no se devolverá **CLSID_OlkAddressBook** como una categoría en \* prgclsidCategory\* .</span><span class="sxs-lookup"><span data-stu-id="77c4e-130">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and the account implements the address book, calling **IOlkAccount::GetAccountInfo** will not return **CLSID_OlkAddressBook** as a category in  *prgclsidCategory*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="77c4e-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="77c4e-131">See also</span></span>

- [<span data-ttu-id="77c4e-132">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="77c4e-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="77c4e-133">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="77c4e-133">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)

