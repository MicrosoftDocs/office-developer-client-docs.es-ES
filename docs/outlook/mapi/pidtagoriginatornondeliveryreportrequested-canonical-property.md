---
title: Propiedad canónica PidTagOriginatorNonDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorNonDeliveryReportRequested
api_type:
- COM
ms.assetid: 0a19ba44-abb0-4868-9d7d-75184058d4c0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 841d2b14efc781d89727b0c7ed677f527526a4ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819865"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a><span data-ttu-id="bc2be-103">Propiedad canónica PidTagOriginatorNonDeliveryReportRequested</span><span class="sxs-lookup"><span data-stu-id="bc2be-103">PidTagOriginatorNonDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="bc2be-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bc2be-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bc2be-105">Contiene TRUE si el remitente de un mensaje, solicita un informe de no entrega para un destinatario concreto.</span><span class="sxs-lookup"><span data-stu-id="bc2be-105">Contains TRUE if a message sender requests a nondelivery report for a particular recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bc2be-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="bc2be-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc2be-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="bc2be-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="bc2be-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bc2be-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc2be-109">0x0C08</span><span class="sxs-lookup"><span data-stu-id="bc2be-109">0x0C08</span></span>  <br/> |
|<span data-ttu-id="bc2be-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="bc2be-110">Data type:</span></span>  <br/> |<span data-ttu-id="bc2be-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bc2be-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="bc2be-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bc2be-112">Area:</span></span>  <br/> |<span data-ttu-id="bc2be-113">MIME</span><span class="sxs-lookup"><span data-stu-id="bc2be-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc2be-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bc2be-114">Remarks</span></span>

<span data-ttu-id="bc2be-115">Esta propiedad se utiliza para dirigir el sistema de mensajería en el control de mensajes no entregados.</span><span class="sxs-lookup"><span data-stu-id="bc2be-115">This property is used to direct the messaging system in handling undelivered messages.</span></span> <span data-ttu-id="bc2be-116">En este caso, el mensaje también debe proporcionar la propiedad **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) que se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="bc2be-116">In this case, the message must also furnish the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bc2be-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc2be-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bc2be-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="bc2be-118">Protocol specifications</span></span>

<span data-ttu-id="bc2be-119">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc2be-119">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc2be-120">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="bc2be-120">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bc2be-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="bc2be-121">Header files</span></span>

<span data-ttu-id="bc2be-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc2be-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc2be-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="bc2be-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc2be-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bc2be-124">Mapitags.h</span></span>
  
> <span data-ttu-id="bc2be-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="bc2be-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc2be-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc2be-126">See also</span></span>



[<span data-ttu-id="bc2be-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bc2be-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc2be-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="bc2be-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc2be-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="bc2be-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc2be-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="bc2be-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

