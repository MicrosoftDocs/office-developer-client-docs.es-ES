---
title: Propiedad canónica PidTagReportSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportSearchKey
api_type:
- COM
ms.assetid: d4f4c40b-b6a8-45f3-b750-07b92c535322
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b82e27358c9f30a649dc10e1a53ee7c321cb3d82
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584964"
---
# <a name="pidtagreportsearchkey-canonical-property"></a><span data-ttu-id="fc3cc-103">Propiedad canónica PidTagReportSearchKey</span><span class="sxs-lookup"><span data-stu-id="fc3cc-103">PidTagReportSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="fc3cc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc3cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc3cc-105">Contiene la clave de búsqueda para el destinatario que debería obtener informes para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="fc3cc-105">Contains the search key for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc3cc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fc3cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc3cc-107">PR_REPORT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="fc3cc-107">PR_REPORT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="fc3cc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fc3cc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fc3cc-109">0x0054</span><span class="sxs-lookup"><span data-stu-id="fc3cc-109">0x0054</span></span>  <br/> |
|<span data-ttu-id="fc3cc-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fc3cc-110">Data type:</span></span>  <br/> |<span data-ttu-id="fc3cc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fc3cc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fc3cc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fc3cc-112">Area:</span></span>  <br/> |<span data-ttu-id="fc3cc-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="fc3cc-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc3cc-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fc3cc-114">Remarks</span></span>

<span data-ttu-id="fc3cc-115">Esta propiedad es una de las propiedades de dirección para el destinatario que el remitente ha delegado para recibir los informes generados para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="fc3cc-115">This property is one of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="fc3cc-116">Una aplicación cliente que se debe enrutar informes a otro usuario debe establecer esta propiedad en tiempo de envío de mensaje.</span><span class="sxs-lookup"><span data-stu-id="fc3cc-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="fc3cc-117">Si no está establecido, los informes se envían al remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="fc3cc-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fc3cc-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc3cc-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fc3cc-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="fc3cc-119">Protocol specifications</span></span>

<span data-ttu-id="fc3cc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc3cc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc3cc-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fc3cc-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fc3cc-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc3cc-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc3cc-123">Especifica las propiedades y operaciones que se permiten en mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="fc3cc-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fc3cc-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fc3cc-124">Header files</span></span>

<span data-ttu-id="fc3cc-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc3cc-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc3cc-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fc3cc-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="fc3cc-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fc3cc-127">Mapitags.h</span></span>
  
> <span data-ttu-id="fc3cc-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="fc3cc-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc3cc-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="fc3cc-129">See also</span></span>



[<span data-ttu-id="fc3cc-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fc3cc-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc3cc-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="fc3cc-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc3cc-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fc3cc-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc3cc-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="fc3cc-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

