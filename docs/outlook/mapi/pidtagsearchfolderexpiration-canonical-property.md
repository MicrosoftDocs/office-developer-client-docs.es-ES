---
title: Propiedad canónica PidTagSearchFolderExpiration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderExpiration
api_type:
- COM
ms.assetid: e5746090-c850-4e95-b1e7-a07e42c87179
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a119bb735f752719d292371d4dc43e72450b33c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336473"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a><span data-ttu-id="89936-103">Propiedad canónica PidTagSearchFolderExpiration</span><span class="sxs-lookup"><span data-stu-id="89936-103">PidTagSearchFolderExpiration Canonical Property</span></span>

  
  
<span data-ttu-id="89936-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89936-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89936-105">Contiene la hora en que el contenedor de la carpeta de búsqueda estará obsoleto y se debe actualizar o volver a crear.</span><span class="sxs-lookup"><span data-stu-id="89936-105">Contains the time at which the search folder container will be stale and should be updated or recreated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="89936-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="89936-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="89936-107">PR_WB_SF_EXPIRATION</span><span class="sxs-lookup"><span data-stu-id="89936-107">PR_WB_SF_EXPIRATION</span></span>  <br/> |
|<span data-ttu-id="89936-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="89936-108">Identifier:</span></span>  <br/> |<span data-ttu-id="89936-109">0x683A</span><span class="sxs-lookup"><span data-stu-id="89936-109">0x683A</span></span>  <br/> |
|<span data-ttu-id="89936-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="89936-110">Data type:</span></span>  <br/> |<span data-ttu-id="89936-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="89936-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="89936-112">Área:</span><span class="sxs-lookup"><span data-stu-id="89936-112">Area:</span></span>  <br/> |<span data-ttu-id="89936-113">Buscar </span><span class="sxs-lookup"><span data-stu-id="89936-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89936-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="89936-114">Remarks</span></span>

<span data-ttu-id="89936-115">Esta propiedad se debe formatear como el número de minutos transcurridos desde la medianoche de la hora universal coordinada (UTC), 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="89936-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="89936-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="89936-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="89936-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="89936-117">Protocol specifications</span></span>

<span data-ttu-id="89936-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89936-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89936-119">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="89936-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="89936-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89936-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89936-121">Especifica las propiedades y operaciones para manipular una configuración de lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="89936-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="89936-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="89936-122">Header files</span></span>

<span data-ttu-id="89936-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="89936-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="89936-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="89936-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="89936-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="89936-125">Mapitags.h</span></span>
  
> <span data-ttu-id="89936-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="89936-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="89936-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="89936-127">See also</span></span>



[<span data-ttu-id="89936-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="89936-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="89936-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="89936-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="89936-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="89936-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="89936-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="89936-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

