---
title: Propiedad canónica PidTagProviderOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderOrdinal
api_type:
- COM
ms.assetid: d062b54d-7c32-4369-ab69-f7193773a1c0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b56ee557884e12728c98827f9eb1a280d7a29c30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819974"
---
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="9189a-103">Propiedad canónica PidTagProviderOrdinal</span><span class="sxs-lookup"><span data-stu-id="9189a-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="9189a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9189a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9189a-105">Contiene el índice de base cero de la posición de un proveedor de servicios en la tabla proveedor.</span><span class="sxs-lookup"><span data-stu-id="9189a-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9189a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9189a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9189a-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="9189a-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="9189a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9189a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9189a-109">0x300D</span><span class="sxs-lookup"><span data-stu-id="9189a-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="9189a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9189a-110">Data type:</span></span>  <br/> |<span data-ttu-id="9189a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9189a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9189a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9189a-112">Area:</span></span>  <br/> |<span data-ttu-id="9189a-113">MAPI comunes</span><span class="sxs-lookup"><span data-stu-id="9189a-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9189a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9189a-114">Remarks</span></span>

<span data-ttu-id="9189a-115">Esta propiedad se calcula mediante MAPI.</span><span class="sxs-lookup"><span data-stu-id="9189a-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="9189a-116">Obtener la tabla de proveedor llamando al método [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) .</span><span class="sxs-lookup"><span data-stu-id="9189a-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="9189a-117">Ordenar la tabla de proveedor de esta propiedad para mostrar el orden de transporte.</span><span class="sxs-lookup"><span data-stu-id="9189a-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9189a-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9189a-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9189a-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9189a-119">Header files</span></span>

<span data-ttu-id="9189a-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9189a-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="9189a-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9189a-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="9189a-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9189a-122">Mapitags.h</span></span>
  
> <span data-ttu-id="9189a-123">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="9189a-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9189a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="9189a-124">See also</span></span>



[<span data-ttu-id="9189a-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9189a-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9189a-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="9189a-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9189a-127">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9189a-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9189a-128">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="9189a-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

