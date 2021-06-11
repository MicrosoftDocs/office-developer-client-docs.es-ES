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
ms.openlocfilehash: ed038faf44f350b041191373cf573e7e185337c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357879"
---
# <a name="pidtagrtfinsync-canonical-property"></a><span data-ttu-id="07bb6-103">Propiedad canónica PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="07bb6-103">PidTagRtfInSync Canonical Property</span></span>

  
  
<span data-ttu-id="07bb6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07bb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07bb6-105">Contiene TRUE si la **propiedad PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) tiene el mismo contenido de texto que la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="07bb6-105">Contains TRUE if the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property has the same text content as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="07bb6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="07bb6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="07bb6-107">PR_RTF_IN_SYNC</span><span class="sxs-lookup"><span data-stu-id="07bb6-107">PR_RTF_IN_SYNC</span></span>  <br/> |
|<span data-ttu-id="07bb6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="07bb6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="07bb6-109">0x0E1F</span><span class="sxs-lookup"><span data-stu-id="07bb6-109">0x0E1F</span></span>  <br/> |
|<span data-ttu-id="07bb6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="07bb6-110">Data type:</span></span>  <br/> |<span data-ttu-id="07bb6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="07bb6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="07bb6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="07bb6-112">Area:</span></span>  <br/> |<span data-ttu-id="07bb6-113">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="07bb6-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07bb6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07bb6-114">Remarks</span></span>

<span data-ttu-id="07bb6-115">Un valor true significa que la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) , la versión de texto sin formato de este mensaje y la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) , la versión de formato de texto enriquecido (RTF), son idénticas excepto para los espacios en blanco en **PR_BODY** y el formato **en PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="07bb6-115">A value of TRUE means that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the plain text version of this message, and the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the Rich Text Format (RTF) version, are identical except for white space in **PR_BODY** and formatting in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="07bb6-116">El texto de las dos versiones consta de los mismos caracteres de la misma secuencia.</span><span class="sxs-lookup"><span data-stu-id="07bb6-116">The text in the two versions consists of the same characters in the same sequence.</span></span>
  
<span data-ttu-id="07bb6-117">Un valor de FALSE significa que las dos versiones no están sincronizadas para el contenido de texto, pero pueden sincronizarse con la [función RTFSync.](rtfsync.md)</span><span class="sxs-lookup"><span data-stu-id="07bb6-117">A value of FALSE means that the two versions are not synchronized for text content but are capable of being synchronized by the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="07bb6-118">Una versión se ha modificado y la otra no.</span><span class="sxs-lookup"><span data-stu-id="07bb6-118">One version has been altered and the other version has not.</span></span> 
  
<span data-ttu-id="07bb6-119">Ningún valor significa que las dos versiones, si existen o existieron alguna vez, no se pueden sincronizar.</span><span class="sxs-lookup"><span data-stu-id="07bb6-119">No value means that the two versions, if both exist or ever existed, cannot be synchronized.</span></span> <span data-ttu-id="07bb6-120">Una versión se ha eliminado o modificado de forma tan radical que la sincronización ya no es posible.</span><span class="sxs-lookup"><span data-stu-id="07bb6-120">One version has been deleted or altered so radically that synchronization is no longer possible.</span></span>
  
<span data-ttu-id="07bb6-121">Una aplicación cliente que haya modificado **PR_RTF_COMPRESSED** debe establecer un valor de FALSE en esta propiedad para forzar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="07bb6-121">A client application that has modified **PR_RTF_COMPRESSED** should set a value of FALSE in this property to force synchronization.</span></span> <span data-ttu-id="07bb6-122">Los almacenes de mensajes compatible con RTF deben realizar la sincronización con **RTFSync** durante una [llamada IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="07bb6-122">RTF-aware message stores should perform the synchronization using **RTFSync** during an [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call.</span></span> <span data-ttu-id="07bb6-123">Los clientes con rtf deben comprobar la configuración de **PR_RTF_IN_SYNC** antes de **leer PR_RTF_COMPRESSED** y llamar primero **a RTFSync** si es necesario.</span><span class="sxs-lookup"><span data-stu-id="07bb6-123">RTF-aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary.</span></span> 
  
<span data-ttu-id="07bb6-124">Si **PR_BODY** ha tenido modificaciones en cualquier cosa que no sea su espacio en blanco, el almacén de mensajes debe eliminar **PR_RTF_IN_SYNC** para finalizar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="07bb6-124">If **PR_BODY** has had modifications to anything other than its white space, the message store must delete **PR_RTF_IN_SYNC** to terminate synchronization.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="07bb6-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="07bb6-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="07bb6-126">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="07bb6-126">Protocol specifications</span></span>

<span data-ttu-id="07bb6-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07bb6-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07bb6-128">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="07bb6-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="07bb6-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07bb6-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07bb6-130">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="07bb6-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="07bb6-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="07bb6-131">Header files</span></span>

<span data-ttu-id="07bb6-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07bb6-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="07bb6-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="07bb6-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="07bb6-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="07bb6-134">Mapitags.h</span></span>
  
> <span data-ttu-id="07bb6-135">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="07bb6-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07bb6-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="07bb6-136">See also</span></span>



[<span data-ttu-id="07bb6-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="07bb6-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="07bb6-138">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="07bb6-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="07bb6-139">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="07bb6-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="07bb6-140">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="07bb6-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

