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
ms.openlocfilehash: 8e8deb67990ce25b10a3b0fc1d373f635f958013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316411"
---
# <a name="pidtagexpiryunits-canonical-property"></a><span data-ttu-id="f9102-103">Propiedad canónica PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="f9102-103">PidTagExpiryUnits Canonical Property</span></span>

  
  
<span data-ttu-id="f9102-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9102-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9102-105">Describe la unidad de tiempo cuando se multiplica **la PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f9102-105">Describes the unit of time when the **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) property multiplies.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9102-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f9102-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f9102-107">PR_EXPIRY_UNITS</span><span class="sxs-lookup"><span data-stu-id="f9102-107">PR_EXPIRY_UNITS</span></span>  <br/> |
|<span data-ttu-id="f9102-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f9102-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f9102-109">0x3FEE</span><span class="sxs-lookup"><span data-stu-id="f9102-109">0x3FEE</span></span>  <br/> |
|<span data-ttu-id="f9102-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f9102-110">Data type:</span></span>  <br/> |<span data-ttu-id="f9102-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f9102-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f9102-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f9102-112">Area:</span></span>  <br/> |<span data-ttu-id="f9102-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="f9102-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9102-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9102-114">Remarks</span></span>

<span data-ttu-id="f9102-115">Esta propiedad, si se establece, debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="f9102-115">This property, if set, must be one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9102-116">PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="f9102-116">PidTagExpiryUnits</span></span>  <br/> |<span data-ttu-id="f9102-117">Descripción (TimeOf)</span><span class="sxs-lookup"><span data-stu-id="f9102-117">Description (TimeOf)</span></span>  <br/> |
|<span data-ttu-id="f9102-118">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9102-118">0x00000000</span></span>  <br/> |<span data-ttu-id="f9102-119">Minutos, por ejemplo, 60 segundos</span><span class="sxs-lookup"><span data-stu-id="f9102-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="f9102-120">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f9102-120">0x00000001</span></span>  <br/> |<span data-ttu-id="f9102-121">Horas, por ejemplo, 60 x 60 segundos</span><span class="sxs-lookup"><span data-stu-id="f9102-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="f9102-122">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f9102-122">0x00000002</span></span>  <br/> |<span data-ttu-id="f9102-123">Day, por ejemplo, 24x60x60 segundos</span><span class="sxs-lookup"><span data-stu-id="f9102-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="f9102-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="f9102-124">0x00000003</span></span>  <br/> |<span data-ttu-id="f9102-125">Semana, por ejemplo, 7x24x60x60 segundos</span><span class="sxs-lookup"><span data-stu-id="f9102-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f9102-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9102-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f9102-127">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="f9102-127">Protocol specifications</span></span>

<span data-ttu-id="f9102-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9102-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9102-129">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f9102-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f9102-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f9102-130">Header files</span></span>

<span data-ttu-id="f9102-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f9102-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="f9102-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f9102-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="f9102-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f9102-133">Mapitags.h</span></span>
  
> <span data-ttu-id="f9102-134">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f9102-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f9102-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9102-135">See also</span></span>



[<span data-ttu-id="f9102-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f9102-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f9102-137">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="f9102-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f9102-138">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f9102-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f9102-139">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f9102-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

