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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359020"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="e503b-103">Propiedad canónica PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="e503b-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="e503b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e503b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e503b-105">Contiene TRUE si se puede seleccionar la entrada de la tabla de un solo elemento.</span><span class="sxs-lookup"><span data-stu-id="e503b-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e503b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e503b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e503b-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="e503b-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="e503b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e503b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e503b-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="e503b-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="e503b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e503b-110">Data type:</span></span>  <br/> |<span data-ttu-id="e503b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e503b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e503b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e503b-112">Area:</span></span>  <br/> |<span data-ttu-id="e503b-113">Contenedor de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="e503b-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e503b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e503b-114">Remarks</span></span>

<span data-ttu-id="e503b-115">Esta propiedad se usa principalmente para el formato visual de una tabla de uso único.</span><span class="sxs-lookup"><span data-stu-id="e503b-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="e503b-116">Las plantillas se pueden agrupar creando una entrada que indique el encabezado del grupo.</span><span class="sxs-lookup"><span data-stu-id="e503b-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="e503b-117">Si se establece esta propiedad en FALSE para el encabezado, el usuario solo puede seleccionar las plantillas reales del grupo y no esta entrada de título.</span><span class="sxs-lookup"><span data-stu-id="e503b-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="e503b-118">Esta propiedad solo se aplica a una tabla única, no a una tabla de jerarquía de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e503b-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="e503b-119">MAPI permite a un proveedor de libreta de direcciones agrupar elementos visualmente por dos medios.</span><span class="sxs-lookup"><span data-stu-id="e503b-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="e503b-120">En primer lugar, determinadas filas pueden funcionar como encabezados al no seleccionarse.</span><span class="sxs-lookup"><span data-stu-id="e503b-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="e503b-121">En segundo lugar, los elementos seleccionables se pueden aplicar sangría con respecto a sus encabezados mediante **la propiedad PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e503b-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="e503b-122">Esta propiedad se usa en dicha agrupación para indicar si este elemento se puede seleccionar de una lista para crear una dirección única.</span><span class="sxs-lookup"><span data-stu-id="e503b-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="e503b-123">Por ejemplo, si un cliente tiene varias plantillas para crear direcciones de fax, puede mostrarlas de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="e503b-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="e503b-124">Plantillas de FAX (profundidad 0, no seleccionables)</span><span class="sxs-lookup"><span data-stu-id="e503b-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="e503b-125">Local (profundidad 1, seleccionable)</span><span class="sxs-lookup"><span data-stu-id="e503b-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="e503b-126">Larga distancia (profundidad 1, seleccionable)</span><span class="sxs-lookup"><span data-stu-id="e503b-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e503b-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e503b-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e503b-128">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="e503b-128">Protocol specifications</span></span>

<span data-ttu-id="e503b-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e503b-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e503b-130">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="e503b-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e503b-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e503b-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e503b-132">Especifica las propiedades y las operaciones permitidas para las plantillas de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e503b-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e503b-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e503b-133">Header files</span></span>

<span data-ttu-id="e503b-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e503b-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="e503b-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e503b-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="e503b-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e503b-136">Mapitags.h</span></span>
  
> <span data-ttu-id="e503b-137">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="e503b-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e503b-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e503b-138">See also</span></span>



[<span data-ttu-id="e503b-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="e503b-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="e503b-140">Propiedad canónica PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="e503b-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="e503b-141">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e503b-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e503b-142">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e503b-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e503b-143">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e503b-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e503b-144">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="e503b-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

