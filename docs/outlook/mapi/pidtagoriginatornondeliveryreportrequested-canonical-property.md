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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341961"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a><span data-ttu-id="baba6-103">Propiedad canónica PidTagOriginatorNonDeliveryReportRequested</span><span class="sxs-lookup"><span data-stu-id="baba6-103">PidTagOriginatorNonDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="baba6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="baba6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="baba6-105">Contiene TRUE si un remitente de mensaje solicita un informe de no entrega para un destinatario determinado.</span><span class="sxs-lookup"><span data-stu-id="baba6-105">Contains TRUE if a message sender requests a nondelivery report for a particular recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="baba6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="baba6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="baba6-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="baba6-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="baba6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="baba6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="baba6-109">0x0C08</span><span class="sxs-lookup"><span data-stu-id="baba6-109">0x0C08</span></span>  <br/> |
|<span data-ttu-id="baba6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="baba6-110">Data type:</span></span>  <br/> |<span data-ttu-id="baba6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="baba6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="baba6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="baba6-112">Area:</span></span>  <br/> |<span data-ttu-id="baba6-113">MIME</span><span class="sxs-lookup"><span data-stu-id="baba6-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="baba6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="baba6-114">Remarks</span></span>

<span data-ttu-id="baba6-115">Esta propiedad se usa para dirigir al sistema de mensajería en el control de mensajes no entregados.</span><span class="sxs-lookup"><span data-stu-id="baba6-115">This property is used to direct the messaging system in handling undelivered messages.</span></span> <span data-ttu-id="baba6-116">En este caso, el mensaje también debe proporcionar la propiedad **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) establecida en FALSE.</span><span class="sxs-lookup"><span data-stu-id="baba6-116">In this case, the message must also furnish the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="baba6-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="baba6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="baba6-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="baba6-118">Protocol specifications</span></span>

<span data-ttu-id="baba6-119">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="baba6-119">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="baba6-120">Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="baba6-120">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="baba6-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="baba6-121">Header files</span></span>

<span data-ttu-id="baba6-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="baba6-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="baba6-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="baba6-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="baba6-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="baba6-124">Mapitags.h</span></span>
  
> <span data-ttu-id="baba6-125">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="baba6-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="baba6-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="baba6-126">See also</span></span>



[<span data-ttu-id="baba6-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="baba6-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="baba6-128">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="baba6-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="baba6-129">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="baba6-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="baba6-130">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="baba6-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

