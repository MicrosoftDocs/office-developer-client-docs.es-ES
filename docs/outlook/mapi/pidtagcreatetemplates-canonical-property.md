---
title: Propiedad canónica PidTagCreateTemplates
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreateTemplates
api_type:
- HeaderDef
ms.assetid: d2530009-5de3-4872-a0a5-be1389c4206e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 08cf1faa0c3cc4cf61e2253b0026361704fdd0e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438186"
---
# <a name="pidtagcreatetemplates-canonical-property"></a><span data-ttu-id="5c8e0-103">Propiedad canónica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="5c8e0-103">PidTagCreateTemplates Canonical Property</span></span>

  
  
<span data-ttu-id="5c8e0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c8e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c8e0-105">Contiene un objeto de tabla incrustado que contiene identificadores de entrada de plantilla de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="5c8e0-105">Contains an embedded table object that contains dialog box template entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c8e0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5c8e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c8e0-107">PR_CREATE_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="5c8e0-107">PR_CREATE_TEMPLATES</span></span>  <br/> |
|<span data-ttu-id="5c8e0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5c8e0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5c8e0-109">0x3604</span><span class="sxs-lookup"><span data-stu-id="5c8e0-109">0x3604</span></span>  <br/> |
|<span data-ttu-id="5c8e0-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5c8e0-110">Data type:</span></span>  <br/> |<span data-ttu-id="5c8e0-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="5c8e0-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="5c8e0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5c8e0-112">Area:</span></span>  <br/> |<span data-ttu-id="5c8e0-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="5c8e0-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c8e0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5c8e0-114">Remarks</span></span>

<span data-ttu-id="5c8e0-115">Para obtener información sobre qué objetos de plantilla se pueden crear dentro de un contenedor, llame al [método IMAPIProp::OpenProperty](imapiprop-openproperty.md) en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="5c8e0-115">To learn what template objects can be created inside a container, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on this property.</span></span> <span data-ttu-id="5c8e0-116">El objeto resultante es la tabla de uso único que proporciona los identificadores de entrada para todas las plantillas que se pueden crear dentro del contenedor.</span><span class="sxs-lookup"><span data-stu-id="5c8e0-116">The resulting object is the one-off table that gives the entry identifiers for all the templates that you can create inside the container.</span></span> 
  
<span data-ttu-id="5c8e0-117">Para crear los objetos de plantilla, llame al método **CreateEntry** del objeto contenedor en los valores de columna **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la tabla de un solo elemento.</span><span class="sxs-lookup"><span data-stu-id="5c8e0-117">To create the template objects, call the container object's **CreateEntry** method on the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column values from the one-off table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5c8e0-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c8e0-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5c8e0-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5c8e0-119">Header files</span></span>

<span data-ttu-id="5c8e0-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c8e0-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c8e0-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5c8e0-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="5c8e0-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5c8e0-122">Mapitags.h</span></span>
  
> <span data-ttu-id="5c8e0-123">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="5c8e0-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c8e0-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c8e0-124">See also</span></span>



[<span data-ttu-id="5c8e0-125">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="5c8e0-125">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)


[<span data-ttu-id="5c8e0-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5c8e0-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c8e0-127">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="5c8e0-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c8e0-128">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5c8e0-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c8e0-129">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="5c8e0-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

