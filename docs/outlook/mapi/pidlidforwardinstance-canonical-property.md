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
# <a name="pidlidforwardinstance-canonical-property"></a><span data-ttu-id="fbede-103">Propiedad canónica PidLidForwardInstance</span><span class="sxs-lookup"><span data-stu-id="fbede-103">PidLidForwardInstance Canonical Property</span></span>

  
  
<span data-ttu-id="fbede-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fbede-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fbede-105">Indica que la convocatoria de reunión representa una excepción en una serie periódica y que se ha reenviado (incluso si la ha reenviado el organizador) en lugar de ser una invitación enviada por el organizador.</span><span class="sxs-lookup"><span data-stu-id="fbede-105">Indicates that the meeting request represents an exception to a recurring series, and it was forwarded (even when forwarded by the organizer) rather than being an invitation sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fbede-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fbede-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fbede-107">dispidFwrdInstance</span><span class="sxs-lookup"><span data-stu-id="fbede-107">dispidFwrdInstance</span></span>  <br/> |
|<span data-ttu-id="fbede-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="fbede-108">Property set:</span></span>  <br/> |<span data-ttu-id="fbede-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="fbede-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="fbede-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="fbede-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fbede-111">0x0000820A</span><span class="sxs-lookup"><span data-stu-id="fbede-111">0x0000820A</span></span>  <br/> |
|<span data-ttu-id="fbede-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fbede-112">Data type:</span></span>  <br/> |<span data-ttu-id="fbede-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="fbede-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="fbede-114">Área:</span><span class="sxs-lookup"><span data-stu-id="fbede-114">Area:</span></span>  <br/> |<span data-ttu-id="fbede-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="fbede-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbede-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fbede-116">Remarks</span></span>

<span data-ttu-id="fbede-117">Un valor de FALSE para esta propiedad indica que la convocatoria de reunión no es una instancia reenviada.</span><span class="sxs-lookup"><span data-stu-id="fbede-117">A value of FALSE for this property indicates that the meeting request is not a forwarded instance.</span></span> <span data-ttu-id="fbede-118">Esta propiedad no es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="fbede-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fbede-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fbede-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fbede-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="fbede-120">Protocol specifications</span></span>

<span data-ttu-id="fbede-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fbede-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fbede-122">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fbede-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fbede-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fbede-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fbede-124">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="fbede-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fbede-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fbede-125">Header files</span></span>

<span data-ttu-id="fbede-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fbede-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="fbede-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fbede-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fbede-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbede-128">See also</span></span>



[<span data-ttu-id="fbede-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fbede-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fbede-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="fbede-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fbede-131">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fbede-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fbede-132">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="fbede-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

