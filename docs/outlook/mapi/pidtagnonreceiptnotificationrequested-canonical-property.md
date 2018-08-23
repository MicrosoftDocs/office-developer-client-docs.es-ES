---
title: Propiedad canónica PidTagNonReceiptNotificationRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNonReceiptNotificationRequested
api_type:
- HeaderDef
ms.assetid: 747f7ba8-42d3-4be3-9908-269e9a347c7f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 896cfa2bf8a1b33fd6dee09649853b71618f31be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582787"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="5747a-103">Propiedad canónica PidTagNonReceiptNotificationRequested</span><span class="sxs-lookup"><span data-stu-id="5747a-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="5747a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5747a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5747a-105">Contiene TRUE si desea que un remitente del mensaje notificación de no recepción para un destinatario especificado.</span><span class="sxs-lookup"><span data-stu-id="5747a-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5747a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5747a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5747a-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="5747a-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="5747a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5747a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5747a-109">0x0C06</span><span class="sxs-lookup"><span data-stu-id="5747a-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="5747a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5747a-110">Data type:</span></span>  <br/> |<span data-ttu-id="5747a-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5747a-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5747a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5747a-112">Area:</span></span>  <br/> |<span data-ttu-id="5747a-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="5747a-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5747a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5747a-114">Remarks</span></span>

<span data-ttu-id="5747a-115">Si esta propiedad contiene FALSE y la propiedad **PR_READ_RECEIPT_REQUESTED de MAPI** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) contiene TRUE, el proveedor de servicios puede invalidar la propiedad **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** y generar un informe de no entrega.</span><span class="sxs-lookup"><span data-stu-id="5747a-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5747a-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5747a-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5747a-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5747a-117">Header files</span></span>

<span data-ttu-id="5747a-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5747a-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="5747a-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5747a-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="5747a-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5747a-120">Mapitags.h</span></span>
  
> <span data-ttu-id="5747a-121">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="5747a-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5747a-122">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5747a-122">See also</span></span>



[<span data-ttu-id="5747a-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5747a-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5747a-124">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5747a-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5747a-125">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5747a-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5747a-126">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5747a-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

