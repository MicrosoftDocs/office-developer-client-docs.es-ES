---
title: Propiedad canónica PidTagProviderUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cca22b466b1e0d2da9ca9cc009586df08316270c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581058"
---
# <a name="pidtagprovideruid-canonical-property"></a><span data-ttu-id="d35ac-103">Propiedad canónica PidTagProviderUid</span><span class="sxs-lookup"><span data-stu-id="d35ac-103">PidTagProviderUid Canonical Property</span></span>

  
  
<span data-ttu-id="d35ac-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d35ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d35ac-105">Contiene una estructura **MAPIUID** del proveedor de servicios que se encarga de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d35ac-105">Contains a **MAPIUID** structure of the service provider that is handling a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d35ac-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d35ac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d35ac-107">PR_PROVIDER_UID</span><span class="sxs-lookup"><span data-stu-id="d35ac-107">PR_PROVIDER_UID</span></span>  <br/> |
|<span data-ttu-id="d35ac-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d35ac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d35ac-109">0x300C</span><span class="sxs-lookup"><span data-stu-id="d35ac-109">0x300C</span></span>  <br/> |
|<span data-ttu-id="d35ac-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d35ac-110">Data type:</span></span>  <br/> |<span data-ttu-id="d35ac-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d35ac-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d35ac-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d35ac-112">Area:</span></span>  <br/> |<span data-ttu-id="d35ac-113">MAPI comunes</span><span class="sxs-lookup"><span data-stu-id="d35ac-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d35ac-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d35ac-114">Remarks</span></span>

<span data-ttu-id="d35ac-115">Esta propiedad se calcula por todos los proveedores de servicio.</span><span class="sxs-lookup"><span data-stu-id="d35ac-115">This property is computed by all service providers.</span></span> <span data-ttu-id="d35ac-116">Contiene una estructura [MAPIUID](mapiuid.md) asociada y normalmente codificado de forma rígida por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="d35ac-116">It contains a [MAPIUID](mapiuid.md) structure associated with, and usually hard-coded by, the provider.</span></span> <span data-ttu-id="d35ac-117">Normalmente se usa por una aplicación cliente que está interesada en sólo los contenedores de la libreta de direcciones proporcionados por un proveedor concreto.</span><span class="sxs-lookup"><span data-stu-id="d35ac-117">It is typically used by a client application that is interested in only the address book containers supplied by a particular provider.</span></span> 
  
<span data-ttu-id="d35ac-118">Esta propiedad aparece sólo como una entrada de la columna en la tabla proveedor.</span><span class="sxs-lookup"><span data-stu-id="d35ac-118">This property appears only as a column entry in the provider table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d35ac-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d35ac-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d35ac-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d35ac-120">Header files</span></span>

<span data-ttu-id="d35ac-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d35ac-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="d35ac-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d35ac-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="d35ac-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d35ac-123">Mapitags.h</span></span>
  
> <span data-ttu-id="d35ac-124">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d35ac-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d35ac-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d35ac-125">See also</span></span>



[<span data-ttu-id="d35ac-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d35ac-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d35ac-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d35ac-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d35ac-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d35ac-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d35ac-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d35ac-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

