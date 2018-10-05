---
title: Propiedad canónica PidTagRecipientProposedStartTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedStartTime
api_type:
- COM
ms.assetid: 6687ff62-7ac6-409c-8c87-4e09d38e45f1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8815728adce809641586c4da5beb4c9fad735507
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397117"
---
# <a name="pidtagrecipientproposedstarttime-canonical-property"></a><span data-ttu-id="121ec-103">Propiedad canónica PidTagRecipientProposedStartTime</span><span class="sxs-lookup"><span data-stu-id="121ec-103">PidTagRecipientProposedStartTime Canonical Property</span></span>

  
  
<span data-ttu-id="121ec-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="121ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="121ec-105">Indica una hora de inicio propuesta de una reunión.</span><span class="sxs-lookup"><span data-stu-id="121ec-105">Indicates a proposed starting time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="121ec-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="121ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="121ec-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span><span class="sxs-lookup"><span data-stu-id="121ec-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span></span>  <br/> |
|<span data-ttu-id="121ec-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="121ec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="121ec-109">0x5FE3</span><span class="sxs-lookup"><span data-stu-id="121ec-109">0x5FE3</span></span>  <br/> |
|<span data-ttu-id="121ec-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="121ec-110">Data type:</span></span>  <br/> |<span data-ttu-id="121ec-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="121ec-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="121ec-112">Área:</span><span class="sxs-lookup"><span data-stu-id="121ec-112">Area:</span></span>  <br/> |<span data-ttu-id="121ec-113">Destinatario del transporte</span><span class="sxs-lookup"><span data-stu-id="121ec-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="121ec-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="121ec-114">Remarks</span></span>

<span data-ttu-id="121ec-115">Cuando el valor de la propiedad **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) se establece en TRUE, el valor de esta propiedad indica el valor solicitado por el Asistente para establecer como el valor de la **dispidApptStartWhole** ([ PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) (propiedad) para el objeto de reunión de una sola instancia o un objeto exception.</span><span class="sxs-lookup"><span data-stu-id="121ec-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="121ec-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="121ec-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="121ec-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="121ec-117">Protocol specifications</span></span>

<span data-ttu-id="121ec-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="121ec-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="121ec-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="121ec-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="121ec-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="121ec-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="121ec-121">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="121ec-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="121ec-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="121ec-122">Header files</span></span>

<span data-ttu-id="121ec-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="121ec-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="121ec-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="121ec-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="121ec-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="121ec-125">Mapitags.h</span></span>
  
> <span data-ttu-id="121ec-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="121ec-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="121ec-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="121ec-127">See also</span></span>



[<span data-ttu-id="121ec-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="121ec-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="121ec-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="121ec-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="121ec-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="121ec-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="121ec-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="121ec-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

