---
title: Propiedad canónica PidTagScheduleInfoMonthsBusy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: b15447d6-89aa-40ad-93fc-21fbfa5e3d0e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 08f8f6e016ff08211bc10e80588ab33e83d6441b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359797"
---
# <a name="pidtagscheduleinfomonthsbusy-canonical-property"></a><span data-ttu-id="209d2-103">Propiedad canónica PidTagScheduleInfoMonthsBusy</span><span class="sxs-lookup"><span data-stu-id="209d2-103">PidTagScheduleInfoMonthsBusy Canonical Property</span></span>

  
  
<span data-ttu-id="209d2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="209d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="209d2-105">Contiene los meses durante los que los datos de disponibilidad del tipo ocupado están presentes en el mensaje de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="209d2-105">Contains the months for which free/busy data of type busy is present in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="209d2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="209d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="209d2-107">PR_SCHDINFO_MONTHS_BUSY</span><span class="sxs-lookup"><span data-stu-id="209d2-107">PR_SCHDINFO_MONTHS_BUSY</span></span>  <br/> |
|<span data-ttu-id="209d2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="209d2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="209d2-109">0x6853</span><span class="sxs-lookup"><span data-stu-id="209d2-109">0x6853</span></span>  <br/> |
|<span data-ttu-id="209d2-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="209d2-110">Data type:</span></span>  <br/> |<span data-ttu-id="209d2-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="209d2-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="209d2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="209d2-112">Area:</span></span>  <br/> |<span data-ttu-id="209d2-113">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="209d2-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="209d2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="209d2-114">Remarks</span></span>

<span data-ttu-id="209d2-115">El formato, el cálculo y las restricciones de esta propiedad son los mismos que los de **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)), pero hacen referencia a citas marcadas como ocupadas en el objeto de calendario asociado.</span><span class="sxs-lookup"><span data-stu-id="209d2-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="209d2-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="209d2-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="209d2-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="209d2-117">Protocol specifications</span></span>

<span data-ttu-id="209d2-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="209d2-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="209d2-119">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="209d2-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="209d2-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="209d2-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="209d2-121">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="209d2-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="209d2-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="209d2-122">Header files</span></span>

<span data-ttu-id="209d2-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="209d2-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="209d2-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="209d2-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="209d2-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="209d2-125">Mapitags.h</span></span>
  
> <span data-ttu-id="209d2-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="209d2-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="209d2-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="209d2-127">See also</span></span>



[<span data-ttu-id="209d2-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="209d2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="209d2-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="209d2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="209d2-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="209d2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="209d2-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="209d2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

