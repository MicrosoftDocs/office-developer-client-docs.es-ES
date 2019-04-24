---
title: IUnknown IABLogon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon
api_type:
- COM
ms.assetid: fe340182-f41e-42e7-b8e8-cc005b1e9a5f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fc8615fcd984623ae9c17c45fb7b51a4498a723b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348835"
---
# <a name="iablogon--iunknown"></a><span data-ttu-id="35fc2-103">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35fc2-103">IABLogon : IUnknown</span></span>

  
  
<span data-ttu-id="35fc2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35fc2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35fc2-105">Tiene acceso a los recursos de un proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="35fc2-105">Accesses resources in an address book provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35fc2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="35fc2-106">Header file:</span></span>  <br/> |<span data-ttu-id="35fc2-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="35fc2-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="35fc2-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="35fc2-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="35fc2-109">Objetos de inicio de sesión de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="35fc2-109">Address book logon objects</span></span>  <br/> |
|<span data-ttu-id="35fc2-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="35fc2-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="35fc2-111">Proveedores de libretas de direcciones</span><span class="sxs-lookup"><span data-stu-id="35fc2-111">Address book providers</span></span>  <br/> |
|<span data-ttu-id="35fc2-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="35fc2-112">Called by:</span></span>  <br/> |<span data-ttu-id="35fc2-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="35fc2-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="35fc2-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="35fc2-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="35fc2-115">IID_IABLogon</span><span class="sxs-lookup"><span data-stu-id="35fc2-115">IID_IABLogon</span></span>  <br/> |
|<span data-ttu-id="35fc2-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="35fc2-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="35fc2-117">LPABLOGON</span><span class="sxs-lookup"><span data-stu-id="35fc2-117">LPABLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="35fc2-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="35fc2-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="35fc2-119">Volvió</span><span class="sxs-lookup"><span data-stu-id="35fc2-119">GetLastError</span></span>](iablogon-getlasterror.md) <br/> |<span data-ttu-id="35fc2-120">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior del proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="35fc2-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span>  <br/> |
|[<span data-ttu-id="35fc2-121">Cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="35fc2-121">Logoff</span></span>](iablogon-logoff.md) <br/> |<span data-ttu-id="35fc2-122">Inicia el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="35fc2-122">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="35fc2-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="35fc2-123">OpenEntry</span></span>](iablogon-openentry.md) <br/> |<span data-ttu-id="35fc2-124">Abre un contenedor, un usuario de mensajería o una lista de distribución y devuelve un puntero a una implementación de interfaz para proporcionar más acceso.</span><span class="sxs-lookup"><span data-stu-id="35fc2-124">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="35fc2-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="35fc2-125">CompareEntryIDs</span></span>](iablogon-compareentryids.md) <br/> |<span data-ttu-id="35fc2-126">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="35fc2-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="35fc2-127">Aconsej</span><span class="sxs-lookup"><span data-stu-id="35fc2-127">Advise</span></span>](iablogon-advise.md) <br/> |<span data-ttu-id="35fc2-128">Registra el autor de la llamada para recibir una notificación de los eventos especificados que afectan a un contenedor, un usuario de mensajería o una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="35fc2-128">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>  <br/> |
|[<span data-ttu-id="35fc2-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="35fc2-129">Unadvise</span></span>](iablogon-unadvise.md) <br/> |<span data-ttu-id="35fc2-130">Cancela las notificaciones que se configuraron anteriormente con una llamada al \*\*\*\* método Advise.</span><span class="sxs-lookup"><span data-stu-id="35fc2-130">Cancels notifications that were previously set up with a call to the **Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="35fc2-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="35fc2-131">OpenStatusEntry</span></span>](iablogon-openstatusentry.md) <br/> |<span data-ttu-id="35fc2-132">Abre el objeto de estado del proveedor.</span><span class="sxs-lookup"><span data-stu-id="35fc2-132">Opens the provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="35fc2-133">OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="35fc2-133">OpenTemplateID</span></span>](iablogon-opentemplateid.md) <br/> |<span data-ttu-id="35fc2-134">Abre una entrada de destinatario que tiene datos que residen en un proveedor de la libreta de direcciones de host.</span><span class="sxs-lookup"><span data-stu-id="35fc2-134">Opens a recipient entry that has data residing in a host address book provider.</span></span>  <br/> |
|[<span data-ttu-id="35fc2-135">GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="35fc2-135">GetOneOffTable</span></span>](iablogon-getoneofftable.md) <br/> |<span data-ttu-id="35fc2-136">Devuelve una tabla de plantillas de uso único para crear los destinatarios que se agregarán a la lista de destinatarios de un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="35fc2-136">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="35fc2-137">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="35fc2-137">PrepareRecips</span></span>](iablogon-preparerecips.md) <br/> |<span data-ttu-id="35fc2-138">Prepara una lista de destinatarios para su uso posterior por parte del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="35fc2-138">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35fc2-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="35fc2-139">Remarks</span></span>

<span data-ttu-id="35fc2-140">Para obtener información general acerca de los métodos de la interfaz **IABLogon** , vea [implementar el inicio de sesión del proveedor de servicios](implementing-service-provider-logon.md).</span><span class="sxs-lookup"><span data-stu-id="35fc2-140">For general information about the methods of the **IABLogon** interface, see [Implementing Service Provider Logon](implementing-service-provider-logon.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="35fc2-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="35fc2-141">See also</span></span>



[<span data-ttu-id="35fc2-142">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="35fc2-142">MAPI Interfaces</span></span>](mapi-interfaces.md)

