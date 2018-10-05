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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387247"
---
# <a name="pidnameacceptlanguage-canonical-property"></a><span data-ttu-id="2ddb0-103">Propiedad canónica PidNameAcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="2ddb0-103">PidNameAcceptLanguage Canonical Property</span></span>

  
  
<span data-ttu-id="2ddb0-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ddb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ddb0-105">Contiene un valor de campo de encabezado Accept-Language de [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="2ddb0-105">Contains an [RFC3282] Accept-Language header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ddb0-106">Nombres descriptivos:</span><span class="sxs-lookup"><span data-stu-id="2ddb0-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="2ddb0-107">AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="2ddb0-107">AcceptLanguage</span></span>  <br/> |
|<span data-ttu-id="2ddb0-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="2ddb0-108">Property set:</span></span>  <br/> |<span data-ttu-id="2ddb0-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="2ddb0-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="2ddb0-110">Nombre de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="2ddb0-110">Property name:</span></span>  <br/> |<span data-ttu-id="2ddb0-111">Idioma acepte</span><span class="sxs-lookup"><span data-stu-id="2ddb0-111">Accept-Language</span></span>  <br/> |
|<span data-ttu-id="2ddb0-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2ddb0-112">Data type:</span></span>  <br/> |<span data-ttu-id="2ddb0-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2ddb0-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2ddb0-114">Área:</span><span class="sxs-lookup"><span data-stu-id="2ddb0-114">Area:</span></span>  <br/> |<span data-ttu-id="2ddb0-115">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="2ddb0-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ddb0-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2ddb0-116">Remarks</span></span>

<span data-ttu-id="2ddb0-117">Para establecer el valor de esta propiedad, los clientes de extensiones multipropósito de mensaje de Internet (MIME) deben escribir un campo de encabezado Accept-Language con el valor deseado.</span><span class="sxs-lookup"><span data-stu-id="2ddb0-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients should write an Accept-Language header field with the desired value.</span></span> <span data-ttu-id="2ddb0-118">Los clientes MIME pueden escribir un campo de encabezado X-Accept-Language en su lugar.</span><span class="sxs-lookup"><span data-stu-id="2ddb0-118">MIME clients may write an X-Accept-Language header field instead.</span></span> <span data-ttu-id="2ddb0-119">Lectores MIME deben copiar el valor de cualquier campo de encabezado para el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2ddb0-119">MIME readers should copy the value of either header field to the value of this property.</span></span> <span data-ttu-id="2ddb0-120">Si ambos campos de encabezado están presentes, lectores MIME deben usar el campo de encabezado Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="2ddb0-120">If both header fields are present, MIME readers should use the Accept-Language header field.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2ddb0-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ddb0-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ddb0-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="2ddb0-122">Protocol specifications</span></span>

<span data-ttu-id="2ddb0-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ddb0-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ddb0-124">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="2ddb0-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2ddb0-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ddb0-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ddb0-126">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="2ddb0-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ddb0-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2ddb0-127">Header files</span></span>

<span data-ttu-id="2ddb0-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ddb0-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ddb0-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2ddb0-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ddb0-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ddb0-130">See also</span></span>



[<span data-ttu-id="2ddb0-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2ddb0-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ddb0-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="2ddb0-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ddb0-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2ddb0-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ddb0-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="2ddb0-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

