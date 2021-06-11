---
title: Propiedad canónica PidTagReportDisposition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 56b9e7bd-eece-4264-8ee5-a1bcbec4f35c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dae31959cddad7ad61ea32f2372ea34bdbff658e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423709"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="338cb-103">Propiedad canónica PidTagReportDisposition</span><span class="sxs-lookup"><span data-stu-id="338cb-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="338cb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="338cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="338cb-105">Indica el estado de recepción de los mensajes que solicitan recibos.</span><span class="sxs-lookup"><span data-stu-id="338cb-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="338cb-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="338cb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="338cb-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="338cb-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="338cb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="338cb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="338cb-109">0x0080</span><span class="sxs-lookup"><span data-stu-id="338cb-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="338cb-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="338cb-110">Data type:</span></span>  <br/> |<span data-ttu-id="338cb-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="338cb-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="338cb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="338cb-112">Area:</span></span>  <br/> |<span data-ttu-id="338cb-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="338cb-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="338cb-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="338cb-114">Remarks</span></span>

<span data-ttu-id="338cb-115">Los valores válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="338cb-115">The following are valid values:</span></span>
  
- <span data-ttu-id="338cb-116">"eliminado"</span><span class="sxs-lookup"><span data-stu-id="338cb-116">"deleted"</span></span>
    
- <span data-ttu-id="338cb-117">"procesado"</span><span class="sxs-lookup"><span data-stu-id="338cb-117">"processed"</span></span>
    
- <span data-ttu-id="338cb-118">"despachado"</span><span class="sxs-lookup"><span data-stu-id="338cb-118">"dispatched"</span></span>
    
- <span data-ttu-id="338cb-119">"denegado"</span><span class="sxs-lookup"><span data-stu-id="338cb-119">"denied"</span></span>
    
- <span data-ttu-id="338cb-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="338cb-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="338cb-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="338cb-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="338cb-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="338cb-122">Protocol specifications</span></span>

<span data-ttu-id="338cb-123">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="338cb-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="338cb-124">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="338cb-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="338cb-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="338cb-125">Header files</span></span>

<span data-ttu-id="338cb-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="338cb-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="338cb-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="338cb-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="338cb-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="338cb-128">Mapitags.h</span></span>
  
> <span data-ttu-id="338cb-129">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="338cb-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="338cb-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="338cb-130">See also</span></span>



[<span data-ttu-id="338cb-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="338cb-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="338cb-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="338cb-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="338cb-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="338cb-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="338cb-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="338cb-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

