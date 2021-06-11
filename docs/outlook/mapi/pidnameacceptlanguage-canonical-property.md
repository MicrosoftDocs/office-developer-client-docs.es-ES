---
title: Propiedad canónica PidNameAcceptLanguage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameAcceptLanguage
api_type:
- COM
ms.assetid: 4b202bc1-f718-446a-950f-634ffee47baf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 855610c43cfaa64fa69e6987743b137b188d84a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360945"
---
# <a name="pidnameacceptlanguage-canonical-property"></a><span data-ttu-id="2a38b-103">Propiedad canónica PidNameAcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="2a38b-103">PidNameAcceptLanguage Canonical Property</span></span>

  
  
<span data-ttu-id="2a38b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a38b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a38b-105">Contiene un valor de campo de encabezado Accept-Language [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="2a38b-105">Contains an [RFC3282] Accept-Language header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a38b-106">Nombres descriptivos:</span><span class="sxs-lookup"><span data-stu-id="2a38b-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="2a38b-107">AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="2a38b-107">AcceptLanguage</span></span>  <br/> |
|<span data-ttu-id="2a38b-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="2a38b-108">Property set:</span></span>  <br/> |<span data-ttu-id="2a38b-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="2a38b-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="2a38b-110">Nombre de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="2a38b-110">Property name:</span></span>  <br/> |<span data-ttu-id="2a38b-111">Accept-Language</span><span class="sxs-lookup"><span data-stu-id="2a38b-111">Accept-Language</span></span>  <br/> |
|<span data-ttu-id="2a38b-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2a38b-112">Data type:</span></span>  <br/> |<span data-ttu-id="2a38b-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2a38b-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2a38b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="2a38b-114">Area:</span></span>  <br/> |<span data-ttu-id="2a38b-115">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="2a38b-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a38b-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2a38b-116">Remarks</span></span>

<span data-ttu-id="2a38b-117">Para establecer el valor de esta propiedad, los clientes de Multipurpose Internet Message Extensions (MIME) deben escribir un campo Accept-Language encabezado con el valor deseado.</span><span class="sxs-lookup"><span data-stu-id="2a38b-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients should write an Accept-Language header field with the desired value.</span></span> <span data-ttu-id="2a38b-118">En su lugar, los clientes MIME pueden escribir un campo de encabezado X-Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="2a38b-118">MIME clients may write an X-Accept-Language header field instead.</span></span> <span data-ttu-id="2a38b-119">Los lectores MIME deben copiar el valor de cualquier campo de encabezado en el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2a38b-119">MIME readers should copy the value of either header field to the value of this property.</span></span> <span data-ttu-id="2a38b-120">Si ambos campos de encabezado están presentes, los lectores MIME deben usar el Accept-Language de encabezado.</span><span class="sxs-lookup"><span data-stu-id="2a38b-120">If both header fields are present, MIME readers should use the Accept-Language header field.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2a38b-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a38b-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2a38b-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="2a38b-122">Protocol specifications</span></span>

<span data-ttu-id="2a38b-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a38b-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a38b-124">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="2a38b-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2a38b-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a38b-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a38b-126">Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="2a38b-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2a38b-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2a38b-127">Header files</span></span>

<span data-ttu-id="2a38b-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2a38b-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="2a38b-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2a38b-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a38b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a38b-130">See also</span></span>



[<span data-ttu-id="2a38b-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2a38b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2a38b-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2a38b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2a38b-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2a38b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2a38b-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2a38b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

