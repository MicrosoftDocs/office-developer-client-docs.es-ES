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
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="2bb7e-103">Propiedad canónica PidTagReportDisposition</span><span class="sxs-lookup"><span data-stu-id="2bb7e-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="2bb7e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2bb7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2bb7e-105">Indica el estado de recepción de los mensajes que solicitan confirmaciones.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2bb7e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2bb7e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2bb7e-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="2bb7e-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="2bb7e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2bb7e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2bb7e-109">0x0080</span><span class="sxs-lookup"><span data-stu-id="2bb7e-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="2bb7e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2bb7e-110">Data type:</span></span>  <br/> |<span data-ttu-id="2bb7e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2bb7e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2bb7e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2bb7e-112">Area:</span></span>  <br/> |<span data-ttu-id="2bb7e-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="2bb7e-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2bb7e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2bb7e-114">Remarks</span></span>

<span data-ttu-id="2bb7e-115">Los valores válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2bb7e-115">The following are valid values:</span></span>
  
- <span data-ttu-id="2bb7e-116">eliminados</span><span class="sxs-lookup"><span data-stu-id="2bb7e-116">"deleted"</span></span>
    
- <span data-ttu-id="2bb7e-117">procesan</span><span class="sxs-lookup"><span data-stu-id="2bb7e-117">"processed"</span></span>
    
- <span data-ttu-id="2bb7e-118">envían</span><span class="sxs-lookup"><span data-stu-id="2bb7e-118">"dispatched"</span></span>
    
- <span data-ttu-id="2bb7e-119">denegado</span><span class="sxs-lookup"><span data-stu-id="2bb7e-119">"denied"</span></span>
    
- <span data-ttu-id="2bb7e-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="2bb7e-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="2bb7e-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2bb7e-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2bb7e-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="2bb7e-122">Protocol specifications</span></span>

<span data-ttu-id="2bb7e-123">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="2bb7e-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="2bb7e-124">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2bb7e-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2bb7e-125">Header files</span></span>

<span data-ttu-id="2bb7e-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2bb7e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2bb7e-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="2bb7e-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2bb7e-128">Mapitags.h</span></span>
  
> <span data-ttu-id="2bb7e-129">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2bb7e-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="2bb7e-130">See also</span></span>



[<span data-ttu-id="2bb7e-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2bb7e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2bb7e-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="2bb7e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2bb7e-133">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2bb7e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2bb7e-134">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2bb7e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

