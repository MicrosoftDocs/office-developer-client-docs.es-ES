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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399483"
---
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="fcad0-103">Propiedad canónica PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="fcad0-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="fcad0-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcad0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcad0-105">Especifica si un mensaje de cita es periódico.</span><span class="sxs-lookup"><span data-stu-id="fcad0-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fcad0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fcad0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fcad0-107">dispidRecurring</span><span class="sxs-lookup"><span data-stu-id="fcad0-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="fcad0-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="fcad0-108">Property set:</span></span>  <br/> |<span data-ttu-id="fcad0-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="fcad0-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="fcad0-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="fcad0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fcad0-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="fcad0-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="fcad0-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fcad0-112">Data type:</span></span>  <br/> |<span data-ttu-id="fcad0-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="fcad0-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="fcad0-114">Área:</span><span class="sxs-lookup"><span data-stu-id="fcad0-114">Area:</span></span>  <br/> |<span data-ttu-id="fcad0-115">Calendario</span><span class="sxs-lookup"><span data-stu-id="fcad0-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fcad0-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fcad0-116">Remarks</span></span>

<span data-ttu-id="fcad0-117">Esta propiedad es TRUE si la cita es una cita periódica y es FALSE si no se repite.</span><span class="sxs-lookup"><span data-stu-id="fcad0-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="fcad0-118">Esta propiedad especifica si el objeto representa una serie periódica.</span><span class="sxs-lookup"><span data-stu-id="fcad0-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="fcad0-119">Un valor de TRUE indica que el objeto representa una serie periódica.</span><span class="sxs-lookup"><span data-stu-id="fcad0-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="fcad0-120">Un valor FALSE, o la ausencia de esta propiedad, indica que el objeto representa una instancia única o una excepción (incluida una instancia huérfana).</span><span class="sxs-lookup"><span data-stu-id="fcad0-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="fcad0-121">Tenga en cuenta la diferencia entre esta propiedad y la propiedad **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fcad0-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fcad0-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fcad0-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fcad0-123">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="fcad0-123">Protocol specifications</span></span>

<span data-ttu-id="fcad0-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcad0-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcad0-125">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fcad0-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fcad0-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcad0-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcad0-127">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="fcad0-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fcad0-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fcad0-128">Header files</span></span>

<span data-ttu-id="fcad0-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fcad0-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="fcad0-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fcad0-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fcad0-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcad0-131">See also</span></span>



[<span data-ttu-id="fcad0-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fcad0-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fcad0-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="fcad0-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fcad0-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fcad0-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fcad0-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="fcad0-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

