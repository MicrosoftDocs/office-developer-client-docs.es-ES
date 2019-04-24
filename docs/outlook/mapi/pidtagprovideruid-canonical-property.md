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
ms.openlocfilehash: 0d79075ea1db451e0c3d327df9a662e5032ebb22
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286418"
---
# <a name="pidtagprovideruid-canonical-property"></a><span data-ttu-id="7514a-103">Propiedad canónica PidTagProviderUid</span><span class="sxs-lookup"><span data-stu-id="7514a-103">PidTagProviderUid Canonical Property</span></span>

  
  
<span data-ttu-id="7514a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7514a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7514a-105">Contiene una estructura **MAPIUID** del proveedor de servicios que controla un mensaje.</span><span class="sxs-lookup"><span data-stu-id="7514a-105">Contains a **MAPIUID** structure of the service provider that is handling a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7514a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7514a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7514a-107">PR_PROVIDER_UID</span><span class="sxs-lookup"><span data-stu-id="7514a-107">PR_PROVIDER_UID</span></span>  <br/> |
|<span data-ttu-id="7514a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7514a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7514a-109">0x300C</span><span class="sxs-lookup"><span data-stu-id="7514a-109">0x300C</span></span>  <br/> |
|<span data-ttu-id="7514a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7514a-110">Data type:</span></span>  <br/> |<span data-ttu-id="7514a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7514a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7514a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7514a-112">Area:</span></span>  <br/> |<span data-ttu-id="7514a-113">Common MAPI</span><span class="sxs-lookup"><span data-stu-id="7514a-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7514a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7514a-114">Remarks</span></span>

<span data-ttu-id="7514a-115">Esta propiedad la calculan todos los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="7514a-115">This property is computed by all service providers.</span></span> <span data-ttu-id="7514a-116">Contiene una estructura [MAPIUID](mapiuid.md) asociada y, normalmente, codificada de forma rígida por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="7514a-116">It contains a [MAPIUID](mapiuid.md) structure associated with, and usually hard-coded by, the provider.</span></span> <span data-ttu-id="7514a-117">Lo suele usar una aplicación cliente que está interesada en solo los contenedores de la libreta de direcciones suministrados por un proveedor en particular.</span><span class="sxs-lookup"><span data-stu-id="7514a-117">It is typically used by a client application that is interested in only the address book containers supplied by a particular provider.</span></span> 
  
<span data-ttu-id="7514a-118">Esta propiedad aparece sólo como una entrada de columna en la tabla del proveedor.</span><span class="sxs-lookup"><span data-stu-id="7514a-118">This property appears only as a column entry in the provider table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7514a-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7514a-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7514a-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7514a-120">Header files</span></span>

<span data-ttu-id="7514a-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7514a-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="7514a-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7514a-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="7514a-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7514a-123">Mapitags.h</span></span>
  
> <span data-ttu-id="7514a-124">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7514a-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7514a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7514a-125">See also</span></span>



[<span data-ttu-id="7514a-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7514a-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7514a-127">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="7514a-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7514a-128">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7514a-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7514a-129">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7514a-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

