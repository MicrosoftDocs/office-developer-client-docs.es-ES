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
ms.openlocfilehash: 431a212b6e024d695fe2de084080996d8b1054d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360414"
---
# <a name="pidtaginternetreferences-canonical-property"></a><span data-ttu-id="407f9-103">Propiedad canónica PidTagInternetReferences</span><span class="sxs-lookup"><span data-stu-id="407f9-103">PidTagInternetReferences Canonical Property</span></span>

  
  
<span data-ttu-id="407f9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="407f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="407f9-105">Contiene el valor del campo de encabezado Referencias de un mensaje Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="407f9-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's References header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="407f9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="407f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="407f9-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span><span class="sxs-lookup"><span data-stu-id="407f9-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span></span>  <br/> |
|<span data-ttu-id="407f9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="407f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="407f9-109">0x1039</span><span class="sxs-lookup"><span data-stu-id="407f9-109">0x1039</span></span>  <br/> |
|<span data-ttu-id="407f9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="407f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="407f9-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="407f9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="407f9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="407f9-112">Area:</span></span>  <br/> |<span data-ttu-id="407f9-113">MIME</span><span class="sxs-lookup"><span data-stu-id="407f9-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="407f9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="407f9-114">Remarks</span></span>

<span data-ttu-id="407f9-115">Para generar un campo de encabezado Referencias, los clientes deben establecer estas propiedades en el valor deseado.</span><span class="sxs-lookup"><span data-stu-id="407f9-115">To generate a References header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="407f9-116">Los escritores MIME deben copiar el valor de estas propiedades en el campo de encabezado Referencias.</span><span class="sxs-lookup"><span data-stu-id="407f9-116">MIME writers must copy the value of these properties to the References header field.</span></span>
  
<span data-ttu-id="407f9-117">Para establecer el valor de estas propiedades, los clientes MIME deben escribir el valor deseado en un campo de encabezado Referencias.</span><span class="sxs-lookup"><span data-stu-id="407f9-117">To set the value of these properties, MIME clients must write the desired value to a References header field.</span></span> <span data-ttu-id="407f9-118">Los lectores MIME deben copiar el valor del campo de encabezado Referencias en estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="407f9-118">MIME readers must copy the value of the References header field to these properties.</span></span> <span data-ttu-id="407f9-119">Los lectores MIME pueden truncar el valor de estas propiedades si supera los 64 KB de longitud.</span><span class="sxs-lookup"><span data-stu-id="407f9-119">MIME readers may truncate the value of these properties if it exceeds 64KB in length.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="407f9-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="407f9-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="407f9-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="407f9-121">Protocol specifications</span></span>

<span data-ttu-id="407f9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="407f9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="407f9-123">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="407f9-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="407f9-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="407f9-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="407f9-125">Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="407f9-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="407f9-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="407f9-126">Header files</span></span>

<span data-ttu-id="407f9-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="407f9-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="407f9-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="407f9-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="407f9-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="407f9-129">Mapitags.h</span></span>
  
> <span data-ttu-id="407f9-130">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="407f9-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="407f9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="407f9-131">See also</span></span>



[<span data-ttu-id="407f9-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="407f9-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="407f9-133">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="407f9-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="407f9-134">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="407f9-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="407f9-135">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="407f9-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

