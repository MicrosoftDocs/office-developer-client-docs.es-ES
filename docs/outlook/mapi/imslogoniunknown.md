---
title: IMSLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon
api_type:
- COM
ms.assetid: d87093dc-f705-465f-ab3c-944ca0cd3e54
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 013903f36bf648c4aed194c88104e7dd981b199f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563943"
---
# <a name="imslogon--iunknown"></a><span data-ttu-id="3fc90-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3fc90-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="3fc90-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fc90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fc90-105">Recursos de accesos en un mensaje almacenan el objeto de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="3fc90-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3fc90-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="3fc90-106">Header file:</span></span>  <br/> |<span data-ttu-id="3fc90-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="3fc90-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="3fc90-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="3fc90-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="3fc90-109">Objetos de inicio de sesión del almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="3fc90-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="3fc90-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="3fc90-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="3fc90-111">Proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="3fc90-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="3fc90-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="3fc90-112">Called by:</span></span>  <br/> |<span data-ttu-id="3fc90-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="3fc90-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="3fc90-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="3fc90-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3fc90-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="3fc90-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="3fc90-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="3fc90-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="3fc90-117">LPMSLOGON</span><span class="sxs-lookup"><span data-stu-id="3fc90-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3fc90-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="3fc90-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3fc90-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="3fc90-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="3fc90-120">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el último error que se ha producido para el objeto de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="3fc90-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="3fc90-121">Cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="3fc90-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="3fc90-122">Proveedor de almacén de registros de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="3fc90-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="3fc90-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="3fc90-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="3fc90-124">Se abre una carpeta o un objeto de mensaje y devuelve un puntero al objeto para proporcionar más acceso.</span><span class="sxs-lookup"><span data-stu-id="3fc90-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="3fc90-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="3fc90-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="3fc90-126">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="3fc90-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="3fc90-127">Aviso</span><span class="sxs-lookup"><span data-stu-id="3fc90-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="3fc90-128">Registra un objeto con un proveedor de almacén de mensajes para las notificaciones sobre cambios en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="3fc90-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="3fc90-129">Desaconsejar</span><span class="sxs-lookup"><span data-stu-id="3fc90-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="3fc90-130">Quita el registro de un objeto de notificación de cambios del almacén de mensajes ha establecido previamente mediante una llamada al método **IMSLogon::Advise** .</span><span class="sxs-lookup"><span data-stu-id="3fc90-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="3fc90-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="3fc90-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="3fc90-132">Abre un objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="3fc90-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fc90-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3fc90-133">Remarks</span></span>

<span data-ttu-id="3fc90-134">El objeto de inicio de sesión del almacén de mensajes es la parte de un proveedor de almacén de abrir el mensaje MAPI llama directamente.</span><span class="sxs-lookup"><span data-stu-id="3fc90-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="3fc90-135">Hay una correspondencia uno a uno entre el objeto de inicio de sesión del almacén de mensajes que las llamadas MAPI y el mensaje de almacenan objetos que llaman a las aplicaciones cliente; Puede pensar en el inicio de sesión y almacenar objetos como un objeto que expone dos interfaces.</span><span class="sxs-lookup"><span data-stu-id="3fc90-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="3fc90-136">Los dos objetos se crean juntos y liberado juntos.</span><span class="sxs-lookup"><span data-stu-id="3fc90-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3fc90-137">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="3fc90-137">See also</span></span>



[<span data-ttu-id="3fc90-138">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="3fc90-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

