---
title: Propiedad canónica PidTagInternetReferences
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReferences
api_type:
- HeaderDef
ms.assetid: 645fe61d-414a-455e-b034-db3cfd003b9d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4558fcdba11aed92eb21972ed62320209ade77ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819639"
---
# <a name="pidtaginternetreferences-canonical-property"></a><span data-ttu-id="a17e8-103">Propiedad canónica PidTagInternetReferences</span><span class="sxs-lookup"><span data-stu-id="a17e8-103">PidTagInternetReferences Canonical Property</span></span>

  
  
<span data-ttu-id="a17e8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a17e8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a17e8-105">Contiene el valor del campo de encabezado de referencias de un mensaje de extensiones multipropósito de correo Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="a17e8-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's References header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a17e8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a17e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a17e8-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span><span class="sxs-lookup"><span data-stu-id="a17e8-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span></span>  <br/> |
|<span data-ttu-id="a17e8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a17e8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a17e8-109">0x1039</span><span class="sxs-lookup"><span data-stu-id="a17e8-109">0x1039</span></span>  <br/> |
|<span data-ttu-id="a17e8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a17e8-110">Data type:</span></span>  <br/> |<span data-ttu-id="a17e8-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a17e8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a17e8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a17e8-112">Area:</span></span>  <br/> |<span data-ttu-id="a17e8-113">MIME</span><span class="sxs-lookup"><span data-stu-id="a17e8-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a17e8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a17e8-114">Remarks</span></span>

<span data-ttu-id="a17e8-115">Para generar un campo de encabezado de referencias, los clientes deben establecer estas propiedades en el valor deseado.</span><span class="sxs-lookup"><span data-stu-id="a17e8-115">To generate a References header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="a17e8-116">Los escritores MIME deben copiar el valor de estas propiedades en el campo de encabezado de referencias.</span><span class="sxs-lookup"><span data-stu-id="a17e8-116">MIME writers must copy the value of these properties to the References header field.</span></span>
  
<span data-ttu-id="a17e8-117">Para establecer el valor de estas propiedades, los clientes MIME deben escribir el valor deseado en un campo de encabezado de referencias.</span><span class="sxs-lookup"><span data-stu-id="a17e8-117">To set the value of these properties, MIME clients must write the desired value to a References header field.</span></span> <span data-ttu-id="a17e8-118">Lectores MIME deben copiar el valor del campo de encabezado de referencias a estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a17e8-118">MIME readers must copy the value of the References header field to these properties.</span></span> <span data-ttu-id="a17e8-119">Lectores MIME pueden truncar el valor de estas propiedades si se excede 64KB de longitud.</span><span class="sxs-lookup"><span data-stu-id="a17e8-119">MIME readers may truncate the value of these properties if it exceeds 64KB in length.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a17e8-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a17e8-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a17e8-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a17e8-121">Protocol specifications</span></span>

<span data-ttu-id="a17e8-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a17e8-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a17e8-123">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a17e8-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a17e8-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a17e8-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a17e8-125">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a17e8-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a17e8-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a17e8-126">Header files</span></span>

<span data-ttu-id="a17e8-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a17e8-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="a17e8-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a17e8-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="a17e8-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a17e8-129">Mapitags.h</span></span>
  
> <span data-ttu-id="a17e8-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a17e8-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a17e8-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a17e8-131">See also</span></span>



[<span data-ttu-id="a17e8-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a17e8-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a17e8-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a17e8-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a17e8-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a17e8-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a17e8-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="a17e8-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

