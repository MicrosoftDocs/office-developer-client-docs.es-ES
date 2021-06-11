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
ms.openlocfilehash: 0c6b56a786ea794587e140c9555cc88cd862b489
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419754"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="8239b-103">Propiedad canónica PidTagNonReceiptNotificationRequested</span><span class="sxs-lookup"><span data-stu-id="8239b-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="8239b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8239b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8239b-105">Contiene TRUE si un remitente de mensaje desea una notificación de no recepción para un destinatario especificado.</span><span class="sxs-lookup"><span data-stu-id="8239b-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8239b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8239b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8239b-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="8239b-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="8239b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8239b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8239b-109">0x0C06</span><span class="sxs-lookup"><span data-stu-id="8239b-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="8239b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8239b-110">Data type:</span></span>  <br/> |<span data-ttu-id="8239b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8239b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8239b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8239b-112">Area:</span></span>  <br/> |<span data-ttu-id="8239b-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="8239b-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8239b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8239b-114">Remarks</span></span>

<span data-ttu-id="8239b-115">Si esta propiedad contiene FALSE y la propiedad **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) contiene TRUE, el proveedor de servicios puede invalidar la propiedad **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** y generar un informe de no entrega.</span><span class="sxs-lookup"><span data-stu-id="8239b-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8239b-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8239b-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8239b-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8239b-117">Header files</span></span>

<span data-ttu-id="8239b-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8239b-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="8239b-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8239b-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="8239b-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8239b-120">Mapitags.h</span></span>
  
> <span data-ttu-id="8239b-121">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="8239b-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8239b-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="8239b-122">See also</span></span>



[<span data-ttu-id="8239b-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8239b-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8239b-124">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8239b-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8239b-125">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8239b-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8239b-126">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="8239b-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

