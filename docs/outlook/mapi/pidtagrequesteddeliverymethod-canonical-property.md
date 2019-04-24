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
ms.openlocfilehash: ecfed5684ba2166c1c00c1fd07fa074b4ce9fd79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331419"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="d2fe8-103">Propiedad canónica PidTagRequestedDeliveryMethod</span><span class="sxs-lookup"><span data-stu-id="d2fe8-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="d2fe8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2fe8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2fe8-105">Esta propiedad contiene una matriz binaria de métodos de entrega (proveedores de servicios), en el orden preferido del remitente de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d2fe8-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2fe8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d2fe8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d2fe8-107">PR_REQUESTED_DELIVERY_METHOD</span><span class="sxs-lookup"><span data-stu-id="d2fe8-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="d2fe8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d2fe8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d2fe8-109">0x0C18</span><span class="sxs-lookup"><span data-stu-id="d2fe8-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="d2fe8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d2fe8-110">Data type:</span></span>  <br/> |<span data-ttu-id="d2fe8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d2fe8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d2fe8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d2fe8-112">Area:</span></span>  <br/> |<span data-ttu-id="d2fe8-113">Destinatario MAPI</span><span class="sxs-lookup"><span data-stu-id="d2fe8-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2fe8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d2fe8-114">Remarks</span></span>

<span data-ttu-id="d2fe8-115">La matriz contenida en la propiedad this consta de los identificadores ASN. 1 de cada uno de los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="d2fe8-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d2fe8-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d2fe8-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d2fe8-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d2fe8-117">Header files</span></span>

<span data-ttu-id="d2fe8-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d2fe8-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="d2fe8-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d2fe8-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="d2fe8-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d2fe8-120">Mapitags.h</span></span>
  
> <span data-ttu-id="d2fe8-121">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="d2fe8-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d2fe8-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2fe8-122">See also</span></span>



[<span data-ttu-id="d2fe8-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d2fe8-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d2fe8-124">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="d2fe8-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d2fe8-125">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d2fe8-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d2fe8-126">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="d2fe8-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

