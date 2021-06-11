---
title: Propiedad canónica PidTagScheduleInfoFreeBusyMerged
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyMerged
api_type:
- COM
ms.assetid: 3ebfccb6-967a-4f8e-9d94-94c50ba65438
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8d15c6cb256fb1e80e3c94bdfe7e71bd8625aa35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338720"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a><span data-ttu-id="7df59-103">Propiedad canónica PidTagScheduleInfoFreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="7df59-103">PidTagScheduleInfoFreeBusyMerged Canonical Property</span></span>

  
  
<span data-ttu-id="7df59-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7df59-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7df59-105">Contiene las horas para las que el estado de disponibilidad está establecido en ocupado u OOF.</span><span class="sxs-lookup"><span data-stu-id="7df59-105">Contains the times for which the free/busy status is set to busy or OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7df59-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7df59-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7df59-107">PR_SCHDINFO_FREEBUSY_MERGED</span><span class="sxs-lookup"><span data-stu-id="7df59-107">PR_SCHDINFO_FREEBUSY_MERGED</span></span>  <br/> |
|<span data-ttu-id="7df59-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7df59-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7df59-109">0x6850</span><span class="sxs-lookup"><span data-stu-id="7df59-109">0x6850</span></span>  <br/> |
|<span data-ttu-id="7df59-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7df59-110">Data type:</span></span>  <br/> |<span data-ttu-id="7df59-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="7df59-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="7df59-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7df59-112">Area:</span></span>  <br/> |<span data-ttu-id="7df59-113">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="7df59-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7df59-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7df59-114">Remarks</span></span>

<span data-ttu-id="7df59-115">Los eventos de tipo de disponibilidad provisional no se incluyen en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="7df59-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="7df59-116">El formato, el cálculo y las restricciones de esta propiedad son los mismos que los de PR_SCHDINFO_FREEBUSY_TENTATIVE ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), pero hacen referencia **a** citas marcadas como OOF o ocupados en el calendario asociado.</span><span class="sxs-lookup"><span data-stu-id="7df59-116">The format, computation and the restrictions of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF or busy on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7df59-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7df59-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7df59-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="7df59-118">Protocol specifications</span></span>

<span data-ttu-id="7df59-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7df59-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7df59-120">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="7df59-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7df59-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7df59-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7df59-122">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="7df59-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7df59-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7df59-123">Header files</span></span>

<span data-ttu-id="7df59-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7df59-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="7df59-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7df59-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="7df59-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7df59-126">Mapitags.h</span></span>
  
> <span data-ttu-id="7df59-127">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7df59-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7df59-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7df59-128">See also</span></span>



[<span data-ttu-id="7df59-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7df59-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7df59-130">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7df59-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7df59-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7df59-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7df59-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7df59-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

