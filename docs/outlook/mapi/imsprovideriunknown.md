---
title: IMSProvider IUnknown
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412866"
---
# <a name="imsprovider--iunknown"></a><span data-ttu-id="eccd6-103">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eccd6-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="eccd6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eccd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eccd6-105">Proporciona acceso a un proveedor de almacenamiento de mensajes a través de un objeto de proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="eccd6-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="eccd6-106">La función de punto de entrada [MSProviderInit](msproviderinit.md) del proveedor del almacén de mensajes devuelve este objeto de proveedor de almacenamiento de mensajes en el inicio de sesión del proveedor de mensajes.</span><span class="sxs-lookup"><span data-stu-id="eccd6-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="eccd6-107">El objeto del proveedor del almacén de mensajes lo usan principalmente las aplicaciones cliente y la cola MAPI para abrir almacenes de mensajes.</span><span class="sxs-lookup"><span data-stu-id="eccd6-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eccd6-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="eccd6-108">Header file:</span></span>  <br/> |<span data-ttu-id="eccd6-109">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="eccd6-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="eccd6-110">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="eccd6-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="eccd6-111">Objetos de proveedor de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="eccd6-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="eccd6-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="eccd6-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="eccd6-113">Proveedores de al almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="eccd6-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="eccd6-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="eccd6-114">Called by:</span></span>  <br/> |<span data-ttu-id="eccd6-115">MAPI y la cola MAPI</span><span class="sxs-lookup"><span data-stu-id="eccd6-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="eccd6-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="eccd6-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="eccd6-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="eccd6-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="eccd6-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="eccd6-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="eccd6-119">LPMSPROVIDER</span><span class="sxs-lookup"><span data-stu-id="eccd6-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="eccd6-120">Orden de tabla virtual</span><span class="sxs-lookup"><span data-stu-id="eccd6-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="eccd6-121">Apagado</span><span class="sxs-lookup"><span data-stu-id="eccd6-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="eccd6-122">Cierra un proveedor de almacén de mensajes de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="eccd6-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="eccd6-123">Inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="eccd6-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="eccd6-124">Registra MAPI en una instancia de un proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="eccd6-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="eccd6-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="eccd6-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="eccd6-126">Registra la cola MAPI en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="eccd6-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="eccd6-127">CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="eccd6-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="eccd6-128">Compara dos identificadores de entrada de almacén de mensajes para determinar si hacen referencia al mismo objeto de almacén.</span><span class="sxs-lookup"><span data-stu-id="eccd6-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eccd6-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eccd6-129">Remarks</span></span>

<span data-ttu-id="eccd6-130">MAPI usa un objeto de proveedor de almacenamiento de mensajes por sesión, independientemente de cuántos almacenes de mensajes abra el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="eccd6-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="eccd6-131">Si una segunda sesión MAPI inicia sesión en algún almacén abierto, MAPI llama a **MSProviderInit** una segunda vez para crear un nuevo objeto de proveedor de almacén de mensajes para que la sesión la use.</span><span class="sxs-lookup"><span data-stu-id="eccd6-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="eccd6-132">Un objeto de proveedor de almacén de mensajes debe contener lo siguiente para funcionar correctamente:</span><span class="sxs-lookup"><span data-stu-id="eccd6-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="eccd6-133">Puntero de rutina de asignación de memoria  _lpMalloc_ para que lo usen todos los almacenes abiertos mediante este objeto de proveedor.</span><span class="sxs-lookup"><span data-stu-id="eccd6-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="eccd6-134">Los punteros de rutina _lpfAllocateBuffer_, _ lpfAllocateMore _y _lpfFreeBuffer_ a las funciones de asignación de memoria [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="eccd6-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="eccd6-135">Una lista vinculada de todos los almacenes abiertos mediante este objeto de proveedor y aún no cerrados.</span><span class="sxs-lookup"><span data-stu-id="eccd6-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eccd6-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="eccd6-136">See also</span></span>



[<span data-ttu-id="eccd6-137">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="eccd6-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

