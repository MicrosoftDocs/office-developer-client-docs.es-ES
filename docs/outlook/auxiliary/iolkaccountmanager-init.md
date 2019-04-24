---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Inicializa el administrador de cuentas para su uso.
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322039"
---
# <a name="iolkaccountmanagerinit"></a><span data-ttu-id="622be-103">IOlkAccountManager::Init</span><span class="sxs-lookup"><span data-stu-id="622be-103">IOlkAccountManager::Init</span></span>

<span data-ttu-id="622be-104">Inicializa el administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="622be-104">Initializes the account manager for use.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="622be-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="622be-105">Quick info</span></span>

<span data-ttu-id="622be-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="622be-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="622be-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="622be-107">Parameters</span></span>

<span data-ttu-id="622be-108">_pAcctHelper_</span><span class="sxs-lookup"><span data-stu-id="622be-108">_pAcctHelper_</span></span>
  
> <span data-ttu-id="622be-109">a Una interfaz [IOlkAccountHelper](iolkaccounthelper.md) que proporciona la funcionalidad auxiliar de cuenta.</span><span class="sxs-lookup"><span data-stu-id="622be-109">[in] An [IOlkAccountHelper](iolkaccounthelper.md) interface that provides account helper functionality.</span></span> 
    
<span data-ttu-id="622be-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="622be-110">_dwFlags_</span></span>
  
> <span data-ttu-id="622be-111">[entrada] Marcadores para modificar el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="622be-111">[in] Flags to modify behavior.</span></span>
    
   - <span data-ttu-id="622be-112">**ACCT_INIT_NO_STORES_CHECK** : evita que una cuenta (por ejemplo, una cuenta IMAP) se sincronice con un almacén asociado.</span><span class="sxs-lookup"><span data-stu-id="622be-112">**ACCT_INIT_NO_STORES_CHECK** —Prevents an account (such as an IMAP account) from synchronizing with an associated store.</span></span> 
    
   - <span data-ttu-id="622be-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** : impide que los servicios MAPI se sincronicen con cuentas.</span><span class="sxs-lookup"><span data-stu-id="622be-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —Prevents MAPI services from synchronizing with accounts.</span></span> 
   
   - <span data-ttu-id="622be-114">**ACCT_INIT_NO_NOTIFICATIONS** : evita que el administrador de cuentas intercepte mensajes de difusión destinados a otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="622be-114">**ACCT_INIT_NO_NOTIFICATIONS** —Prevents the Account Manager from intercepting broadcast messages intended for other applications.</span></span> 
   
   - <span data-ttu-id="622be-115">**OLK_ACCOUNT_NO_FLAGS** : sincroniza los servicios MAPI con cuentas.</span><span class="sxs-lookup"><span data-stu-id="622be-115">**OLK_ACCOUNT_NO_FLAGS** —Synchronizes MAPI services with accounts.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="622be-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="622be-116">Return values</span></span>

|<span data-ttu-id="622be-117">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="622be-117">**HRESULT**</span></span>|<span data-ttu-id="622be-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="622be-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="622be-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="622be-119">S_OK</span></span>  <br/> |<span data-ttu-id="622be-120">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="622be-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="622be-121">E_OLK_ALREADY_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="622be-121">E_OLK_ALREADY_INITIALIZED</span></span>  <br/> |<span data-ttu-id="622be-122">Ya se ha llamado a **init** .</span><span class="sxs-lookup"><span data-stu-id="622be-122">**Init** has already been called.</span></span>  <br/> |
|<span data-ttu-id="622be-123">E_OLK_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="622be-123">E_OLK_REGISTRY</span></span>  <br/> |<span data-ttu-id="622be-124">El administrador de cuentas no pudo obtener acceso a la configuración del registro requerida.</span><span class="sxs-lookup"><span data-stu-id="622be-124">The account manager could not access the required registry settings.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="622be-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="622be-125">Remarks</span></span>

<span data-ttu-id="622be-126">El cliente debe llamar a **IOlkAccountManager:: init** para inicializar el administrador de cuentas antes de usar el administrador de cuentas para obtener acceso a las cuentas o configurar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="622be-126">The client must call **IOlkAccountManager::Init** to initialize the account manager before using the account manager to access accounts or set up notifications.</span></span> <span data-ttu-id="622be-127">Como Outlook sincroniza automáticamente los servicios MAPI con las cuentas durante el inicio, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** a menos que haya una causa específica para la sincronización.</span><span class="sxs-lookup"><span data-stu-id="622be-127">Because Outlook automatically synchronizes MAPI services with accounts on startup, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** unless there is a specific cause to synchronize.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="622be-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="622be-128">See also</span></span>

- [<span data-ttu-id="622be-129">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="622be-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

