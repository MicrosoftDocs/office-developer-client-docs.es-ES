---
title: Propiedad canónica PidTagRecipientProposed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposed
api_type:
- COM
ms.assetid: 8cb0e46c-0937-482f-be78-1f2e5261b210
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1b09d8d7621121b3652ceb9824f6d36b53844206
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283138"
---
# <a name="pidtagrecipientproposed-canonical-property"></a><span data-ttu-id="770fa-103">Propiedad canónica PidTagRecipientProposed</span><span class="sxs-lookup"><span data-stu-id="770fa-103">PidTagRecipientProposed Canonical Property</span></span>

  
  
<span data-ttu-id="770fa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="770fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="770fa-105">Indica si un asistente para la reunión ha respondido.</span><span class="sxs-lookup"><span data-stu-id="770fa-105">Indicates whether a meeting attendee has responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="770fa-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="770fa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="770fa-107">PR_RECIPIENT_PROPOSED</span><span class="sxs-lookup"><span data-stu-id="770fa-107">PR_RECIPIENT_PROPOSED</span></span>  <br/> |
|<span data-ttu-id="770fa-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="770fa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="770fa-109">0x5FE1</span><span class="sxs-lookup"><span data-stu-id="770fa-109">0x5FE1</span></span>  <br/> |
|<span data-ttu-id="770fa-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="770fa-110">Data type:</span></span>  <br/> |<span data-ttu-id="770fa-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="770fa-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="770fa-112">Área:</span><span class="sxs-lookup"><span data-stu-id="770fa-112">Area:</span></span>  <br/> |<span data-ttu-id="770fa-113">Destinatario de transporte</span><span class="sxs-lookup"><span data-stu-id="770fa-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="770fa-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="770fa-114">Remarks</span></span>

<span data-ttu-id="770fa-115">Un valor de TRUE para esta propiedad indica que el asistente propuso una nueva fecha u hora.</span><span class="sxs-lookup"><span data-stu-id="770fa-115">A value of TRUE for this property indicates that the attendee proposed a new date and/or time.</span></span> <span data-ttu-id="770fa-116">Un valor de FALSE o la ausencia de esta propiedad significa que el asistente todavía no ha respondido o que la respuesta más reciente del asistente no incluyó una nueva propuesta de fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="770fa-116">A value of FALSE, or the absence of this property, means either that the attendee has not yet responded, or the most recent response from the attendee did not include a new date/ time proposal.</span></span> <span data-ttu-id="770fa-117">Este valor no debe ser TRUE para los asistentes en una serie periódica.</span><span class="sxs-lookup"><span data-stu-id="770fa-117">This value must not be TRUE for attendees in a recurring series.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="770fa-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="770fa-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="770fa-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="770fa-119">Protocol specifications</span></span>

<span data-ttu-id="770fa-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="770fa-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="770fa-121">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="770fa-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="770fa-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="770fa-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="770fa-123">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="770fa-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="770fa-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="770fa-124">Header files</span></span>

<span data-ttu-id="770fa-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="770fa-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="770fa-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="770fa-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="770fa-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="770fa-127">Mapitags.h</span></span>
  
> <span data-ttu-id="770fa-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="770fa-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="770fa-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="770fa-129">See also</span></span>



[<span data-ttu-id="770fa-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="770fa-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="770fa-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="770fa-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="770fa-132">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="770fa-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="770fa-133">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="770fa-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

