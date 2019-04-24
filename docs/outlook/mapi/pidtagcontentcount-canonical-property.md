---
title: Propiedad canónica PidTagContentCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCount
api_type:
- HeaderDef
ms.assetid: 27c75031-a968-4636-98a6-4a5b7422f57c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7e9994da72bbc38a546f220e5ecf8768b80c6f1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331958"
---
# <a name="pidtagcontentcount-canonical-property"></a><span data-ttu-id="cb912-103">Propiedad canónica PidTagContentCount</span><span class="sxs-lookup"><span data-stu-id="cb912-103">PidTagContentCount Canonical Property</span></span>

  
  
<span data-ttu-id="cb912-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb912-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb912-105">Contiene el número de mensajes de una carpeta, tal y como calcula el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="cb912-105">Contains the number of messages in a folder, as computed by the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb912-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cb912-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb912-107">PR_CONTENT_COUNT</span><span class="sxs-lookup"><span data-stu-id="cb912-107">PR_CONTENT_COUNT</span></span>  <br/> |
|<span data-ttu-id="cb912-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cb912-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cb912-109">0x3602</span><span class="sxs-lookup"><span data-stu-id="cb912-109">0x3602</span></span>  <br/> |
|<span data-ttu-id="cb912-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cb912-110">Data type:</span></span>  <br/> |<span data-ttu-id="cb912-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cb912-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cb912-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cb912-112">Area:</span></span>  <br/> |<span data-ttu-id="cb912-113">Folder</span><span class="sxs-lookup"><span data-stu-id="cb912-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb912-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb912-114">Remarks</span></span>

<span data-ttu-id="cb912-115">Esta propiedad calculada por el almacén de mensajes se utiliza para dos propósitos diferentes, aunque relacionados.</span><span class="sxs-lookup"><span data-stu-id="cb912-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="cb912-116">En un objeto MapiFolder, contiene el número de mensajes que hay en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="cb912-116">On a MapiFolder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="cb912-117">En una fila de encabezado de las tablas MAPI por categorías, contiene el número de mensajes no asociados en la categoría correspondiente a esa fila de encabezado.</span><span class="sxs-lookup"><span data-stu-id="cb912-117">In a heading row in categorized MAPI tables, it contains the number of non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="cb912-118">El número contenido en esta propiedad no incluye las entradas asociadas en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="cb912-118">The number contained in this property does not include associated entries in the folder.</span></span> <span data-ttu-id="cb912-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contiene el número de mensajes no leídos para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="cb912-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contains the count of unread messages for the folder.</span></span> <span data-ttu-id="cb912-120">Una aplicación cliente puede leer pero no cambiar esta propiedad y **PR_CONTENT_UNREAD**.</span><span class="sxs-lookup"><span data-stu-id="cb912-120">A client application can read but not change this property and **PR_CONTENT_UNREAD**.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cb912-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb912-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cb912-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="cb912-122">Protocol specifications</span></span>

<span data-ttu-id="cb912-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb912-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb912-124">Proporciona referencias a especificaciones del Protocolo de Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="cb912-124">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cb912-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb912-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb912-126">Controla las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="cb912-126">Handles folder operations.</span></span>
    
<span data-ttu-id="cb912-127">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb912-127">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb912-128">Incluye operaciones admitidas para los objetos de la tabla principal.</span><span class="sxs-lookup"><span data-stu-id="cb912-128">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cb912-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cb912-129">Header files</span></span>

<span data-ttu-id="cb912-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cb912-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb912-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cb912-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="cb912-132">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="cb912-132">Mapitags.h</span></span>
  
> <span data-ttu-id="cb912-133">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="cb912-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb912-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb912-134">See also</span></span>



[<span data-ttu-id="cb912-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cb912-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb912-136">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="cb912-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb912-137">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cb912-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb912-138">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="cb912-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

