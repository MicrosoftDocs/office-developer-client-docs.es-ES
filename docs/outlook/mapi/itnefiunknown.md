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
ms.openlocfilehash: e8267b254648870cea4e16b4dea0e9c92e316fb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818012"
---
# <a name="itnef--iunknown"></a><span data-ttu-id="c778d-103">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c778d-103">ITnef : IUnknown</span></span>

  
  
<span data-ttu-id="c778d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c778d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c778d-105">Proporciona métodos para encapsular las propiedades de MAPI que no son compatibles con un sistema de mensajería en secuencias binario que se pueden adjuntar a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="c778d-105">Provides methods for encapsulating MAPI properties that are not supported by a messaging system into binary streams that can be attached to messages.</span></span> <span data-ttu-id="c778d-106">El formato utilizado para esta encapsulación es el formato de encapsulación neutro para el transporte (TNEF).</span><span class="sxs-lookup"><span data-stu-id="c778d-106">The format used for this encapsulation is the Transport-Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="c778d-107">El proveedor de transporte de destino o la aplicación de cliente basado en MAPI puede, a continuación, al recibir un mensaje que incluye datos adjuntos TNEF, recuperar las propiedades de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="c778d-107">The target transport provider or MAPI-based client application can then, on receiving a message that includes a TNEF attachment, recover the properties from the attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c778d-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c778d-108">Header file:</span></span>  <br/> |<span data-ttu-id="c778d-109">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="c778d-109">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="c778d-110">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="c778d-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="c778d-111">Objetos TNEF</span><span class="sxs-lookup"><span data-stu-id="c778d-111">TNEF objects</span></span>  <br/> |
|<span data-ttu-id="c778d-112">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="c778d-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="c778d-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="c778d-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="c778d-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c778d-114">Called by:</span></span>  <br/> |<span data-ttu-id="c778d-115">Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace</span><span class="sxs-lookup"><span data-stu-id="c778d-115">Transport providers, message store providers, and gateways</span></span>  <br/> |
|<span data-ttu-id="c778d-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="c778d-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c778d-117">IID_ITNEF</span><span class="sxs-lookup"><span data-stu-id="c778d-117">IID_ITNEF</span></span>  <br/> |
|<span data-ttu-id="c778d-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="c778d-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="c778d-119">LPTNEF</span><span class="sxs-lookup"><span data-stu-id="c778d-119">LPTNEF</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c778d-120">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="c778d-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c778d-121">AddProps</span><span class="sxs-lookup"><span data-stu-id="c778d-121">AddProps</span></span>](itnef-addprops.md) <br/> |<span data-ttu-id="c778d-122">Permite que el proveedor de servicios de llamada o la puerta de enlace Agregar propiedades a la encapsulación de un mensaje o datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="c778d-122">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span>  <br/> |
|[<span data-ttu-id="c778d-123">ExtractProps</span><span class="sxs-lookup"><span data-stu-id="c778d-123">ExtractProps</span></span>](itnef-extractprops.md) <br/> |<span data-ttu-id="c778d-124">Extrae las propiedades de una encapsulación TNEF.</span><span class="sxs-lookup"><span data-stu-id="c778d-124">Extracts the properties from a TNEF encapsulation.</span></span>  <br/> |
|[<span data-ttu-id="c778d-125">Finish</span><span class="sxs-lookup"><span data-stu-id="c778d-125">Finish</span></span>](itnef-finish.md) <br/> |<span data-ttu-id="c778d-126">Termina de procesamiento para todas las operaciones de TNEF que se ponen en cola y a la espera.</span><span class="sxs-lookup"><span data-stu-id="c778d-126">Finishes processing for all TNEF operations that are queued and waiting.</span></span>  <br/> |
|[<span data-ttu-id="c778d-127">OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="c778d-127">OpenTaggedBody</span></span>](itnef-opentaggedbody.md) <br/> |<span data-ttu-id="c778d-128">Se abre una interfaz de secuencia en el texto de un mensaje de encapsulado.</span><span class="sxs-lookup"><span data-stu-id="c778d-128">Opens a stream interface on the text of an encapsulated message.</span></span>  <br/> |
|[<span data-ttu-id="c778d-129">SetProps</span><span class="sxs-lookup"><span data-stu-id="c778d-129">SetProps</span></span>](itnef-setprops.md) <br/> |<span data-ttu-id="c778d-130">Establece el valor de una o más propiedades para un mensaje encapsulado o adjunto sin modificar el mensaje original o datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="c778d-130">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span>  <br/> |
|[<span data-ttu-id="c778d-131">EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="c778d-131">EncodeRecips</span></span>](itnef-encoderecips.md) <br/> |<span data-ttu-id="c778d-132">Codifica una vista de tabla de destinatarios de un mensaje en la secuencia de datos TNEF para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="c778d-132">Encodes a view for a message's recipient table in the TNEF data stream for the message.</span></span>  <br/> |
|[<span data-ttu-id="c778d-133">FinishComponent</span><span class="sxs-lookup"><span data-stu-id="c778d-133">FinishComponent</span></span>](itnef-finishcomponent.md) <br/> |<span data-ttu-id="c778d-134">Procesa los componentes individuales de un mensaje de uno a la vez en una secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="c778d-134">Processes individual components from a message one at a time into a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c778d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c778d-135">See also</span></span>



[<span data-ttu-id="c778d-136">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="c778d-136">MAPI Interfaces</span></span>](mapi-interfaces.md)
