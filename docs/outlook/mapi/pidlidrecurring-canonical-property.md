---
title: Propiedad canónica PidLidRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurring
api_type:
- COM
ms.assetid: 3d39a053-277f-4d59-ab2e-cee81710f2ab
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 85e78695a7c4fca5a1e5cd28b0254d4559be0c13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315921"
---
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="46c04-103">Propiedad canónica PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="46c04-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="46c04-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46c04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46c04-105">Especifica si un mensaje de cita es recurrente.</span><span class="sxs-lookup"><span data-stu-id="46c04-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46c04-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="46c04-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46c04-107">dispidRecurring</span><span class="sxs-lookup"><span data-stu-id="46c04-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="46c04-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="46c04-108">Property set:</span></span>  <br/> |<span data-ttu-id="46c04-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="46c04-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="46c04-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="46c04-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="46c04-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="46c04-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="46c04-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="46c04-112">Data type:</span></span>  <br/> |<span data-ttu-id="46c04-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="46c04-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="46c04-114">Área:</span><span class="sxs-lookup"><span data-stu-id="46c04-114">Area:</span></span>  <br/> |<span data-ttu-id="46c04-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="46c04-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46c04-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46c04-116">Remarks</span></span>

<span data-ttu-id="46c04-117">Esta propiedad es TRUE si la cita es una cita periódica y es FALSE si no es periódica.</span><span class="sxs-lookup"><span data-stu-id="46c04-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="46c04-118">Esta propiedad especifica si el objeto representa o no una serie periódica.</span><span class="sxs-lookup"><span data-stu-id="46c04-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="46c04-119">Un valor TRUE indica que el objeto representa una serie periódica.</span><span class="sxs-lookup"><span data-stu-id="46c04-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="46c04-120">Un valor FALSE, o la ausencia de esta propiedad, indica que el objeto representa una instancia única o una excepción (incluida una instancia huérfana).</span><span class="sxs-lookup"><span data-stu-id="46c04-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="46c04-121">Tenga en cuenta la diferencia entre esta propiedad y **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="46c04-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="46c04-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="46c04-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="46c04-123">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="46c04-123">Protocol specifications</span></span>

<span data-ttu-id="46c04-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46c04-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46c04-125">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="46c04-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="46c04-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46c04-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46c04-127">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="46c04-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="46c04-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="46c04-128">Header files</span></span>

<span data-ttu-id="46c04-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="46c04-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="46c04-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="46c04-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46c04-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="46c04-131">See also</span></span>



[<span data-ttu-id="46c04-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="46c04-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="46c04-133">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="46c04-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="46c04-134">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="46c04-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="46c04-135">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="46c04-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

