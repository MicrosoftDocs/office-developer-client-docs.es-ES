---
title: Propiedad canónica PidLidCleanGlobalObjectId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c48fa333d407492b69da5287fa75c565bfd10e11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349220"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a><span data-ttu-id="60c3f-103">Propiedad canónica PidLidCleanGlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="60c3f-103">PidLidCleanGlobalObjectId Canonical Property</span></span>

  
  
<span data-ttu-id="60c3f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60c3f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60c3f-105">Especifica el **objectid** global limpio .</span><span class="sxs-lookup"><span data-stu-id="60c3f-105">Specifies the clean global **ObjectID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="60c3f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="60c3f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="60c3f-107">dispidCleanGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="60c3f-107">dispidCleanGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="60c3f-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="60c3f-108">Property set:</span></span>  <br/> |<span data-ttu-id="60c3f-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="60c3f-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="60c3f-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="60c3f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="60c3f-111">0x00000023</span><span class="sxs-lookup"><span data-stu-id="60c3f-111">0x00000023</span></span>  <br/> |
|<span data-ttu-id="60c3f-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="60c3f-112">Data type:</span></span>  <br/> |<span data-ttu-id="60c3f-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="60c3f-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="60c3f-114">Área:</span><span class="sxs-lookup"><span data-stu-id="60c3f-114">Area:</span></span>  <br/> |<span data-ttu-id="60c3f-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="60c3f-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60c3f-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="60c3f-116">Remarks</span></span>

<span data-ttu-id="60c3f-117">El formato de esta propiedad es el mismo que el de **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="60c3f-117">The format of this property is the same as that of **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span></span> <span data-ttu-id="60c3f-118">El valor de esta propiedad debe ser igual al valor de **LID_GLOBAL_OBJID**, excepto que los campos YH, YL, M y D deben ser cero.</span><span class="sxs-lookup"><span data-stu-id="60c3f-118">The value of this property must be equal to the value of **LID_GLOBAL_OBJID**, except the YH, YL, M, and D fields must be zero.</span></span> <span data-ttu-id="60c3f-119">Todos los objetos que hacen referencia a una instancia de una serie periódica (incluida una instancia huérfana), así como la propia serie periódica, tendrán el mismo valor para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="60c3f-119">All objects that refer to an Instance of a recurring series (including an orphan instance), as well as the recurring series itself, will have the same value for this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="60c3f-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="60c3f-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="60c3f-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="60c3f-121">Protocol specifications</span></span>

<span data-ttu-id="60c3f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60c3f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60c3f-123">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="60c3f-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="60c3f-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60c3f-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60c3f-125">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="60c3f-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="60c3f-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="60c3f-126">Header files</span></span>

<span data-ttu-id="60c3f-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="60c3f-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="60c3f-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="60c3f-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="60c3f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="60c3f-129">See also</span></span>



[<span data-ttu-id="60c3f-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="60c3f-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="60c3f-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="60c3f-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="60c3f-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="60c3f-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="60c3f-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="60c3f-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

