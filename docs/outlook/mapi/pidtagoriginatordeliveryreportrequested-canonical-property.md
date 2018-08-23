---
title: Propiedad canónica PidTagOriginatorDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorDeliveryReportRequested
api_type:
- COM
ms.assetid: 4461b35d-e2b9-41ff-b079-31bfef02e2bb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9e508f9c3d84272a0641a27e18c94e0620a7072c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574408"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a><span data-ttu-id="33def-103">Propiedad canónica PidTagOriginatorDeliveryReportRequested</span><span class="sxs-lookup"><span data-stu-id="33def-103">PidTagOriginatorDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="33def-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33def-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33def-105">Contiene TRUE si el remitente del mensaje solicita un informe de entrega para un destinatario concreto desde el sistema de mensajería antes de que el mensaje se coloca en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="33def-105">Contains TRUE if a message sender requests a delivery report for a particular recipient from the messaging system before the message is placed in the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33def-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="33def-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33def-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="33def-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="33def-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="33def-108">Identifier:</span></span>  <br/> |<span data-ttu-id="33def-109">0x0023</span><span class="sxs-lookup"><span data-stu-id="33def-109">0x0023</span></span>  <br/> |
|<span data-ttu-id="33def-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="33def-110">Data type:</span></span>  <br/> |<span data-ttu-id="33def-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="33def-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="33def-112">Área:</span><span class="sxs-lookup"><span data-stu-id="33def-112">Area:</span></span>  <br/> |<span data-ttu-id="33def-113">MIME</span><span class="sxs-lookup"><span data-stu-id="33def-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33def-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="33def-114">Remarks</span></span>

<span data-ttu-id="33def-115">Esta propiedad se utiliza para dirigir el sistema de mensajería en el control de los mensajes entregados.</span><span class="sxs-lookup"><span data-stu-id="33def-115">This property is used to direct the messaging system in handling delivered messages.</span></span> <span data-ttu-id="33def-116">En este caso, el mensaje también debe proporcionar la propiedad **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) que se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="33def-116">In this case, the message must also furnish the **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
<span data-ttu-id="33def-117">Establecimiento de la propiedad **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** en un mensaje es una forma para solicitar informes de estado de entrega para todos los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="33def-117">Setting the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** property on a message is a way to request delivery status reports for all recipients.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="33def-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="33def-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33def-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="33def-119">Protocol specifications</span></span>

<span data-ttu-id="33def-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33def-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33def-121">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="33def-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33def-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="33def-122">Header files</span></span>

<span data-ttu-id="33def-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="33def-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="33def-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="33def-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="33def-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="33def-125">Mapitags.h</span></span>
  
> <span data-ttu-id="33def-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="33def-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33def-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="33def-127">See also</span></span>



[<span data-ttu-id="33def-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="33def-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33def-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="33def-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33def-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="33def-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33def-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="33def-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

