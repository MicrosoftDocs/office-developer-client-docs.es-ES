---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Inicializa el Administrador de cuentas para su uso.
ms.openlocfilehash: 621c6a73ab2bcbdff17b87ce15af8b4e0c2e1e24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816220"
---
# <a name="iolkaccountmanagerinit"></a><span data-ttu-id="2a757-103">IOlkAccountManager::Init</span><span class="sxs-lookup"><span data-stu-id="2a757-103">IOlkAccountManager::Init</span></span>

<span data-ttu-id="2a757-104">Inicializa el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="2a757-104">Initializes the account manager for use.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2a757-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="2a757-105">Quick info</span></span>

<span data-ttu-id="2a757-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="2a757-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="2a757-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a757-107">Parameters</span></span>

<span data-ttu-id="2a757-108">_pAcctHelper_</span><span class="sxs-lookup"><span data-stu-id="2a757-108">_pAcctHelper_</span></span>
  
> <span data-ttu-id="2a757-109">[entrada] Una interfaz [IOlkAccountHelper](iolkaccounthelper.md) que proporciona funcionalidad de cuenta auxiliar.</span><span class="sxs-lookup"><span data-stu-id="2a757-109">[in] An [IOlkAccountHelper](iolkaccounthelper.md) interface that provides account helper functionality.</span></span> 
    
<span data-ttu-id="2a757-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="2a757-110">_dwFlags_</span></span>
  
> <span data-ttu-id="2a757-111">[entrada] Marcadores para modificar el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="2a757-111">[in] Flags to modify behavior.</span></span>
    
   - <span data-ttu-id="2a757-112">**ACCT_INIT_NO_STORES_CHECK** : impide que se sincronice con un almacén asociado una cuenta (por ejemplo, una cuenta IMAP).</span><span class="sxs-lookup"><span data-stu-id="2a757-112">**ACCT_INIT_NO_STORES_CHECK** —Prevents an account (such as an IMAP account) from synchronizing with an associated store.</span></span> 
    
   - <span data-ttu-id="2a757-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** : servicios de MAPI impide que de la sincronización con las cuentas.</span><span class="sxs-lookup"><span data-stu-id="2a757-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —Prevents MAPI services from synchronizing with accounts.</span></span> 
    
   - <span data-ttu-id="2a757-114">**OLK_ACCOUNT_NO_FLAGS** : servicios de MAPI se sincroniza con las cuentas.</span><span class="sxs-lookup"><span data-stu-id="2a757-114">**OLK_ACCOUNT_NO_FLAGS** —Synchronizes MAPI services with accounts.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="2a757-115">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="2a757-115">Return values</span></span>

|<span data-ttu-id="2a757-116">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="2a757-116">**HRESULT**</span></span>|<span data-ttu-id="2a757-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="2a757-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2a757-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="2a757-118">S_OK</span></span>  <br/> |<span data-ttu-id="2a757-119">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="2a757-119">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="2a757-120">E_OLK_ALREADY_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="2a757-120">E_OLK_ALREADY_INITIALIZED</span></span>  <br/> |<span data-ttu-id="2a757-121">Ya se ha llamado **Init** .</span><span class="sxs-lookup"><span data-stu-id="2a757-121">**Init** has already been called.</span></span>  <br/> |
|<span data-ttu-id="2a757-122">E_OLK_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="2a757-122">E_OLK_REGISTRY</span></span>  <br/> |<span data-ttu-id="2a757-123">El Administrador de cuentas no pudo tener acceso a la configuración del registro necesaria.</span><span class="sxs-lookup"><span data-stu-id="2a757-123">The account manager could not access the required registry settings.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a757-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2a757-124">Remarks</span></span>

<span data-ttu-id="2a757-125">El cliente debe llamar a **IOlkAccountManager::Init** para inicializar la cuenta de administrador antes de usar el Administrador de cuentas para obtener acceso a cuentas o configurar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="2a757-125">The client must call **IOlkAccountManager::Init** to initialize the account manager before using the account manager to access accounts or set up notifications.</span></span> <span data-ttu-id="2a757-126">Debido a que Outlook sincroniza automáticamente servicios MAPI con las cuentas de inicio, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** a menos que haya una causa específica para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="2a757-126">Because Outlook automatically synchronizes MAPI services with accounts on startup, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** unless there is a specific cause to synchronize.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2a757-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a757-127">See also</span></span>

- [<span data-ttu-id="2a757-128">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="2a757-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

