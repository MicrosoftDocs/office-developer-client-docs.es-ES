---
title: Propiedad canónica PidTagOwnerAppointmentId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnerAppointmentId
api_type:
- COM
ms.assetid: b5eea554-6bca-42d1-b943-1327f0d70584
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a6fc194a3ef7d82be656a8d6c3f5fb9ad8326ceb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819891"
---
# <a name="pidtagownerappointmentid-canonical-property"></a><span data-ttu-id="daba8-103">Propiedad canónica PidTagOwnerAppointmentId</span><span class="sxs-lookup"><span data-stu-id="daba8-103">PidTagOwnerAppointmentId Canonical Property</span></span>

  
  
<span data-ttu-id="daba8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="daba8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="daba8-105">Contiene un identificador para una cita en programación del propietario.</span><span class="sxs-lookup"><span data-stu-id="daba8-105">Contains an identifier for an appointment in the owner's schedule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="daba8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="daba8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="daba8-107">PR_OWNER_APPT_ID</span><span class="sxs-lookup"><span data-stu-id="daba8-107">PR_OWNER_APPT_ID</span></span>  <br/> |
|<span data-ttu-id="daba8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="daba8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="daba8-109">0x0062</span><span class="sxs-lookup"><span data-stu-id="daba8-109">0x0062</span></span>  <br/> |
|<span data-ttu-id="daba8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="daba8-110">Data type:</span></span>  <br/> |<span data-ttu-id="daba8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="daba8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="daba8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="daba8-112">Area:</span></span>  <br/> |<span data-ttu-id="daba8-113">Cita</span><span class="sxs-lookup"><span data-stu-id="daba8-113">Appointment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="daba8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="daba8-114">Remarks</span></span>

<span data-ttu-id="daba8-115">Esta propiedad se usa en las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="daba8-115">This property is used in meeting requests.</span></span> <span data-ttu-id="daba8-116">No representa un identificador de entrada, pero un entero largo que identifica de forma exclusiva la cita dentro de programación de la dirección del remitente.</span><span class="sxs-lookup"><span data-stu-id="daba8-116">It does not represent an entry identifier, but a long integer that uniquely identifies the appointment within the sender's schedule.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="daba8-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="daba8-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="daba8-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="daba8-118">Protocol specifications</span></span>

<span data-ttu-id="daba8-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="daba8-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="daba8-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="daba8-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="daba8-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="daba8-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="daba8-122">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="daba8-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="daba8-123">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="daba8-123">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="daba8-124">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="daba8-124">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="daba8-125">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="daba8-125">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="daba8-126">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="daba8-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="daba8-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="daba8-127">Header files</span></span>

<span data-ttu-id="daba8-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="daba8-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="daba8-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="daba8-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="daba8-130">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="daba8-130">mapitags.h</span></span>
  
> <span data-ttu-id="daba8-131">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="daba8-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="daba8-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="daba8-132">See also</span></span>



[<span data-ttu-id="daba8-133">Propiedad canónica PidTagOriginalAuthorSearchKey</span><span class="sxs-lookup"><span data-stu-id="daba8-133">PidTagOriginalAuthorSearchKey Canonical Property</span></span>](pidtagoriginalauthorsearchkey-canonical-property.md)


[<span data-ttu-id="daba8-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="daba8-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="daba8-135">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="daba8-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="daba8-136">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="daba8-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="daba8-137">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="daba8-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

