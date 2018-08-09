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
ms.openlocfilehash: 293e8648374b61784f5bda0db124506f345b2701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820236"
---
# <a name="pidtagscheduleinfomonthsbusy-canonical-property"></a><span data-ttu-id="b7331-103">Propiedad canónica PidTagScheduleInfoMonthsBusy</span><span class="sxs-lookup"><span data-stu-id="b7331-103">PidTagScheduleInfoMonthsBusy Canonical Property</span></span>

  
  
<span data-ttu-id="b7331-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7331-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7331-105">Contiene los meses para el que están presentes en el mensaje de libre/ocupado datos de disponibilidad de tipo ocupado.</span><span class="sxs-lookup"><span data-stu-id="b7331-105">Contains the months for which free/busy data of type busy is present in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7331-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b7331-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7331-107">PR_SCHDINFO_MONTHS_BUSY</span><span class="sxs-lookup"><span data-stu-id="b7331-107">PR_SCHDINFO_MONTHS_BUSY</span></span>  <br/> |
|<span data-ttu-id="b7331-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b7331-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b7331-109">0x6853</span><span class="sxs-lookup"><span data-stu-id="b7331-109">0x6853</span></span>  <br/> |
|<span data-ttu-id="b7331-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b7331-110">Data type:</span></span>  <br/> |<span data-ttu-id="b7331-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="b7331-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="b7331-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b7331-112">Area:</span></span>  <br/> |<span data-ttu-id="b7331-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="b7331-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7331-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b7331-114">Remarks</span></span>

<span data-ttu-id="b7331-115">El formato, el cálculo y las restricciones de esta propiedad son los mismos que los de **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) pero hacer referencia a las citas que están marcadas ocupadas en el objeto de calendario asociado.</span><span class="sxs-lookup"><span data-stu-id="b7331-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b7331-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7331-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7331-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b7331-117">Protocol specifications</span></span>

<span data-ttu-id="b7331-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7331-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7331-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b7331-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b7331-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7331-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7331-121">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="b7331-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b7331-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b7331-122">Header files</span></span>

<span data-ttu-id="b7331-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7331-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7331-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b7331-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b7331-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b7331-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b7331-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="b7331-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7331-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7331-127">See also</span></span>



[<span data-ttu-id="b7331-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b7331-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7331-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b7331-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7331-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b7331-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7331-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="b7331-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

