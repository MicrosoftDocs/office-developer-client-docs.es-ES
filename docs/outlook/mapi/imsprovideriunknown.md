---
title: IUnknown IMSProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider
api_type:
- COM
ms.assetid: 0f17aa44-abcb-4732-b013-d91652847cf6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c5305ddd20b690f5c2e5807fb7ce2410549f7124
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317253"
---
# <a name="imsprovider--iunknown"></a><span data-ttu-id="63cee-103">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="63cee-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="63cee-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63cee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63cee-105">Proporciona acceso a un proveedor de almacenamiento de mensajes a través de un objeto de proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="63cee-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="63cee-106">Este objeto de proveedor de almacén de mensajes se devuelve al iniciar la sesión de proveedor mediante la función de punto de entrada [MSProviderInit](msproviderinit.md) del proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="63cee-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="63cee-107">El objeto de proveedor de almacén de mensajes lo usan principalmente las aplicaciones cliente y la cola MAPI para abrir los almacenes de mensajes.</span><span class="sxs-lookup"><span data-stu-id="63cee-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="63cee-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="63cee-108">Header file:</span></span>  <br/> |<span data-ttu-id="63cee-109">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="63cee-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="63cee-110">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="63cee-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="63cee-111">Objetos de proveedor de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="63cee-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="63cee-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="63cee-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="63cee-113">Proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="63cee-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="63cee-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="63cee-114">Called by:</span></span>  <br/> |<span data-ttu-id="63cee-115">MAPI y la cola MAPI</span><span class="sxs-lookup"><span data-stu-id="63cee-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="63cee-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="63cee-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="63cee-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="63cee-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="63cee-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="63cee-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="63cee-119">LPMSPROVIDER</span><span class="sxs-lookup"><span data-stu-id="63cee-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="63cee-120">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="63cee-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="63cee-121">Apagado</span><span class="sxs-lookup"><span data-stu-id="63cee-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="63cee-122">Cierra un proveedor de almacenamiento de mensajes de manera ordenada.</span><span class="sxs-lookup"><span data-stu-id="63cee-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="63cee-123">Inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="63cee-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="63cee-124">Registra MAPI en una instancia de un proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="63cee-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="63cee-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="63cee-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="63cee-126">Registra la cola MAPI en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="63cee-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="63cee-127">CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="63cee-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="63cee-128">Compara dos identificadores de entrada del almacén de mensajes para determinar si hacen referencia al mismo objeto Store.</span><span class="sxs-lookup"><span data-stu-id="63cee-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63cee-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63cee-129">Remarks</span></span>

<span data-ttu-id="63cee-130">MAPI usa un objeto de proveedor de almacén de mensajes por sesión, independientemente de cuántos almacenes de mensajes haya abierto el proveedor del almacén.</span><span class="sxs-lookup"><span data-stu-id="63cee-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="63cee-131">Si una segunda sesión MAPI inicia sesión en cualquier tienda abierta, las llamadas MAPI **MSProviderInit** una segunda vez para crear un nuevo objeto de proveedor de almacén de mensajes para que la sesión la use.</span><span class="sxs-lookup"><span data-stu-id="63cee-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="63cee-132">Un objeto de proveedor de almacén de mensajes debe contener lo siguiente para funcionar correctamente:</span><span class="sxs-lookup"><span data-stu-id="63cee-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="63cee-133">Un puntero de rutina de asignación de memoria de _lpMalloc_ para su uso en todos los almacenes abiertos mediante este objeto de proveedor.</span><span class="sxs-lookup"><span data-stu-id="63cee-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="63cee-134">Los punteros de la rutina _lpfAllocateBuffer_, _ lpfAllocateMore _ y _lpfFreeBuffer_ a las funciones de asignación de memoria [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="63cee-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="63cee-135">Una lista vinculada de todos los almacenes abiertos con este objeto de proveedor y que aún no se han cerrado.</span><span class="sxs-lookup"><span data-stu-id="63cee-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63cee-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="63cee-136">See also</span></span>



[<span data-ttu-id="63cee-137">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="63cee-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

