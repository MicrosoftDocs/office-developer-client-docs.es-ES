---
title: Propiedad canónica PidLidIsRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsRecurring
api_type:
- COM
ms.assetid: 1f8ecc22-badc-4278-a3c6-fcd398f5bf24
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c920cd42a27c03ffcff63bbd2e0049ddb6f81158
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390852"
---
# <a name="pidlidisrecurring-canonical-property"></a><span data-ttu-id="18677-103">Propiedad canónica PidLidIsRecurring</span><span class="sxs-lookup"><span data-stu-id="18677-103">PidLidIsRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="18677-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18677-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18677-105">Especifica si el objeto está asociado con una serie periódica.</span><span class="sxs-lookup"><span data-stu-id="18677-105">Specifies whether or not the object is associated with a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18677-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="18677-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18677-107">LID_IS_RECURRING</span><span class="sxs-lookup"><span data-stu-id="18677-107">LID_IS_RECURRING</span></span>  <br/> |
|<span data-ttu-id="18677-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="18677-108">Property set:</span></span>  <br/> |<span data-ttu-id="18677-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="18677-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="18677-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="18677-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="18677-111">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="18677-111">0x00000005</span></span>  <br/> |
|<span data-ttu-id="18677-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="18677-112">Data type:</span></span>  <br/> |<span data-ttu-id="18677-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="18677-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="18677-114">Área:</span><span class="sxs-lookup"><span data-stu-id="18677-114">Area:</span></span>  <br/> |<span data-ttu-id="18677-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="18677-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18677-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="18677-116">Remarks</span></span>

<span data-ttu-id="18677-117">Un valor de TRUE indica que el objeto representa una serie periódica o una excepción (incluida una instancia huérfana).</span><span class="sxs-lookup"><span data-stu-id="18677-117">A value of TRUE indicates that the object represents either a recurring series or an exception (including an orphan instance).</span></span> <span data-ttu-id="18677-118">Un valor FALSE, o la ausencia de esta propiedad indica que el objeto representa una instancia única.</span><span class="sxs-lookup"><span data-stu-id="18677-118">A value of FALSE, or the absence of this property, indicates that the object represents a single instance.</span></span> <span data-ttu-id="18677-119">Tenga en cuenta la diferencia entre esta propiedad y la propiedad **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="18677-119">Note the difference between this property and the **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="18677-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="18677-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18677-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="18677-121">Protocol specifications</span></span>

<span data-ttu-id="18677-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18677-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18677-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="18677-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="18677-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18677-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18677-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="18677-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18677-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="18677-126">Header files</span></span>

<span data-ttu-id="18677-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18677-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="18677-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="18677-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18677-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="18677-129">See also</span></span>



[<span data-ttu-id="18677-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="18677-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18677-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="18677-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18677-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="18677-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18677-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="18677-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

