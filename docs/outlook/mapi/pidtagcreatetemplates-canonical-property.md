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
ms.openlocfilehash: 82da274670c9266a746defcf6bbd5dbcf621901b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819400"
---
# <a name="pidtagcreatetemplates-canonical-property"></a><span data-ttu-id="a9107-103">Propiedad canónica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="a9107-103">PidTagCreateTemplates Canonical Property</span></span>

  
  
<span data-ttu-id="a9107-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a9107-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a9107-105">Contiene un objeto incrustado de tabla que contiene los identificadores de entrada de plantilla de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a9107-105">Contains an embedded table object that contains dialog box template entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9107-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a9107-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9107-107">PR_CREATE_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="a9107-107">PR_CREATE_TEMPLATES</span></span>  <br/> |
|<span data-ttu-id="a9107-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a9107-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a9107-109">0x3604</span><span class="sxs-lookup"><span data-stu-id="a9107-109">0x3604</span></span>  <br/> |
|<span data-ttu-id="a9107-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a9107-110">Data type:</span></span>  <br/> |<span data-ttu-id="a9107-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="a9107-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="a9107-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a9107-112">Area:</span></span>  <br/> |<span data-ttu-id="a9107-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="a9107-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9107-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a9107-114">Remarks</span></span>

<span data-ttu-id="a9107-115">Para obtener información sobre qué plantilla se pueden crear objetos dentro de un contenedor, llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="a9107-115">To learn what template objects can be created inside a container, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on this property.</span></span> <span data-ttu-id="a9107-116">El objeto resultante es la tabla de uso único que proporciona a los identificadores de entrada para todas las plantillas que se pueden crear dentro del contenedor.</span><span class="sxs-lookup"><span data-stu-id="a9107-116">The resulting object is the one-off table that gives the entry identifiers for all the templates that you can create inside the container.</span></span> 
  
<span data-ttu-id="a9107-117">Para crear los objetos de plantilla, se ha de llamar al método **CreateEntry** del objeto de contenedor en los valores de columna de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la tabla de uso único.</span><span class="sxs-lookup"><span data-stu-id="a9107-117">To create the template objects, call the container object's **CreateEntry** method on the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column values from the one-off table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a9107-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a9107-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a9107-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a9107-119">Header files</span></span>

<span data-ttu-id="a9107-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a9107-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="a9107-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a9107-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="a9107-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a9107-122">Mapitags.h</span></span>
  
> <span data-ttu-id="a9107-123">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="a9107-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9107-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9107-124">See also</span></span>



[<span data-ttu-id="a9107-125">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="a9107-125">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)


[<span data-ttu-id="a9107-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a9107-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a9107-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a9107-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a9107-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a9107-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a9107-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="a9107-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

