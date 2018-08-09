---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Registra a un cliente con el Administrador de cuentas para las notificaciones con respecto a todas las cuentas.
ms.openlocfilehash: 1fb697fef44b9ed32888527c3c9e467be69ba4c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816216"
---
# <a name="iolkaccountmanageradvise"></a><span data-ttu-id="62215-103">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="62215-103">IOlkAccountManager::Advise</span></span>

<span data-ttu-id="62215-104">Registra a un cliente con el Administrador de cuentas para las notificaciones con respecto a todas las cuentas.</span><span class="sxs-lookup"><span data-stu-id="62215-104">Registers a client with the account manager for notifications regarding all accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="62215-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="62215-105">Quick info</span></span>

<span data-ttu-id="62215-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="62215-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a><span data-ttu-id="62215-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62215-107">Parameters</span></span>

<span data-ttu-id="62215-108">_pNotify_</span><span class="sxs-lookup"><span data-stu-id="62215-108">_pNotify_</span></span>
  
> <span data-ttu-id="62215-109">[entrada] Una interfaz de [IOlkAccountNotify](iolkaccountnotify.md) que va a usar el Administrador de cuentas para enviar las notificaciones para el cliente.</span><span class="sxs-lookup"><span data-stu-id="62215-109">[in] An [IOlkAccountNotify](iolkaccountnotify.md) interface that the account manager will use to send notifications to the client.</span></span> 
    
<span data-ttu-id="62215-110">_pdwCookie_</span><span class="sxs-lookup"><span data-stu-id="62215-110">_pdwCookie_</span></span>
  
> <span data-ttu-id="62215-111">[out] Una cookie que va a usar [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) al quitar el registro de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="62215-111">[out] A cookie that [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) will use when removing the registration for the account.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="62215-112">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="62215-112">Return values</span></span>

|<span data-ttu-id="62215-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="62215-113">**HRESULT**</span></span>|<span data-ttu-id="62215-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="62215-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="62215-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="62215-115">S_OK</span></span>  <br/> |<span data-ttu-id="62215-116">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="62215-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="62215-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="62215-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="62215-118">Se ha proporcionado un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="62215-118">An invalid argument has been provided.</span></span>  <br/> |
|<span data-ttu-id="62215-119">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="62215-119">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="62215-120">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="62215-120">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="62215-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="62215-121">See also</span></span>

- [<span data-ttu-id="62215-122">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="62215-122">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="62215-123">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="62215-123">IOlkAccountManager::Unadvise</span></span>](iolkaccountmanager-unadvise.md)

