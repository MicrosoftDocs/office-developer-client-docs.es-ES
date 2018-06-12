---
title: Propiedad canónico PidNameContentBase
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentBase
api_type:
- COM
ms.assetid: ab197ace-6e7d-4ec5-9f6d-4a63a1eda11c
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 21469b944bb2ce5db0576e40012335d89d48cb49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819113"
---
# <a name="pidnamecontentbase-canonical-property"></a><span data-ttu-id="c6b35-103">Propiedad canónico PidNameContentBase</span><span class="sxs-lookup"><span data-stu-id="c6b35-103">PidNameContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="c6b35-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c6b35-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c6b35-105">Contiene un valor de campo de encabezado de Base de contenido de [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="c6b35-105">Contains an [RFC3282] Content-Base header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c6b35-106">Nombres descriptivos:</span><span class="sxs-lookup"><span data-stu-id="c6b35-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="c6b35-107">BodyContentBase</span><span class="sxs-lookup"><span data-stu-id="c6b35-107">BodyContentBase</span></span>  <br/> |
|<span data-ttu-id="c6b35-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="c6b35-108">Property set:</span></span>  <br/> |<span data-ttu-id="c6b35-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="c6b35-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="c6b35-110">Nombre de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="c6b35-110">Property name:</span></span>  <br/> |<span data-ttu-id="c6b35-111">Base de contenido</span><span class="sxs-lookup"><span data-stu-id="c6b35-111">Content-Base</span></span>  <br/> |
|<span data-ttu-id="c6b35-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c6b35-112">Data type:</span></span>  <br/> |<span data-ttu-id="c6b35-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c6b35-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c6b35-114">Área:</span><span class="sxs-lookup"><span data-stu-id="c6b35-114">Area:</span></span>  <br/> |<span data-ttu-id="c6b35-115">Email</span><span class="sxs-lookup"><span data-stu-id="c6b35-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6b35-116">Notas</span><span class="sxs-lookup"><span data-stu-id="c6b35-116">Remarks</span></span>

<span data-ttu-id="c6b35-117">Para establecer el valor de esta propiedad, los clientes de extensiones multipropósito de mensaje de Internet (MIME) deben escribir el valor deseado a un campo de encabezado Content-Base en una entidad MIME que se asigna a un cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c6b35-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to a Content-Base header field on a MIME entity that maps to a message body.</span></span> <span data-ttu-id="c6b35-118">Lectores MIME deben copiar el valor de un campo de encabezado Content-Base en dicha una entidad MIME para el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c6b35-118">MIME readers must copy the value of a Content-Base header field on such a MIME entity to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c6b35-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6b35-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c6b35-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c6b35-120">Protocol specifications</span></span>

<span data-ttu-id="c6b35-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6b35-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6b35-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c6b35-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c6b35-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6b35-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6b35-124">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c6b35-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c6b35-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c6b35-125">Header files</span></span>

<span data-ttu-id="c6b35-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c6b35-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c6b35-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c6b35-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c6b35-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="c6b35-128">See also</span></span>



[<span data-ttu-id="c6b35-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c6b35-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c6b35-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c6b35-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c6b35-131">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="c6b35-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c6b35-132">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c6b35-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

