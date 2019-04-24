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
ms.openlocfilehash: 2dec706252eb6aa1b28f68f6f46473df04f3fbe7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355639"
---
# <a name="pidtagrecipienttrackstatustime-canonical-property"></a><span data-ttu-id="b02c7-103">Propiedad canónica PidTagRecipientTrackStatusTime</span><span class="sxs-lookup"><span data-stu-id="b02c7-103">PidTagRecipientTrackStatusTime Canonical Property</span></span>

  
  
<span data-ttu-id="b02c7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b02c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b02c7-105">Contiene la fecha y la hora en que respondió el asistente.</span><span class="sxs-lookup"><span data-stu-id="b02c7-105">Contains the date and time when the attendee responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b02c7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b02c7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b02c7-107">PR_RECIPIENT_TRACKSTATUS_TIME</span><span class="sxs-lookup"><span data-stu-id="b02c7-107">PR_RECIPIENT_TRACKSTATUS_TIME</span></span>  <br/> |
|<span data-ttu-id="b02c7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b02c7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b02c7-109">0x5FFB</span><span class="sxs-lookup"><span data-stu-id="b02c7-109">0x5FFB</span></span>  <br/> |
|<span data-ttu-id="b02c7-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b02c7-110">Data type:</span></span>  <br/> |<span data-ttu-id="b02c7-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b02c7-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b02c7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b02c7-112">Area:</span></span>  <br/> |<span data-ttu-id="b02c7-113">Destinatario de transporte</span><span class="sxs-lookup"><span data-stu-id="b02c7-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b02c7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b02c7-114">Remarks</span></span>

<span data-ttu-id="b02c7-115">El valor debe especificarse en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="b02c7-115">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b02c7-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b02c7-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b02c7-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b02c7-117">Protocol specifications</span></span>

<span data-ttu-id="b02c7-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b02c7-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b02c7-119">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b02c7-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b02c7-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b02c7-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b02c7-121">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="b02c7-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b02c7-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b02c7-122">Header files</span></span>

<span data-ttu-id="b02c7-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b02c7-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b02c7-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b02c7-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b02c7-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b02c7-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b02c7-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="b02c7-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b02c7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b02c7-127">See also</span></span>



[<span data-ttu-id="b02c7-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b02c7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b02c7-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="b02c7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b02c7-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b02c7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b02c7-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="b02c7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

