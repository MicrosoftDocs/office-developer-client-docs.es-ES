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
ms.openlocfilehash: 585e1a5400965288aa4a4c321888a570270021c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357774"
---
# <a name="pidlidforwardinstance-canonical-property"></a><span data-ttu-id="81780-103">Propiedad canónica PidLidForwardInstance</span><span class="sxs-lookup"><span data-stu-id="81780-103">PidLidForwardInstance Canonical Property</span></span>

  
  
<span data-ttu-id="81780-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81780-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81780-105">Indica que la convocatoria de reunión representa una excepción a una serie periódica y se reenvía (incluso cuando el organizador la reenvía) en lugar de ser una invitación enviada por el organizador.</span><span class="sxs-lookup"><span data-stu-id="81780-105">Indicates that the meeting request represents an exception to a recurring series, and it was forwarded (even when forwarded by the organizer) rather than being an invitation sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81780-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="81780-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81780-107">dispidFwrdInstance</span><span class="sxs-lookup"><span data-stu-id="81780-107">dispidFwrdInstance</span></span>  <br/> |
|<span data-ttu-id="81780-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="81780-108">Property set:</span></span>  <br/> |<span data-ttu-id="81780-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="81780-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="81780-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="81780-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="81780-111">0x0000820A</span><span class="sxs-lookup"><span data-stu-id="81780-111">0x0000820A</span></span>  <br/> |
|<span data-ttu-id="81780-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="81780-112">Data type:</span></span>  <br/> |<span data-ttu-id="81780-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="81780-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="81780-114">Área:</span><span class="sxs-lookup"><span data-stu-id="81780-114">Area:</span></span>  <br/> |<span data-ttu-id="81780-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="81780-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81780-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81780-116">Remarks</span></span>

<span data-ttu-id="81780-117">Un valor FALSE para esta propiedad indica que la solicitud de reunión no es una instancia reenviada.</span><span class="sxs-lookup"><span data-stu-id="81780-117">A value of FALSE for this property indicates that the meeting request is not a forwarded instance.</span></span> <span data-ttu-id="81780-118">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="81780-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="81780-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="81780-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="81780-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="81780-120">Protocol specifications</span></span>

<span data-ttu-id="81780-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81780-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81780-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="81780-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="81780-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81780-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81780-124">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="81780-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="81780-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="81780-125">Header files</span></span>

<span data-ttu-id="81780-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81780-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="81780-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="81780-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81780-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="81780-128">See also</span></span>



[<span data-ttu-id="81780-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="81780-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81780-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="81780-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81780-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="81780-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81780-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="81780-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

