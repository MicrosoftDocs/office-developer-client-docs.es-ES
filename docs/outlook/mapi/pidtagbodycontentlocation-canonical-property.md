---
title: Propiedad canónica PidTagBodyContentLocation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyContentLocation
api_type:
- HeaderDef
ms.assetid: a66d1c64-5c5a-4980-9acd-72448108fd2c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4b10daf3bdc11d406b6f7248fd6aaa9e3c6c2a68
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584719"
---
# <a name="pidtagbodycontentlocation-canonical-property"></a><span data-ttu-id="354be-103">Propiedad canónica PidTagBodyContentLocation</span><span class="sxs-lookup"><span data-stu-id="354be-103">PidTagBodyContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="354be-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="354be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="354be-105">Contiene el valor de un campo de encabezado MIME Content-Location.</span><span class="sxs-lookup"><span data-stu-id="354be-105">Contains the value of a MIME Content-Location header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="354be-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="354be-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="354be-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="354be-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="354be-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="354be-108">Identifier:</span></span>  <br/> |<span data-ttu-id="354be-109">0x1014</span><span class="sxs-lookup"><span data-stu-id="354be-109">0x1014</span></span>  <br/> |
|<span data-ttu-id="354be-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="354be-110">Data type:</span></span>  <br/> |<span data-ttu-id="354be-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="354be-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="354be-112">Área:</span><span class="sxs-lookup"><span data-stu-id="354be-112">Area:</span></span>  <br/> |<span data-ttu-id="354be-113">MIME</span><span class="sxs-lookup"><span data-stu-id="354be-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="354be-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="354be-114">Remarks</span></span>

<span data-ttu-id="354be-115">Para establecer el valor de estas propiedades, los clientes MIME deben escribir el valor deseado en un campo de encabezado Content-Location en una entidad MIME que se asigna a un cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="354be-115">To set the value of these properties, MIME clients should write the desired value to a Content-Location header field on a MIME entity that maps to a message body.</span></span>
  
<span data-ttu-id="354be-116">Lectores MIME deben copiar el valor de un campo de encabezado Content-Location en dicha una entidad MIME para el valor de estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="354be-116">MIME readers should copy the value of a Content-Location header field on such a MIME entity to the value of these properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="354be-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="354be-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="354be-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="354be-118">Protocol specifications</span></span>

<span data-ttu-id="354be-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="354be-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="354be-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="354be-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="354be-121">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="354be-121">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="354be-122">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="354be-122">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="354be-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="354be-123">Header files</span></span>

<span data-ttu-id="354be-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="354be-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="354be-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="354be-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="354be-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="354be-126">Mapitags.h</span></span>
  
> <span data-ttu-id="354be-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="354be-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="354be-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="354be-128">See also</span></span>



[<span data-ttu-id="354be-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="354be-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="354be-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="354be-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="354be-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="354be-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="354be-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="354be-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

