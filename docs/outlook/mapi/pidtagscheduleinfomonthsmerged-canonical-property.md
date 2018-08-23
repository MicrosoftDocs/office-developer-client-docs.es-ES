---
title: Propiedad canónica PidTagScheduleInfoMonthsMerged
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsMerged
api_type:
- COM
ms.assetid: b13b5d7b-413e-4405-8a35-0422477a9e86
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6de470a284b91126854a0c1324f5665fd72868ef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577355"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a><span data-ttu-id="dda3c-103">Propiedad canónica PidTagScheduleInfoMonthsMerged</span><span class="sxs-lookup"><span data-stu-id="dda3c-103">PidTagScheduleInfoMonthsMerged Canonical Property</span></span>

  
  
<span data-ttu-id="dda3c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dda3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dda3c-105">Contiene una lista de los meses para los datos de libre/ocupado de tipo ocupado o un fuera de oficina (OOF) mensaje está presente en el mensaje de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="dda3c-105">Contains a list of the months for which free/busy data of type busy or an out of office (OOF) message is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dda3c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="dda3c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dda3c-107">PR_SCHDINFO_MONTHS_MERGED</span><span class="sxs-lookup"><span data-stu-id="dda3c-107">PR_SCHDINFO_MONTHS_MERGED</span></span>  <br/> |
|<span data-ttu-id="dda3c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dda3c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dda3c-109">0x684F</span><span class="sxs-lookup"><span data-stu-id="dda3c-109">0x684F</span></span>  <br/> |
|<span data-ttu-id="dda3c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="dda3c-110">Data type:</span></span>  <br/> |<span data-ttu-id="dda3c-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="dda3c-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="dda3c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dda3c-112">Area:</span></span>  <br/> |<span data-ttu-id="dda3c-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="dda3c-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dda3c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dda3c-114">Remarks</span></span>

<span data-ttu-id="dda3c-115">Eventos de tipo de libre/ocupado provisional no se incluyen en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="dda3c-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="dda3c-116">La sintaxis y formato y restricciones de esta propiedad son los mismos que los de **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) pero hacer referencia a las citas que están marcadas OOF o no disponible en el objeto de calendario asociado.</span><span class="sxs-lookup"><span data-stu-id="dda3c-116">The syntax/format and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked OOF or Busy on the associated calendar object.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dda3c-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dda3c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dda3c-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="dda3c-118">Protocol specifications</span></span>

<span data-ttu-id="dda3c-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dda3c-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dda3c-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="dda3c-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dda3c-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dda3c-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dda3c-122">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="dda3c-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dda3c-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="dda3c-123">Header files</span></span>

<span data-ttu-id="dda3c-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dda3c-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="dda3c-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="dda3c-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="dda3c-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dda3c-126">Mapitags.h</span></span>
  
> <span data-ttu-id="dda3c-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="dda3c-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dda3c-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="dda3c-128">See also</span></span>



[<span data-ttu-id="dda3c-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dda3c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dda3c-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="dda3c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dda3c-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="dda3c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dda3c-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="dda3c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

