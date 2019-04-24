---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Anula el registro de un cliente con el administrador de cuentas para las notificaciones de todas las cuentas.
ms.openlocfilehash: 0b954413b06cb1aa1b6fc4e0e9666f108bf81fbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322011"
---
# <a name="iolkaccountmanagerunadvise"></a><span data-ttu-id="55b85-103">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="55b85-103">IOlkAccountManager::Unadvise</span></span>

<span data-ttu-id="55b85-104">Anula el registro de un cliente con el administrador de cuentas para las notificaciones de todas las cuentas.</span><span class="sxs-lookup"><span data-stu-id="55b85-104">Unregisters a client with the account manager for notifications for all accounts.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="55b85-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="55b85-105">Quick info</span></span>

<span data-ttu-id="55b85-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="55b85-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a><span data-ttu-id="55b85-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="55b85-107">Parameters</span></span>

<span data-ttu-id="55b85-108">_dwCookie_</span><span class="sxs-lookup"><span data-stu-id="55b85-108">_dwCookie_</span></span>
  
> <span data-ttu-id="55b85-109">a La cookie devuelta por [IOlkAccountManager:: Advise](iolkaccountmanager-advise.md).</span><span class="sxs-lookup"><span data-stu-id="55b85-109">[in] The cookie returned by [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="55b85-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="55b85-110">Return values</span></span>

|<span data-ttu-id="55b85-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="55b85-111">**HRESULT**</span></span>|<span data-ttu-id="55b85-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="55b85-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55b85-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="55b85-113">S_OK</span></span>  <br/> |<span data-ttu-id="55b85-114">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="55b85-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="55b85-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="55b85-115">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="55b85-116">Uno o más argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="55b85-116">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="55b85-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="55b85-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="55b85-118">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="55b85-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55b85-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="55b85-119">See also</span></span>

- [<span data-ttu-id="55b85-120">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="55b85-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="55b85-121">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="55b85-121">IOlkAccountManager::Advise</span></span>](iolkaccountmanager-advise.md)

