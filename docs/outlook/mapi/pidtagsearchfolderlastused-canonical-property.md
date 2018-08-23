---
title: Propiedad canónica PidTagSearchFolderLastUsed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderLastUsed
api_type:
- COM
ms.assetid: e4071307-6205-4079-ab65-7499d14f145c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6cafa336bf915abd35de07a11ee65baf9ac4d69f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572693"
---
# <a name="pidtagsearchfolderlastused-canonical-property"></a><span data-ttu-id="97a05-103">Propiedad canónica PidTagSearchFolderLastUsed</span><span class="sxs-lookup"><span data-stu-id="97a05-103">PidTagSearchFolderLastUsed Canonical Property</span></span>

  
  
<span data-ttu-id="97a05-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97a05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97a05-105">Representa la última vez que se obtiene acceso a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="97a05-105">Represents the last time the folder was accessed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97a05-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="97a05-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="97a05-107">PR_WB_SF_LAST_USED</span><span class="sxs-lookup"><span data-stu-id="97a05-107">PR_WB_SF_LAST_USED</span></span>  <br/> |
|<span data-ttu-id="97a05-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="97a05-108">Identifier:</span></span>  <br/> |<span data-ttu-id="97a05-109">0x6834</span><span class="sxs-lookup"><span data-stu-id="97a05-109">0x6834</span></span>  <br/> |
|<span data-ttu-id="97a05-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="97a05-110">Data type:</span></span>  <br/> |<span data-ttu-id="97a05-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="97a05-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="97a05-112">Área:</span><span class="sxs-lookup"><span data-stu-id="97a05-112">Area:</span></span>  <br/> |<span data-ttu-id="97a05-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="97a05-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97a05-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97a05-114">Remarks</span></span>

<span data-ttu-id="97a05-115">Esta propiedad debe tener el formato como el número de minutos transcurridos desde la medianoche hora Universal coordinada (UTC) del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="97a05-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="97a05-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="97a05-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="97a05-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="97a05-117">Protocol specifications</span></span>

<span data-ttu-id="97a05-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97a05-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97a05-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="97a05-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="97a05-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97a05-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97a05-121">Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="97a05-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="97a05-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="97a05-122">Header files</span></span>

<span data-ttu-id="97a05-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97a05-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="97a05-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="97a05-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="97a05-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="97a05-125">Mapitags.h</span></span>
  
> <span data-ttu-id="97a05-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="97a05-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97a05-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="97a05-127">See also</span></span>



[<span data-ttu-id="97a05-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="97a05-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97a05-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="97a05-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97a05-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="97a05-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97a05-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="97a05-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

