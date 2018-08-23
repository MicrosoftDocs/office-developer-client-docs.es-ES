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
ms.openlocfilehash: f7813125e18f437087fa06c57f8442c84a81d80d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574065"
---
# <a name="pidlidisrecurring-canonical-property"></a><span data-ttu-id="5a144-103">Propiedad canónica PidLidIsRecurring</span><span class="sxs-lookup"><span data-stu-id="5a144-103">PidLidIsRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="5a144-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a144-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a144-105">Especifica si el objeto está asociado con una serie periódica.</span><span class="sxs-lookup"><span data-stu-id="5a144-105">Specifies whether or not the object is associated with a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a144-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5a144-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a144-107">LID_IS_RECURRING</span><span class="sxs-lookup"><span data-stu-id="5a144-107">LID_IS_RECURRING</span></span>  <br/> |
|<span data-ttu-id="5a144-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="5a144-108">Property set:</span></span>  <br/> |<span data-ttu-id="5a144-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="5a144-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="5a144-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="5a144-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5a144-111">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="5a144-111">0x00000005</span></span>  <br/> |
|<span data-ttu-id="5a144-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5a144-112">Data type:</span></span>  <br/> |<span data-ttu-id="5a144-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5a144-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5a144-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5a144-114">Area:</span></span>  <br/> |<span data-ttu-id="5a144-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="5a144-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a144-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5a144-116">Remarks</span></span>

<span data-ttu-id="5a144-117">Un valor de TRUE indica que el objeto representa una serie periódica o una excepción (incluida una instancia huérfana).</span><span class="sxs-lookup"><span data-stu-id="5a144-117">A value of TRUE indicates that the object represents either a recurring series or an exception (including an orphan instance).</span></span> <span data-ttu-id="5a144-118">Un valor FALSE, o la ausencia de esta propiedad indica que el objeto representa una instancia única.</span><span class="sxs-lookup"><span data-stu-id="5a144-118">A value of FALSE, or the absence of this property, indicates that the object represents a single instance.</span></span> <span data-ttu-id="5a144-119">Tenga en cuenta la diferencia entre esta propiedad y la propiedad **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5a144-119">Note the difference between this property and the **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5a144-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a144-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a144-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5a144-121">Protocol specifications</span></span>

<span data-ttu-id="5a144-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a144-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a144-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5a144-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5a144-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a144-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a144-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a144-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a144-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5a144-126">Header files</span></span>

<span data-ttu-id="5a144-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a144-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a144-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5a144-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a144-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5a144-129">See also</span></span>



[<span data-ttu-id="5a144-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5a144-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a144-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5a144-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a144-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5a144-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a144-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5a144-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

