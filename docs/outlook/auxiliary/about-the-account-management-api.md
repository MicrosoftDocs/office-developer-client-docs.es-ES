---
title: Acerca de la API de administración de cuenta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'La API de administración de la cuenta proporciona acceso a información de la cuenta y es compatible con las notificaciones de cambios de cuenta. Como los clientes de esta API, los proveedores de correo, haga lo siguiente:'
ms.openlocfilehash: 678143def25395c47f1c17cc99dcdcd1fb145e1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816051"
---
# <a name="about-the-account-management-api"></a><span data-ttu-id="00ffd-104">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="00ffd-104">About the Account Management API</span></span>

<span data-ttu-id="00ffd-105">La API de administración de la cuenta proporciona acceso a información de la cuenta y es compatible con las notificaciones de cambios de cuenta.</span><span class="sxs-lookup"><span data-stu-id="00ffd-105">The Account Management API provides access to account information and supports notifications of account changes.</span></span> <span data-ttu-id="00ffd-106">Como los clientes de esta API, los proveedores de correo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="00ffd-106">As clients of this API, mail providers do the following:</span></span>
  
1. <span data-ttu-id="00ffd-107">Use [IOlkAccountManager](iolkaccountmanager.md) para administrar el acceso a las cuentas y configurar las notificaciones sobre cambios de cuenta.</span><span class="sxs-lookup"><span data-stu-id="00ffd-107">Use [IOlkAccountManager](iolkaccountmanager.md) to manage access to accounts and set up notifications about account changes.</span></span> 
    
2. <span data-ttu-id="00ffd-108">Implementar y utilizar [IOlkAccountNotify](iolkaccountnotify.md) para enviar notificaciones sobre cambios de cuenta.</span><span class="sxs-lookup"><span data-stu-id="00ffd-108">Implement and use [IOlkAccountNotify](iolkaccountnotify.md) to send notifications about account changes.</span></span> 
    
3. <span data-ttu-id="00ffd-109">Use [IOlkEnum](iolkenum.md) para enumerar las cuentas.</span><span class="sxs-lookup"><span data-stu-id="00ffd-109">Use [IOlkEnum](iolkenum.md) to enumerate accounts.</span></span> 
    
4. <span data-ttu-id="00ffd-110">Use [IOlkAccount](iolkaccount.md) para obtener y establecer propiedades y otra información acerca de una cuenta.</span><span class="sxs-lookup"><span data-stu-id="00ffd-110">Use [IOlkAccount](iolkaccount.md) to get and set properties and other information about an account.</span></span> <span data-ttu-id="00ffd-111">Los clientes obtienen esta interfaz a través de [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) o [IOlkEnum::GetNext](iolkenum-getnext.md) para tener acceso a una cuenta individual.</span><span class="sxs-lookup"><span data-stu-id="00ffd-111">Clients obtain this interface through [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) or [IOlkEnum::GetNext](iolkenum-getnext.md) to access an individual account.</span></span> 
    
5. <span data-ttu-id="00ffd-112">Implementar y utilizar [IOlkAccountHelper](iolkaccounthelper.md) para proporcionar la funcionalidad de auxiliares de cuenta Administrador, incluida la obtención de nombre de perfil de la cuenta y la sesión MAPI actual.</span><span class="sxs-lookup"><span data-stu-id="00ffd-112">Implement and use [IOlkAccountHelper](iolkaccounthelper.md) to provide the account manager helper functionality, including getting an account's profile name and the current MAPI session.</span></span> 
    
6. <span data-ttu-id="00ffd-113">Implementar y utilizar [IOlkErrorUnknown](iolkerrorunknown.md) para proporcionar información adicional sobre un error en **IOlkAccountManager**, **IOlkAccountNotify**y **IOlkAccount**.</span><span class="sxs-lookup"><span data-stu-id="00ffd-113">Implement and use [IOlkErrorUnknown](iolkerrorunknown.md) to provide extra information about an error in **IOlkAccountManager**, **IOlkAccountNotify**, and **IOlkAccount**.</span></span> 

##  <a name="account-management-api-components"></a><span data-ttu-id="00ffd-114">Componentes de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="00ffd-114">Account Management API components</span></span>

<span data-ttu-id="00ffd-115">La API de administración de la cuenta proporciona las siguientes definiciones, tipos de datos, interfaces, denominadas propiedades y propiedades de.</span><span class="sxs-lookup"><span data-stu-id="00ffd-115">The Account Management API provides the following definitions, data types, interfaces, named properties, and properties.</span></span>
  
### <a name="definitions"></a><span data-ttu-id="00ffd-116">Definiciones</span><span class="sxs-lookup"><span data-stu-id="00ffd-116">Definitions</span></span>
  
- [<span data-ttu-id="00ffd-117">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="00ffd-117">Constants (Account management API)</span></span>](constants-account-management-api.md)
    
### <a name="data-types"></a><span data-ttu-id="00ffd-118">Tipos de datos</span><span class="sxs-lookup"><span data-stu-id="00ffd-118">Data types</span></span>
  
