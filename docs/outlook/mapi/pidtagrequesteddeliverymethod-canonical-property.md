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
ms.openlocfilehash: f18d726c1b06a6fb7f79964165bbdb9074a6d4d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571370"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="64889-103">Propiedad canónica PidTagRequestedDeliveryMethod</span><span class="sxs-lookup"><span data-stu-id="64889-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="64889-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64889-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64889-105">Esta propiedad contiene una matriz binaria de métodos de entrega (proveedores de servicios), en orden de preferencia del remitente de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="64889-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64889-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="64889-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64889-107">PR_REQUESTED_DELIVERY_METHOD</span><span class="sxs-lookup"><span data-stu-id="64889-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="64889-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="64889-108">Identifier:</span></span>  <br/> |<span data-ttu-id="64889-109">0x0C18</span><span class="sxs-lookup"><span data-stu-id="64889-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="64889-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="64889-110">Data type:</span></span>  <br/> |<span data-ttu-id="64889-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="64889-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="64889-112">Área:</span><span class="sxs-lookup"><span data-stu-id="64889-112">Area:</span></span>  <br/> |<span data-ttu-id="64889-113">Destinatario MAPI</span><span class="sxs-lookup"><span data-stu-id="64889-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64889-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="64889-114">Remarks</span></span>

<span data-ttu-id="64889-115">La matriz contenida en esta propiedad consta de ASN.1 identificadores para cada uno de los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="64889-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="64889-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="64889-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="64889-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="64889-117">Header files</span></span>

<span data-ttu-id="64889-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64889-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="64889-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="64889-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="64889-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="64889-120">Mapitags.h</span></span>
  
> <span data-ttu-id="64889-121">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="64889-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64889-122">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="64889-122">See also</span></span>



[<span data-ttu-id="64889-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="64889-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64889-124">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="64889-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64889-125">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="64889-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64889-126">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="64889-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

