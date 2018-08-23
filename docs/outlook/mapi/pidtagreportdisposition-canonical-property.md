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
ms.openlocfilehash: 1e84308f3a9f9457c5db23c1ad9d42d6e856519e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583634"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="8796c-103">Propiedad canónica PidTagReportDisposition</span><span class="sxs-lookup"><span data-stu-id="8796c-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="8796c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8796c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8796c-105">Indica el estado de los mensajes que solicitar confirmaciones de recibo.</span><span class="sxs-lookup"><span data-stu-id="8796c-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8796c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8796c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8796c-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="8796c-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="8796c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8796c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8796c-109">0 x 0080</span><span class="sxs-lookup"><span data-stu-id="8796c-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="8796c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8796c-110">Data type:</span></span>  <br/> |<span data-ttu-id="8796c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8796c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8796c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8796c-112">Area:</span></span>  <br/> |<span data-ttu-id="8796c-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="8796c-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8796c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8796c-114">Remarks</span></span>

<span data-ttu-id="8796c-115">Los valores válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8796c-115">The following are valid values:</span></span>
  
- <span data-ttu-id="8796c-116">"eliminar"</span><span class="sxs-lookup"><span data-stu-id="8796c-116">"deleted"</span></span>
    
- <span data-ttu-id="8796c-117">"procesar"</span><span class="sxs-lookup"><span data-stu-id="8796c-117">"processed"</span></span>
    
- <span data-ttu-id="8796c-118">"distribuye"</span><span class="sxs-lookup"><span data-stu-id="8796c-118">"dispatched"</span></span>
    
- <span data-ttu-id="8796c-119">"denegado"</span><span class="sxs-lookup"><span data-stu-id="8796c-119">"denied"</span></span>
    
- <span data-ttu-id="8796c-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="8796c-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="8796c-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8796c-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8796c-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8796c-122">Protocol specifications</span></span>

<span data-ttu-id="8796c-123">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="8796c-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="8796c-124">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8796c-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8796c-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8796c-125">Header files</span></span>

<span data-ttu-id="8796c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8796c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="8796c-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8796c-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="8796c-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8796c-128">Mapitags.h</span></span>
  
> <span data-ttu-id="8796c-129">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="8796c-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8796c-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8796c-130">See also</span></span>



[<span data-ttu-id="8796c-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8796c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8796c-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="8796c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8796c-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8796c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8796c-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="8796c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

