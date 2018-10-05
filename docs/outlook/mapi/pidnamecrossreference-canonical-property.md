---
title: Propiedad canónica PidNameCrossReference
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameCrossReference
api_type:
- COM
ms.assetid: d16e1adf-c911-427e-9c98-678a303e6791
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8f8706ec3db36cddbe7be7420ba27683c190cd43
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382501"
---
# <a name="pidnamecrossreference-canonical-property"></a><span data-ttu-id="0178c-103">Propiedad canónica PidNameCrossReference</span><span class="sxs-lookup"><span data-stu-id="0178c-103">PidNameCrossReference Canonical Property</span></span>

  
  
<span data-ttu-id="0178c-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0178c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0178c-105">Contiene un valor de campo de encabezado de ref [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="0178c-105">Contains an [RFC3282] Xref header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0178c-106">Nombres descriptivos:</span><span class="sxs-lookup"><span data-stu-id="0178c-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="0178c-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0178c-107">None</span></span>  <br/> |
|<span data-ttu-id="0178c-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="0178c-108">Property set:</span></span>  <br/> |<span data-ttu-id="0178c-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="0178c-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="0178c-110">Nombre de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="0178c-110">Property name:</span></span>  <br/> |<span data-ttu-id="0178c-111">Ref</span><span class="sxs-lookup"><span data-stu-id="0178c-111">Xref</span></span>  <br/> |
|<span data-ttu-id="0178c-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0178c-112">Data type:</span></span>  <br/> |<span data-ttu-id="0178c-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0178c-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0178c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0178c-114">Area:</span></span>  <br/> |<span data-ttu-id="0178c-115">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="0178c-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0178c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0178c-116">Remarks</span></span>

<span data-ttu-id="0178c-117">Para establecer el valor de esta propiedad, los clientes de extensiones multipropósito de mensaje de Internet (MIME) deben escribir el valor deseado en un campo de encabezado de ref.</span><span class="sxs-lookup"><span data-stu-id="0178c-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to an XRef header field.</span></span> <span data-ttu-id="0178c-118">Lectores MIME deben copiar el valor de un campo de encabezado ref en el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0178c-118">MIME readers must copy the value of an XRef header field to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0178c-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0178c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0178c-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0178c-120">Protocol specifications</span></span>

<span data-ttu-id="0178c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0178c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0178c-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0178c-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0178c-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0178c-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0178c-124">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="0178c-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0178c-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0178c-125">Header files</span></span>

<span data-ttu-id="0178c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0178c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0178c-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0178c-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0178c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0178c-128">See also</span></span>



[<span data-ttu-id="0178c-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0178c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0178c-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0178c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0178c-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0178c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0178c-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="0178c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

