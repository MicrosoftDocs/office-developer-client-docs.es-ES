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
ms.openlocfilehash: fc2774efed1a15fe79e167149f2cb162bae7642c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358537"
---
# <a name="pidtaginconflict-canonical-property"></a><span data-ttu-id="91a11-103">Propiedad canónica PidTagInConflict</span><span class="sxs-lookup"><span data-stu-id="91a11-103">PidTagInConflict Canonical Property</span></span>

  
  
<span data-ttu-id="91a11-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91a11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91a11-105">Contiene TRUE cuando los datos adjuntos representan una réplica alternativa.</span><span class="sxs-lookup"><span data-stu-id="91a11-105">Contains TRUE when the attachment represents an alternate replica.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91a11-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="91a11-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91a11-107">PR_IN_CONFLICT</span><span class="sxs-lookup"><span data-stu-id="91a11-107">PR_IN_CONFLICT</span></span>  <br/> |
|<span data-ttu-id="91a11-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="91a11-108">Identifier:</span></span>  <br/> |<span data-ttu-id="91a11-109">0x666C</span><span class="sxs-lookup"><span data-stu-id="91a11-109">0x666C</span></span>  <br/> |
|<span data-ttu-id="91a11-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="91a11-110">Data type:</span></span>  <br/> |<span data-ttu-id="91a11-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="91a11-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="91a11-112">Área:</span><span class="sxs-lookup"><span data-stu-id="91a11-112">Area:</span></span>  <br/> |<span data-ttu-id="91a11-113">Nota de conflicto</span><span class="sxs-lookup"><span data-stu-id="91a11-113">Conflict note</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91a11-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="91a11-114">Remarks</span></span>

<span data-ttu-id="91a11-115">El cliente de correo electrónico y el servidor deben generar un mensaje de resolución de conflictos al detectar un conflicto con la versión actual de un mensaje en la réplica durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="91a11-115">The email client and server must generate a conflict resolve message when detecting a conflict against the current version of a message in the replica during synchronization.</span></span> <span data-ttu-id="91a11-116">Es importante comprender que es posible que la versión actual del mensaje en la réplica local se transmitió durante la operación de sincronización actual.</span><span class="sxs-lookup"><span data-stu-id="91a11-116">It is important to understand that it is possible that the current version of the message in the local replica was transmitted during the current synchronization operation.</span></span> <span data-ttu-id="91a11-117">Esto ocurrirá cuando el conflicto ya exista en el servidor antes de que alguno de los mensajes en conflicto se descargara en la réplica local.</span><span class="sxs-lookup"><span data-stu-id="91a11-117">This will happen when the conflict already exists on the server before any of the conflicting messages were downloaded to the local replica.</span></span> <span data-ttu-id="91a11-118">Un mensaje de resolución de conflictos debe sincronizarse como réplicas independientes con LAS PCL en conflicto.</span><span class="sxs-lookup"><span data-stu-id="91a11-118">A conflict resolve message must be synchronized as independent replicas with conflicting PCLs.</span></span> <span data-ttu-id="91a11-119">El mensaje de resolución de conflictos en sí no debe sincronizarse entre el cliente y el servidor; solo se deben intercambiar las réplicas independientes.</span><span class="sxs-lookup"><span data-stu-id="91a11-119">The conflict resolve message itself must not be synchronized between client and server; only the independent replicas should be exchanged.</span></span> <span data-ttu-id="91a11-120">A continuación, el asociado de sincronización debe generar un nuevo mensaje que coincida con la estructura del mensaje en conflicto.</span><span class="sxs-lookup"><span data-stu-id="91a11-120">The synchronization partner must then generate a new message that matches the structure of the conflict message.</span></span> <span data-ttu-id="91a11-121">Por lo tanto, es importante que el cliente y el servidor usen el mismo algoritmo para detectar el elemento "ganador".</span><span class="sxs-lookup"><span data-stu-id="91a11-121">Therefore, it is important that client and server use the same algorithm to detect the "winner" item.</span></span> <span data-ttu-id="91a11-122">Se deben aplicar las siguientes reglas para detectar el "ganador":</span><span class="sxs-lookup"><span data-stu-id="91a11-122">The following rules must be applied to detect the "winner":</span></span>
  
1. <span data-ttu-id="91a11-123">Última hora de modificación.</span><span class="sxs-lookup"><span data-stu-id="91a11-123">Last modification time.</span></span>
    
2. <span data-ttu-id="91a11-124">GUID CN superior (con comparación de memoria) para romper la vinculación.</span><span class="sxs-lookup"><span data-stu-id="91a11-124">Higher CN GUID (using memory compare) to break tie.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="91a11-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="91a11-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91a11-126">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="91a11-126">Protocol specifications</span></span>

<span data-ttu-id="91a11-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91a11-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91a11-128">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="91a11-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91a11-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91a11-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91a11-130">Controla la sincronización de datos de objetos de mensajería entre un servidor y un cliente.</span><span class="sxs-lookup"><span data-stu-id="91a11-130">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91a11-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="91a11-131">Header files</span></span>

<span data-ttu-id="91a11-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91a11-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="91a11-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="91a11-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="91a11-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="91a11-134">Mapitags.h</span></span>
  
> <span data-ttu-id="91a11-135">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="91a11-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91a11-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="91a11-136">See also</span></span>



[<span data-ttu-id="91a11-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="91a11-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91a11-138">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="91a11-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91a11-139">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="91a11-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91a11-140">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="91a11-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

