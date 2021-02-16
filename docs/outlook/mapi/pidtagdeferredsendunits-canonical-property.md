---
title: Propiedad canónica PidTagDeferredSendUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendUnits
api_type:
- HeaderDef
ms.assetid: 2386be9f-18c9-4949-a2aa-efc8e212801c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: becc076efe0f4f805eb2a8db071b70ad731ee256
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359909"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a><span data-ttu-id="d94f5-103">Propiedad canónica PidTagDeferredSendUnits</span><span class="sxs-lookup"><span data-stu-id="d94f5-103">PidTagDeferredSendUnits Canonical Property</span></span>

  
  
<span data-ttu-id="d94f5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d94f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d94f5-105">Especifica la unidad de tiempo por la que se debe multiplicar **el valor PR_DEFERRED_SEND_NUMBER** propiedad ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d94f5-105">Specifies the unit of time by which the **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) property value should be multiplied.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d94f5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d94f5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d94f5-107">PR_DEFERRED_SEND_UNITS</span><span class="sxs-lookup"><span data-stu-id="d94f5-107">PR_DEFERRED_SEND_UNITS</span></span>  <br/> |
|<span data-ttu-id="d94f5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d94f5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d94f5-109">0x3FEC</span><span class="sxs-lookup"><span data-stu-id="d94f5-109">0x3FEC</span></span>  <br/> |
|<span data-ttu-id="d94f5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d94f5-110">Data type:</span></span>  <br/> |<span data-ttu-id="d94f5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d94f5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d94f5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d94f5-112">Area:</span></span>  <br/> |<span data-ttu-id="d94f5-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="d94f5-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d94f5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d94f5-114">Remarks</span></span>

<span data-ttu-id="d94f5-115">Si se establece, esta propiedad debe tener uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="d94f5-115">If set, this property must have one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d94f5-116">**PidTagDeferredSendUnits**</span><span class="sxs-lookup"><span data-stu-id="d94f5-116">**PidTagDeferredSendUnits**</span></span> <br/> |<span data-ttu-id="d94f5-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d94f5-117">Description</span></span>  <br/> |
|<span data-ttu-id="d94f5-118">0</span><span class="sxs-lookup"><span data-stu-id="d94f5-118">0</span></span>  <br/> |<span data-ttu-id="d94f5-119">Minutos, por ejemplo, 60 segundos</span><span class="sxs-lookup"><span data-stu-id="d94f5-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="d94f5-120">1 </span><span class="sxs-lookup"><span data-stu-id="d94f5-120">1</span></span>  <br/> |<span data-ttu-id="d94f5-121">Horas, por ejemplo, 60 x 60 segundos</span><span class="sxs-lookup"><span data-stu-id="d94f5-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="d94f5-122">2 </span><span class="sxs-lookup"><span data-stu-id="d94f5-122">2</span></span>  <br/> |<span data-ttu-id="d94f5-123">Día, por ejemplo 24 x 60 x 60 segundos</span><span class="sxs-lookup"><span data-stu-id="d94f5-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="d94f5-124">3 </span><span class="sxs-lookup"><span data-stu-id="d94f5-124">3</span></span>  <br/> |<span data-ttu-id="d94f5-125">Semana, por ejemplo, 7 x 24 x 60 x 60 segundos</span><span class="sxs-lookup"><span data-stu-id="d94f5-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d94f5-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d94f5-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d94f5-127">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="d94f5-127">Protocol specifications</span></span>

<span data-ttu-id="d94f5-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d94f5-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d94f5-129">Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="d94f5-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d94f5-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d94f5-130">Header files</span></span>

<span data-ttu-id="d94f5-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d94f5-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="d94f5-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d94f5-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="d94f5-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d94f5-133">Mapitags.h</span></span>
  
> <span data-ttu-id="d94f5-134">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d94f5-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d94f5-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d94f5-135">See also</span></span>



[<span data-ttu-id="d94f5-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d94f5-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d94f5-137">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="d94f5-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d94f5-138">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d94f5-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d94f5-139">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="d94f5-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

