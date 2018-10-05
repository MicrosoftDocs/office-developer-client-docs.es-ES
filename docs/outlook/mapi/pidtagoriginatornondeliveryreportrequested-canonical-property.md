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
ms.openlocfilehash: 227ceb468c54cea98519057b2f837a4aee84820c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387219"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a><span data-ttu-id="92611-103">Propiedad canónica PidTagOriginatorNonDeliveryReportRequested</span><span class="sxs-lookup"><span data-stu-id="92611-103">PidTagOriginatorNonDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="92611-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92611-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92611-105">Contiene TRUE si el remitente de un mensaje, solicita un informe de no entrega para un destinatario concreto.</span><span class="sxs-lookup"><span data-stu-id="92611-105">Contains TRUE if a message sender requests a nondelivery report for a particular recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="92611-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="92611-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92611-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="92611-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="92611-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="92611-108">Identifier:</span></span>  <br/> |<span data-ttu-id="92611-109">0x0C08</span><span class="sxs-lookup"><span data-stu-id="92611-109">0x0C08</span></span>  <br/> |
|<span data-ttu-id="92611-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="92611-110">Data type:</span></span>  <br/> |<span data-ttu-id="92611-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="92611-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="92611-112">Área:</span><span class="sxs-lookup"><span data-stu-id="92611-112">Area:</span></span>  <br/> |<span data-ttu-id="92611-113">MIME</span><span class="sxs-lookup"><span data-stu-id="92611-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92611-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="92611-114">Remarks</span></span>

<span data-ttu-id="92611-115">Esta propiedad se utiliza para dirigir el sistema de mensajería en el control de mensajes no entregados.</span><span class="sxs-lookup"><span data-stu-id="92611-115">This property is used to direct the messaging system in handling undelivered messages.</span></span> <span data-ttu-id="92611-116">En este caso, el mensaje también debe proporcionar la propiedad **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) que se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="92611-116">In this case, the message must also furnish the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="92611-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="92611-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="92611-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="92611-118">Protocol specifications</span></span>

<span data-ttu-id="92611-119">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92611-119">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92611-120">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="92611-120">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="92611-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="92611-121">Header files</span></span>

<span data-ttu-id="92611-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92611-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="92611-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="92611-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="92611-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="92611-124">Mapitags.h</span></span>
  
> <span data-ttu-id="92611-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="92611-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92611-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="92611-126">See also</span></span>



[<span data-ttu-id="92611-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="92611-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="92611-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="92611-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="92611-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="92611-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="92611-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="92611-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

