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
ms.openlocfilehash: fbeb63bbae23f8f7f78c92d3abed6bea1c3ac85d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438354"
---
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="7eeb0-103">Propiedad canónica PidTagProviderOrdinal</span><span class="sxs-lookup"><span data-stu-id="7eeb0-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="7eeb0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7eeb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7eeb0-105">Contiene el índice de base cero de la posición de un proveedor de servicios en la tabla del proveedor.</span><span class="sxs-lookup"><span data-stu-id="7eeb0-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7eeb0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7eeb0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7eeb0-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="7eeb0-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="7eeb0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7eeb0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7eeb0-109">0x300D</span><span class="sxs-lookup"><span data-stu-id="7eeb0-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="7eeb0-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7eeb0-110">Data type:</span></span>  <br/> |<span data-ttu-id="7eeb0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7eeb0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7eeb0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7eeb0-112">Area:</span></span>  <br/> |<span data-ttu-id="7eeb0-113">Common MAPI</span><span class="sxs-lookup"><span data-stu-id="7eeb0-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7eeb0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7eeb0-114">Remarks</span></span>

<span data-ttu-id="7eeb0-115">MAPI calcula esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="7eeb0-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="7eeb0-116">Para obtener la tabla del proveedor, llame al método [IMsgServiceAdmin:: GetProviderTable](imsgserviceadmin-getprovidertable.md) .</span><span class="sxs-lookup"><span data-stu-id="7eeb0-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="7eeb0-117">Ordene la tabla de proveedores en esta propiedad para mostrar el orden de transporte.</span><span class="sxs-lookup"><span data-stu-id="7eeb0-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7eeb0-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7eeb0-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7eeb0-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7eeb0-119">Header files</span></span>

<span data-ttu-id="7eeb0-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7eeb0-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="7eeb0-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7eeb0-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="7eeb0-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7eeb0-122">Mapitags.h</span></span>
  
> <span data-ttu-id="7eeb0-123">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7eeb0-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7eeb0-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="7eeb0-124">See also</span></span>



[<span data-ttu-id="7eeb0-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7eeb0-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7eeb0-126">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="7eeb0-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7eeb0-127">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7eeb0-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7eeb0-128">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7eeb0-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