- [<span data-ttu-id="00ffd-119">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="00ffd-119">ACCT_BIN</span></span>](acct_bin.md)
    
- [<span data-ttu-id="00ffd-120">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="00ffd-120">ACCT_VARIANT</span></span>](acct_variant.md)
    
### <a name="interfaces"></a><span data-ttu-id="00ffd-121">Interfaces</span><span class="sxs-lookup"><span data-stu-id="00ffd-121">Interfaces</span></span>
  
- [<span data-ttu-id="00ffd-122">IOlkAccount</span><span class="sxs-lookup"><span data-stu-id="00ffd-122">IOlkAccount</span></span>](iolkaccount.md)
    
- [<span data-ttu-id="00ffd-123">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="00ffd-123">IOlkAccountHelper</span></span>](iolkaccounthelper.md)
    
- [<span data-ttu-id="00ffd-124">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="00ffd-124">IOlkAccountManager</span></span>](iolkaccountmanager.md)
    
- [<span data-ttu-id="00ffd-125">IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="00ffd-125">IOlkAccountNotify</span></span>](iolkaccountnotify.md)
    
- [<span data-ttu-id="00ffd-126">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="00ffd-126">IOlkEnum</span></span>](iolkenum.md)
    
- [<span data-ttu-id="00ffd-127">IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="00ffd-127">IOlkErrorUnknown</span></span>](iolkerrorunknown.md)
    
### <a name="named-properties"></a><span data-ttu-id="00ffd-128">Propiedades con nombre</span><span class="sxs-lookup"><span data-stu-id="00ffd-128">Named properties</span></span>
  
- [<span data-ttu-id="00ffd-129">PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="00ffd-129">PidLidInternetAccountName</span></span>](pidlidinternetaccountname.md)
    
- [<span data-ttu-id="00ffd-130">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="00ffd-130">PidLidInternetAccountStamp</span></span>](pidlidinternetaccountstamp.md)
    
### <a name="properties"></a><span data-ttu-id="00ffd-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="00ffd-131">Properties</span></span>
  
- [<span data-ttu-id="00ffd-132">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="00ffd-132">PidTagNextSendAcct</span></span>](pidtagnextsendacct.md)
    
- [<span data-ttu-id="00ffd-133">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="00ffd-133">PidTagPrimarySendAccount</span></span>](pidtagprimarysendaccount.md)
    
- [<span data-ttu-id="00ffd-134">PROP_ACCT_DELIVERY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="00ffd-134">PROP_ACCT_DELIVERY_FOLDER</span></span>](prop_acct_delivery_folder.md)
    
- [<span data-ttu-id="00ffd-135">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="00ffd-135">PROP_ACCT_DELIVERY_STORE</span></span>](prop_acct_delivery_store.md)
    
- [<span data-ttu-id="00ffd-136">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="00ffd-136">PROP_ACCT_ID</span></span>](prop_acct_id.md)
    
- [<span data-ttu-id="00ffd-137">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="00ffd-137">PROP_ACCT_IS_EXCH</span></span>](prop_acct_is_exch.md)
    
- [<span data-ttu-id="00ffd-138">PROP_ACCT_NAME</span><span class="sxs-lookup"><span data-stu-id="00ffd-138">PROP_ACCT_NAME</span></span>](prop_acct_name.md)
    
- [<span data-ttu-id="00ffd-139">PROP_ACCT_PREFERENCES_UID</span><span class="sxs-lookup"><span data-stu-id="00ffd-139">PROP_ACCT_PREFERENCES_UID</span></span>](prop_acct_preferences_uid.md)
    
- [<span data-ttu-id="00ffd-140">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="00ffd-140">PROP_ACCT_SEND_STAMP</span></span>](prop_acct_send_stamp.md)
    
- [<span data-ttu-id="00ffd-141">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="00ffd-141">PROP_ACCT_SENTITEMS_EID</span></span>](prop_acct_sentitems_eid.md)
    
- [<span data-ttu-id="00ffd-142">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="00ffd-142">PROP_ACCT_STAMP</span></span>](prop_acct_stamp.md)
    
- [<span data-ttu-id="00ffd-143">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="00ffd-143">PROP_ACCT_USER_EMAIL_ADDR</span></span>](prop_acct_user_email_addr.md)
    
- [<span data-ttu-id="00ffd-144">PROP_ACCT_USER_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="00ffd-144">PROP_ACCT_USER_DISPLAY_NAME</span></span>](prop_acct_user_display_name.md)
    
- [<span data-ttu-id="00ffd-145">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="00ffd-145">PROP_MAPI_EMSMDB_UID</span></span>](prop_mapi_emsmdb_uid.md)
    
- [<span data-ttu-id="00ffd-146">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="00ffd-146">PROP_MAPI_IDENTITY_ENTRYID</span></span>](prop_mapi_identity_entryid.md)
    
- [<span data-ttu-id="00ffd-147">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="00ffd-147">PROP_MAPI_TRANSPORT_FLAGS</span></span>](prop_mapi_transport_flags.md)
    

