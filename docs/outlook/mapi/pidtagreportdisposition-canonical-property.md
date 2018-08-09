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
ms.openlocfilehash: 62d5b04086e45b6b3d2cfa960472010827d60d6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820098"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="d9c92-103">Propiedad canónica PidTagReportDisposition</span><span class="sxs-lookup"><span data-stu-id="d9c92-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="d9c92-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9c92-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9c92-105">Indica el estado de los mensajes que solicitar confirmaciones de recibo.</span><span class="sxs-lookup"><span data-stu-id="d9c92-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9c92-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d9c92-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9c92-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="d9c92-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="d9c92-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d9c92-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d9c92-109">0 x 0080</span><span class="sxs-lookup"><span data-stu-id="d9c92-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="d9c92-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d9c92-110">Data type:</span></span>  <br/> |<span data-ttu-id="d9c92-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d9c92-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d9c92-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d9c92-112">Area:</span></span>  <br/> |<span data-ttu-id="d9c92-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="d9c92-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9c92-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d9c92-114">Remarks</span></span>

<span data-ttu-id="d9c92-115">Los valores válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d9c92-115">The following are valid values:</span></span>
  
- <span data-ttu-id="d9c92-116">"eliminar"</span><span class="sxs-lookup"><span data-stu-id="d9c92-116">"deleted"</span></span>
    
- <span data-ttu-id="d9c92-117">"procesar"</span><span class="sxs-lookup"><span data-stu-id="d9c92-117">"processed"</span></span>
    
- <span data-ttu-id="d9c92-118">"distribuye"</span><span class="sxs-lookup"><span data-stu-id="d9c92-118">"dispatched"</span></span>
    
- <span data-ttu-id="d9c92-119">"denegado"</span><span class="sxs-lookup"><span data-stu-id="d9c92-119">"denied"</span></span>
    
- <span data-ttu-id="d9c92-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="d9c92-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="d9c92-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9c92-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9c92-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d9c92-122">Protocol specifications</span></span>

<span data-ttu-id="d9c92-123">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="d9c92-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="d9c92-124">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d9c92-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9c92-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d9c92-125">Header files</span></span>

<span data-ttu-id="d9c92-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9c92-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9c92-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d9c92-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="d9c92-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d9c92-128">Mapitags.h</span></span>
  
> <span data-ttu-id="d9c92-129">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="d9c92-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9c92-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9c92-130">See also</span></span>



[<span data-ttu-id="d9c92-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d9c92-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9c92-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d9c92-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9c92-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d9c92-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9c92-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d9c92-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

