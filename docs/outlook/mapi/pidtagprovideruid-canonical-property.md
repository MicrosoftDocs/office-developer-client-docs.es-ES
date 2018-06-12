---
title: Propiedad canónico PidTagProviderUid
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 7a42a3b50cfa5630ac66cb03caac06dd7cb00e6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819966"
---
# <a name="pidtagprovideruid-canonical-property"></a><span data-ttu-id="5df85-103">Propiedad canónico PidTagProviderUid</span><span class="sxs-lookup"><span data-stu-id="5df85-103">PidTagProviderUid Canonical Property</span></span>

  
  
<span data-ttu-id="5df85-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5df85-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5df85-105">Contiene una estructura **MAPIUID** del proveedor de servicios que se encarga de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="5df85-105">Contains a **MAPIUID** structure of the service provider that is handling a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5df85-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5df85-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5df85-107">PR_PROVIDER_UID</span><span class="sxs-lookup"><span data-stu-id="5df85-107">PR_PROVIDER_UID</span></span>  <br/> |
|<span data-ttu-id="5df85-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5df85-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5df85-109">0x300C</span><span class="sxs-lookup"><span data-stu-id="5df85-109">0x300C</span></span>  <br/> |
|<span data-ttu-id="5df85-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5df85-110">Data type:</span></span>  <br/> |<span data-ttu-id="5df85-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5df85-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5df85-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5df85-112">Area:</span></span>  <br/> |<span data-ttu-id="5df85-113">MAPI comunes</span><span class="sxs-lookup"><span data-stu-id="5df85-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5df85-114">Notas</span><span class="sxs-lookup"><span data-stu-id="5df85-114">Remarks</span></span>

<span data-ttu-id="5df85-115">Esta propiedad se calcula por todos los proveedores de servicio.</span><span class="sxs-lookup"><span data-stu-id="5df85-115">This property is computed by all service providers.</span></span> <span data-ttu-id="5df85-116">Contiene una estructura [MAPIUID](mapiuid.md) asociada y normalmente codificado de forma rígida por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="5df85-116">It contains a [MAPIUID](mapiuid.md) structure associated with, and usually hard-coded by, the provider.</span></span> <span data-ttu-id="5df85-117">Normalmente se usa por una aplicación cliente que está interesada en sólo los contenedores de la libreta de direcciones proporcionados por un proveedor concreto.</span><span class="sxs-lookup"><span data-stu-id="5df85-117">It is typically used by a client application that is interested in only the address book containers supplied by a particular provider.</span></span> 
  
<span data-ttu-id="5df85-118">Esta propiedad aparece sólo como una entrada de la columna en la tabla proveedor.</span><span class="sxs-lookup"><span data-stu-id="5df85-118">This property appears only as a column entry in the provider table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5df85-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5df85-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5df85-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5df85-120">Header files</span></span>

<span data-ttu-id="5df85-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5df85-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="5df85-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5df85-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="5df85-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5df85-123">Mapitags.h</span></span>
  
> <span data-ttu-id="5df85-124">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5df85-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5df85-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="5df85-125">See also</span></span>



[<span data-ttu-id="5df85-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5df85-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5df85-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5df85-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5df85-128">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="5df85-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5df85-129">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5df85-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

