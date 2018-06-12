---
title: Propiedad canónico PidTagReportTime
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 95972d53f20f432bc8007f8bbc6734889773f938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820105"
---
# <a name="pidtagreporttime-canonical-property"></a><span data-ttu-id="4d84a-103">Propiedad canónico PidTagReportTime</span><span class="sxs-lookup"><span data-stu-id="4d84a-103">PidTagReportTime Canonical Property</span></span>

  
  
<span data-ttu-id="4d84a-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4d84a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4d84a-105">Contiene la fecha y la hora cuando el sistema de mensajería genera un informe.</span><span class="sxs-lookup"><span data-stu-id="4d84a-105">Contains the date and time when the messaging system generated a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4d84a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4d84a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d84a-107">PR_REPORT_TIME</span><span class="sxs-lookup"><span data-stu-id="4d84a-107">PR_REPORT_TIME</span></span>  <br/> |
|<span data-ttu-id="4d84a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4d84a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4d84a-109">0x0032</span><span class="sxs-lookup"><span data-stu-id="4d84a-109">0x0032</span></span>  <br/> |
|<span data-ttu-id="4d84a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4d84a-110">Data type:</span></span>  <br/> |<span data-ttu-id="4d84a-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="4d84a-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="4d84a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4d84a-112">Area:</span></span>  <br/> |<span data-ttu-id="4d84a-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="4d84a-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d84a-114">Notas</span><span class="sxs-lookup"><span data-stu-id="4d84a-114">Remarks</span></span>

<span data-ttu-id="4d84a-115">Esta propiedad representa una propiedad por destinatario en los informes de entrega y no entrega y una propiedad de cada mensaje en informes de lectura y nonread.</span><span class="sxs-lookup"><span data-stu-id="4d84a-115">This property represents a per-recipient property on delivery and nondelivery reports and a per-message property on read and nonread reports.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4d84a-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d84a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4d84a-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="4d84a-117">Protocol specifications</span></span>

<span data-ttu-id="4d84a-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d84a-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d84a-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4d84a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4d84a-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d84a-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d84a-121">Especifica las propiedades y operaciones que se permiten en mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4d84a-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="4d84a-122">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d84a-122">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d84a-123">Permite la manipulación de las listas Permitir o bloquear y la determinación de los mensajes de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="4d84a-123">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4d84a-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4d84a-124">Header files</span></span>

<span data-ttu-id="4d84a-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4d84a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d84a-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4d84a-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="4d84a-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4d84a-127">Mapitags.h</span></span>
  
> <span data-ttu-id="4d84a-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4d84a-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d84a-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="4d84a-129">See also</span></span>



[<span data-ttu-id="4d84a-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4d84a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d84a-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4d84a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d84a-132">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="4d84a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d84a-133">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4d84a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

