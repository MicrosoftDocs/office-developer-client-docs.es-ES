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
ms.openlocfilehash: 90a873174b5b990f165d0b2173efa38fc7df2d9d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394920"
---
# <a name="pidtagbodycontentlocation-canonical-property"></a><span data-ttu-id="01940-103">Propiedad canónica PidTagBodyContentLocation</span><span class="sxs-lookup"><span data-stu-id="01940-103">PidTagBodyContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="01940-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01940-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01940-105">Contiene el valor de un campo de encabezado MIME Content-Location.</span><span class="sxs-lookup"><span data-stu-id="01940-105">Contains the value of a MIME Content-Location header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="01940-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="01940-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="01940-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="01940-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="01940-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="01940-108">Identifier:</span></span>  <br/> |<span data-ttu-id="01940-109">0x1014</span><span class="sxs-lookup"><span data-stu-id="01940-109">0x1014</span></span>  <br/> |
|<span data-ttu-id="01940-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="01940-110">Data type:</span></span>  <br/> |<span data-ttu-id="01940-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="01940-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="01940-112">Área:</span><span class="sxs-lookup"><span data-stu-id="01940-112">Area:</span></span>  <br/> |<span data-ttu-id="01940-113">MIME</span><span class="sxs-lookup"><span data-stu-id="01940-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01940-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="01940-114">Remarks</span></span>

<span data-ttu-id="01940-115">Para establecer el valor de estas propiedades, los clientes MIME deben escribir el valor deseado en un campo de encabezado Content-Location en una entidad MIME que se asigna a un cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="01940-115">To set the value of these properties, MIME clients should write the desired value to a Content-Location header field on a MIME entity that maps to a message body.</span></span>
  
<span data-ttu-id="01940-116">Lectores MIME deben copiar el valor de un campo de encabezado Content-Location en dicha una entidad MIME para el valor de estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="01940-116">MIME readers should copy the value of a Content-Location header field on such a MIME entity to the value of these properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="01940-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="01940-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="01940-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="01940-118">Protocol specifications</span></span>

<span data-ttu-id="01940-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01940-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01940-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="01940-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="01940-121">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01940-121">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01940-122">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="01940-122">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="01940-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="01940-123">Header files</span></span>

<span data-ttu-id="01940-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="01940-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="01940-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="01940-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="01940-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="01940-126">Mapitags.h</span></span>
  
> <span data-ttu-id="01940-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="01940-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="01940-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="01940-128">See also</span></span>



[<span data-ttu-id="01940-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="01940-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="01940-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="01940-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="01940-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="01940-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="01940-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="01940-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

