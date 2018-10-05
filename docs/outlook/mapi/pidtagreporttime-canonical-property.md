---
title: Propiedad canónica PidTagReportTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTime
api_type:
- COM
ms.assetid: b3646505-a9f0-4a72-8277-b238c909f66f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 298c53e537819f800a3acc5cf07c01a7b9f978ec
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387604"
---
# <a name="pidtagreporttime-canonical-property"></a><span data-ttu-id="c616d-103">Propiedad canónica PidTagReportTime</span><span class="sxs-lookup"><span data-stu-id="c616d-103">PidTagReportTime Canonical Property</span></span>

  
  
<span data-ttu-id="c616d-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c616d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c616d-105">Contiene la fecha y la hora cuando el sistema de mensajería genera un informe.</span><span class="sxs-lookup"><span data-stu-id="c616d-105">Contains the date and time when the messaging system generated a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c616d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c616d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c616d-107">PR_REPORT_TIME</span><span class="sxs-lookup"><span data-stu-id="c616d-107">PR_REPORT_TIME</span></span>  <br/> |
|<span data-ttu-id="c616d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c616d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c616d-109">0x0032</span><span class="sxs-lookup"><span data-stu-id="c616d-109">0x0032</span></span>  <br/> |
|<span data-ttu-id="c616d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c616d-110">Data type:</span></span>  <br/> |<span data-ttu-id="c616d-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c616d-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c616d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c616d-112">Area:</span></span>  <br/> |<span data-ttu-id="c616d-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="c616d-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c616d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c616d-114">Remarks</span></span>

<span data-ttu-id="c616d-115">Esta propiedad representa una propiedad por destinatario en los informes de entrega y no entrega y una propiedad de cada mensaje en informes de lectura y nonread.</span><span class="sxs-lookup"><span data-stu-id="c616d-115">This property represents a per-recipient property on delivery and nondelivery reports and a per-message property on read and nonread reports.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c616d-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c616d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c616d-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c616d-117">Protocol specifications</span></span>

<span data-ttu-id="c616d-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c616d-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c616d-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c616d-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c616d-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c616d-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c616d-121">Especifica las propiedades y operaciones que se permiten en mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c616d-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="c616d-122">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c616d-122">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c616d-123">Permite la manipulación de las listas Permitir o bloquear y la determinación de los mensajes de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="c616d-123">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c616d-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c616d-124">Header files</span></span>

<span data-ttu-id="c616d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c616d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c616d-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c616d-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c616d-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c616d-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c616d-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c616d-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c616d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c616d-129">See also</span></span>



[<span data-ttu-id="c616d-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c616d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c616d-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c616d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c616d-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c616d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c616d-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c616d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

