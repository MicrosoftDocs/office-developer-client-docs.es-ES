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
ms.openlocfilehash: 4cd865fbc443a20ebf4b4cd9722fe52c44d5eddc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573813"
---
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="25f5b-103">Propiedad canónica PidTagProviderOrdinal</span><span class="sxs-lookup"><span data-stu-id="25f5b-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="25f5b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25f5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25f5b-105">Contiene el índice de base cero de la posición de un proveedor de servicios en la tabla proveedor.</span><span class="sxs-lookup"><span data-stu-id="25f5b-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25f5b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="25f5b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25f5b-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="25f5b-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="25f5b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="25f5b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="25f5b-109">0x300D</span><span class="sxs-lookup"><span data-stu-id="25f5b-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="25f5b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="25f5b-110">Data type:</span></span>  <br/> |<span data-ttu-id="25f5b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="25f5b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="25f5b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="25f5b-112">Area:</span></span>  <br/> |<span data-ttu-id="25f5b-113">MAPI comunes</span><span class="sxs-lookup"><span data-stu-id="25f5b-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25f5b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25f5b-114">Remarks</span></span>

<span data-ttu-id="25f5b-115">Esta propiedad se calcula mediante MAPI.</span><span class="sxs-lookup"><span data-stu-id="25f5b-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="25f5b-116">Obtener la tabla de proveedor llamando al método [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) .</span><span class="sxs-lookup"><span data-stu-id="25f5b-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="25f5b-117">Ordenar la tabla de proveedor de esta propiedad para mostrar el orden de transporte.</span><span class="sxs-lookup"><span data-stu-id="25f5b-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="25f5b-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="25f5b-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="25f5b-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="25f5b-119">Header files</span></span>

<span data-ttu-id="25f5b-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25f5b-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="25f5b-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="25f5b-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="25f5b-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="25f5b-122">Mapitags.h</span></span>
  
> <span data-ttu-id="25f5b-123">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="25f5b-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25f5b-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="25f5b-124">See also</span></span>



[<span data-ttu-id="25f5b-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="25f5b-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25f5b-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="25f5b-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25f5b-127">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="25f5b-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25f5b-128">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="25f5b-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

