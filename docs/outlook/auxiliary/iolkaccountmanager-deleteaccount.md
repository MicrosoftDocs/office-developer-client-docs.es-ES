---
title: IOlkAccountManagerDeleteAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: df210364-fe20-8e33-a455-9902f04ec739
description: Elimina la cuenta especificada.
ms.openlocfilehash: 1c0b246af10dac1af9c61f368d082a92c7b3616a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816224"
---
# <a name="iolkaccountmanagerdeleteaccount"></a><span data-ttu-id="82520-103">IOlkAccountManager::DeleteAccount</span><span class="sxs-lookup"><span data-stu-id="82520-103">IOlkAccountManager::DeleteAccount</span></span>

<span data-ttu-id="82520-104">Elimina la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="82520-104">Deletes the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="82520-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="82520-105">Quick info</span></span>

<span data-ttu-id="82520-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="82520-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DeleteAccount (  
    DWORD dwAcctID, 
);
```

## <a name="parameters"></a><span data-ttu-id="82520-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82520-107">Parameters</span></span>

<span data-ttu-id="82520-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="82520-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="82520-109">[entrada] El identificador de cuenta de la cuenta que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="82520-109">[in] The account ID of the account to be deleted.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="82520-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="82520-110">Return values</span></span>

|<span data-ttu-id="82520-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="82520-111">**HRESULT**</span></span>|<span data-ttu-id="82520-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="82520-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="82520-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="82520-113">S_OK</span></span>  <br/> |<span data-ttu-id="82520-114">La llamada se ha realizado correctamente</span><span class="sxs-lookup"><span data-stu-id="82520-114">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="82520-115">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="82520-115">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="82520-116">No se encuentra la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="82520-116">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="82520-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="82520-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="82520-118">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="82520-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82520-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="82520-119">See also</span></span>

- [<span data-ttu-id="82520-120">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="82520-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="82520-121">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="82520-121">IOlkAccountManager::FindAccount</span></span>](iolkaccountmanager-findaccount.md)

