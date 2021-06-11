---
title: IMAPISession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession
api_type:
- COM
ms.assetid: 5650fa2a-6e62-451c-964e-363f7bee2344
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1c1a66f61fe1533e436f4e35a542f53d938b4d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413384"
---
# <a name="imapisession--iunknown"></a><span data-ttu-id="03e08-103">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="03e08-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="03e08-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03e08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03e08-105">Administra objetos asociados a una sesión de inicio de sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="03e08-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03e08-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="03e08-106">Header file:</span></span>  <br/> |<span data-ttu-id="03e08-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="03e08-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="03e08-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="03e08-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="03e08-109">Objetos Session</span><span class="sxs-lookup"><span data-stu-id="03e08-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="03e08-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="03e08-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="03e08-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="03e08-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="03e08-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="03e08-112">Called by:</span></span>  <br/> |<span data-ttu-id="03e08-113">Aplicaciones cliente y MAPI</span><span class="sxs-lookup"><span data-stu-id="03e08-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="03e08-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="03e08-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="03e08-115">IID_IMAPISession</span><span class="sxs-lookup"><span data-stu-id="03e08-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="03e08-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="03e08-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="03e08-117">LPMAPISESSION</span><span class="sxs-lookup"><span data-stu-id="03e08-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="03e08-118">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="03e08-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="03e08-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="03e08-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="03e08-120">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error de sesión anterior.</span><span class="sxs-lookup"><span data-stu-id="03e08-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="03e08-121">GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="03e08-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="03e08-122">Proporciona acceso a la tabla de almacén de mensajes que contiene información sobre todos los almacenes de mensajes del perfil de sesión.</span><span class="sxs-lookup"><span data-stu-id="03e08-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="03e08-123">OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="03e08-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="03e08-124">Abre un almacén de mensajes y devuelve un puntero [IMsgStore](imsgstoreimapiprop.md) para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="03e08-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="03e08-125">OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="03e08-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="03e08-126">Abre la libreta de direcciones integrada MAPI y devuelve un puntero [IAddrBook](iaddrbookimapiprop.md) para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="03e08-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="03e08-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="03e08-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="03e08-128">Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="03e08-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="03e08-129">GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="03e08-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="03e08-130">Proporciona acceso a la tabla de estado, una tabla que contiene información sobre todos los recursos MAPI de la sesión.</span><span class="sxs-lookup"><span data-stu-id="03e08-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="03e08-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="03e08-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="03e08-132">Abre un objeto y devuelve un puntero de interfaz para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="03e08-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="03e08-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="03e08-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="03e08-134">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="03e08-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="03e08-135">Aconsejar</span><span class="sxs-lookup"><span data-stu-id="03e08-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="03e08-136">Se registra para recibir una notificación de eventos especificados que afectan a la sesión.</span><span class="sxs-lookup"><span data-stu-id="03e08-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="03e08-137">Unadvise</span><span class="sxs-lookup"><span data-stu-id="03e08-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="03e08-138">Cancela el envío de notificaciones configuradas anteriormente con una llamada al **método Advise.**</span><span class="sxs-lookup"><span data-stu-id="03e08-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="03e08-139">**MessageOptions**</span><span class="sxs-lookup"><span data-stu-id="03e08-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="03e08-140">*No se admite ni se documenta.*</span><span class="sxs-lookup"><span data-stu-id="03e08-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="03e08-141">**QueryDefaultMessageOpt**</span><span class="sxs-lookup"><span data-stu-id="03e08-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="03e08-142">*No se admite ni se documenta.*</span><span class="sxs-lookup"><span data-stu-id="03e08-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="03e08-143">EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="03e08-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="03e08-144">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="03e08-144">Deprecated.</span></span> <span data-ttu-id="03e08-145">Devuelve los tipos de direcciones que pueden controlar todos los proveedores de transporte de la sesión.</span><span class="sxs-lookup"><span data-stu-id="03e08-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="03e08-146">QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="03e08-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="03e08-147">Devuelve el identificador de entrada del objeto que proporciona la identidad principal de la sesión.</span><span class="sxs-lookup"><span data-stu-id="03e08-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="03e08-148">Cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="03e08-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="03e08-149">Finaliza una sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="03e08-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="03e08-150">SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="03e08-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="03e08-151">Establece un almacén de mensajes como almacén de mensajes predeterminado para la sesión.</span><span class="sxs-lookup"><span data-stu-id="03e08-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="03e08-152">AdminServices</span><span class="sxs-lookup"><span data-stu-id="03e08-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="03e08-153">Devuelve un [puntero IMsgServiceAdmin](imsgserviceadminiunknown.md) para realizar cambios en los servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="03e08-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="03e08-154">ShowForm</span><span class="sxs-lookup"><span data-stu-id="03e08-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="03e08-155">Muestra un formulario.</span><span class="sxs-lookup"><span data-stu-id="03e08-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="03e08-156">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="03e08-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="03e08-157">Crea un token numérico que el **método ShowForm** usa para obtener acceso a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="03e08-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="03e08-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="03e08-158">See also</span></span>



[<span data-ttu-id="03e08-159">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="03e08-159">MAPI Interfaces</span></span>](mapi-interfaces.md)

