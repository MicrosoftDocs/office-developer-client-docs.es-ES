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
ms.openlocfilehash: bd70d18242fadee964ad96305728e63617a0276f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820244"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a><span data-ttu-id="7576a-103">Propiedad canónica PidTagSearchFolderExpiration</span><span class="sxs-lookup"><span data-stu-id="7576a-103">PidTagSearchFolderExpiration Canonical Property</span></span>

  
  
<span data-ttu-id="7576a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7576a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7576a-105">Contiene la hora en que el contenedor de la carpeta de búsqueda será obsoleto y deben actualizarse o volver a crear.</span><span class="sxs-lookup"><span data-stu-id="7576a-105">Contains the time at which the search folder container will be stale and should be updated or recreated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7576a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7576a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7576a-107">PR_WB_SF_EXPIRATION</span><span class="sxs-lookup"><span data-stu-id="7576a-107">PR_WB_SF_EXPIRATION</span></span>  <br/> |
|<span data-ttu-id="7576a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7576a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7576a-109">0x683A</span><span class="sxs-lookup"><span data-stu-id="7576a-109">0x683A</span></span>  <br/> |
|<span data-ttu-id="7576a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7576a-110">Data type:</span></span>  <br/> |<span data-ttu-id="7576a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7576a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7576a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7576a-112">Area:</span></span>  <br/> |<span data-ttu-id="7576a-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="7576a-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7576a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7576a-114">Remarks</span></span>

<span data-ttu-id="7576a-115">Esta propiedad debe tener el formato como el número de minutos transcurridos desde la medianoche hora Universal coordinada (UTC) del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="7576a-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7576a-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7576a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7576a-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7576a-117">Protocol specifications</span></span>

<span data-ttu-id="7576a-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7576a-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7576a-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7576a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7576a-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7576a-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7576a-121">Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="7576a-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7576a-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7576a-122">Header files</span></span>

<span data-ttu-id="7576a-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7576a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7576a-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7576a-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7576a-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7576a-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7576a-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7576a-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7576a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="7576a-127">See also</span></span>



[<span data-ttu-id="7576a-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7576a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7576a-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="7576a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7576a-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7576a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7576a-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="7576a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

