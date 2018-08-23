---
title: Propiedad canónica PidTagFreeBusyCountMonths
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyCountMonths
api_type:
- HeaderDef
ms.assetid: 278a77f2-65ec-4281-b406-942cc416a476
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e7dc8c06fca48c5f7c124a1fdf2228ebeb9da450
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569984"
---
# <a name="pidtagfreebusycountmonths-canonical-property"></a><span data-ttu-id="3db57-103">Propiedad canónica PidTagFreeBusyCountMonths</span><span class="sxs-lookup"><span data-stu-id="3db57-103">PidTagFreeBusyCountMonths Canonical Property</span></span>

  
  
<span data-ttu-id="3db57-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3db57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3db57-105">Contiene el valor para calcular las fechas de inicio y fin del rango de datos de disponibilidad para su publicación en carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="3db57-105">Contains the value for calculating the start and end dates of the range of free/busy data to be published to public folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3db57-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3db57-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3db57-107">PR_FREEBUSY_COUNT_MONTHS</span><span class="sxs-lookup"><span data-stu-id="3db57-107">PR_FREEBUSY_COUNT_MONTHS</span></span>  <br/> |
|<span data-ttu-id="3db57-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3db57-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3db57-109">0x6869</span><span class="sxs-lookup"><span data-stu-id="3db57-109">0x6869</span></span>  <br/> |
|<span data-ttu-id="3db57-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3db57-110">Data type:</span></span>  <br/> |<span data-ttu-id="3db57-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3db57-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3db57-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3db57-112">Area:</span></span>  <br/> |<span data-ttu-id="3db57-113">Mensaje definido por la clase transmisible</span><span class="sxs-lookup"><span data-stu-id="3db57-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3db57-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3db57-114">Remarks</span></span>

<span data-ttu-id="3db57-115">Valor de esta propiedad debe ser mayor o igual que 0 y menor o igual a 36.</span><span class="sxs-lookup"><span data-stu-id="3db57-115">This property's value must be greater than or equal to 0 and less than or equal to 36.</span></span> <span data-ttu-id="3db57-116">No es una propiedad necesaria.</span><span class="sxs-lookup"><span data-stu-id="3db57-116">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3db57-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3db57-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3db57-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="3db57-118">Protocol specifications</span></span>

<span data-ttu-id="3db57-119">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3db57-119">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3db57-120">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="3db57-120">Publishes the availability of a user or resource.</span></span>
    
<span data-ttu-id="3db57-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3db57-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3db57-122">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="3db57-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3db57-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3db57-123">Header files</span></span>

<span data-ttu-id="3db57-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3db57-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="3db57-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3db57-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="3db57-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3db57-126">Mapitags.h</span></span>
  
> <span data-ttu-id="3db57-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="3db57-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3db57-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="3db57-128">See also</span></span>



[<span data-ttu-id="3db57-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3db57-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3db57-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="3db57-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3db57-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3db57-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3db57-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="3db57-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

