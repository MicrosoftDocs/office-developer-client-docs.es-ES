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
ms.openlocfilehash: 991e48aa458a58ad2d7d688e81dbb357ef9bda5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428882"
---
# <a name="imslogon--iunknown"></a><span data-ttu-id="94259-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="94259-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="94259-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94259-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94259-105">Accede a los recursos de un objeto de inicio de sesión del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="94259-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="94259-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="94259-106">Header file:</span></span>  <br/> |<span data-ttu-id="94259-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="94259-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="94259-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="94259-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="94259-109">Objetos de inicio de sesión del almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="94259-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="94259-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="94259-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="94259-111">Proveedores de al almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="94259-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="94259-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="94259-112">Called by:</span></span>  <br/> |<span data-ttu-id="94259-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="94259-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="94259-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="94259-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="94259-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="94259-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="94259-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="94259-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="94259-117">LPMSLOGON</span><span class="sxs-lookup"><span data-stu-id="94259-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="94259-118">Orden de tabla virtual</span><span class="sxs-lookup"><span data-stu-id="94259-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="94259-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="94259-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="94259-120">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el último error que se produjo para el objeto de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="94259-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="94259-121">Cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="94259-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="94259-122">Cierra la sesión de un proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="94259-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="94259-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="94259-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="94259-124">Abre una carpeta o un objeto de mensaje y devuelve un puntero al objeto para proporcionar más acceso.</span><span class="sxs-lookup"><span data-stu-id="94259-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="94259-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="94259-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="94259-126">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="94259-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="94259-127">Aconsejar</span><span class="sxs-lookup"><span data-stu-id="94259-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="94259-128">Registra un objeto con un proveedor de almacenamiento de mensajes para recibir notificaciones sobre los cambios en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="94259-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="94259-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="94259-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="94259-130">Quita el registro de un objeto para la notificación de los cambios del almacén de mensajes establecidos anteriormente mediante una llamada al método **IMSLogon::Advise.**</span><span class="sxs-lookup"><span data-stu-id="94259-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="94259-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="94259-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="94259-132">Abre un objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="94259-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94259-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="94259-133">Remarks</span></span>

<span data-ttu-id="94259-134">El objeto de inicio de sesión del almacén de mensajes es la parte de un proveedor de almacén de mensajes abierto al que MAPI llama directamente.</span><span class="sxs-lookup"><span data-stu-id="94259-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="94259-135">Hay una correspondencia uno a uno entre el objeto de inicio de sesión del almacén de mensajes al que llama MAPI y el objeto de almacén de mensajes al que llaman las aplicaciones cliente; Puede pensar en el inicio de sesión y almacenar objetos como un objeto que expone dos interfaces.</span><span class="sxs-lookup"><span data-stu-id="94259-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="94259-136">Los dos objetos se crean juntos y se liberan juntos.</span><span class="sxs-lookup"><span data-stu-id="94259-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="94259-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="94259-137">See also</span></span>



[<span data-ttu-id="94259-138">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="94259-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

