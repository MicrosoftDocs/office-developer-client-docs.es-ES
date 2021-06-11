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
ms.openlocfilehash: 7aef4c1d83672033662502ad0950b7bac9f58c52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429505"
---
# <a name="pidtagparentdisplay-canonical-property"></a><span data-ttu-id="15a25-103">Propiedad canónica PidTagParentDisplay</span><span class="sxs-lookup"><span data-stu-id="15a25-103">PidTagParentDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="15a25-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15a25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15a25-105">Contiene el nombre para mostrar de la carpeta donde se encontró un mensaje durante una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="15a25-105">Contains the display name of the folder where a message was found during a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15a25-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="15a25-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15a25-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="15a25-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="15a25-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="15a25-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15a25-109">0x0E05</span><span class="sxs-lookup"><span data-stu-id="15a25-109">0x0E05</span></span>  <br/> |
|<span data-ttu-id="15a25-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="15a25-110">Data type:</span></span>  <br/> |<span data-ttu-id="15a25-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="15a25-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="15a25-112">Área:</span><span class="sxs-lookup"><span data-stu-id="15a25-112">Area:</span></span>  <br/> |<span data-ttu-id="15a25-113">MAPI no transmitible</span><span class="sxs-lookup"><span data-stu-id="15a25-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15a25-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="15a25-114">Remarks</span></span>

<span data-ttu-id="15a25-115">Estas propiedades no están en ningún objeto.</span><span class="sxs-lookup"><span data-stu-id="15a25-115">These properties is not on any object.</span></span> <span data-ttu-id="15a25-116">Solo pueden aparecer en la tabla de contenido de una carpeta de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="15a25-116">They can only appear in the contents table of a search-results folder.</span></span>
  
<span data-ttu-id="15a25-117">Estas propiedades **y PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) no están relacionadas entre sí.</span><span class="sxs-lookup"><span data-stu-id="15a25-117">These properties and **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) properties are not related to each other.</span></span> <span data-ttu-id="15a25-118">Pertenecen a contextos totalmente diferentes.</span><span class="sxs-lookup"><span data-stu-id="15a25-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="15a25-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="15a25-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="15a25-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="15a25-120">Header files</span></span>

<span data-ttu-id="15a25-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15a25-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="15a25-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="15a25-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="15a25-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="15a25-123">Mapitags.h</span></span>
  
> <span data-ttu-id="15a25-124">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="15a25-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15a25-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="15a25-125">See also</span></span>



[<span data-ttu-id="15a25-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="15a25-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15a25-127">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="15a25-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15a25-128">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="15a25-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15a25-129">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="15a25-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

