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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390439"
---
# <a name="pidtagaginggranularity-canonical-property"></a><span data-ttu-id="fcfa3-103">Propiedad canónica PidTagAgingGranularity</span><span class="sxs-lookup"><span data-stu-id="fcfa3-103">PidTagAgingGranularity Canonical Property</span></span>

  
  
<span data-ttu-id="fcfa3-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcfa3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcfa3-105">Representa la unidad de tiempo que se usa para determinar la longitud de tiempo que permanece un elemento en una carpeta antes de que se archiva el elemento.</span><span class="sxs-lookup"><span data-stu-id="fcfa3-105">Represents the unit of time that is used in determining the length of time an item remains in a folder before the item is archived.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fcfa3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fcfa3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fcfa3-107">PR_AGING_GRANULARITY</span><span class="sxs-lookup"><span data-stu-id="fcfa3-107">PR_AGING_GRANULARITY</span></span>  <br/> |
|<span data-ttu-id="fcfa3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fcfa3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fcfa3-109">0x36EE</span><span class="sxs-lookup"><span data-stu-id="fcfa3-109">0x36EE</span></span>  <br/> |
|<span data-ttu-id="fcfa3-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fcfa3-110">Data type:</span></span>  <br/> |<span data-ttu-id="fcfa3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fcfa3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fcfa3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fcfa3-112">Area:</span></span>  <br/> |<span data-ttu-id="fcfa3-113">Varios</span><span class="sxs-lookup"><span data-stu-id="fcfa3-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fcfa3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fcfa3-114">Remarks</span></span>

<span data-ttu-id="fcfa3-115">Los valores posibles para **PR_AGING_GRANULARITY** pueden ser una de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="fcfa3-115">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
|<span data-ttu-id="fcfa3-116">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="fcfa3-116">**Name**</span></span>|<span data-ttu-id="fcfa3-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fcfa3-117">**Value**</span></span>|<span data-ttu-id="fcfa3-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fcfa3-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fcfa3-119">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="fcfa3-119">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="fcfa3-120">0</span><span class="sxs-lookup"><span data-stu-id="fcfa3-120">0</span></span>  <br/> |<span data-ttu-id="fcfa3-121">**PR_AGING_PERIOD** se define en el número de meses.</span><span class="sxs-lookup"><span data-stu-id="fcfa3-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="fcfa3-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="fcfa3-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="fcfa3-123">1</span><span class="sxs-lookup"><span data-stu-id="fcfa3-123">1</span></span>  <br/> |<span data-ttu-id="fcfa3-124">**PR_AGING_PERIOD** se define en el número de semanas.</span><span class="sxs-lookup"><span data-stu-id="fcfa3-124">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="fcfa3-125">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="fcfa3-125">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="fcfa3-126">2</span><span class="sxs-lookup"><span data-stu-id="fcfa3-126">2</span></span>  <br/> |<span data-ttu-id="fcfa3-127">**PR_AGING_PERIOD** se define en el número de días.</span><span class="sxs-lookup"><span data-stu-id="fcfa3-127">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="fcfa3-128">El período de tiempo que permanece un producto en una carpeta antes de que se archiva el elemento se determina mediante dos propiedades, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) y **PR_AGING_GRANULARITY**.</span><span class="sxs-lookup"><span data-stu-id="fcfa3-128">The length of time that an item remains in a folder before the item is archived is determined by two properties, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) and **PR_AGING_GRANULARITY**.</span></span> <span data-ttu-id="fcfa3-129">**PR_AGING_PERIOD** representa el número de unidades de tiempo que el elemento permanecerá en la carpeta antes de ser archivados.</span><span class="sxs-lookup"><span data-stu-id="fcfa3-129">**PR_AGING_PERIOD** represents the number of time units that the item remains in the folder before it is archived.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fcfa3-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fcfa3-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fcfa3-131">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="fcfa3-131">Protocol specifications</span></span>

<span data-ttu-id="fcfa3-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcfa3-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcfa3-133">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fcfa3-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fcfa3-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcfa3-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcfa3-135">Define las estructuras de datos básicos que se usan en las operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="fcfa3-135">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="fcfa3-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcfa3-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcfa3-137">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="fcfa3-137">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fcfa3-138">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fcfa3-138">Header files</span></span>

<span data-ttu-id="fcfa3-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fcfa3-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="fcfa3-140">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fcfa3-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="fcfa3-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fcfa3-141">Mapitags.h</span></span>
  
> <span data-ttu-id="fcfa3-142">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="fcfa3-142">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fcfa3-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcfa3-143">See also</span></span>



[<span data-ttu-id="fcfa3-144">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fcfa3-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fcfa3-145">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="fcfa3-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fcfa3-146">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fcfa3-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fcfa3-147">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="fcfa3-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

