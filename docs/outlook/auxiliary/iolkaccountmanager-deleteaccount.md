---
title: IOlkAccountManagerDeleteAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: df210364-fe20-8e33-a455-9902f04ec739
description: Elimina la cuenta especificada.
ms.openlocfilehash: 3e39b7b9af57f64dd124e1bf836db68664709b8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322214"
---
# <a name="iolkaccountmanagerdeleteaccount"></a><span data-ttu-id="83805-103">IOlkAccountManager::DeleteAccount</span><span class="sxs-lookup"><span data-stu-id="83805-103">IOlkAccountManager::DeleteAccount</span></span>

<span data-ttu-id="83805-104">Elimina la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="83805-104">Deletes the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="83805-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="83805-105">Quick info</span></span>

<span data-ttu-id="83805-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="83805-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DeleteAccount (  
    DWORD dwAcctID, 
);
```

## <a name="parameters"></a><span data-ttu-id="83805-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="83805-107">Parameters</span></span>

<span data-ttu-id="83805-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="83805-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="83805-109">a IDENTIFICADOR de cuenta de la cuenta que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="83805-109">[in] The account ID of the account to be deleted.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="83805-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="83805-110">Return values</span></span>

|<span data-ttu-id="83805-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="83805-111">**HRESULT**</span></span>|<span data-ttu-id="83805-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="83805-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="83805-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="83805-113">S_OK</span></span>  <br/> |<span data-ttu-id="83805-114">La llamada se realizó correctamente</span><span class="sxs-lookup"><span data-stu-id="83805-114">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="83805-115">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="83805-115">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="83805-116">No se encuentra la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="83805-116">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="83805-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="83805-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="83805-118">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="83805-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83805-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="83805-119">See also</span></span>

- [<span data-ttu-id="83805-120">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="83805-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="83805-121">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="83805-121">IOlkAccountManager::FindAccount</span></span>](iolkaccountmanager-findaccount.md)

