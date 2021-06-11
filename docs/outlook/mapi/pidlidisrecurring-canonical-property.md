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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315438"
---
# <a name="pidlidisrecurring-canonical-property"></a><span data-ttu-id="e763c-103">Propiedad canónica PidLidIsRecurring</span><span class="sxs-lookup"><span data-stu-id="e763c-103">PidLidIsRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="e763c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e763c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e763c-105">Especifica si el objeto está asociado a una serie periódica.</span><span class="sxs-lookup"><span data-stu-id="e763c-105">Specifies whether or not the object is associated with a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e763c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e763c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e763c-107">LID_IS_RECURRING</span><span class="sxs-lookup"><span data-stu-id="e763c-107">LID_IS_RECURRING</span></span>  <br/> |
|<span data-ttu-id="e763c-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e763c-108">Property set:</span></span>  <br/> |<span data-ttu-id="e763c-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="e763c-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="e763c-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="e763c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e763c-111">0x00000005</span><span class="sxs-lookup"><span data-stu-id="e763c-111">0x00000005</span></span>  <br/> |
|<span data-ttu-id="e763c-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e763c-112">Data type:</span></span>  <br/> |<span data-ttu-id="e763c-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e763c-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e763c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e763c-114">Area:</span></span>  <br/> |<span data-ttu-id="e763c-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="e763c-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e763c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e763c-116">Remarks</span></span>

<span data-ttu-id="e763c-117">Un valor de TRUE indica que el objeto representa una serie periódica o una excepción (incluida una instancia huérfana).</span><span class="sxs-lookup"><span data-stu-id="e763c-117">A value of TRUE indicates that the object represents either a recurring series or an exception (including an orphan instance).</span></span> <span data-ttu-id="e763c-118">Un valor de FALSE, o la ausencia de esta propiedad, indica que el objeto representa una única instancia.</span><span class="sxs-lookup"><span data-stu-id="e763c-118">A value of FALSE, or the absence of this property, indicates that the object represents a single instance.</span></span> <span data-ttu-id="e763c-119">Tenga en cuenta la diferencia entre esta propiedad y **la PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="e763c-119">Note the difference between this property and the **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e763c-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e763c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e763c-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="e763c-121">Protocol specifications</span></span>

<span data-ttu-id="e763c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e763c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e763c-123">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="e763c-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e763c-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e763c-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e763c-125">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="e763c-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e763c-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e763c-126">Header files</span></span>

<span data-ttu-id="e763c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e763c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e763c-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e763c-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e763c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e763c-129">See also</span></span>



[<span data-ttu-id="e763c-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e763c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e763c-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e763c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e763c-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e763c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e763c-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="e763c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

