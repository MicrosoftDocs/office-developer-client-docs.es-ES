---
title: Propiedad canónica PidTagScheduleInfoFreeBusyBusy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyBusy
api_type:
- COM
ms.assetid: 84d9c5b5-e734-4c07-b4cc-1d7b13c1ed19
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4fbf0d8b80fdb48e44480b2739a71aec43b88a05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338657"
---
# <a name="pidtagscheduleinfofreebusybusy-canonical-property"></a><span data-ttu-id="c35e3-103">Propiedad canónica PidTagScheduleInfoFreeBusyBusy</span><span class="sxs-lookup"><span data-stu-id="c35e3-103">PidTagScheduleInfoFreeBusyBusy Canonical Property</span></span>

  
  
<span data-ttu-id="c35e3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c35e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c35e3-105">Contiene los bloques de tiempo durante los que el estado está ocupado.</span><span class="sxs-lookup"><span data-stu-id="c35e3-105">Contains the blocks of time for which the status is busy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c35e3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c35e3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c35e3-107">PR_SCHDINFO_FREEBUSY_BUSY</span><span class="sxs-lookup"><span data-stu-id="c35e3-107">PR_SCHDINFO_FREEBUSY_BUSY</span></span>  <br/> |
|<span data-ttu-id="c35e3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c35e3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c35e3-109">0x6854</span><span class="sxs-lookup"><span data-stu-id="c35e3-109">0x6854</span></span>  <br/> |
|<span data-ttu-id="c35e3-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c35e3-110">Data type:</span></span>  <br/> |<span data-ttu-id="c35e3-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="c35e3-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="c35e3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c35e3-112">Area:</span></span>  <br/> |<span data-ttu-id="c35e3-113">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="c35e3-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c35e3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c35e3-114">Remarks</span></span>

<span data-ttu-id="c35e3-115">El formato, el cálculo y las restricciones de esta propiedad son los mismos que los de PR_SCHDINFO_FREEBUSY_TENTATIVE ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), pero hacen referencia **a** citas marcadas como ocupadas en el objeto de calendario asociado.</span><span class="sxs-lookup"><span data-stu-id="c35e3-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c35e3-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c35e3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c35e3-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="c35e3-117">Protocol specifications</span></span>

<span data-ttu-id="c35e3-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c35e3-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c35e3-119">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="c35e3-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c35e3-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c35e3-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c35e3-121">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="c35e3-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c35e3-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c35e3-122">Header files</span></span>

<span data-ttu-id="c35e3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c35e3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c35e3-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c35e3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c35e3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c35e3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c35e3-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c35e3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c35e3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c35e3-127">See also</span></span>



[<span data-ttu-id="c35e3-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c35e3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c35e3-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c35e3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c35e3-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c35e3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c35e3-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="c35e3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

