---
title: Propiedad canónico PidTagScheduleInfoFreeBusyMerged
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 0e1fbab53589a4ebf8681d5fe738ad625d31c18f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820222"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a><span data-ttu-id="64667-103">Propiedad canónico PidTagScheduleInfoFreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="64667-103">PidTagScheduleInfoFreeBusyMerged Canonical Property</span></span>

  
  
<span data-ttu-id="64667-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="64667-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="64667-105">Contiene las horas para la que se establece el estado de disponibilidad a ocupado o fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="64667-105">Contains the times for which the free/busy status is set to busy or OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64667-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="64667-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64667-107">PR_SCHDINFO_FREEBUSY_MERGED</span><span class="sxs-lookup"><span data-stu-id="64667-107">PR_SCHDINFO_FREEBUSY_MERGED</span></span>  <br/> |
|<span data-ttu-id="64667-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="64667-108">Identifier:</span></span>  <br/> |<span data-ttu-id="64667-109">0x6850</span><span class="sxs-lookup"><span data-stu-id="64667-109">0x6850</span></span>  <br/> |
|<span data-ttu-id="64667-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="64667-110">Data type:</span></span>  <br/> |<span data-ttu-id="64667-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="64667-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="64667-112">Área:</span><span class="sxs-lookup"><span data-stu-id="64667-112">Area:</span></span>  <br/> |<span data-ttu-id="64667-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="64667-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64667-114">Notas</span><span class="sxs-lookup"><span data-stu-id="64667-114">Remarks</span></span>

<span data-ttu-id="64667-115">Eventos de tipo de libre/ocupado provisional no se incluyen en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="64667-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="64667-116">El formato, cálculo y las restricciones de esta propiedad son los mismos que los de **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) pero hacer referencia a las citas que están marcadas OOF u ocupado en el calendario asociado.</span><span class="sxs-lookup"><span data-stu-id="64667-116">The format, computation and the restrictions of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF or busy on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="64667-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="64667-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64667-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="64667-118">Protocol specifications</span></span>

<span data-ttu-id="64667-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64667-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64667-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="64667-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="64667-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64667-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64667-122">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="64667-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64667-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="64667-123">Header files</span></span>

<span data-ttu-id="64667-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64667-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="64667-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="64667-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="64667-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="64667-126">Mapitags.h</span></span>
  
> <span data-ttu-id="64667-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="64667-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64667-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="64667-128">See also</span></span>



[<span data-ttu-id="64667-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="64667-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64667-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="64667-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64667-131">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="64667-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64667-132">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="64667-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

