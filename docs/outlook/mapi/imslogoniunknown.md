---
title: IUnknown IMSLogon
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
ms.openlocfilehash: 991e48aa458a58ad2d7d688e81dbb357ef9bda5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428882"
---
# <a name="imslogon--iunknown"></a><span data-ttu-id="e1542-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1542-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="e1542-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1542-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1542-105">Obtiene acceso a los recursos de un objeto de inicio de sesión del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e1542-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1542-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e1542-106">Header file:</span></span>  <br/> |<span data-ttu-id="e1542-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="e1542-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="e1542-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="e1542-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="e1542-109">Objetos de inicio de sesión del almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="e1542-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="e1542-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e1542-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="e1542-111">Proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="e1542-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="e1542-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e1542-112">Called by:</span></span>  <br/> |<span data-ttu-id="e1542-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="e1542-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="e1542-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="e1542-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e1542-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="e1542-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="e1542-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="e1542-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="e1542-117">LPMSLOGON</span><span class="sxs-lookup"><span data-stu-id="e1542-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e1542-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="e1542-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e1542-119">Volvió</span><span class="sxs-lookup"><span data-stu-id="e1542-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="e1542-120">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el último error que se produjo en el objeto de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e1542-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="e1542-121">Cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="e1542-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="e1542-122">Cierra la sesión de un proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e1542-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="e1542-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="e1542-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="e1542-124">Abre un objeto Folder o Message y devuelve un puntero al objeto para proporcionar más acceso.</span><span class="sxs-lookup"><span data-stu-id="e1542-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="e1542-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="e1542-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="e1542-126">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="e1542-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="e1542-127">Aconsej</span><span class="sxs-lookup"><span data-stu-id="e1542-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="e1542-128">Registra un objeto con un proveedor de almacenamiento de mensajes para notificaciones sobre cambios en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e1542-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="e1542-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="e1542-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="e1542-130">Quita el registro de un objeto para notificaciones de cambios del almacén de mensajes previamente establecidos mediante una llamada al método **IMSLogon:: Advise** .</span><span class="sxs-lookup"><span data-stu-id="e1542-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="e1542-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="e1542-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="e1542-132">Abre un objeto status.</span><span class="sxs-lookup"><span data-stu-id="e1542-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1542-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e1542-133">Remarks</span></span>

<span data-ttu-id="e1542-134">El objeto de inicio de sesión del almacén de mensajes es la parte de un proveedor de almacenamiento de mensajes abierto que MAPI llama directamente.</span><span class="sxs-lookup"><span data-stu-id="e1542-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="e1542-135">Hay una correspondencia de uno a uno entre el objeto de inicio de sesión del almacén de mensajes al que llaman las llamadas MAPI y el objeto almacén de mensajes al que llaman las aplicaciones cliente; puede considerar los objetos de inicio de sesión y de almacén como un objeto que expone dos interfaces.</span><span class="sxs-lookup"><span data-stu-id="e1542-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="e1542-136">Los dos objetos se crean y se liberan juntos.</span><span class="sxs-lookup"><span data-stu-id="e1542-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e1542-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="e1542-137">See also</span></span>



[<span data-ttu-id="e1542-138">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="e1542-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

