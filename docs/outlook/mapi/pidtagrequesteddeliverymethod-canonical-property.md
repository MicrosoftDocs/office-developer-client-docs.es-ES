---
title: Propiedad canónica PidTagRequestedDeliveryMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRequestedDeliveryMethod
api_type:
- COM
ms.assetid: cc55089b-e389-405e-8174-f5b5ec352f78
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8a2199ee2bba8b3b41af7bf26de6cdd3d8d0956e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820114"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="bca6f-103">Propiedad canónica PidTagRequestedDeliveryMethod</span><span class="sxs-lookup"><span data-stu-id="bca6f-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="bca6f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bca6f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bca6f-105">Esta propiedad contiene una matriz binaria de métodos de entrega (proveedores de servicios), en orden de preferencia del remitente de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="bca6f-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bca6f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="bca6f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bca6f-107">PR_REQUESTED_DELIVERY_METHOD</span><span class="sxs-lookup"><span data-stu-id="bca6f-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="bca6f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bca6f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bca6f-109">0x0C18</span><span class="sxs-lookup"><span data-stu-id="bca6f-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="bca6f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="bca6f-110">Data type:</span></span>  <br/> |<span data-ttu-id="bca6f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bca6f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bca6f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bca6f-112">Area:</span></span>  <br/> |<span data-ttu-id="bca6f-113">Destinatario MAPI</span><span class="sxs-lookup"><span data-stu-id="bca6f-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bca6f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bca6f-114">Remarks</span></span>

<span data-ttu-id="bca6f-115">La matriz contenida en esta propiedad consta de ASN.1 identificadores para cada uno de los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="bca6f-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bca6f-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bca6f-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bca6f-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="bca6f-117">Header files</span></span>

<span data-ttu-id="bca6f-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bca6f-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="bca6f-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="bca6f-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="bca6f-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bca6f-120">Mapitags.h</span></span>
  
> <span data-ttu-id="bca6f-121">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="bca6f-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bca6f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="bca6f-122">See also</span></span>



[<span data-ttu-id="bca6f-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bca6f-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bca6f-124">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="bca6f-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bca6f-125">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="bca6f-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bca6f-126">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="bca6f-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

