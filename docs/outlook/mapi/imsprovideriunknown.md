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
ms.openlocfilehash: 9444806347c97077b03922b116e2ed7f61665cc1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817808"
---
# <a name="imsprovider--iunknown"></a><span data-ttu-id="40323-103">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="40323-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="40323-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40323-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40323-105">Proporciona acceso a un proveedor de almacén de mensajes a través de un objeto de proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="40323-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="40323-106">Este objeto de proveedor de almacén de mensajes se devuelve al inicio de sesión de proveedor mediante la función de punto de entrada de [MSProviderInit](msproviderinit.md) del proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="40323-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="40323-107">El objeto de proveedor de almacén de mensajes se usa principalmente en las aplicaciones cliente y la cola de MAPI para abrir los almacenes de mensajes.</span><span class="sxs-lookup"><span data-stu-id="40323-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40323-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="40323-108">Header file:</span></span>  <br/> |<span data-ttu-id="40323-109">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="40323-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="40323-110">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="40323-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="40323-111">Objetos de proveedor de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="40323-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="40323-112">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="40323-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="40323-113">Proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="40323-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="40323-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="40323-114">Called by:</span></span>  <br/> |<span data-ttu-id="40323-115">MAPI y la cola de MAPI</span><span class="sxs-lookup"><span data-stu-id="40323-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="40323-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="40323-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="40323-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="40323-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="40323-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="40323-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="40323-119">LPMSPROVIDER</span><span class="sxs-lookup"><span data-stu-id="40323-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="40323-120">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="40323-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="40323-121">Apagado</span><span class="sxs-lookup"><span data-stu-id="40323-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="40323-122">Cierra un proveedor de almacén de mensajes de una forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="40323-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="40323-123">Inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="40323-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="40323-124">Registros MAPI sesión en una instancia de un proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="40323-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="40323-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="40323-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="40323-126">Inicie sesión en un almacén de mensajes en la cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="40323-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="40323-127">CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="40323-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="40323-128">Compara dos mensajes almacén de los identificadores de entrada para determinar si hacen referencia al mismo objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="40323-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40323-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40323-129">Remarks</span></span>

<span data-ttu-id="40323-130">MAPI utiliza un objeto de proveedor de almacén de mensajes por sesión, independientemente de cuántos mensajes se abren los almacenes por el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="40323-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="40323-131">Si un segundo MAPI sesión inicia sesión en todos los almacenes, MAPI llama **MSProviderInit** una segunda vez para crear un nuevo objeto de proveedor de almacén de mensajes de esa sesión a usar.</span><span class="sxs-lookup"><span data-stu-id="40323-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="40323-132">Un objeto de proveedor de almacén de mensajes debe contener lo siguiente para funcionar correctamente:</span><span class="sxs-lookup"><span data-stu-id="40323-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="40323-133">Un _lpMalloc_ asignación de memoria rutinarias puntero para su uso por todos los almacenes que se abrieron con este objeto de proveedor.</span><span class="sxs-lookup"><span data-stu-id="40323-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="40323-134">El _lpfAllocateBuffer_, _ lpfAllocateMore _ y punteros de rutina _lpfFreeBuffer_ a las funciones de asignación de memoria [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="40323-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="40323-135">Una lista vinculada de todos los almacenes abierto mediante el uso de este objeto de proveedor y aún no se ha cerrado.</span><span class="sxs-lookup"><span data-stu-id="40323-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40323-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="40323-136">See also</span></span>



[<span data-ttu-id="40323-137">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="40323-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

