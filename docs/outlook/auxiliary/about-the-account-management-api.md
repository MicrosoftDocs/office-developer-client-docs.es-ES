---
title: Información sobre la API de administración de cuentas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'La API de administración de cuentas proporciona acceso a la información de cuentas y admite notificaciones de cambios en las cuentas. Como clientes de esta API, los proveedores de correo hacen lo siguiente:'
ms.openlocfilehash: 76520b7cc7f28ede28257729e4e4fbe2d5096290
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316943"
---
# <a name="about-the-account-management-api"></a><span data-ttu-id="dac86-104">Información sobre la API de administración de cuentas</span><span class="sxs-lookup"><span data-stu-id="dac86-104">About the Account Management API</span></span>

<span data-ttu-id="dac86-105">La API de administración de cuentas proporciona acceso a la información de cuentas y admite notificaciones de cambios en las cuentas.</span><span class="sxs-lookup"><span data-stu-id="dac86-105">The Account Management API provides access to account information and supports notifications of account changes.</span></span> <span data-ttu-id="dac86-106">Como clientes de esta API, los proveedores de correo hacen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="dac86-106">As clients of this API, mail providers do the following:</span></span>
  
1. <span data-ttu-id="dac86-107">Use [IOlkAccountManager](iolkaccountmanager.md) para administrar el acceso a las cuentas y configurar las notificaciones sobre cambios en las cuentas.</span><span class="sxs-lookup"><span data-stu-id="dac86-107">Use [IOlkAccountManager](iolkaccountmanager.md) to manage access to accounts and set up notifications about account changes.</span></span> 
    
2. <span data-ttu-id="dac86-108">Implemente y use [IOlkAccountNotify](iolkaccountnotify.md) para enviar notificaciones sobre los cambios en las cuentas.</span><span class="sxs-lookup"><span data-stu-id="dac86-108">Implement and use [IOlkAccountNotify](iolkaccountnotify.md) to send notifications about account changes.</span></span> 
    
3. <span data-ttu-id="dac86-109">Use [IOlkEnum](iolkenum.md) para enumerar las cuentas.</span><span class="sxs-lookup"><span data-stu-id="dac86-109">Use [IOlkEnum](iolkenum.md) to enumerate accounts.</span></span> 
    
4. <span data-ttu-id="dac86-110">Use [IOlkAccount](iolkaccount.md) para obtener y establecer propiedades y otra información sobre una cuenta.</span><span class="sxs-lookup"><span data-stu-id="dac86-110">Use [IOlkAccount](iolkaccount.md) to get and set properties and other information about an account.</span></span> <span data-ttu-id="dac86-111">Los clientes obtienen esta interfaz a través de [IOlkAccountManager:: FindAccount](iolkaccountmanager-findaccount.md) o [IOlkEnum:: Getnext](iolkenum-getnext.md) para obtener acceso a una cuenta individual.</span><span class="sxs-lookup"><span data-stu-id="dac86-111">Clients obtain this interface through [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) or [IOlkEnum::GetNext](iolkenum-getnext.md) to access an individual account.</span></span> 
    
5. <span data-ttu-id="dac86-112">Implemente y use [IOlkAccountHelper](iolkaccounthelper.md) para proporcionar la funcionalidad auxiliar de administrador de cuentas, incluida la obtención de un nombre de Perfil de cuenta y la sesión MAPI actual.</span><span class="sxs-lookup"><span data-stu-id="dac86-112">Implement and use [IOlkAccountHelper](iolkaccounthelper.md) to provide the account manager helper functionality, including getting an account's profile name and the current MAPI session.</span></span> 
    
6. <span data-ttu-id="dac86-113">Implemente y use [IOlkErrorUnknown](iolkerrorunknown.md) para proporcionar información adicional sobre un error de **IOlkAccountManager**, **IOlkAccountNotify**y **IOlkAccount**.</span><span class="sxs-lookup"><span data-stu-id="dac86-113">Implement and use [IOlkErrorUnknown](iolkerrorunknown.md) to provide extra information about an error in **IOlkAccountManager**, **IOlkAccountNotify**, and **IOlkAccount**.</span></span> 

##  <a name="account-management-api-components"></a><span data-ttu-id="dac86-114">Componentes de la API de administración de cuentas</span><span class="sxs-lookup"><span data-stu-id="dac86-114">Account Management API components</span></span>

<span data-ttu-id="dac86-115">La API de administración de cuentas proporciona las siguientes definiciones, tipos de datos, interfaces, propiedades con nombre y propiedades.</span><span class="sxs-lookup"><span data-stu-id="dac86-115">The Account Management API provides the following definitions, data types, interfaces, named properties, and properties.</span></span>
  
### <a name="definitions"></a><span data-ttu-id="dac86-116">Definiciones</span><span class="sxs-lookup"><span data-stu-id="dac86-116">Definitions</span></span>
  
- [<span data-ttu-id="dac86-117">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="dac86-117">Constants (Account management API)</span></span>](constants-account-management-api.md)
    
