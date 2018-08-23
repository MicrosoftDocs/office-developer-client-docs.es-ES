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
ms.openlocfilehash: a2f72f68926665087ee8e3a0c9e8394042a8f955
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590774"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a><span data-ttu-id="0d229-103">Propiedad canónica PidTagSearchFolderExpiration</span><span class="sxs-lookup"><span data-stu-id="0d229-103">PidTagSearchFolderExpiration Canonical Property</span></span>

  
  
<span data-ttu-id="0d229-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d229-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d229-105">Contiene la hora en que el contenedor de la carpeta de búsqueda será obsoleto y deben actualizarse o volver a crear.</span><span class="sxs-lookup"><span data-stu-id="0d229-105">Contains the time at which the search folder container will be stale and should be updated or recreated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0d229-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0d229-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0d229-107">PR_WB_SF_EXPIRATION</span><span class="sxs-lookup"><span data-stu-id="0d229-107">PR_WB_SF_EXPIRATION</span></span>  <br/> |
|<span data-ttu-id="0d229-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0d229-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0d229-109">0x683A</span><span class="sxs-lookup"><span data-stu-id="0d229-109">0x683A</span></span>  <br/> |
|<span data-ttu-id="0d229-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0d229-110">Data type:</span></span>  <br/> |<span data-ttu-id="0d229-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0d229-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0d229-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0d229-112">Area:</span></span>  <br/> |<span data-ttu-id="0d229-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="0d229-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d229-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0d229-114">Remarks</span></span>

<span data-ttu-id="0d229-115">Esta propiedad debe tener el formato como el número de minutos transcurridos desde la medianoche hora Universal coordinada (UTC) del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="0d229-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0d229-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d229-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0d229-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0d229-117">Protocol specifications</span></span>

<span data-ttu-id="0d229-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d229-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d229-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0d229-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0d229-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d229-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d229-121">Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="0d229-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0d229-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0d229-122">Header files</span></span>

<span data-ttu-id="0d229-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d229-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="0d229-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0d229-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="0d229-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0d229-125">Mapitags.h</span></span>
  
> <span data-ttu-id="0d229-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0d229-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0d229-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="0d229-127">See also</span></span>



[<span data-ttu-id="0d229-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0d229-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0d229-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0d229-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0d229-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0d229-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0d229-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="0d229-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

