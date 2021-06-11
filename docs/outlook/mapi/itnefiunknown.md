---
title: ITnef IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef
api_type:
- COM
ms.assetid: eddca896-9497-4425-9904-87ef3cbae298
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1f815a914deb5e21f3d913abe46a84cc7a32b4ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428518"
---
# <a name="itnef--iunknown"></a><span data-ttu-id="b0f7f-103">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0f7f-103">ITnef : IUnknown</span></span>

  
  
<span data-ttu-id="b0f7f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0f7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0f7f-105">Proporciona métodos para encapsular propiedades MAPI que no son compatibles con un sistema de mensajería en secuencias binarias que se pueden adjuntar a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="b0f7f-105">Provides methods for encapsulating MAPI properties that are not supported by a messaging system into binary streams that can be attached to messages.</span></span> <span data-ttu-id="b0f7f-106">El formato usado para esta encapsulación es el Transport-Neutral de encapsulación (TNEF).</span><span class="sxs-lookup"><span data-stu-id="b0f7f-106">The format used for this encapsulation is the Transport-Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="b0f7f-107">A continuación, el proveedor de transporte de destino o la aplicación cliente basada en MAPI pueden, al recibir un mensaje que incluye datos adjuntos de TNEF, recuperar las propiedades de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="b0f7f-107">The target transport provider or MAPI-based client application can then, on receiving a message that includes a TNEF attachment, recover the properties from the attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0f7f-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b0f7f-108">Header file:</span></span>  <br/> |<span data-ttu-id="b0f7f-109">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="b0f7f-109">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="b0f7f-110">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="b0f7f-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="b0f7f-111">Objetos TNEF</span><span class="sxs-lookup"><span data-stu-id="b0f7f-111">TNEF objects</span></span>  <br/> |
|<span data-ttu-id="b0f7f-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b0f7f-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="b0f7f-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="b0f7f-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="b0f7f-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="b0f7f-114">Called by:</span></span>  <br/> |<span data-ttu-id="b0f7f-115">Proveedores de transporte, proveedores de almacén de mensajes y puertas de enlace</span><span class="sxs-lookup"><span data-stu-id="b0f7f-115">Transport providers, message store providers, and gateways</span></span>  <br/> |
|<span data-ttu-id="b0f7f-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="b0f7f-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b0f7f-117">IID_ITNEF</span><span class="sxs-lookup"><span data-stu-id="b0f7f-117">IID_ITNEF</span></span>  <br/> |
|<span data-ttu-id="b0f7f-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="b0f7f-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="b0f7f-119">LPTNEF</span><span class="sxs-lookup"><span data-stu-id="b0f7f-119">LPTNEF</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b0f7f-120">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="b0f7f-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b0f7f-121">AddProps</span><span class="sxs-lookup"><span data-stu-id="b0f7f-121">AddProps</span></span>](itnef-addprops.md) <br/> |<span data-ttu-id="b0f7f-122">Permite al proveedor de servicios de llamadas o puerta de enlace agregar propiedades a la encapsulación de un mensaje o datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="b0f7f-122">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span>  <br/> |
|[<span data-ttu-id="b0f7f-123">ExtractProps</span><span class="sxs-lookup"><span data-stu-id="b0f7f-123">ExtractProps</span></span>](itnef-extractprops.md) <br/> |<span data-ttu-id="b0f7f-124">Extrae las propiedades de una encapsulación TNEF.</span><span class="sxs-lookup"><span data-stu-id="b0f7f-124">Extracts the properties from a TNEF encapsulation.</span></span>  <br/> |
|[<span data-ttu-id="b0f7f-125">Finish</span><span class="sxs-lookup"><span data-stu-id="b0f7f-125">Finish</span></span>](itnef-finish.md) <br/> |<span data-ttu-id="b0f7f-126">Finaliza el procesamiento de todas las operaciones TNEF que están en cola y en espera.</span><span class="sxs-lookup"><span data-stu-id="b0f7f-126">Finishes processing for all TNEF operations that are queued and waiting.</span></span>  <br/> |
|[<span data-ttu-id="b0f7f-127">OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="b0f7f-127">OpenTaggedBody</span></span>](itnef-opentaggedbody.md) <br/> |<span data-ttu-id="b0f7f-128">Abre una interfaz de secuencia en el texto de un mensaje encapsulado.</span><span class="sxs-lookup"><span data-stu-id="b0f7f-128">Opens a stream interface on the text of an encapsulated message.</span></span>  <br/> |
|[<span data-ttu-id="b0f7f-129">SetProps</span><span class="sxs-lookup"><span data-stu-id="b0f7f-129">SetProps</span></span>](itnef-setprops.md) <br/> |<span data-ttu-id="b0f7f-130">Establece el valor de una o más propiedades para un mensaje encapsulado o datos adjuntos sin modificar el mensaje o los datos adjuntos originales.</span><span class="sxs-lookup"><span data-stu-id="b0f7f-130">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span>  <br/> |
|[<span data-ttu-id="b0f7f-131">EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="b0f7f-131">EncodeRecips</span></span>](itnef-encoderecips.md) <br/> |<span data-ttu-id="b0f7f-132">Codifica una vista de la tabla de destinatarios de un mensaje en la secuencia de datos TNEF del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b0f7f-132">Encodes a view for a message's recipient table in the TNEF data stream for the message.</span></span>  <br/> |
|[<span data-ttu-id="b0f7f-133">FinishComponent</span><span class="sxs-lookup"><span data-stu-id="b0f7f-133">FinishComponent</span></span>](itnef-finishcomponent.md) <br/> |<span data-ttu-id="b0f7f-134">Procesa componentes individuales de un mensaje uno a uno en una secuencia de TNEF.</span><span class="sxs-lookup"><span data-stu-id="b0f7f-134">Processes individual components from a message one at a time into a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0f7f-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0f7f-135">See also</span></span>



[<span data-ttu-id="b0f7f-136">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="b0f7f-136">MAPI Interfaces</span></span>](mapi-interfaces.md)