### <a name="data-types"></a><span data-ttu-id="dac86-118">Tipos de datos</span><span class="sxs-lookup"><span data-stu-id="dac86-118">Data types</span></span>
  
- [<span data-ttu-id="dac86-119">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="dac86-119">ACCT_BIN</span></span>](acct_bin.md)
    
- [<span data-ttu-id="dac86-120">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="dac86-120">ACCT_VARIANT</span></span>](acct_variant.md)
    
### <a name="interfaces"></a><span data-ttu-id="dac86-121">Interfaces</span><span class="sxs-lookup"><span data-stu-id="dac86-121">Interfaces</span></span>
  
- [<span data-ttu-id="dac86-122">IOlkAccount</span><span class="sxs-lookup"><span data-stu-id="dac86-122">IOlkAccount</span></span>](iolkaccount.md)
    
- [<span data-ttu-id="dac86-123">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="dac86-123">IOlkAccountHelper</span></span>](iolkaccounthelper.md)
    
- [<span data-ttu-id="dac86-124">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="dac86-124">IOlkAccountManager</span></span>](iolkaccountmanager.md)
    
- [<span data-ttu-id="dac86-125">IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="dac86-125">IOlkAccountNotify</span></span>](iolkaccountnotify.md)
    
- [<span data-ttu-id="dac86-126">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="dac86-126">IOlkEnum</span></span>](iolkenum.md)
    
- [<span data-ttu-id="dac86-127">IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="dac86-127">IOlkErrorUnknown</span></span>](iolkerrorunknown.md)
    
### <a name="named-properties"></a><span data-ttu-id="dac86-128">Propiedades con nombre</span><span class="sxs-lookup"><span data-stu-id="dac86-128">Named properties</span></span>
  
- [<span data-ttu-id="dac86-129">PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="dac86-129">PidLidInternetAccountName</span></span>](pidlidinternetaccountname.md)
    
- [<span data-ttu-id="dac86-130">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="dac86-130">PidLidInternetAccountStamp</span></span>](pidlidinternetaccountstamp.md)
    
### <a name="properties"></a><span data-ttu-id="dac86-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dac86-131">Properties</span></span>
  
- [<span data-ttu-id="dac86-132">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="dac86-132">PidTagNextSendAcct</span></span>](pidtagnextsendacct.md)
    
- [<span data-ttu-id="dac86-133">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="dac86-133">PidTagPrimarySendAccount</span></span>](pidtagprimarysendaccount.md)
    
- [<span data-ttu-id="dac86-134">PROP_ACCT_DELIVERY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="dac86-134">PROP_ACCT_DELIVERY_FOLDER</span></span>](prop_acct_delivery_folder.md)
    
- [<span data-ttu-id="dac86-135">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="dac86-135">PROP_ACCT_DELIVERY_STORE</span></span>](prop_acct_delivery_store.md)
    
- [<span data-ttu-id="dac86-136">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="dac86-136">PROP_ACCT_ID</span></span>](prop_acct_id.md)
    
- [<span data-ttu-id="dac86-137">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="dac86-137">PROP_ACCT_IS_EXCH</span></span>](prop_acct_is_exch.md)
    
- [<span data-ttu-id="dac86-138">PROP_ACCT_NAME</span><span class="sxs-lookup"><span data-stu-id="dac86-138">PROP_ACCT_NAME</span></span>](prop_acct_name.md)
    
- [<span data-ttu-id="dac86-139">PROP_ACCT_PREFERENCES_UID</span><span class="sxs-lookup"><span data-stu-id="dac86-139">PROP_ACCT_PREFERENCES_UID</span></span>](prop_acct_preferences_uid.md)
    
- [<span data-ttu-id="dac86-140">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="dac86-140">PROP_ACCT_SEND_STAMP</span></span>](prop_acct_send_stamp.md)
    
- [<span data-ttu-id="dac86-141">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="dac86-141">PROP_ACCT_SENTITEMS_EID</span></span>](prop_acct_sentitems_eid.md)
    
- [<span data-ttu-id="dac86-142">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="dac86-142">PROP_ACCT_STAMP</span></span>](prop_acct_stamp.md)
    
- [<span data-ttu-id="dac86-143">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="dac86-143">PROP_ACCT_USER_EMAIL_ADDR</span></span>](prop_acct_user_email_addr.md)
    
- [<span data-ttu-id="dac86-144">PROP_ACCT_USER_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="dac86-144">PROP_ACCT_USER_DISPLAY_NAME</span></span>](prop_acct_user_display_name.md)
    
- [<span data-ttu-id="dac86-145">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="dac86-145">PROP_MAPI_EMSMDB_UID</span></span>](prop_mapi_emsmdb_uid.md)
    
- [<span data-ttu-id="dac86-146">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="dac86-146">PROP_MAPI_IDENTITY_ENTRYID</span></span>](prop_mapi_identity_entryid.md)
    
- [<span data-ttu-id="dac86-147">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="dac86-147">PROP_MAPI_TRANSPORT_FLAGS</span></span>](prop_mapi_transport_flags.md)
    

