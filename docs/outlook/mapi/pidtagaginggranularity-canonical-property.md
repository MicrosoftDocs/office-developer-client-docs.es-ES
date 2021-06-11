---
title: Propiedad canónica PidTagAgingGranularity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingGranularity
api_type:
- HeaderDef
ms.assetid: b79ec87d-d97c-4e6c-899b-78ebf1b485a7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b4006b62758b32598a64eaa4eb333c7ce5b12605
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325588"
---
# <a name="pidtagaginggranularity-canonical-property"></a><span data-ttu-id="94d2c-103">Propiedad canónica PidTagAgingGranularity</span><span class="sxs-lookup"><span data-stu-id="94d2c-103">PidTagAgingGranularity Canonical Property</span></span>

  
  
<span data-ttu-id="94d2c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94d2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94d2c-105">Representa la unidad de tiempo que se usa para determinar el tiempo que un elemento permanece en una carpeta antes de archivar el elemento.</span><span class="sxs-lookup"><span data-stu-id="94d2c-105">Represents the unit of time that is used in determining the length of time an item remains in a folder before the item is archived.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="94d2c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="94d2c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94d2c-107">PR_AGING_GRANULARITY</span><span class="sxs-lookup"><span data-stu-id="94d2c-107">PR_AGING_GRANULARITY</span></span>  <br/> |
|<span data-ttu-id="94d2c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="94d2c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="94d2c-109">0x36EE</span><span class="sxs-lookup"><span data-stu-id="94d2c-109">0x36EE</span></span>  <br/> |
|<span data-ttu-id="94d2c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="94d2c-110">Data type:</span></span>  <br/> |<span data-ttu-id="94d2c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="94d2c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="94d2c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="94d2c-112">Area:</span></span>  <br/> |<span data-ttu-id="94d2c-113">Varios</span><span class="sxs-lookup"><span data-stu-id="94d2c-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94d2c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="94d2c-114">Remarks</span></span>

<span data-ttu-id="94d2c-115">Los valores posibles **PR_AGING_GRANULARITY** pueden ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="94d2c-115">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
|<span data-ttu-id="94d2c-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="94d2c-116">**Name**</span></span>|<span data-ttu-id="94d2c-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="94d2c-117">**Value**</span></span>|<span data-ttu-id="94d2c-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="94d2c-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="94d2c-119">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="94d2c-119">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="94d2c-120">0</span><span class="sxs-lookup"><span data-stu-id="94d2c-120">0</span></span>  <br/> |<span data-ttu-id="94d2c-121">**PR_AGING_PERIOD** se define en número de meses.</span><span class="sxs-lookup"><span data-stu-id="94d2c-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="94d2c-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="94d2c-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="94d2c-123">1</span><span class="sxs-lookup"><span data-stu-id="94d2c-123">1</span></span>  <br/> |<span data-ttu-id="94d2c-124">**PR_AGING_PERIOD** se define en número de semanas.</span><span class="sxs-lookup"><span data-stu-id="94d2c-124">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="94d2c-125">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="94d2c-125">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="94d2c-126">2</span><span class="sxs-lookup"><span data-stu-id="94d2c-126">2</span></span>  <br/> |<span data-ttu-id="94d2c-127">**PR_AGING_PERIOD** se define en número de días.</span><span class="sxs-lookup"><span data-stu-id="94d2c-127">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="94d2c-128">El tiempo que un elemento permanece en una carpeta antes de archivar el elemento está determinado por dos propiedades, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) y **PR_AGING_GRANULARITY**.</span><span class="sxs-lookup"><span data-stu-id="94d2c-128">The length of time that an item remains in a folder before the item is archived is determined by two properties, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) and **PR_AGING_GRANULARITY**.</span></span> <span data-ttu-id="94d2c-129">**PR_AGING_PERIOD** representa el número de unidades de tiempo que el elemento permanece en la carpeta antes de archivarlo.</span><span class="sxs-lookup"><span data-stu-id="94d2c-129">**PR_AGING_PERIOD** represents the number of time units that the item remains in the folder before it is archived.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="94d2c-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="94d2c-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="94d2c-131">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="94d2c-131">Protocol specifications</span></span>

<span data-ttu-id="94d2c-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94d2c-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94d2c-133">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="94d2c-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="94d2c-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94d2c-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94d2c-135">Define las estructuras de datos básicas que se usan en operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="94d2c-135">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="94d2c-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94d2c-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94d2c-137">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="94d2c-137">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="94d2c-138">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="94d2c-138">Header files</span></span>

<span data-ttu-id="94d2c-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="94d2c-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="94d2c-140">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="94d2c-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="94d2c-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="94d2c-141">Mapitags.h</span></span>
  
> <span data-ttu-id="94d2c-142">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="94d2c-142">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94d2c-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="94d2c-143">See also</span></span>



[<span data-ttu-id="94d2c-144">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="94d2c-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94d2c-145">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="94d2c-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94d2c-146">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="94d2c-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94d2c-147">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="94d2c-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

