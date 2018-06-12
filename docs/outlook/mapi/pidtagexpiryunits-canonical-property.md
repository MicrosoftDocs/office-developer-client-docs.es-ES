---
title: Propiedad canónico PidTagExpiryUnits
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 1c753bb84ccbfe2fa6869d56806fd042a6d60e9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819479"
---
# <a name="pidtagexpiryunits-canonical-property"></a><span data-ttu-id="d304d-103">Propiedad canónico PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="d304d-103">PidTagExpiryUnits Canonical Property</span></span>

  
  
<span data-ttu-id="d304d-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d304d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d304d-105">Describe la unidad de tiempo cuando la propiedad **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) multiplica.</span><span class="sxs-lookup"><span data-stu-id="d304d-105">Describes the unit of time when the **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) property multiplies.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d304d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d304d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d304d-107">PR_EXPIRY_UNITS</span><span class="sxs-lookup"><span data-stu-id="d304d-107">PR_EXPIRY_UNITS</span></span>  <br/> |
|<span data-ttu-id="d304d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d304d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d304d-109">0x3FEE</span><span class="sxs-lookup"><span data-stu-id="d304d-109">0x3FEE</span></span>  <br/> |
|<span data-ttu-id="d304d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d304d-110">Data type:</span></span>  <br/> |<span data-ttu-id="d304d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d304d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d304d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d304d-112">Area:</span></span>  <br/> |<span data-ttu-id="d304d-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="d304d-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d304d-114">Notas</span><span class="sxs-lookup"><span data-stu-id="d304d-114">Remarks</span></span>

<span data-ttu-id="d304d-115">Esta propiedad, si establece, debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="d304d-115">This property, if set, must be one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d304d-116">PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="d304d-116">PidTagExpiryUnits</span></span>  <br/> |<span data-ttu-id="d304d-117">Descripción (TimeOf)</span><span class="sxs-lookup"><span data-stu-id="d304d-117">Description (TimeOf)</span></span>  <br/> |
|<span data-ttu-id="d304d-118">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d304d-118">0x00000000</span></span>  <br/> |<span data-ttu-id="d304d-119">Minutos, por ejemplo 60 segundos</span><span class="sxs-lookup"><span data-stu-id="d304d-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="d304d-120">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d304d-120">0x00000001</span></span>  <br/> |<span data-ttu-id="d304d-121">Horas, por ejemplo 60 x 60 segundos</span><span class="sxs-lookup"><span data-stu-id="d304d-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="d304d-122">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d304d-122">0x00000002</span></span>  <br/> |<span data-ttu-id="d304d-123">Día, por ejemplo 24 x 60 x 60 segundos</span><span class="sxs-lookup"><span data-stu-id="d304d-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="d304d-124">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="d304d-124">0x00000003</span></span>  <br/> |<span data-ttu-id="d304d-125">Semana, por ejemplo 7x24x60x60 segundos</span><span class="sxs-lookup"><span data-stu-id="d304d-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d304d-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d304d-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d304d-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d304d-127">Protocol specifications</span></span>

<span data-ttu-id="d304d-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d304d-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d304d-129">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="d304d-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d304d-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d304d-130">Header files</span></span>

<span data-ttu-id="d304d-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d304d-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="d304d-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d304d-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="d304d-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d304d-133">Mapitags.h</span></span>
  
> <span data-ttu-id="d304d-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d304d-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d304d-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="d304d-135">See also</span></span>



[<span data-ttu-id="d304d-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d304d-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d304d-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d304d-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d304d-138">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="d304d-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d304d-139">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d304d-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

