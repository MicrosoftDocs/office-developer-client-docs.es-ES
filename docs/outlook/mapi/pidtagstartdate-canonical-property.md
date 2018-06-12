---
title: Propiedad canónico PidTagStartDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStartDate
api_type:
- COM
ms.assetid: 908c2d9f-53f4-4aa8-b309-2f3ac2dca5b5
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 14a077dfdb0f0781ab0d9f085c758c7a7d6285af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820332"
---
# <a name="pidtagstartdate-canonical-property"></a><span data-ttu-id="c15c9-103">Propiedad canónico PidTagStartDate</span><span class="sxs-lookup"><span data-stu-id="c15c9-103">PidTagStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="c15c9-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c15c9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c15c9-105">Contiene la fecha y hora de una cita como administrado por una aplicación de programación de inicio.</span><span class="sxs-lookup"><span data-stu-id="c15c9-105">Contains the starting date and time of an appointment as managed by a scheduling application.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c15c9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c15c9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c15c9-107">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="c15c9-107">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="c15c9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c15c9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c15c9-109">0x0060</span><span class="sxs-lookup"><span data-stu-id="c15c9-109">0x0060</span></span>  <br/> |
|<span data-ttu-id="c15c9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c15c9-110">Data type:</span></span>  <br/> |<span data-ttu-id="c15c9-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c15c9-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c15c9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c15c9-112">Area:</span></span>  <br/> |<span data-ttu-id="c15c9-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="c15c9-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c15c9-114">Notas</span><span class="sxs-lookup"><span data-stu-id="c15c9-114">Remarks</span></span>

<span data-ttu-id="c15c9-115">Programación de aplicaciones debe establecer esta propiedad y las propiedades de **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) al enviar convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="c15c9-115">Scheduling applications should set both this property and **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) properties when sending meeting requests.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c15c9-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c15c9-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c15c9-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c15c9-117">Protocol specifications</span></span>

<span data-ttu-id="c15c9-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c15c9-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c15c9-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c15c9-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c15c9-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c15c9-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c15c9-121">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="c15c9-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c15c9-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c15c9-122">Header files</span></span>

<span data-ttu-id="c15c9-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c15c9-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c15c9-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c15c9-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c15c9-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c15c9-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c15c9-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c15c9-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c15c9-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="c15c9-127">See also</span></span>



[<span data-ttu-id="c15c9-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c15c9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c15c9-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c15c9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c15c9-130">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="c15c9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c15c9-131">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c15c9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

