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
ms.openlocfilehash: 1c753bb84ccbfe2fa6869d56806fd042a6d60e9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819479"
---
# <a name="pidtagexpiryunits-canonical-property"></a><span data-ttu-id="74fe6-103">Propiedad canónica PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="74fe6-103">PidTagExpiryUnits Canonical Property</span></span>

  
  
<span data-ttu-id="74fe6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="74fe6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="74fe6-105">Describe la unidad de tiempo cuando la propiedad **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) multiplica.</span><span class="sxs-lookup"><span data-stu-id="74fe6-105">Describes the unit of time when the **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) property multiplies.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74fe6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="74fe6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74fe6-107">PR_EXPIRY_UNITS</span><span class="sxs-lookup"><span data-stu-id="74fe6-107">PR_EXPIRY_UNITS</span></span>  <br/> |
|<span data-ttu-id="74fe6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="74fe6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="74fe6-109">0x3FEE</span><span class="sxs-lookup"><span data-stu-id="74fe6-109">0x3FEE</span></span>  <br/> |
|<span data-ttu-id="74fe6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="74fe6-110">Data type:</span></span>  <br/> |<span data-ttu-id="74fe6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="74fe6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="74fe6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="74fe6-112">Area:</span></span>  <br/> |<span data-ttu-id="74fe6-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="74fe6-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74fe6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74fe6-114">Remarks</span></span>

<span data-ttu-id="74fe6-115">Esta propiedad, si establece, debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="74fe6-115">This property, if set, must be one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74fe6-116">PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="74fe6-116">PidTagExpiryUnits</span></span>  <br/> |<span data-ttu-id="74fe6-117">Descripción (TimeOf)</span><span class="sxs-lookup"><span data-stu-id="74fe6-117">Description (TimeOf)</span></span>  <br/> |
|<span data-ttu-id="74fe6-118">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74fe6-118">0x00000000</span></span>  <br/> |<span data-ttu-id="74fe6-119">Minutos, por ejemplo 60 segundos</span><span class="sxs-lookup"><span data-stu-id="74fe6-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="74fe6-120">0x00000001</span><span class="sxs-lookup"><span data-stu-id="74fe6-120">0x00000001</span></span>  <br/> |<span data-ttu-id="74fe6-121">Horas, por ejemplo 60 x 60 segundos</span><span class="sxs-lookup"><span data-stu-id="74fe6-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="74fe6-122">0x00000002</span><span class="sxs-lookup"><span data-stu-id="74fe6-122">0x00000002</span></span>  <br/> |<span data-ttu-id="74fe6-123">Día, por ejemplo 24 x 60 x 60 segundos</span><span class="sxs-lookup"><span data-stu-id="74fe6-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="74fe6-124">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="74fe6-124">0x00000003</span></span>  <br/> |<span data-ttu-id="74fe6-125">Semana, por ejemplo 7x24x60x60 segundos</span><span class="sxs-lookup"><span data-stu-id="74fe6-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="74fe6-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="74fe6-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="74fe6-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="74fe6-127">Protocol specifications</span></span>

<span data-ttu-id="74fe6-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74fe6-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74fe6-129">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="74fe6-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="74fe6-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="74fe6-130">Header files</span></span>

<span data-ttu-id="74fe6-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74fe6-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="74fe6-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="74fe6-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="74fe6-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="74fe6-133">Mapitags.h</span></span>
  
> <span data-ttu-id="74fe6-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="74fe6-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74fe6-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="74fe6-135">See also</span></span>



[<span data-ttu-id="74fe6-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="74fe6-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74fe6-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="74fe6-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74fe6-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="74fe6-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74fe6-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="74fe6-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

