---
title: IMAPIStatus IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus
api_type:
- COM
ms.assetid: 17b2aa43-0267-45b6-8c57-11b7a5c67333
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f90cf661c069ecd476bd02c5719147633a8392e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408302"
---
# <a name="imapistatus--imapiprop"></a><span data-ttu-id="96181-103">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="96181-103">IMAPIStatus : IMAPIProp</span></span>

  
  
<span data-ttu-id="96181-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96181-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96181-105">Proporciona información de estado sobre el subsistema MAPI, la libreta de direcciones integrada y la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="96181-105">Provides status information about the MAPI subsystem, the integrated address book, and the MAPI spooler.</span></span> <span data-ttu-id="96181-106">Un proveedor de servicios implementa **IMAPIStatus para** proporcionar información sobre su propio estado.</span><span class="sxs-lookup"><span data-stu-id="96181-106">A service provider implements **IMAPIStatus** to supply information about its own status.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96181-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="96181-107">Header file:</span></span>  <br/> |<span data-ttu-id="96181-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96181-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="96181-109">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="96181-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="96181-110">Objetos de estado</span><span class="sxs-lookup"><span data-stu-id="96181-110">Status objects</span></span>  <br/> |
|<span data-ttu-id="96181-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="96181-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="96181-112">Proveedores de servicios y MAPI</span><span class="sxs-lookup"><span data-stu-id="96181-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="96181-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="96181-113">Called by:</span></span>  <br/> |<span data-ttu-id="96181-114">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="96181-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="96181-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="96181-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="96181-116">IID_IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="96181-116">IID_IMAPIStatus</span></span>  <br/> |
|<span data-ttu-id="96181-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="96181-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="96181-118">LPMAPISTATUS</span><span class="sxs-lookup"><span data-stu-id="96181-118">LPMAPISTATUS</span></span>  <br/> |
|<span data-ttu-id="96181-119">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="96181-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="96181-120">No transacted</span><span class="sxs-lookup"><span data-stu-id="96181-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="96181-121">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="96181-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="96181-122">ValidateState</span><span class="sxs-lookup"><span data-stu-id="96181-122">ValidateState</span></span>](imapistatus-validatestate.md) <br/> |<span data-ttu-id="96181-123">Confirma la información de estado externo disponible para el recurso MAPI o el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="96181-123">Confirms the external status information available for the MAPI resource or the service provider.</span></span>  <br/> |
|[<span data-ttu-id="96181-124">SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="96181-124">SettingsDialog</span></span>](imapistatus-settingsdialog.md) <br/> |<span data-ttu-id="96181-125">Muestra una hoja de propiedades que permite al usuario cambiar la configuración de un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="96181-125">Displays a property sheet that enables the user to change a service provider's configuration.</span></span>  <br/> |
|[<span data-ttu-id="96181-126">ChangePassword</span><span class="sxs-lookup"><span data-stu-id="96181-126">ChangePassword</span></span>](imapistatus-changepassword.md) <br/> |<span data-ttu-id="96181-127">Modifica la contraseña de un proveedor de servicios sin mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="96181-127">Modifies a service provider's password without displaying a user interface.</span></span>  <br/> |
|[<span data-ttu-id="96181-128">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="96181-128">FlushQueues</span></span>](imapistatus-flushqueues.md) <br/> |<span data-ttu-id="96181-129">Fuerza a que todos los mensajes que esperan ser enviados o recibidos se carguen o descarguen inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="96181-129">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span>  <br/> |
   
|<span data-ttu-id="96181-130">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="96181-130">**Required properties**</span></span>|<span data-ttu-id="96181-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="96181-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="96181-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="96181-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="96181-133">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="96181-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="96181-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="96181-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="96181-135">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="96181-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="96181-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="96181-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="96181-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="96181-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="96181-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="96181-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="96181-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="96181-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="96181-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="96181-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="96181-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="96181-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="96181-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="96181-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="96181-143">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="96181-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="96181-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="96181-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="96181-145">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="96181-145">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96181-146">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96181-146">Remarks</span></span>

<span data-ttu-id="96181-147">Los objetos de estado que implementa MAPI admiten los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="96181-147">The status objects that MAPI implements support the following methods:</span></span>
  
|<span data-ttu-id="96181-148">**Status (objeto)**</span><span class="sxs-lookup"><span data-stu-id="96181-148">**Status object**</span></span>|<span data-ttu-id="96181-149">**Métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="96181-149">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="96181-150">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="96181-150">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="96181-151">**ValidateState** only</span><span class="sxs-lookup"><span data-stu-id="96181-151">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="96181-152">Libreta de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="96181-152">MAPI address book</span></span>  <br/> |<span data-ttu-id="96181-153">**ValidateState** only</span><span class="sxs-lookup"><span data-stu-id="96181-153">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="96181-154">Cola MAPI</span><span class="sxs-lookup"><span data-stu-id="96181-154">MAPI spooler</span></span>  <br/> |<span data-ttu-id="96181-155">**ValidateState** y **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="96181-155">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="96181-156">Los objetos de estado que implementa MAPI son necesarios para tener una versión de solo lectura de los métodos de la [interfaz IMAPIProp](imapipropiunknown.md) y para admitir el **método ValidateState.**</span><span class="sxs-lookup"><span data-stu-id="96181-156">The status objects that MAPI implements are required to have a read-only version of the methods of the [IMAPIProp](imapipropiunknown.md) interface and to support the **ValidateState** method.</span></span> <span data-ttu-id="96181-157">Los proveedores de transporte también deben **admitir FlushQueues**.</span><span class="sxs-lookup"><span data-stu-id="96181-157">Transport providers should also support **FlushQueues**.</span></span> <span data-ttu-id="96181-158">Todos los proveedores deben admitir **SettingsDialog**; La compatibilidad **con ChangePassword** es opcional.</span><span class="sxs-lookup"><span data-stu-id="96181-158">All providers should support **SettingsDialog**; support for **ChangePassword** is optional.</span></span> 
  
<span data-ttu-id="96181-159">Los clientes usan objetos de estado para realizar la configuración y para obtener información sobre el estado de la sesión.</span><span class="sxs-lookup"><span data-stu-id="96181-159">Clients use status objects to perform configuration and to learn about the state of the session.</span></span> <span data-ttu-id="96181-160">Obtienen acceso a un objeto de estado llamando al método **OpenStatusEntry** de un objeto de inicio de sesión del proveedor de servicios o al método [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para recuperar el objeto status.</span><span class="sxs-lookup"><span data-stu-id="96181-160">They access a status object by calling the **OpenStatusEntry** method of a service provider logon object or the [IMAPISession::GetStatusTable](imapisession-getstatustable.md) method to retrieve the status object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="96181-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="96181-161">See also</span></span>



[<span data-ttu-id="96181-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="96181-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

