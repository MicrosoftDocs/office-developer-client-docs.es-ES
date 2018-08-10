---
title: Propiedad canónica PidTagReportEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportEntryId
api_type:
- COM
ms.assetid: ea2bcc06-0089-4999-b115-06a14de4a0f1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a1d81581afa3bb9df8bd7aded5c265dfa8f04676
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820092"
---
# <a name="pidtagreportentryid-canonical-property"></a><span data-ttu-id="d7206-103">Propiedad canónica PidTagReportEntryId</span><span class="sxs-lookup"><span data-stu-id="d7206-103">PidTagReportEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="d7206-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7206-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7206-105">Contiene el identificador de entrada para el destinatario que debe recibir informes para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="d7206-105">Contains the entry identifier for the recipient who should receive reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7206-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d7206-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7206-107">PR_REPORT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d7206-107">PR_REPORT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="d7206-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d7206-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d7206-109">0x0045</span><span class="sxs-lookup"><span data-stu-id="d7206-109">0x0045</span></span>  <br/> |
|<span data-ttu-id="d7206-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d7206-110">Data type:</span></span>  <br/> |<span data-ttu-id="d7206-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d7206-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d7206-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d7206-112">Area:</span></span>  <br/> |<span data-ttu-id="d7206-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="d7206-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7206-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d7206-114">Remarks</span></span>

<span data-ttu-id="d7206-115">Esta propiedad es una de las propiedades de dirección para el destinatario que el remitente ha delegado para recibir los informes generados para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="d7206-115">This property is one of the address properties for the recipient who the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="d7206-116">Una aplicación cliente que se debe enrutar informes a otro usuario debe establecer esta propiedad en tiempo de envío de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d7206-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="d7206-117">Si no está establecido, los informes se envían al remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d7206-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d7206-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7206-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d7206-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d7206-119">Protocol specifications</span></span>

<span data-ttu-id="d7206-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7206-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7206-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d7206-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d7206-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7206-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7206-123">Especifica las propiedades y operaciones que se permiten en mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="d7206-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d7206-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d7206-124">Header files</span></span>

<span data-ttu-id="d7206-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7206-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7206-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d7206-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7206-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d7206-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d7206-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d7206-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7206-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7206-129">See also</span></span>



[<span data-ttu-id="d7206-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d7206-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7206-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d7206-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7206-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d7206-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7206-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d7206-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
