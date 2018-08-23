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
ms.openlocfilehash: 28611e442f816e4d091cc6b29e2ee69195a63d09
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563362"
---
# <a name="pidtagcreatetemplates-canonical-property"></a><span data-ttu-id="aa33f-103">Propiedad canónica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="aa33f-103">PidTagCreateTemplates Canonical Property</span></span>

  
  
<span data-ttu-id="aa33f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa33f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa33f-105">Contiene un objeto incrustado de tabla que contiene los identificadores de entrada de plantilla de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="aa33f-105">Contains an embedded table object that contains dialog box template entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aa33f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="aa33f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aa33f-107">PR_CREATE_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="aa33f-107">PR_CREATE_TEMPLATES</span></span>  <br/> |
|<span data-ttu-id="aa33f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="aa33f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aa33f-109">0x3604</span><span class="sxs-lookup"><span data-stu-id="aa33f-109">0x3604</span></span>  <br/> |
|<span data-ttu-id="aa33f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="aa33f-110">Data type:</span></span>  <br/> |<span data-ttu-id="aa33f-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="aa33f-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="aa33f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="aa33f-112">Area:</span></span>  <br/> |<span data-ttu-id="aa33f-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="aa33f-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa33f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa33f-114">Remarks</span></span>

<span data-ttu-id="aa33f-115">Para obtener información sobre qué plantilla se pueden crear objetos dentro de un contenedor, llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="aa33f-115">To learn what template objects can be created inside a container, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on this property.</span></span> <span data-ttu-id="aa33f-116">El objeto resultante es la tabla de uso único que proporciona a los identificadores de entrada para todas las plantillas que se pueden crear dentro del contenedor.</span><span class="sxs-lookup"><span data-stu-id="aa33f-116">The resulting object is the one-off table that gives the entry identifiers for all the templates that you can create inside the container.</span></span> 
  
<span data-ttu-id="aa33f-117">Para crear los objetos de plantilla, se ha de llamar al método **CreateEntry** del objeto de contenedor en los valores de columna de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la tabla de uso único.</span><span class="sxs-lookup"><span data-stu-id="aa33f-117">To create the template objects, call the container object's **CreateEntry** method on the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column values from the one-off table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aa33f-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa33f-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="aa33f-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="aa33f-119">Header files</span></span>

<span data-ttu-id="aa33f-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aa33f-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="aa33f-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="aa33f-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="aa33f-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aa33f-122">Mapitags.h</span></span>
  
> <span data-ttu-id="aa33f-123">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="aa33f-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aa33f-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="aa33f-124">See also</span></span>



[<span data-ttu-id="aa33f-125">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="aa33f-125">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)


[<span data-ttu-id="aa33f-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="aa33f-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aa33f-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="aa33f-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aa33f-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="aa33f-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aa33f-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="aa33f-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

