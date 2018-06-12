---
title: Propiedad canónico PidTagScheduleInfoMonthsAway
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsAway
api_type:
- COM
ms.assetid: 282a8ba1-b786-4d17-b6c5-17e935e59a6b
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 6301cd86a81dfbf38666b6fb3ea326bc1f801490
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820233"
---
# <a name="pidtagscheduleinfomonthsaway-canonical-property"></a><span data-ttu-id="a3903-103">Propiedad canónico PidTagScheduleInfoMonthsAway</span><span class="sxs-lookup"><span data-stu-id="a3903-103">PidTagScheduleInfoMonthsAway Canonical Property</span></span>

  
  
<span data-ttu-id="a3903-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a3903-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a3903-105">Contiene una lista de los meses para el que están presentes en el mensaje de libre/ocupado datos de disponibilidad del tipo fuera de la oficina (OOF).</span><span class="sxs-lookup"><span data-stu-id="a3903-105">Contains a list of the months for which free/busy data of type out of office (OOF) is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3903-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a3903-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a3903-107">PR_SCHDINFO_MONTHS_OOF</span><span class="sxs-lookup"><span data-stu-id="a3903-107">PR_SCHDINFO_MONTHS_OOF</span></span>  <br/> |
|<span data-ttu-id="a3903-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a3903-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a3903-109">0x6855</span><span class="sxs-lookup"><span data-stu-id="a3903-109">0x6855</span></span>  <br/> |
|<span data-ttu-id="a3903-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a3903-110">Data type:</span></span>  <br/> |<span data-ttu-id="a3903-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="a3903-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="a3903-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a3903-112">Area:</span></span>  <br/> |<span data-ttu-id="a3903-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="a3903-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3903-114">Notas</span><span class="sxs-lookup"><span data-stu-id="a3903-114">Remarks</span></span>

<span data-ttu-id="a3903-115">El formato, el cálculo y las restricciones de esta propiedad son los mismos que los de **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) pero hacer referencia a las citas que están marcadas fuera de la oficina (OOF) en el asociado objeto Calendar.</span><span class="sxs-lookup"><span data-stu-id="a3903-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked out of office (OOF) on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a3903-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3903-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a3903-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a3903-117">Protocol specifications</span></span>

<span data-ttu-id="a3903-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3903-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3903-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a3903-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a3903-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3903-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3903-121">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="a3903-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a3903-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a3903-122">Header files</span></span>

<span data-ttu-id="a3903-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a3903-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a3903-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a3903-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a3903-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a3903-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a3903-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a3903-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a3903-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="a3903-127">See also</span></span>



[<span data-ttu-id="a3903-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a3903-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a3903-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a3903-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a3903-130">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="a3903-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a3903-131">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a3903-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

