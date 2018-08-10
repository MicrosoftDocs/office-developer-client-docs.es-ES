---
title: Propiedad canónica PidTagRecipientTrackStatusTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatusTime
api_type:
- COM
ms.assetid: f14dfe47-a9f8-4475-bb26-7da3411d8c6f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0db4efcf1e05536ee7abb3459caa0159f84ef798
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820047"
---
# <a name="pidtagrecipienttrackstatustime-canonical-property"></a><span data-ttu-id="fe9b2-103">Propiedad canónica PidTagRecipientTrackStatusTime</span><span class="sxs-lookup"><span data-stu-id="fe9b2-103">PidTagRecipientTrackStatusTime Canonical Property</span></span>

  
  
<span data-ttu-id="fe9b2-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe9b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe9b2-105">Contiene la fecha y la hora cuando el asistente ha respondido.</span><span class="sxs-lookup"><span data-stu-id="fe9b2-105">Contains the date and time when the attendee responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe9b2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fe9b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe9b2-107">PR_RECIPIENT_TRACKSTATUS_TIME</span><span class="sxs-lookup"><span data-stu-id="fe9b2-107">PR_RECIPIENT_TRACKSTATUS_TIME</span></span>  <br/> |
|<span data-ttu-id="fe9b2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fe9b2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fe9b2-109">0x5FFB</span><span class="sxs-lookup"><span data-stu-id="fe9b2-109">0x5FFB</span></span>  <br/> |
|<span data-ttu-id="fe9b2-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fe9b2-110">Data type:</span></span>  <br/> |<span data-ttu-id="fe9b2-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="fe9b2-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="fe9b2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fe9b2-112">Area:</span></span>  <br/> |<span data-ttu-id="fe9b2-113">Destinatario del transporte</span><span class="sxs-lookup"><span data-stu-id="fe9b2-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe9b2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fe9b2-114">Remarks</span></span>

<span data-ttu-id="fe9b2-115">El valor debe especificarse en hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="fe9b2-115">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fe9b2-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe9b2-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fe9b2-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="fe9b2-117">Protocol specifications</span></span>

<span data-ttu-id="fe9b2-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe9b2-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe9b2-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fe9b2-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fe9b2-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe9b2-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe9b2-121">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe9b2-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fe9b2-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fe9b2-122">Header files</span></span>

<span data-ttu-id="fe9b2-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe9b2-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe9b2-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fe9b2-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="fe9b2-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fe9b2-125">Mapitags.h</span></span>
  
> <span data-ttu-id="fe9b2-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="fe9b2-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe9b2-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe9b2-127">See also</span></span>



[<span data-ttu-id="fe9b2-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fe9b2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe9b2-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="fe9b2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe9b2-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fe9b2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe9b2-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="fe9b2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
