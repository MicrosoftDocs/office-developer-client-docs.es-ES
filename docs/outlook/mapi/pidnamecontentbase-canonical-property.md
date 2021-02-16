---
title: Propiedad canónica PidNameContentBase
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 501b54cfb7846a91aec7172cbe1d846c24704923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331503"
---
# <a name="pidnamecontentbase-canonical-property"></a><span data-ttu-id="3a0aa-103">Propiedad canónica PidNameContentBase</span><span class="sxs-lookup"><span data-stu-id="3a0aa-103">PidNameContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="3a0aa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a0aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a0aa-105">Contiene un valor de campo de encabezado Base de contenido [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="3a0aa-105">Contains an [RFC3282] Content-Base header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3a0aa-106">Nombres descriptivos:</span><span class="sxs-lookup"><span data-stu-id="3a0aa-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="3a0aa-107">BodyContentBase</span><span class="sxs-lookup"><span data-stu-id="3a0aa-107">BodyContentBase</span></span>  <br/> |
|<span data-ttu-id="3a0aa-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="3a0aa-108">Property set:</span></span>  <br/> |<span data-ttu-id="3a0aa-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="3a0aa-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="3a0aa-110">Nombre de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="3a0aa-110">Property name:</span></span>  <br/> |<span data-ttu-id="3a0aa-111">Content-Base</span><span class="sxs-lookup"><span data-stu-id="3a0aa-111">Content-Base</span></span>  <br/> |
|<span data-ttu-id="3a0aa-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3a0aa-112">Data type:</span></span>  <br/> |<span data-ttu-id="3a0aa-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3a0aa-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3a0aa-114">Área:</span><span class="sxs-lookup"><span data-stu-id="3a0aa-114">Area:</span></span>  <br/> |<span data-ttu-id="3a0aa-115">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="3a0aa-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a0aa-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3a0aa-116">Remarks</span></span>

<span data-ttu-id="3a0aa-117">Para establecer el valor de esta propiedad, los clientes de Extensiones multipropósito a mensajes de Internet (MIME) deben escribir el valor deseado en un campo de encabezado Base de contenido en una entidad MIME que se asigna a un cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="3a0aa-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to a Content-Base header field on a MIME entity that maps to a message body.</span></span> <span data-ttu-id="3a0aa-118">Los lectores MIME deben copiar el valor de un campo de encabezado Content-Base en dicha entidad MIME en el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="3a0aa-118">MIME readers must copy the value of a Content-Base header field on such a MIME entity to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3a0aa-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a0aa-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3a0aa-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="3a0aa-120">Protocol specifications</span></span>

<span data-ttu-id="3a0aa-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a0aa-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a0aa-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="3a0aa-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3a0aa-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a0aa-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a0aa-124">Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="3a0aa-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3a0aa-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3a0aa-125">Header files</span></span>

<span data-ttu-id="3a0aa-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a0aa-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="3a0aa-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3a0aa-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a0aa-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3a0aa-128">See also</span></span>



[<span data-ttu-id="3a0aa-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3a0aa-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3a0aa-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="3a0aa-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3a0aa-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3a0aa-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3a0aa-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="3a0aa-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

