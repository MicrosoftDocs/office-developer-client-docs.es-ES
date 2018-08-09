---
title: IABLogon IUnknown
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
ms.openlocfilehash: 784430f1286c9a017337a0fae4b269757a56a3e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817122"
---
# <a name="iablogon--iunknown"></a><span data-ttu-id="0caf4-103">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0caf4-103">IABLogon : IUnknown</span></span>

  
  
<span data-ttu-id="0caf4-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0caf4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0caf4-105">Recursos de accesos en un proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="0caf4-105">Accesses resources in an address book provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0caf4-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0caf4-106">Header file:</span></span>  <br/> |<span data-ttu-id="0caf4-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="0caf4-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="0caf4-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="0caf4-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="0caf4-109">Objetos de inicio de sesión de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="0caf4-109">Address book logon objects</span></span>  <br/> |
|<span data-ttu-id="0caf4-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="0caf4-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="0caf4-111">Proveedores de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="0caf4-111">Address book providers</span></span>  <br/> |
|<span data-ttu-id="0caf4-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="0caf4-112">Called by:</span></span>  <br/> |<span data-ttu-id="0caf4-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="0caf4-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="0caf4-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="0caf4-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0caf4-115">IID_IABLogon</span><span class="sxs-lookup"><span data-stu-id="0caf4-115">IID_IABLogon</span></span>  <br/> |
|<span data-ttu-id="0caf4-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="0caf4-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="0caf4-117">LPABLOGON</span><span class="sxs-lookup"><span data-stu-id="0caf4-117">LPABLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0caf4-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="0caf4-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0caf4-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="0caf4-119">GetLastError</span></span>](iablogon-getlasterror.md) <br/> |<span data-ttu-id="0caf4-120">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de proveedor de la libreta de direcciones anterior.</span><span class="sxs-lookup"><span data-stu-id="0caf4-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span>  <br/> |
|[<span data-ttu-id="0caf4-121">Cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="0caf4-121">Logoff</span></span>](iablogon-logoff.md) <br/> |<span data-ttu-id="0caf4-122">Inicia el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="0caf4-122">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="0caf4-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="0caf4-123">OpenEntry</span></span>](iablogon-openentry.md) <br/> |<span data-ttu-id="0caf4-124">Se abre un contenedor, usuario o lista de distribución, de mensajería y devuelve un puntero a una implementación de interfaz para proporcionar más acceso.</span><span class="sxs-lookup"><span data-stu-id="0caf4-124">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="0caf4-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="0caf4-125">CompareEntryIDs</span></span>](iablogon-compareentryids.md) <br/> |<span data-ttu-id="0caf4-126">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="0caf4-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="0caf4-127">Aviso</span><span class="sxs-lookup"><span data-stu-id="0caf4-127">Advise</span></span>](iablogon-advise.md) <br/> |<span data-ttu-id="0caf4-128">Registra el autor de la llamada para recibir notificaciones de los eventos que afectan a un contenedor, usuario o lista de distribución de mensajería.</span><span class="sxs-lookup"><span data-stu-id="0caf4-128">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>  <br/> |
|[<span data-ttu-id="0caf4-129">Desaconsejar</span><span class="sxs-lookup"><span data-stu-id="0caf4-129">Unadvise</span></span>](iablogon-unadvise.md) <br/> |<span data-ttu-id="0caf4-130">Cancela las notificaciones que se han configurado previamente con una llamada al método **Advise** .</span><span class="sxs-lookup"><span data-stu-id="0caf4-130">Cancels notifications that were previously set up with a call to the **Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="0caf4-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="0caf4-131">OpenStatusEntry</span></span>](iablogon-openstatusentry.md) <br/> |<span data-ttu-id="0caf4-132">Se abre el objeto de estado del proveedor.</span><span class="sxs-lookup"><span data-stu-id="0caf4-132">Opens the provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="0caf4-133">OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="0caf4-133">OpenTemplateID</span></span>](iablogon-opentemplateid.md) <br/> |<span data-ttu-id="0caf4-134">Se abre una entrada del destinatario que tiene datos que residen en un proveedor de libreta de direcciones de host.</span><span class="sxs-lookup"><span data-stu-id="0caf4-134">Opens a recipient entry that has data residing in a host address book provider.</span></span>  <br/> |
|[<span data-ttu-id="0caf4-135">GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="0caf4-135">GetOneOffTable</span></span>](iablogon-getoneofftable.md) <br/> |<span data-ttu-id="0caf4-136">Devuelve un objeto table de plantillas de uso único para la creación de los destinatarios que se agregará a la lista de destinatarios de un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="0caf4-136">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="0caf4-137">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="0caf4-137">PrepareRecips</span></span>](iablogon-preparerecips.md) <br/> |<span data-ttu-id="0caf4-138">Prepara una lista de destinatarios para usarlo más adelante mediante el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="0caf4-138">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0caf4-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0caf4-139">Remarks</span></span>

<span data-ttu-id="0caf4-140">Para obtener información general acerca de los métodos de la interfaz **IABLogon** , vea [Implementación de inicio de sesión de proveedor de servicio](implementing-service-provider-logon.md).</span><span class="sxs-lookup"><span data-stu-id="0caf4-140">For general information about the methods of the **IABLogon** interface, see [Implementing Service Provider Logon](implementing-service-provider-logon.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0caf4-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="0caf4-141">See also</span></span>



[<span data-ttu-id="0caf4-142">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="0caf4-142">MAPI Interfaces</span></span>](mapi-interfaces.md)

