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
ms.openlocfilehash: 42e2633ac6d534be2c75c47b24c1da5ed9771e18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817810"
---
# <a name="imslogon--iunknown"></a><span data-ttu-id="09940-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="09940-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="09940-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="09940-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="09940-105">Recursos de accesos en un mensaje almacenan el objeto de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="09940-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="09940-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="09940-106">Header file:</span></span>  <br/> |<span data-ttu-id="09940-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="09940-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="09940-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="09940-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="09940-109">Objetos de inicio de sesión del almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="09940-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="09940-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="09940-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="09940-111">Proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="09940-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="09940-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="09940-112">Called by:</span></span>  <br/> |<span data-ttu-id="09940-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="09940-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="09940-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="09940-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="09940-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="09940-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="09940-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="09940-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="09940-117">LPMSLOGON</span><span class="sxs-lookup"><span data-stu-id="09940-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="09940-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="09940-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="09940-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="09940-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="09940-120">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el último error que se ha producido para el objeto de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="09940-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="09940-121">Cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="09940-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="09940-122">Proveedor de almacén de registros de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="09940-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="09940-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="09940-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="09940-124">Se abre una carpeta o un objeto de mensaje y devuelve un puntero al objeto para proporcionar más acceso.</span><span class="sxs-lookup"><span data-stu-id="09940-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="09940-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="09940-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="09940-126">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="09940-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="09940-127">Aviso</span><span class="sxs-lookup"><span data-stu-id="09940-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="09940-128">Registra un objeto con un proveedor de almacén de mensajes para las notificaciones sobre cambios en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="09940-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="09940-129">Desaconsejar</span><span class="sxs-lookup"><span data-stu-id="09940-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="09940-130">Quita el registro de un objeto de notificación de cambios del almacén de mensajes ha establecido previamente mediante una llamada al método **IMSLogon::Advise** .</span><span class="sxs-lookup"><span data-stu-id="09940-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="09940-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="09940-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="09940-132">Abre un objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="09940-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="09940-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09940-133">Remarks</span></span>

<span data-ttu-id="09940-134">El objeto de inicio de sesión del almacén de mensajes es la parte de un proveedor de almacén de abrir el mensaje MAPI llama directamente.</span><span class="sxs-lookup"><span data-stu-id="09940-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="09940-135">Hay una correspondencia uno a uno entre el objeto de inicio de sesión del almacén de mensajes que las llamadas MAPI y el mensaje de almacenan objetos que llaman a las aplicaciones cliente; Puede pensar en el inicio de sesión y almacenar objetos como un objeto que expone dos interfaces.</span><span class="sxs-lookup"><span data-stu-id="09940-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="09940-136">Los dos objetos se crean juntos y liberado juntos.</span><span class="sxs-lookup"><span data-stu-id="09940-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="09940-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="09940-137">See also</span></span>



[<span data-ttu-id="09940-138">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="09940-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

