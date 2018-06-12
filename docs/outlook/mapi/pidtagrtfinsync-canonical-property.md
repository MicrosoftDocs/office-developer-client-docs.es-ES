---
title: Propiedad canónico PidTagRtfInSync
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 85e517601d291f144652befa267d8fd8f76dea64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820147"
---
# <a name="pidtagrtfinsync-canonical-property"></a><span data-ttu-id="73b62-103">Propiedad canónico PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="73b62-103">PidTagRtfInSync Canonical Property</span></span>

  
  
<span data-ttu-id="73b62-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73b62-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73b62-105">Contiene TRUE si la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) tiene el mismo contenido de texto que la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="73b62-105">Contains TRUE if the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property has the same text content as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="73b62-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="73b62-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="73b62-107">PR_RTF_IN_SYNC</span><span class="sxs-lookup"><span data-stu-id="73b62-107">PR_RTF_IN_SYNC</span></span>  <br/> |
|<span data-ttu-id="73b62-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="73b62-108">Identifier:</span></span>  <br/> |<span data-ttu-id="73b62-109">0x0E1F</span><span class="sxs-lookup"><span data-stu-id="73b62-109">0x0E1F</span></span>  <br/> |
|<span data-ttu-id="73b62-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="73b62-110">Data type:</span></span>  <br/> |<span data-ttu-id="73b62-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="73b62-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="73b62-112">Área:</span><span class="sxs-lookup"><span data-stu-id="73b62-112">Area:</span></span>  <br/> |<span data-ttu-id="73b62-113">Email</span><span class="sxs-lookup"><span data-stu-id="73b62-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73b62-114">Notas</span><span class="sxs-lookup"><span data-stu-id="73b62-114">Remarks</span></span>

<span data-ttu-id="73b62-115">Un valor de TRUE significa que la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la versión de texto sin formato de este mensaje y la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la versión de formato de texto enriquecido (RTF), son idénticas, excepto para espacio en blanco en **PR_BODY** y el formato **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="73b62-115">A value of TRUE means that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the plain text version of this message, and the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the Rich Text Format (RTF) version, are identical except for white space in **PR_BODY** and formatting in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="73b62-116">El texto en las dos versiones consta de los mismos caracteres en la misma secuencia.</span><span class="sxs-lookup"><span data-stu-id="73b62-116">The text in the two versions consists of the same characters in the same sequence.</span></span>
  
<span data-ttu-id="73b62-117">Un valor de FALSE significa que las dos versiones no están sincronizadas para el contenido de texto, pero son capaces de que se están sincronizando por la función [RTFSync](rtfsync.md) .</span><span class="sxs-lookup"><span data-stu-id="73b62-117">A value of FALSE means that the two versions are not synchronized for text content but are capable of being synchronized by the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="73b62-118">Se ha modificado una versión y la otra versión no tiene.</span><span class="sxs-lookup"><span data-stu-id="73b62-118">One version has been altered and the other version has not.</span></span> 
  
<span data-ttu-id="73b62-119">Ningún valor significa que las dos versiones, si ambos existen o nunca existían, no se puede sincronizar.</span><span class="sxs-lookup"><span data-stu-id="73b62-119">No value means that the two versions, if both exist or ever existed, cannot be synchronized.</span></span> <span data-ttu-id="73b62-120">Se ha eliminado o modificado completamente que ya no es posible la sincronización de una versión.</span><span class="sxs-lookup"><span data-stu-id="73b62-120">One version has been deleted or altered so radically that synchronization is no longer possible.</span></span>
  
<span data-ttu-id="73b62-121">Una aplicación cliente que ha modificado **PR_RTF_COMPRESSED** debe establecer el valor FALSE en esta propiedad para forzar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="73b62-121">A client application that has modified **PR_RTF_COMPRESSED** should set a value of FALSE in this property to force synchronization.</span></span> <span data-ttu-id="73b62-122">Los almacenes de mensajes RTF reconozca deben realizar la sincronización con **RTFSync** durante una llamada de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="73b62-122">RTF-aware message stores should perform the synchronization using **RTFSync** during an [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call.</span></span> <span data-ttu-id="73b62-123">Los clientes de tener en cuenta RTF deben comprobar la configuración de **PR_RTF_IN_SYNC** antes de leer **PR_RTF_COMPRESSED**y llamar primero a **RTFSync** si es necesario.</span><span class="sxs-lookup"><span data-stu-id="73b62-123">RTF-aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary.</span></span> 
  
<span data-ttu-id="73b62-124">Si **PR_BODY** ha tenido modificaciones en un valor distinto de su espacio en blanco, el almacén de mensajes debe eliminar **PR_RTF_IN_SYNC** para finalizar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="73b62-124">If **PR_BODY** has had modifications to anything other than its white space, the message store must delete **PR_RTF_IN_SYNC** to terminate synchronization.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="73b62-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="73b62-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="73b62-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="73b62-126">Protocol specifications</span></span>

<span data-ttu-id="73b62-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73b62-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73b62-128">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="73b62-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="73b62-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73b62-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73b62-130">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="73b62-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="73b62-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="73b62-131">Header files</span></span>

<span data-ttu-id="73b62-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="73b62-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="73b62-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="73b62-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="73b62-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="73b62-134">Mapitags.h</span></span>
  
> <span data-ttu-id="73b62-135">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="73b62-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="73b62-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="73b62-136">See also</span></span>



[<span data-ttu-id="73b62-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="73b62-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="73b62-138">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="73b62-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="73b62-139">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="73b62-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="73b62-140">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="73b62-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

