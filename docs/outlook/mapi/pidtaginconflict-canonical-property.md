---
title: Propiedad canónica PidTagInConflict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInConflict
api_type:
- HeaderDef
ms.assetid: e83c05c6-a7c0-486c-a112-58a39255767a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 33bf77029207e2d8d734d5c49735262135896660
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593728"
---
# <a name="pidtaginconflict-canonical-property"></a><span data-ttu-id="30c86-103">Propiedad canónica PidTagInConflict</span><span class="sxs-lookup"><span data-stu-id="30c86-103">PidTagInConflict Canonical Property</span></span>

  
  
<span data-ttu-id="30c86-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30c86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30c86-105">Contiene TRUE cuando los datos adjuntos representa una réplica alternativa.</span><span class="sxs-lookup"><span data-stu-id="30c86-105">Contains TRUE when the attachment represents an alternate replica.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30c86-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="30c86-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="30c86-107">PR_IN_CONFLICT</span><span class="sxs-lookup"><span data-stu-id="30c86-107">PR_IN_CONFLICT</span></span>  <br/> |
|<span data-ttu-id="30c86-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="30c86-108">Identifier:</span></span>  <br/> |<span data-ttu-id="30c86-109">0x666C</span><span class="sxs-lookup"><span data-stu-id="30c86-109">0x666C</span></span>  <br/> |
|<span data-ttu-id="30c86-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="30c86-110">Data type:</span></span>  <br/> |<span data-ttu-id="30c86-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="30c86-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="30c86-112">Área:</span><span class="sxs-lookup"><span data-stu-id="30c86-112">Area:</span></span>  <br/> |<span data-ttu-id="30c86-113">Nota de conflicto</span><span class="sxs-lookup"><span data-stu-id="30c86-113">Conflict note</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30c86-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="30c86-114">Remarks</span></span>

<span data-ttu-id="30c86-115">El cliente de correo electrónico y el servidor deben generar un mensaje de resolución de conflictos cuando se detecte un conflicto con la versión actual de un mensaje en la réplica durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="30c86-115">The email client and server must generate a conflict resolve message when detecting a conflict against the current version of a message in the replica during synchronization.</span></span> <span data-ttu-id="30c86-116">Es importante comprender que es posible que la versión actual del mensaje en la réplica local se transmite durante la operación de sincronización actual.</span><span class="sxs-lookup"><span data-stu-id="30c86-116">It is important to understand that it is possible that the current version of the message in the local replica was transmitted during the current synchronization operation.</span></span> <span data-ttu-id="30c86-117">Esto ocurrirá cuando el conflicto ya existe en el servidor antes de cualquiera de los mensajes en conflicto se han descargado a la réplica local.</span><span class="sxs-lookup"><span data-stu-id="30c86-117">This will happen when the conflict already exists on the server before any of the conflicting messages were downloaded to the local replica.</span></span> <span data-ttu-id="30c86-118">Un conflicto de resolver el mensaje debe sincronizarse como réplicas independientes con PCLs en conflicto.</span><span class="sxs-lookup"><span data-stu-id="30c86-118">A conflict resolve message must be synchronized as independent replicas with conflicting PCLs.</span></span> <span data-ttu-id="30c86-119">El conflicto resolver propio mensaje no debe sincronizarse entre cliente y servidor; sólo las réplicas independientes que se va a intercambiar.</span><span class="sxs-lookup"><span data-stu-id="30c86-119">The conflict resolve message itself must not be synchronized between client and server; only the independent replicas should be exchanged.</span></span> <span data-ttu-id="30c86-120">El asociado de sincronización, a continuación, debe generar un nuevo mensaje que coincide con la estructura del mensaje de conflicto.</span><span class="sxs-lookup"><span data-stu-id="30c86-120">The synchronization partner must then generate a new message that matches the structure of the conflict message.</span></span> <span data-ttu-id="30c86-121">Por lo tanto, es importante que cliente y el servidor utilizan el mismo algoritmo para detectar el elemento "ganador".</span><span class="sxs-lookup"><span data-stu-id="30c86-121">Therefore, it is important that client and server use the same algorithm to detect the "winner" item.</span></span> <span data-ttu-id="30c86-122">Para detectar el "ganador", se deben aplicar las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="30c86-122">The following rules must be applied to detect the "winner":</span></span>
  
1. <span data-ttu-id="30c86-123">Hora de última modificación.</span><span class="sxs-lookup"><span data-stu-id="30c86-123">Last modification time.</span></span>
    
2. <span data-ttu-id="30c86-124">Superior GUID CN (mediante la comparación de memoria) para la placa de interrupción.</span><span class="sxs-lookup"><span data-stu-id="30c86-124">Higher CN GUID (using memory compare) to break tie.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="30c86-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="30c86-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="30c86-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="30c86-126">Protocol specifications</span></span>

<span data-ttu-id="30c86-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30c86-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30c86-128">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="30c86-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="30c86-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30c86-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30c86-130">Controla la sincronización de datos de objeto mensajería entre un servidor y un cliente.</span><span class="sxs-lookup"><span data-stu-id="30c86-130">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="30c86-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="30c86-131">Header files</span></span>

<span data-ttu-id="30c86-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30c86-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="30c86-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="30c86-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="30c86-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="30c86-134">Mapitags.h</span></span>
  
> <span data-ttu-id="30c86-135">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="30c86-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30c86-136">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="30c86-136">See also</span></span>



[<span data-ttu-id="30c86-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="30c86-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="30c86-138">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="30c86-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="30c86-139">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="30c86-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="30c86-140">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="30c86-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

