---
title: Propiedad canónica PidTagSelectable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSelectable
api_type:
- COM
ms.assetid: eeecd957-dd50-4849-9698-8bc7106301e9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383460"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="c8aff-103">Propiedad canónica PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="c8aff-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="c8aff-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8aff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8aff-105">Contiene TRUE si se puede seleccionar la entrada en la tabla de uso único.</span><span class="sxs-lookup"><span data-stu-id="c8aff-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8aff-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c8aff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8aff-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="c8aff-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="c8aff-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c8aff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c8aff-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="c8aff-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="c8aff-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c8aff-110">Data type:</span></span>  <br/> |<span data-ttu-id="c8aff-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c8aff-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c8aff-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c8aff-112">Area:</span></span>  <br/> |<span data-ttu-id="c8aff-113">Contenedor de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="c8aff-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8aff-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8aff-114">Remarks</span></span>

<span data-ttu-id="c8aff-115">Esta propiedad se usa principalmente para el formato visual de una tabla de uso único.</span><span class="sxs-lookup"><span data-stu-id="c8aff-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="c8aff-116">Las plantillas se pueden agrupar mediante la creación de una entrada que indica el título para el grupo.</span><span class="sxs-lookup"><span data-stu-id="c8aff-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="c8aff-117">Al establecer esta propiedad en FALSE para el encabezado se asegura de que el usuario puede seleccionar sólo las plantillas reales en el grupo y no esta entrada del encabezado.</span><span class="sxs-lookup"><span data-stu-id="c8aff-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="c8aff-118">Esta propiedad se aplica sólo a una tabla de uso único, no a una tabla de jerarquía de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c8aff-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="c8aff-119">MAPI permite a un proveedor de la libreta de direcciones para agrupar los elementos visualmente por medio de dos.</span><span class="sxs-lookup"><span data-stu-id="c8aff-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="c8aff-120">En primer lugar, algunas filas pueden funcionar como encabezados de forma no seleccionable.</span><span class="sxs-lookup"><span data-stu-id="c8aff-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="c8aff-121">En segundo lugar, los elementos seleccionables aplicará sangría con respecto a sus encabezados mediante el uso de la propiedad **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c8aff-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="c8aff-122">Esta propiedad se usa en esa agrupación para indicar si este elemento se puede seleccionar de una lista para crear una dirección de uso único.</span><span class="sxs-lookup"><span data-stu-id="c8aff-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="c8aff-123">Por ejemplo, si un cliente tiene varias plantillas para la creación de direcciones de fax, lo puede mostrarlos como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="c8aff-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="c8aff-124">Plantillas de FAX (profundidad 0, no se puede seleccionar)</span><span class="sxs-lookup"><span data-stu-id="c8aff-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="c8aff-125">Local (profundidad 1, seleccionable)</span><span class="sxs-lookup"><span data-stu-id="c8aff-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="c8aff-126">Llamadas de larga distancia (profundidad de 1, seleccionable)</span><span class="sxs-lookup"><span data-stu-id="c8aff-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c8aff-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c8aff-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c8aff-128">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c8aff-128">Protocol specifications</span></span>

<span data-ttu-id="c8aff-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8aff-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8aff-130">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c8aff-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c8aff-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8aff-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8aff-132">Especifica las propiedades y operaciones que se permiten para las plantillas de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c8aff-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c8aff-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c8aff-133">Header files</span></span>

<span data-ttu-id="c8aff-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8aff-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8aff-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c8aff-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="c8aff-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c8aff-136">Mapitags.h</span></span>
  
> <span data-ttu-id="c8aff-137">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="c8aff-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8aff-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8aff-138">See also</span></span>



[<span data-ttu-id="c8aff-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="c8aff-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="c8aff-140">Propiedad canónica PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="c8aff-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="c8aff-141">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c8aff-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8aff-142">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c8aff-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8aff-143">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c8aff-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8aff-144">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c8aff-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

