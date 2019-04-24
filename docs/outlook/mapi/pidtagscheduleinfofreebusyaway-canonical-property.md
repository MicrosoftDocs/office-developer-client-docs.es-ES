---
title: Propiedad canónica PidTagScheduleInfoFreeBusyAway
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyAway
api_type:
- COM
ms.assetid: 7b5d013a-15ac-469a-98c8-3ed1e80f6faf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7520c473ee9373f8c23c4f5b4bb020291e2be007
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338510"
---
# <a name="pidtagscheduleinfofreebusyaway-canonical-property"></a><span data-ttu-id="97a31-103">Propiedad canónica PidTagScheduleInfoFreeBusyAway</span><span class="sxs-lookup"><span data-stu-id="97a31-103">PidTagScheduleInfoFreeBusyAway Canonical Property</span></span>

  
  
<span data-ttu-id="97a31-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97a31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97a31-105">Contiene las horas en las que se establece el estado de disponibilidad en OOF.</span><span class="sxs-lookup"><span data-stu-id="97a31-105">Contains the times for which the free/busy status is set to OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97a31-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="97a31-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="97a31-107">PR_SCHDINFO_FREEBUSY_OOF</span><span class="sxs-lookup"><span data-stu-id="97a31-107">PR_SCHDINFO_FREEBUSY_OOF</span></span>  <br/> |
|<span data-ttu-id="97a31-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="97a31-108">Identifier:</span></span>  <br/> |<span data-ttu-id="97a31-109">0x6856</span><span class="sxs-lookup"><span data-stu-id="97a31-109">0x6856</span></span>  <br/> |
|<span data-ttu-id="97a31-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="97a31-110">Data type:</span></span>  <br/> |<span data-ttu-id="97a31-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="97a31-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="97a31-112">Área:</span><span class="sxs-lookup"><span data-stu-id="97a31-112">Area:</span></span>  <br/> |<span data-ttu-id="97a31-113">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="97a31-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97a31-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97a31-114">Remarks</span></span>

<span data-ttu-id="97a31-115">El formato, las computaciones y las restricciones de esta propiedad son los mismos que los de **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), pero hacen referencia a las citas que están marcadas como OOF en el calendario asociado.</span><span class="sxs-lookup"><span data-stu-id="97a31-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="97a31-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="97a31-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="97a31-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="97a31-117">Protocol specifications</span></span>

<span data-ttu-id="97a31-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97a31-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97a31-119">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="97a31-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="97a31-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97a31-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97a31-121">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="97a31-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="97a31-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="97a31-122">Header files</span></span>

<span data-ttu-id="97a31-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="97a31-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="97a31-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="97a31-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="97a31-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="97a31-125">Mapitags.h</span></span>
  
> <span data-ttu-id="97a31-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="97a31-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97a31-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="97a31-127">See also</span></span>



[<span data-ttu-id="97a31-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="97a31-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97a31-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="97a31-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97a31-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="97a31-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97a31-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="97a31-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

