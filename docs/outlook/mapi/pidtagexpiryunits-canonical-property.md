---
title: Propiedad canónica PidTagExpiryUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryUnits
api_type:
- HeaderDef
ms.assetid: f6a1ca22-cf4c-4e59-8846-6bd937fa8f6e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c6aab4228af0f584d96a2a8cc02c5f36e05a01e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569606"
---
# <a name="pidtagexpiryunits-canonical-property"></a><span data-ttu-id="faf51-103">Propiedad canónica PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="faf51-103">PidTagExpiryUnits Canonical Property</span></span>

  
  
<span data-ttu-id="faf51-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="faf51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="faf51-105">Describe la unidad de tiempo cuando la propiedad **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) multiplica.</span><span class="sxs-lookup"><span data-stu-id="faf51-105">Describes the unit of time when the **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) property multiplies.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="faf51-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="faf51-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="faf51-107">PR_EXPIRY_UNITS</span><span class="sxs-lookup"><span data-stu-id="faf51-107">PR_EXPIRY_UNITS</span></span>  <br/> |
|<span data-ttu-id="faf51-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="faf51-108">Identifier:</span></span>  <br/> |<span data-ttu-id="faf51-109">0x3FEE</span><span class="sxs-lookup"><span data-stu-id="faf51-109">0x3FEE</span></span>  <br/> |
|<span data-ttu-id="faf51-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="faf51-110">Data type:</span></span>  <br/> |<span data-ttu-id="faf51-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="faf51-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="faf51-112">Área:</span><span class="sxs-lookup"><span data-stu-id="faf51-112">Area:</span></span>  <br/> |<span data-ttu-id="faf51-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="faf51-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="faf51-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="faf51-114">Remarks</span></span>

<span data-ttu-id="faf51-115">Esta propiedad, si establece, debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="faf51-115">This property, if set, must be one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="faf51-116">PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="faf51-116">PidTagExpiryUnits</span></span>  <br/> |<span data-ttu-id="faf51-117">Descripción (TimeOf)</span><span class="sxs-lookup"><span data-stu-id="faf51-117">Description (TimeOf)</span></span>  <br/> |
|<span data-ttu-id="faf51-118">0x00000000</span><span class="sxs-lookup"><span data-stu-id="faf51-118">0x00000000</span></span>  <br/> |<span data-ttu-id="faf51-119">Minutos, por ejemplo 60 segundos</span><span class="sxs-lookup"><span data-stu-id="faf51-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="faf51-120">0x00000001</span><span class="sxs-lookup"><span data-stu-id="faf51-120">0x00000001</span></span>  <br/> |<span data-ttu-id="faf51-121">Horas, por ejemplo 60 x 60 segundos</span><span class="sxs-lookup"><span data-stu-id="faf51-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="faf51-122">0x00000002</span><span class="sxs-lookup"><span data-stu-id="faf51-122">0x00000002</span></span>  <br/> |<span data-ttu-id="faf51-123">Día, por ejemplo 24 x 60 x 60 segundos</span><span class="sxs-lookup"><span data-stu-id="faf51-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="faf51-124">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="faf51-124">0x00000003</span></span>  <br/> |<span data-ttu-id="faf51-125">Semana, por ejemplo 7x24x60x60 segundos</span><span class="sxs-lookup"><span data-stu-id="faf51-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="faf51-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="faf51-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="faf51-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="faf51-127">Protocol specifications</span></span>

<span data-ttu-id="faf51-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="faf51-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="faf51-129">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="faf51-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="faf51-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="faf51-130">Header files</span></span>

<span data-ttu-id="faf51-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="faf51-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="faf51-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="faf51-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="faf51-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="faf51-133">Mapitags.h</span></span>
  
> <span data-ttu-id="faf51-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="faf51-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="faf51-135">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="faf51-135">See also</span></span>



[<span data-ttu-id="faf51-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="faf51-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="faf51-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="faf51-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="faf51-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="faf51-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="faf51-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="faf51-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

