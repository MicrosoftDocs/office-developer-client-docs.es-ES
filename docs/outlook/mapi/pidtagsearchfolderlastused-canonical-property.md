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
# <a name="pidtagsearchfolderlastused-canonical-property"></a><span data-ttu-id="c7177-103">Propiedad canónica PidTagSearchFolderLastUsed</span><span class="sxs-lookup"><span data-stu-id="c7177-103">PidTagSearchFolderLastUsed Canonical Property</span></span>

  
  
<span data-ttu-id="c7177-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7177-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7177-105">Representa la última vez que se tuvo acceso a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="c7177-105">Represents the last time the folder was accessed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c7177-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c7177-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c7177-107">PR_WB_SF_LAST_USED</span><span class="sxs-lookup"><span data-stu-id="c7177-107">PR_WB_SF_LAST_USED</span></span>  <br/> |
|<span data-ttu-id="c7177-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c7177-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c7177-109">0x6834</span><span class="sxs-lookup"><span data-stu-id="c7177-109">0x6834</span></span>  <br/> |
|<span data-ttu-id="c7177-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c7177-110">Data type:</span></span>  <br/> |<span data-ttu-id="c7177-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c7177-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c7177-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c7177-112">Area:</span></span>  <br/> |<span data-ttu-id="c7177-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="c7177-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7177-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c7177-114">Remarks</span></span>

<span data-ttu-id="c7177-115">Esta propiedad debe tener el formato de número de minutos desde la medianoche hora universal coordinada (UTC) 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="c7177-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c7177-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7177-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c7177-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="c7177-117">Protocol specifications</span></span>

<span data-ttu-id="c7177-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7177-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7177-119">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="c7177-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c7177-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7177-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7177-121">Especifica las propiedades y las operaciones para manipular una configuración de lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c7177-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c7177-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c7177-122">Header files</span></span>

<span data-ttu-id="c7177-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c7177-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c7177-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c7177-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c7177-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c7177-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c7177-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c7177-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7177-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7177-127">See also</span></span>



[<span data-ttu-id="c7177-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c7177-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c7177-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c7177-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c7177-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c7177-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c7177-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="c7177-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

