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
ms.openlocfilehash: 610e9d396442f981b7bcbf126e3086e6885399d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316194"
---
# <a name="pidtagfreebusycountmonths-canonical-property"></a><span data-ttu-id="fd853-103">Propiedad canónica PidTagFreeBusyCountMonths</span><span class="sxs-lookup"><span data-stu-id="fd853-103">PidTagFreeBusyCountMonths Canonical Property</span></span>

  
  
<span data-ttu-id="fd853-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd853-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd853-105">Contiene el valor para calcular las fechas de inicio y finalización del intervalo de datos de disponibilidad que se van a publicar en carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="fd853-105">Contains the value for calculating the start and end dates of the range of free/busy data to be published to public folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fd853-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fd853-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fd853-107">PR_FREEBUSY_COUNT_MONTHS</span><span class="sxs-lookup"><span data-stu-id="fd853-107">PR_FREEBUSY_COUNT_MONTHS</span></span>  <br/> |
|<span data-ttu-id="fd853-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fd853-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fd853-109">0x6869</span><span class="sxs-lookup"><span data-stu-id="fd853-109">0x6869</span></span>  <br/> |
|<span data-ttu-id="fd853-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fd853-110">Data type:</span></span>  <br/> |<span data-ttu-id="fd853-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fd853-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fd853-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fd853-112">Area:</span></span>  <br/> |<span data-ttu-id="fd853-113">Transmitible definida por la clase message</span><span class="sxs-lookup"><span data-stu-id="fd853-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd853-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fd853-114">Remarks</span></span>

<span data-ttu-id="fd853-115">El valor de esta propiedad debe ser mayor o igual que 0 y menor o igual que 36.</span><span class="sxs-lookup"><span data-stu-id="fd853-115">This property's value must be greater than or equal to 0 and less than or equal to 36.</span></span> <span data-ttu-id="fd853-116">No es una propiedad obligatoria.</span><span class="sxs-lookup"><span data-stu-id="fd853-116">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fd853-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd853-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fd853-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="fd853-118">Protocol specifications</span></span>

<span data-ttu-id="fd853-119">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd853-119">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd853-120">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="fd853-120">Publishes the availability of a user or resource.</span></span>
    
<span data-ttu-id="fd853-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd853-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd853-122">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="fd853-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fd853-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fd853-123">Header files</span></span>

<span data-ttu-id="fd853-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fd853-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="fd853-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fd853-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="fd853-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fd853-126">Mapitags.h</span></span>
  
> <span data-ttu-id="fd853-127">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="fd853-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd853-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd853-128">See also</span></span>



[<span data-ttu-id="fd853-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fd853-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fd853-130">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fd853-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fd853-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fd853-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fd853-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="fd853-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

