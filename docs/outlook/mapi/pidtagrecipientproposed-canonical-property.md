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
ms.openlocfilehash: 3b05f33328e9e0b90251a99defa9816f86971337
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820037"
---
# <a name="pidtagrecipientproposed-canonical-property"></a><span data-ttu-id="67e09-103">Propiedad canónica PidTagRecipientProposed</span><span class="sxs-lookup"><span data-stu-id="67e09-103">PidTagRecipientProposed Canonical Property</span></span>

  
  
<span data-ttu-id="67e09-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="67e09-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="67e09-105">Indica si ha respondido o asistente a una reunión.</span><span class="sxs-lookup"><span data-stu-id="67e09-105">Indicates whether a meeting attendee has responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="67e09-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="67e09-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67e09-107">PR_RECIPIENT_PROPOSED</span><span class="sxs-lookup"><span data-stu-id="67e09-107">PR_RECIPIENT_PROPOSED</span></span>  <br/> |
|<span data-ttu-id="67e09-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="67e09-108">Identifier:</span></span>  <br/> |<span data-ttu-id="67e09-109">0x5FE1</span><span class="sxs-lookup"><span data-stu-id="67e09-109">0x5FE1</span></span>  <br/> |
|<span data-ttu-id="67e09-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="67e09-110">Data type:</span></span>  <br/> |<span data-ttu-id="67e09-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="67e09-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="67e09-112">Área:</span><span class="sxs-lookup"><span data-stu-id="67e09-112">Area:</span></span>  <br/> |<span data-ttu-id="67e09-113">Destinatario del transporte</span><span class="sxs-lookup"><span data-stu-id="67e09-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67e09-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="67e09-114">Remarks</span></span>

<span data-ttu-id="67e09-115">Un valor de TRUE para esta propiedad indica que el Asistente propuesto una nueva fecha u hora.</span><span class="sxs-lookup"><span data-stu-id="67e09-115">A value of TRUE for this property indicates that the attendee proposed a new date and/or time.</span></span> <span data-ttu-id="67e09-116">Un valor de FALSE, o la ausencia de esta propiedad, significa que el asistente no ha respondido todavía o la respuesta más reciente del asistente no incluye una nueva fecha / hora propuesta.</span><span class="sxs-lookup"><span data-stu-id="67e09-116">A value of FALSE, or the absence of this property, means either that the attendee has not yet responded, or the most recent response from the attendee did not include a new date/ time proposal.</span></span> <span data-ttu-id="67e09-117">Este valor no debe ser TRUE para los asistentes de una serie periódica.</span><span class="sxs-lookup"><span data-stu-id="67e09-117">This value must not be TRUE for attendees in a recurring series.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="67e09-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="67e09-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="67e09-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="67e09-119">Protocol specifications</span></span>

<span data-ttu-id="67e09-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67e09-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67e09-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="67e09-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="67e09-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67e09-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67e09-123">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="67e09-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="67e09-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="67e09-124">Header files</span></span>

<span data-ttu-id="67e09-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67e09-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="67e09-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="67e09-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="67e09-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="67e09-127">Mapitags.h</span></span>
  
> <span data-ttu-id="67e09-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="67e09-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="67e09-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="67e09-129">See also</span></span>



[<span data-ttu-id="67e09-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="67e09-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="67e09-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="67e09-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="67e09-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="67e09-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="67e09-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="67e09-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

