---
title: Propiedad canónica PidTagSpoolerStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 426d26cae147faf3f843ac547de9d205d766ac44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348212"
---
# <a name="pidtagspoolerstatus-canonical-property"></a><span data-ttu-id="b4e43-103">Propiedad canónica PidTagSpoolerStatus</span><span class="sxs-lookup"><span data-stu-id="b4e43-103">PidTagSpoolerStatus Canonical Property</span></span>

  
  
<span data-ttu-id="b4e43-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4e43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4e43-105">Contiene el estado del mensaje en función de la información que está disponible para la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="b4e43-105">Contains the status of the message based on information that is available to the MAPI spooler.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4e43-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b4e43-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4e43-107">PR_SPOOLER_STATUS</span><span class="sxs-lookup"><span data-stu-id="b4e43-107">PR_SPOOLER_STATUS</span></span>  <br/> |
|<span data-ttu-id="b4e43-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b4e43-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4e43-109">0x0E10</span><span class="sxs-lookup"><span data-stu-id="b4e43-109">0x0E10</span></span>  <br/> |
|<span data-ttu-id="b4e43-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b4e43-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4e43-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b4e43-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b4e43-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b4e43-112">Area:</span></span>  <br/> |<span data-ttu-id="b4e43-113">MAPI no transmitible</span><span class="sxs-lookup"><span data-stu-id="b4e43-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4e43-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b4e43-114">Remarks</span></span>

<span data-ttu-id="b4e43-115">MAPI calcula esta propiedad en los objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b4e43-115">This property is computed by MAPI on message objects.</span></span>
  
<span data-ttu-id="b4e43-116">Esta propiedad aparece sólo en los mensajes entrantes y está reservada en los demás casos.</span><span class="sxs-lookup"><span data-stu-id="b4e43-116">This property appears on inbound messages only and is reserved in all other cases.</span></span> <span data-ttu-id="b4e43-117">Indica si un mensaje se ha entregado o no a su ubicación final o si un proveedor de mensajes de mensajería puede eliminar el mensaje mientras se reenruta.</span><span class="sxs-lookup"><span data-stu-id="b4e43-117">It indicates whether or not a message has been delivered to its final location or whether a messaging hook provider potentially deleted the message while rerouting it.</span></span>
  
<span data-ttu-id="b4e43-118">Las aplicaciones cliente nunca deben establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b4e43-118">Client applications should never set this property.</span></span> <span data-ttu-id="b4e43-119">Para un mensaje entrante, un proveedor de servicios o cliente puede llamar a [IMAPIProp:: GetProps](imapiprop-getprops.md) en esta propiedad para determinar el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b4e43-119">For an inbound message, a client or service provider can call [IMAPIProp::GetProps](imapiprop-getprops.md) on this property to determine the message status.</span></span> <span data-ttu-id="b4e43-120">El valor S_OK indica que el mensaje se entregó correctamente al almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b4e43-120">The value S_OK indicates that the message was successfully delivered to the message store.</span></span> <span data-ttu-id="b4e43-121">El valor MAPI_E_OBJECT_DELETED indica que el mensaje se eliminó y que nunca se confirmó en el almacén.</span><span class="sxs-lookup"><span data-stu-id="b4e43-121">The value MAPI_E_OBJECT_DELETED indicates that the message was deleted and was never committed to the store.</span></span> 
  
<span data-ttu-id="b4e43-122">Los proveedores de almacenamiento de mensajes deben admitir esta propiedad en los mensajes, las tablas de destinatarios y la tabla de colas de salida.</span><span class="sxs-lookup"><span data-stu-id="b4e43-122">Message store providers should support this property on messages, recipient tables, and the outgoing queue table.</span></span> <span data-ttu-id="b4e43-123">Los clientes y proveedores deben poder establecer columnas en la tabla de colas de salida y restringir en función de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b4e43-123">Clients and providers should be able to set columns on the outgoing queue table and restrict based on this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b4e43-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4e43-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b4e43-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b4e43-125">Header files</span></span>

<span data-ttu-id="b4e43-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b4e43-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4e43-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b4e43-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="b4e43-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b4e43-128">Mapitags.h</span></span>
  
> <span data-ttu-id="b4e43-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="b4e43-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4e43-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4e43-130">See also</span></span>



[<span data-ttu-id="b4e43-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b4e43-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4e43-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="b4e43-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4e43-133">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b4e43-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4e43-134">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="b4e43-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

