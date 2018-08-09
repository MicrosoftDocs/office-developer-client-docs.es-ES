---
title: Propiedad canónica PidTagParentDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentDisplay
api_type:
- COM
ms.assetid: 6a36f4fb-17c0-4271-87d4-a92895f35f23
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ce9fea80a2dfed25002e5500dd4defaf5ff04421
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819915"
---
# <a name="pidtagparentdisplay-canonical-property"></a><span data-ttu-id="224f1-103">Propiedad canónica PidTagParentDisplay</span><span class="sxs-lookup"><span data-stu-id="224f1-103">PidTagParentDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="224f1-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="224f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="224f1-105">Contiene el nombre para mostrar de la carpeta donde se ha encontrado un mensaje durante una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="224f1-105">Contains the display name of the folder where a message was found during a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="224f1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="224f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="224f1-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="224f1-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="224f1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="224f1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="224f1-109">0x0E05</span><span class="sxs-lookup"><span data-stu-id="224f1-109">0x0E05</span></span>  <br/> |
|<span data-ttu-id="224f1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="224f1-110">Data type:</span></span>  <br/> |<span data-ttu-id="224f1-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="224f1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="224f1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="224f1-112">Area:</span></span>  <br/> |<span data-ttu-id="224f1-113">MAPI no transmisible</span><span class="sxs-lookup"><span data-stu-id="224f1-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="224f1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="224f1-114">Remarks</span></span>

<span data-ttu-id="224f1-115">Estas propiedades no está en cualquier objeto.</span><span class="sxs-lookup"><span data-stu-id="224f1-115">These properties is not on any object.</span></span> <span data-ttu-id="224f1-116">Sólo puede aparecer en la tabla de contenido de una carpeta de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="224f1-116">They can only appear in the contents table of a search-results folder.</span></span>
  
<span data-ttu-id="224f1-117">Estas propiedades y propiedades de **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) no están relacionadas entre sí.</span><span class="sxs-lookup"><span data-stu-id="224f1-117">These properties and **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) properties are not related to each other.</span></span> <span data-ttu-id="224f1-118">Pertenecieran a contextos totalmente diferentes.</span><span class="sxs-lookup"><span data-stu-id="224f1-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="224f1-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="224f1-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="224f1-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="224f1-120">Header files</span></span>

<span data-ttu-id="224f1-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="224f1-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="224f1-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="224f1-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="224f1-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="224f1-123">Mapitags.h</span></span>
  
> <span data-ttu-id="224f1-124">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="224f1-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="224f1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="224f1-125">See also</span></span>



[<span data-ttu-id="224f1-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="224f1-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="224f1-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="224f1-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="224f1-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="224f1-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="224f1-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="224f1-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

