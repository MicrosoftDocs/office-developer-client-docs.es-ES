---
title: Propiedad canónica PidNameContentClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentClass
api_type:
- COM
ms.assetid: 6f623345-b30e-452f-a822-9308b455697a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 51788a49d1c0d01ef7ff5daca853000a8f1e34a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356353"
---
# <a name="pidnamecontentclass-canonical-property"></a><span data-ttu-id="7c57f-103">Propiedad canónica PidNameContentClass</span><span class="sxs-lookup"><span data-stu-id="7c57f-103">PidNameContentClass Canonical Property</span></span>

  
  
<span data-ttu-id="7c57f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c57f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c57f-105">Contiene un valor de campo de encabezado de clase de contenido [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="7c57f-105">Contains an [RFC3282] Content-Class header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c57f-106">Nombres descriptivos:</span><span class="sxs-lookup"><span data-stu-id="7c57f-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="7c57f-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7c57f-107">None</span></span>  <br/> |
|<span data-ttu-id="7c57f-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="7c57f-108">Property set:</span></span>  <br/> |<span data-ttu-id="7c57f-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="7c57f-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="7c57f-110">Nombre de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="7c57f-110">Property name:</span></span>  <br/> |<span data-ttu-id="7c57f-111">Content-Class</span><span class="sxs-lookup"><span data-stu-id="7c57f-111">Content-Class</span></span>  <br/> |
|<span data-ttu-id="7c57f-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7c57f-112">Data type:</span></span>  <br/> |<span data-ttu-id="7c57f-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7c57f-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7c57f-114">Área:</span><span class="sxs-lookup"><span data-stu-id="7c57f-114">Area:</span></span>  <br/> |<span data-ttu-id="7c57f-115">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="7c57f-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c57f-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7c57f-116">Remarks</span></span>

<span data-ttu-id="7c57f-117">Para establecer el valor de esta propiedad, los clientes de Extensiones multipropósito a mensajes de Internet (MIME) deben escribir un campo de encabezado Content-Class con el valor deseado.</span><span class="sxs-lookup"><span data-stu-id="7c57f-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write a Content-Class header field with the desired value.</span></span> <span data-ttu-id="7c57f-118">Los lectores MIME deben copiar el valor de un campo de encabezado Content-Class en el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="7c57f-118">MIME readers must copy the value of a Content-Class header field to the value of this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7c57f-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7c57f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7c57f-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="7c57f-120">Protocol specifications</span></span>

<span data-ttu-id="7c57f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c57f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c57f-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="7c57f-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7c57f-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c57f-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c57f-124">Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="7c57f-124">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="7c57f-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c57f-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c57f-126">Especifica las propiedades de los mensajes codificados con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="7c57f-126">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7c57f-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7c57f-127">Header files</span></span>

<span data-ttu-id="7c57f-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7c57f-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c57f-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7c57f-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c57f-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7c57f-130">See also</span></span>



[<span data-ttu-id="7c57f-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7c57f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c57f-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="7c57f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c57f-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7c57f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c57f-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7c57f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

