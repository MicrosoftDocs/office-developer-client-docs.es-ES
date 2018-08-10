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
ms.openlocfilehash: 14b1b424bc55a3a8c898eaac386a5344c2e5cf99
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819413"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a><span data-ttu-id="b169a-103">Propiedad canónica PidTagDeferredSendUnits</span><span class="sxs-lookup"><span data-stu-id="b169a-103">PidTagDeferredSendUnits Canonical Property</span></span>

  
  
<span data-ttu-id="b169a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b169a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b169a-105">Especifica la unidad de tiempo por el que se multiplicará el valor de la propiedad **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b169a-105">Specifies the unit of time by which the **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) property value should be multiplied.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b169a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b169a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b169a-107">PR_DEFERRED_SEND_UNITS</span><span class="sxs-lookup"><span data-stu-id="b169a-107">PR_DEFERRED_SEND_UNITS</span></span>  <br/> |
|<span data-ttu-id="b169a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b169a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b169a-109">0x3FEC</span><span class="sxs-lookup"><span data-stu-id="b169a-109">0x3FEC</span></span>  <br/> |
|<span data-ttu-id="b169a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b169a-110">Data type:</span></span>  <br/> |<span data-ttu-id="b169a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b169a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b169a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b169a-112">Area:</span></span>  <br/> |<span data-ttu-id="b169a-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="b169a-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b169a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b169a-114">Remarks</span></span>

<span data-ttu-id="b169a-115">Si se establece, esta propiedad debe tener uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="b169a-115">If set, this property must have one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b169a-116">**PidTagDeferredSendUnits**</span><span class="sxs-lookup"><span data-stu-id="b169a-116">**PidTagDeferredSendUnits**</span></span> <br/> |<span data-ttu-id="b169a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b169a-117">Description</span></span>  <br/> |
|<span data-ttu-id="b169a-118">0</span><span class="sxs-lookup"><span data-stu-id="b169a-118">0</span></span>  <br/> |<span data-ttu-id="b169a-119">Minutos, por ejemplo 60 segundos</span><span class="sxs-lookup"><span data-stu-id="b169a-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="b169a-120">1</span><span class="sxs-lookup"><span data-stu-id="b169a-120">1</span></span>  <br/> |<span data-ttu-id="b169a-121">Horas, por ejemplo 60 x 60 segundos</span><span class="sxs-lookup"><span data-stu-id="b169a-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="b169a-122">2</span><span class="sxs-lookup"><span data-stu-id="b169a-122">2</span></span>  <br/> |<span data-ttu-id="b169a-123">Día, por ejemplo 24 x 60 x 60 segundos</span><span class="sxs-lookup"><span data-stu-id="b169a-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="b169a-124">3</span><span class="sxs-lookup"><span data-stu-id="b169a-124">3</span></span>  <br/> |<span data-ttu-id="b169a-125">Semana, por ejemplo 7x24x60x60 segundos</span><span class="sxs-lookup"><span data-stu-id="b169a-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b169a-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b169a-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b169a-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b169a-127">Protocol specifications</span></span>

<span data-ttu-id="b169a-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b169a-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b169a-129">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b169a-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b169a-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b169a-130">Header files</span></span>

<span data-ttu-id="b169a-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b169a-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="b169a-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b169a-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="b169a-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b169a-133">Mapitags.h</span></span>
  
> <span data-ttu-id="b169a-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="b169a-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b169a-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b169a-135">See also</span></span>



[<span data-ttu-id="b169a-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b169a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b169a-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b169a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b169a-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b169a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b169a-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="b169a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
