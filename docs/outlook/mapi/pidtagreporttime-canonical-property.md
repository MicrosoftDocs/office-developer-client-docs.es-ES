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
ms.openlocfilehash: 4efe68745c10521de243677c10a9ca32debd7122
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577803"
---
# <a name="pidtagreporttime-canonical-property"></a><span data-ttu-id="d1036-103">Propiedad canónica PidTagReportTime</span><span class="sxs-lookup"><span data-stu-id="d1036-103">PidTagReportTime Canonical Property</span></span>

  
  
<span data-ttu-id="d1036-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1036-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1036-105">Contiene la fecha y la hora cuando el sistema de mensajería genera un informe.</span><span class="sxs-lookup"><span data-stu-id="d1036-105">Contains the date and time when the messaging system generated a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1036-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d1036-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1036-107">PR_REPORT_TIME</span><span class="sxs-lookup"><span data-stu-id="d1036-107">PR_REPORT_TIME</span></span>  <br/> |
|<span data-ttu-id="d1036-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d1036-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d1036-109">0x0032</span><span class="sxs-lookup"><span data-stu-id="d1036-109">0x0032</span></span>  <br/> |
|<span data-ttu-id="d1036-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d1036-110">Data type:</span></span>  <br/> |<span data-ttu-id="d1036-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d1036-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d1036-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d1036-112">Area:</span></span>  <br/> |<span data-ttu-id="d1036-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="d1036-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1036-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d1036-114">Remarks</span></span>

<span data-ttu-id="d1036-115">Esta propiedad representa una propiedad por destinatario en los informes de entrega y no entrega y una propiedad de cada mensaje en informes de lectura y nonread.</span><span class="sxs-lookup"><span data-stu-id="d1036-115">This property represents a per-recipient property on delivery and nondelivery reports and a per-message property on read and nonread reports.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d1036-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1036-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d1036-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d1036-117">Protocol specifications</span></span>

<span data-ttu-id="d1036-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1036-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1036-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d1036-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d1036-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1036-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1036-121">Especifica las propiedades y operaciones que se permiten en mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="d1036-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="d1036-122">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1036-122">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1036-123">Permite la manipulación de las listas Permitir o bloquear y la determinación de los mensajes de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="d1036-123">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d1036-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d1036-124">Header files</span></span>

<span data-ttu-id="d1036-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1036-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1036-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d1036-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d1036-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d1036-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d1036-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d1036-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1036-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d1036-129">See also</span></span>



[<span data-ttu-id="d1036-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d1036-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1036-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d1036-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1036-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d1036-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1036-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d1036-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

