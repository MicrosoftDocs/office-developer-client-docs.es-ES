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
ms.openlocfilehash: 7ff6df6eddc8e610341cb09ccb152f4ad748a984
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336536"
---
# <a name="pidtagsearchfolderlastused-canonical-property"></a><span data-ttu-id="d9779-103">Propiedad canónica PidTagSearchFolderLastUsed</span><span class="sxs-lookup"><span data-stu-id="d9779-103">PidTagSearchFolderLastUsed Canonical Property</span></span>

  
  
<span data-ttu-id="d9779-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9779-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9779-105">Representa la última vez que se tuvo acceso a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d9779-105">Represents the last time the folder was accessed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9779-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d9779-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9779-107">PR_WB_SF_LAST_USED</span><span class="sxs-lookup"><span data-stu-id="d9779-107">PR_WB_SF_LAST_USED</span></span>  <br/> |
|<span data-ttu-id="d9779-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d9779-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d9779-109">0x6834</span><span class="sxs-lookup"><span data-stu-id="d9779-109">0x6834</span></span>  <br/> |
|<span data-ttu-id="d9779-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d9779-110">Data type:</span></span>  <br/> |<span data-ttu-id="d9779-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d9779-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d9779-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d9779-112">Area:</span></span>  <br/> |<span data-ttu-id="d9779-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="d9779-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9779-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d9779-114">Remarks</span></span>

<span data-ttu-id="d9779-115">Esta propiedad debe tener el formato de número de minutos desde la medianoche hora universal coordinada (UTC) del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="d9779-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d9779-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9779-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9779-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="d9779-117">Protocol specifications</span></span>

<span data-ttu-id="d9779-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9779-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9779-119">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="d9779-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d9779-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9779-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9779-121">Especifica las propiedades y las operaciones para manipular una configuración de lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d9779-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9779-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d9779-122">Header files</span></span>

<span data-ttu-id="d9779-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9779-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9779-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d9779-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d9779-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d9779-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d9779-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d9779-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9779-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d9779-127">See also</span></span>



[<span data-ttu-id="d9779-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d9779-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9779-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="d9779-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9779-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d9779-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9779-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="d9779-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

