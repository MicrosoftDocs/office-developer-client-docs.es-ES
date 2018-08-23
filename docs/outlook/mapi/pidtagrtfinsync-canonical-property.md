---
title: Propiedad canónica PidTagRtfInSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfInSync
api_type:
- COM
ms.assetid: 443cc68e-7898-4285-a606-f916fcd18554
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b182d2b568a3c7cf874dfe2fcf7a7503aa44193f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574492"
---
# <a name="pidtagrtfinsync-canonical-property"></a><span data-ttu-id="e28c8-103">Propiedad canónica PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="e28c8-103">PidTagRtfInSync Canonical Property</span></span>

  
  
<span data-ttu-id="e28c8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e28c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e28c8-105">Contiene TRUE si la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) tiene el mismo contenido de texto que la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="e28c8-105">Contains TRUE if the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property has the same text content as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e28c8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e28c8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e28c8-107">PR_RTF_IN_SYNC</span><span class="sxs-lookup"><span data-stu-id="e28c8-107">PR_RTF_IN_SYNC</span></span>  <br/> |
|<span data-ttu-id="e28c8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e28c8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e28c8-109">0x0E1F</span><span class="sxs-lookup"><span data-stu-id="e28c8-109">0x0E1F</span></span>  <br/> |
|<span data-ttu-id="e28c8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e28c8-110">Data type:</span></span>  <br/> |<span data-ttu-id="e28c8-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e28c8-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e28c8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e28c8-112">Area:</span></span>  <br/> |<span data-ttu-id="e28c8-113">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="e28c8-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e28c8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e28c8-114">Remarks</span></span>

<span data-ttu-id="e28c8-115">Un valor de TRUE significa que la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la versión de texto sin formato de este mensaje y la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la versión de formato de texto enriquecido (RTF), son idénticas, excepto para espacio en blanco en **PR_BODY** y el formato **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="e28c8-115">A value of TRUE means that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the plain text version of this message, and the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the Rich Text Format (RTF) version, are identical except for white space in **PR_BODY** and formatting in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="e28c8-116">El texto en las dos versiones consta de los mismos caracteres en la misma secuencia.</span><span class="sxs-lookup"><span data-stu-id="e28c8-116">The text in the two versions consists of the same characters in the same sequence.</span></span>
  
<span data-ttu-id="e28c8-117">Un valor de FALSE significa que las dos versiones no están sincronizadas para el contenido de texto, pero son capaces de que se están sincronizando por la función [RTFSync](rtfsync.md) .</span><span class="sxs-lookup"><span data-stu-id="e28c8-117">A value of FALSE means that the two versions are not synchronized for text content but are capable of being synchronized by the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="e28c8-118">Se ha modificado una versión y la otra versión no tiene.</span><span class="sxs-lookup"><span data-stu-id="e28c8-118">One version has been altered and the other version has not.</span></span> 
  
<span data-ttu-id="e28c8-119">Ningún valor significa que las dos versiones, si ambos existen o nunca existían, no se puede sincronizar.</span><span class="sxs-lookup"><span data-stu-id="e28c8-119">No value means that the two versions, if both exist or ever existed, cannot be synchronized.</span></span> <span data-ttu-id="e28c8-120">Se ha eliminado o modificado completamente que ya no es posible la sincronización de una versión.</span><span class="sxs-lookup"><span data-stu-id="e28c8-120">One version has been deleted or altered so radically that synchronization is no longer possible.</span></span>
  
<span data-ttu-id="e28c8-121">Una aplicación cliente que ha modificado **PR_RTF_COMPRESSED** debe establecer el valor FALSE en esta propiedad para forzar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="e28c8-121">A client application that has modified **PR_RTF_COMPRESSED** should set a value of FALSE in this property to force synchronization.</span></span> <span data-ttu-id="e28c8-122">Los almacenes de mensajes RTF reconozca deben realizar la sincronización con **RTFSync** durante una llamada de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="e28c8-122">RTF-aware message stores should perform the synchronization using **RTFSync** during an [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call.</span></span> <span data-ttu-id="e28c8-123">Los clientes de tener en cuenta RTF deben comprobar la configuración de **PR_RTF_IN_SYNC** antes de leer **PR_RTF_COMPRESSED**y llamar primero a **RTFSync** si es necesario.</span><span class="sxs-lookup"><span data-stu-id="e28c8-123">RTF-aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary.</span></span> 
  
<span data-ttu-id="e28c8-124">Si **PR_BODY** ha tenido modificaciones en un valor distinto de su espacio en blanco, el almacén de mensajes debe eliminar **PR_RTF_IN_SYNC** para finalizar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="e28c8-124">If **PR_BODY** has had modifications to anything other than its white space, the message store must delete **PR_RTF_IN_SYNC** to terminate synchronization.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e28c8-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e28c8-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e28c8-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e28c8-126">Protocol specifications</span></span>

<span data-ttu-id="e28c8-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e28c8-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e28c8-128">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e28c8-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e28c8-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e28c8-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e28c8-130">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e28c8-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e28c8-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e28c8-131">Header files</span></span>

<span data-ttu-id="e28c8-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e28c8-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="e28c8-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e28c8-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="e28c8-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e28c8-134">Mapitags.h</span></span>
  
> <span data-ttu-id="e28c8-135">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="e28c8-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e28c8-136">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e28c8-136">See also</span></span>



[<span data-ttu-id="e28c8-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e28c8-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e28c8-138">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e28c8-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e28c8-139">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e28c8-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e28c8-140">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e28c8-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

