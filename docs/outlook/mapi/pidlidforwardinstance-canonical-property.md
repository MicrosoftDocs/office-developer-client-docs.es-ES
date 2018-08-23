---
title: Propiedad canónica PidLidForwardInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidForwardInstance
api_type:
- COM
ms.assetid: 055bdcaf-5002-44a6-b2b6-87244b2bea93
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 47dd6f10d1dbd25ea275ea96a2eddb6e9c6dfacb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571776"
---
# <a name="pidlidforwardinstance-canonical-property"></a><span data-ttu-id="6859f-103">Propiedad canónica PidLidForwardInstance</span><span class="sxs-lookup"><span data-stu-id="6859f-103">PidLidForwardInstance Canonical Property</span></span>

  
  
<span data-ttu-id="6859f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6859f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6859f-105">Indica que la convocatoria de reunión representa una excepción a una serie periódica, y que se reenvió (incluso cuando reenviados mediante el organizador) en lugar de ser una invitación enviada por el organizador.</span><span class="sxs-lookup"><span data-stu-id="6859f-105">Indicates that the meeting request represents an exception to a recurring series, and it was forwarded (even when forwarded by the organizer) rather than being an invitation sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6859f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6859f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6859f-107">dispidFwrdInstance</span><span class="sxs-lookup"><span data-stu-id="6859f-107">dispidFwrdInstance</span></span>  <br/> |
|<span data-ttu-id="6859f-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="6859f-108">Property set:</span></span>  <br/> |<span data-ttu-id="6859f-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="6859f-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="6859f-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="6859f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6859f-111">0x0000820A</span><span class="sxs-lookup"><span data-stu-id="6859f-111">0x0000820A</span></span>  <br/> |
|<span data-ttu-id="6859f-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6859f-112">Data type:</span></span>  <br/> |<span data-ttu-id="6859f-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6859f-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6859f-114">Área:</span><span class="sxs-lookup"><span data-stu-id="6859f-114">Area:</span></span>  <br/> |<span data-ttu-id="6859f-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="6859f-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6859f-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6859f-116">Remarks</span></span>

<span data-ttu-id="6859f-117">El valor FALSE para esta propiedad indica que la convocatoria de reunión no es una instancia de reenvío.</span><span class="sxs-lookup"><span data-stu-id="6859f-117">A value of FALSE for this property indicates that the meeting request is not a forwarded instance.</span></span> <span data-ttu-id="6859f-118">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="6859f-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6859f-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6859f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6859f-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6859f-120">Protocol specifications</span></span>

<span data-ttu-id="6859f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6859f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6859f-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6859f-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6859f-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6859f-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6859f-124">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="6859f-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6859f-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6859f-125">Header files</span></span>

<span data-ttu-id="6859f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6859f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6859f-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6859f-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6859f-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="6859f-128">See also</span></span>



[<span data-ttu-id="6859f-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6859f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6859f-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="6859f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6859f-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6859f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6859f-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="6859f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

