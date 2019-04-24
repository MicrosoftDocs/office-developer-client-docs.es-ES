---
title: IUnknown IMAPISession
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328290"
---
# <a name="imapisession--iunknown"></a><span data-ttu-id="8273f-103">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8273f-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="8273f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8273f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8273f-105">Administra objetos asociados con una sesión de inicio de sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="8273f-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8273f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8273f-106">Header file:</span></span>  <br/> |<span data-ttu-id="8273f-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="8273f-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="8273f-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="8273f-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8273f-109">Objetos de sesión</span><span class="sxs-lookup"><span data-stu-id="8273f-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="8273f-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="8273f-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8273f-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="8273f-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="8273f-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="8273f-112">Called by:</span></span>  <br/> |<span data-ttu-id="8273f-113">Aplicaciones cliente y MAPI</span><span class="sxs-lookup"><span data-stu-id="8273f-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="8273f-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="8273f-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8273f-115">IID_IMAPISession</span><span class="sxs-lookup"><span data-stu-id="8273f-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="8273f-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="8273f-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="8273f-117">LPMAPISESSION</span><span class="sxs-lookup"><span data-stu-id="8273f-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8273f-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="8273f-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8273f-119">Volvió</span><span class="sxs-lookup"><span data-stu-id="8273f-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="8273f-120">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de sesión anterior.</span><span class="sxs-lookup"><span data-stu-id="8273f-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="8273f-121">GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="8273f-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="8273f-122">Proporciona acceso a la tabla de almacén de mensajes que contiene información acerca de todos los almacenes de mensajes del perfil de sesión.</span><span class="sxs-lookup"><span data-stu-id="8273f-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="8273f-123">OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="8273f-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="8273f-124">Abre un almacén de mensajes y devuelve un puntero [IMsgStore](imsgstoreimapiprop.md) para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="8273f-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="8273f-125">OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="8273f-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="8273f-126">Abre la libreta de direcciones MAPI integrada y devuelve un puntero [IAddrBook](iaddrbookimapiprop.md) para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="8273f-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="8273f-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="8273f-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="8273f-128">Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="8273f-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="8273f-129">GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="8273f-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="8273f-130">Proporciona acceso a la tabla de estado, una tabla que contiene información sobre todos los recursos MAPI de la sesión.</span><span class="sxs-lookup"><span data-stu-id="8273f-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="8273f-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="8273f-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="8273f-132">Abre un objeto y devuelve un puntero de interfaz para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="8273f-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="8273f-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="8273f-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="8273f-134">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="8273f-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="8273f-135">Aconsej</span><span class="sxs-lookup"><span data-stu-id="8273f-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="8273f-136">Se registra para recibir una notificación de eventos especificados que afectan a la sesión.</span><span class="sxs-lookup"><span data-stu-id="8273f-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="8273f-137">Unadvise</span><span class="sxs-lookup"><span data-stu-id="8273f-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="8273f-138">Cancela el envío de notificaciones previamente configurado con una llamada al método adVise \*\*\*\* .</span><span class="sxs-lookup"><span data-stu-id="8273f-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="8273f-139">**MessageOptions**</span><span class="sxs-lookup"><span data-stu-id="8273f-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="8273f-140">*No es compatible o documentado.*</span><span class="sxs-lookup"><span data-stu-id="8273f-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="8273f-141">**QueryDefaultMessageOpt**</span><span class="sxs-lookup"><span data-stu-id="8273f-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="8273f-142">*No es compatible o documentado.*</span><span class="sxs-lookup"><span data-stu-id="8273f-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="8273f-143">EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="8273f-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="8273f-144">En desuso.</span><span class="sxs-lookup"><span data-stu-id="8273f-144">Deprecated.</span></span> <span data-ttu-id="8273f-145">Devuelve los tipos de direcciones que pueden controlar todos los proveedores de transporte de la sesión.</span><span class="sxs-lookup"><span data-stu-id="8273f-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="8273f-146">QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="8273f-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="8273f-147">Devuelve el identificador de entrada del objeto que proporciona la identidad principal para la sesión.</span><span class="sxs-lookup"><span data-stu-id="8273f-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="8273f-148">Cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="8273f-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="8273f-149">Finaliza una sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="8273f-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="8273f-150">SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="8273f-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="8273f-151">Establece un almacén de mensajes como el almacén de mensajes predeterminado para la sesión.</span><span class="sxs-lookup"><span data-stu-id="8273f-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="8273f-152">AdminServices</span><span class="sxs-lookup"><span data-stu-id="8273f-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="8273f-153">Devuelve un puntero [IMsgServiceAdmin](imsgserviceadminiunknown.md) para realizar cambios en los servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8273f-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="8273f-154">ShowForm</span><span class="sxs-lookup"><span data-stu-id="8273f-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="8273f-155">Muestra un formulario.</span><span class="sxs-lookup"><span data-stu-id="8273f-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="8273f-156">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="8273f-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="8273f-157">Crea un token numérico que el método **ShowForm** usa para obtener acceso a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8273f-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8273f-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="8273f-158">See also</span></span>



[<span data-ttu-id="8273f-159">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="8273f-159">MAPI Interfaces</span></span>](mapi-interfaces.md)

