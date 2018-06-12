---
title: Propiedad canónico PidTagScheduleInfoFreeBusyBusy
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: e0c59b569f4f01584fd65a7c3e13d6daac69d8a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820225"
---
# <a name="pidtagscheduleinfofreebusybusy-canonical-property"></a><span data-ttu-id="4a0d0-103">Propiedad canónico PidTagScheduleInfoFreeBusyBusy</span><span class="sxs-lookup"><span data-stu-id="4a0d0-103">PidTagScheduleInfoFreeBusyBusy Canonical Property</span></span>

  
  
<span data-ttu-id="4a0d0-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a0d0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a0d0-105">Contiene los bloques de tiempo para la que el estado es no disponible.</span><span class="sxs-lookup"><span data-stu-id="4a0d0-105">Contains the blocks of time for which the status is busy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a0d0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4a0d0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a0d0-107">PR_SCHDINFO_FREEBUSY_BUSY</span><span class="sxs-lookup"><span data-stu-id="4a0d0-107">PR_SCHDINFO_FREEBUSY_BUSY</span></span>  <br/> |
|<span data-ttu-id="4a0d0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4a0d0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a0d0-109">0x6854</span><span class="sxs-lookup"><span data-stu-id="4a0d0-109">0x6854</span></span>  <br/> |
|<span data-ttu-id="4a0d0-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4a0d0-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a0d0-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="4a0d0-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="4a0d0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4a0d0-112">Area:</span></span>  <br/> |<span data-ttu-id="4a0d0-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="4a0d0-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a0d0-114">Notas</span><span class="sxs-lookup"><span data-stu-id="4a0d0-114">Remarks</span></span>

<span data-ttu-id="4a0d0-115">El formato, el cálculo y las restricciones de esta propiedad son los mismos que los de **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) pero hacer referencia a las citas que están marcadas ocupadas en el objeto de calendario asociado.</span><span class="sxs-lookup"><span data-stu-id="4a0d0-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4a0d0-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a0d0-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a0d0-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="4a0d0-117">Protocol specifications</span></span>

<span data-ttu-id="4a0d0-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a0d0-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a0d0-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4a0d0-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a0d0-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a0d0-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a0d0-121">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="4a0d0-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a0d0-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4a0d0-122">Header files</span></span>

<span data-ttu-id="4a0d0-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a0d0-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a0d0-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4a0d0-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a0d0-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4a0d0-125">Mapitags.h</span></span>
  
> <span data-ttu-id="4a0d0-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4a0d0-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a0d0-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="4a0d0-127">See also</span></span>



[<span data-ttu-id="4a0d0-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4a0d0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a0d0-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4a0d0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a0d0-130">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="4a0d0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a0d0-131">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4a0d0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

