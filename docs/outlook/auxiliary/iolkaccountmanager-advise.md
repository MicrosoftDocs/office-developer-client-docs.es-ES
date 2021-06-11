---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Registra un cliente con el administrador de cuentas para recibir notificaciones sobre todas las cuentas.
ms.openlocfilehash: 5460d55d906d382ce40ecd3fd9277cf370295680
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427713"
---
# <a name="iolkaccountmanageradvise"></a><span data-ttu-id="20b58-103">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="20b58-103">IOlkAccountManager::Advise</span></span>

<span data-ttu-id="20b58-104">Registra un cliente con el administrador de cuentas para recibir notificaciones sobre todas las cuentas.</span><span class="sxs-lookup"><span data-stu-id="20b58-104">Registers a client with the account manager for notifications regarding all accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="20b58-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="20b58-105">Quick info</span></span>

<span data-ttu-id="20b58-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="20b58-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a><span data-ttu-id="20b58-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="20b58-107">Parameters</span></span>

<span data-ttu-id="20b58-108">_pNotify_</span><span class="sxs-lookup"><span data-stu-id="20b58-108">_pNotify_</span></span>
  
> <span data-ttu-id="20b58-109">[in] Una [interfaz IOlkAccountNotify](iolkaccountnotify.md) que el administrador de cuentas usará para enviar notificaciones al cliente.</span><span class="sxs-lookup"><span data-stu-id="20b58-109">[in] An [IOlkAccountNotify](iolkaccountnotify.md) interface that the account manager will use to send notifications to the client.</span></span> 
    
<span data-ttu-id="20b58-110">_pdwCookie_</span><span class="sxs-lookup"><span data-stu-id="20b58-110">_pdwCookie_</span></span>
  
> <span data-ttu-id="20b58-111">[salida] Cookie que [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) usará al quitar el registro de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="20b58-111">[out] A cookie that [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) will use when removing the registration for the account.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="20b58-112">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="20b58-112">Return values</span></span>

|<span data-ttu-id="20b58-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="20b58-113">**HRESULT**</span></span>|<span data-ttu-id="20b58-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="20b58-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20b58-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="20b58-115">S_OK</span></span>  <br/> |<span data-ttu-id="20b58-116">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="20b58-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="20b58-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="20b58-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="20b58-118">Se ha proporcionado un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="20b58-118">An invalid argument has been provided.</span></span>  <br/> |
|<span data-ttu-id="20b58-119">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="20b58-119">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="20b58-120">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="20b58-120">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20b58-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="20b58-121">See also</span></span>

- [<span data-ttu-id="20b58-122">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="20b58-122">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="20b58-123">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="20b58-123">IOlkAccountManager::Unadvise</span></span>](iolkaccountmanager-unadvise.md)

