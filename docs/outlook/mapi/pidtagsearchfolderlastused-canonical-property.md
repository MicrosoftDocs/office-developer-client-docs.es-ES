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
ms.openlocfilehash: b90639675fa566a83dd78c6ac250f743d68480e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820241"
---
# <a name="pidtagsearchfolderlastused-canonical-property"></a><span data-ttu-id="ea9f4-103">Propiedad canónica PidTagSearchFolderLastUsed</span><span class="sxs-lookup"><span data-stu-id="ea9f4-103">PidTagSearchFolderLastUsed Canonical Property</span></span>

  
  
<span data-ttu-id="ea9f4-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ea9f4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ea9f4-105">Representa la última vez que se obtiene acceso a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="ea9f4-105">Represents the last time the folder was accessed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ea9f4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ea9f4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ea9f4-107">PR_WB_SF_LAST_USED</span><span class="sxs-lookup"><span data-stu-id="ea9f4-107">PR_WB_SF_LAST_USED</span></span>  <br/> |
|<span data-ttu-id="ea9f4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ea9f4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ea9f4-109">0x6834</span><span class="sxs-lookup"><span data-stu-id="ea9f4-109">0x6834</span></span>  <br/> |
|<span data-ttu-id="ea9f4-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ea9f4-110">Data type:</span></span>  <br/> |<span data-ttu-id="ea9f4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ea9f4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ea9f4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ea9f4-112">Area:</span></span>  <br/> |<span data-ttu-id="ea9f4-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="ea9f4-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea9f4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ea9f4-114">Remarks</span></span>

<span data-ttu-id="ea9f4-115">Esta propiedad debe tener el formato como el número de minutos transcurridos desde la medianoche hora Universal coordinada (UTC) del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="ea9f4-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ea9f4-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea9f4-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ea9f4-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="ea9f4-117">Protocol specifications</span></span>

<span data-ttu-id="ea9f4-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea9f4-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea9f4-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ea9f4-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ea9f4-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea9f4-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea9f4-121">Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ea9f4-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ea9f4-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ea9f4-122">Header files</span></span>

<span data-ttu-id="ea9f4-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ea9f4-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="ea9f4-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ea9f4-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="ea9f4-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ea9f4-125">Mapitags.h</span></span>
  
> <span data-ttu-id="ea9f4-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ea9f4-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ea9f4-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea9f4-127">See also</span></span>



[<span data-ttu-id="ea9f4-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ea9f4-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ea9f4-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="ea9f4-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ea9f4-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ea9f4-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ea9f4-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="ea9f4-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

