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
ms.openlocfilehash: a37d8138547c8c4e9308dbb0ebbc6750b152d795
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817469"
---
# <a name="imapisession--iunknown"></a><span data-ttu-id="327bd-103">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="327bd-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="327bd-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="327bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="327bd-105">Administra los objetos asociados a una sesión de inicio de sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="327bd-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="327bd-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="327bd-106">Header file:</span></span>  <br/> |<span data-ttu-id="327bd-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="327bd-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="327bd-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="327bd-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="327bd-109">Objetos de sesión</span><span class="sxs-lookup"><span data-stu-id="327bd-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="327bd-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="327bd-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="327bd-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="327bd-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="327bd-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="327bd-112">Called by:</span></span>  <br/> |<span data-ttu-id="327bd-113">Las aplicaciones cliente y MAPI</span><span class="sxs-lookup"><span data-stu-id="327bd-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="327bd-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="327bd-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="327bd-115">IID_IMAPISession</span><span class="sxs-lookup"><span data-stu-id="327bd-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="327bd-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="327bd-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="327bd-117">LPMAPISESSION</span><span class="sxs-lookup"><span data-stu-id="327bd-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="327bd-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="327bd-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="327bd-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="327bd-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="327bd-120">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de la sesión anterior.</span><span class="sxs-lookup"><span data-stu-id="327bd-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="327bd-121">GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="327bd-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="327bd-122">Proporciona acceso a la tabla de almacenamiento de mensaje que contiene información acerca de todos los almacenes de mensaje en el perfil de sesión.</span><span class="sxs-lookup"><span data-stu-id="327bd-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="327bd-123">OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="327bd-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="327bd-124">Se abre un almacén de mensajes y devuelve un puntero [IMsgStore](imsgstoreimapiprop.md) para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="327bd-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="327bd-125">OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="327bd-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="327bd-126">Se abre la libreta de direcciones integrada de MAPI, la devolución de un puntero [IAddrBook](iaddrbookimapiprop.md) para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="327bd-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="327bd-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="327bd-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="327bd-128">Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="327bd-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="327bd-129">GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="327bd-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="327bd-130">Proporciona acceso a la tabla de estado, una tabla que contiene información acerca de todos los recursos MAPI en la sesión.</span><span class="sxs-lookup"><span data-stu-id="327bd-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="327bd-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="327bd-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="327bd-132">Se abre un objeto y devuelve un puntero de interfaz para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="327bd-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="327bd-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="327bd-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="327bd-134">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="327bd-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="327bd-135">Aviso</span><span class="sxs-lookup"><span data-stu-id="327bd-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="327bd-136">Se registra para recibir notificaciones de los eventos que afectan a la sesión.</span><span class="sxs-lookup"><span data-stu-id="327bd-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="327bd-137">Desaconsejar</span><span class="sxs-lookup"><span data-stu-id="327bd-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="327bd-138">Cancela el envío de notificaciones configuradas previamente con una llamada al método **Advise** .</span><span class="sxs-lookup"><span data-stu-id="327bd-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="327bd-139">**Opciones de mensaje**</span><span class="sxs-lookup"><span data-stu-id="327bd-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="327bd-140">*No se admiten o documentado.*</span><span class="sxs-lookup"><span data-stu-id="327bd-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="327bd-141">**QueryDefaultMessageOpt**</span><span class="sxs-lookup"><span data-stu-id="327bd-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="327bd-142">*No se admiten o documentado.*</span><span class="sxs-lookup"><span data-stu-id="327bd-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="327bd-143">EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="327bd-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="327bd-144">En desuso.</span><span class="sxs-lookup"><span data-stu-id="327bd-144">Deprecated.</span></span> <span data-ttu-id="327bd-145">Devuelve los tipos de direcciones que se pueden controlar por todos los proveedores de transporte en la sesión.</span><span class="sxs-lookup"><span data-stu-id="327bd-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="327bd-146">QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="327bd-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="327bd-147">Devuelve el identificador de entrada del objeto que proporciona la identidad principal para la sesión.</span><span class="sxs-lookup"><span data-stu-id="327bd-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="327bd-148">Cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="327bd-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="327bd-149">Termina una sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="327bd-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="327bd-150">SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="327bd-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="327bd-151">Establece un almacén de mensajes como el almacén de mensajes predeterminado para la sesión.</span><span class="sxs-lookup"><span data-stu-id="327bd-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="327bd-152">AdminServices</span><span class="sxs-lookup"><span data-stu-id="327bd-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="327bd-153">Devuelve un puntero [IMsgServiceAdmin](imsgserviceadminiunknown.md) para realizar cambios en los servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="327bd-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="327bd-154">ShowForm</span><span class="sxs-lookup"><span data-stu-id="327bd-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="327bd-155">Muestra un formulario.</span><span class="sxs-lookup"><span data-stu-id="327bd-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="327bd-156">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="327bd-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="327bd-157">Crea un token numérico que usa el método **ShowForm** para tener acceso a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="327bd-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="327bd-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="327bd-158">See also</span></span>



[<span data-ttu-id="327bd-159">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="327bd-159">MAPI Interfaces</span></span>](mapi-interfaces.md)

