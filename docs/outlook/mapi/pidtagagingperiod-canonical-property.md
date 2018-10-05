---
title: Propiedad canónica PidTagAgingPeriod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingPeriod
api_type:
- HeaderDef
ms.assetid: 762020d1-4bc8-d60d-0f66-3929aae24bfb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d42b58bf4fd445f34064b179c873c8bc15b11b3f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391181"
---
# <a name="pidtagagingperiod-canonical-property"></a><span data-ttu-id="3afc7-103">Propiedad canónica PidTagAgingPeriod</span><span class="sxs-lookup"><span data-stu-id="3afc7-103">PidTagAgingPeriod Canonical Property</span></span>

  
  
<span data-ttu-id="3afc7-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3afc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3afc7-105">Representa el número de unidades de tiempo que se usan para determinar el período de tiempo que permanece un producto en una carpeta antes de que se archiva el elemento.</span><span class="sxs-lookup"><span data-stu-id="3afc7-105">Represents the number of time units that are used to determine the length of time that an item remains in a folder before the item is archived.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="3afc7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3afc7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3afc7-107">PR_AGING_PERIOD</span><span class="sxs-lookup"><span data-stu-id="3afc7-107">PR_AGING_PERIOD</span></span>  <br/> |
|<span data-ttu-id="3afc7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3afc7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3afc7-109">0x36EC</span><span class="sxs-lookup"><span data-stu-id="3afc7-109">0x36EC</span></span>  <br/> |
|<span data-ttu-id="3afc7-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="3afc7-110">Property type:</span></span>  <br/> |<span data-ttu-id="3afc7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3afc7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3afc7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3afc7-112">Area:</span></span>  <br/> |<span data-ttu-id="3afc7-113">Varios</span><span class="sxs-lookup"><span data-stu-id="3afc7-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3afc7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3afc7-114">Remarks</span></span>

<span data-ttu-id="3afc7-115">El período de tiempo que permanece un producto en una carpeta antes de que se archiva el elemento se determina mediante dos propiedades, **PR_AGING_PERIOD** y **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="3afc7-115">The length of time that an item remains in a folder before the item is archived is determined by two properties, **PR_AGING_PERIOD** and **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span></span> <span data-ttu-id="3afc7-116">**PR_AGING_GRANULARITY** representa la unidad de tiempo en que se expresa **PR_AGING_PERIOD** , al determinar este período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3afc7-116">**PR_AGING_GRANULARITY** represents the time unit in which **PR_AGING_PERIOD** is expressed, when determining this length of time.</span></span> 
  
<span data-ttu-id="3afc7-117">Los valores posibles para **PR_AGING_GRANULARITY** pueden ser una de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="3afc7-117">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
****

|<span data-ttu-id="3afc7-118">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="3afc7-118">**Name**</span></span>|<span data-ttu-id="3afc7-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3afc7-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3afc7-120">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="3afc7-120">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="3afc7-121">**PR_AGING_PERIOD** se define en el número de meses.</span><span class="sxs-lookup"><span data-stu-id="3afc7-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="3afc7-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="3afc7-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="3afc7-123">**PR_AGING_PERIOD** se define en el número de semanas.</span><span class="sxs-lookup"><span data-stu-id="3afc7-123">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="3afc7-124">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="3afc7-124">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="3afc7-125">**PR_AGING_PERIOD** se define en el número de días.</span><span class="sxs-lookup"><span data-stu-id="3afc7-125">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="3afc7-126">Por ejemplo, si un archivos de carpeta es un elemento sólo después de que el elemento ha sido en la carpeta para dos semanas y, a continuación, **PR_AGING_GRANULARITY** **AG_WEEKS** y **PR_AGING_PERIOD** es 2.</span><span class="sxs-lookup"><span data-stu-id="3afc7-126">For example, if a folder archives an item only after the item has been in the folder for two weeks, then **PR_AGING_GRANULARITY** is **AG_WEEKS** and **PR_AGING_PERIOD** is 2.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3afc7-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3afc7-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3afc7-128">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="3afc7-128">Protocol specifications</span></span>

<span data-ttu-id="3afc7-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3afc7-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3afc7-130">Proporciona definiciones de conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="3afc7-130">Provides property set definitions.</span></span>
    
<span data-ttu-id="3afc7-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3afc7-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3afc7-132">Define las estructuras de datos básicos que se usan en las operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="3afc7-132">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="3afc7-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3afc7-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3afc7-134">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="3afc7-134">Specifies the properties and operations that are permitted for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3afc7-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3afc7-135">Header files</span></span>

<span data-ttu-id="3afc7-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3afc7-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="3afc7-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3afc7-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="3afc7-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3afc7-138">Mapitags.h</span></span>
  
> <span data-ttu-id="3afc7-139">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="3afc7-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3afc7-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="3afc7-140">See also</span></span>



[<span data-ttu-id="3afc7-141">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3afc7-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3afc7-142">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="3afc7-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3afc7-143">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3afc7-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3afc7-144">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="3afc7-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

