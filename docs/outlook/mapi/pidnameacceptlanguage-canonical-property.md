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
ms.openlocfilehash: f66a570273d78f63ced110a4bdc8a12a49c531b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595247"
---
# <a name="pidnameacceptlanguage-canonical-property"></a><span data-ttu-id="352fe-103">Propiedad canónica PidNameAcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="352fe-103">PidNameAcceptLanguage Canonical Property</span></span>

  
  
<span data-ttu-id="352fe-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="352fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="352fe-105">Contiene un valor de campo de encabezado Accept-Language de [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="352fe-105">Contains an [RFC3282] Accept-Language header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="352fe-106">Nombres descriptivos:</span><span class="sxs-lookup"><span data-stu-id="352fe-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="352fe-107">AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="352fe-107">AcceptLanguage</span></span>  <br/> |
|<span data-ttu-id="352fe-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="352fe-108">Property set:</span></span>  <br/> |<span data-ttu-id="352fe-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="352fe-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="352fe-110">Nombre de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="352fe-110">Property name:</span></span>  <br/> |<span data-ttu-id="352fe-111">Idioma acepte</span><span class="sxs-lookup"><span data-stu-id="352fe-111">Accept-Language</span></span>  <br/> |
|<span data-ttu-id="352fe-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="352fe-112">Data type:</span></span>  <br/> |<span data-ttu-id="352fe-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="352fe-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="352fe-114">Área:</span><span class="sxs-lookup"><span data-stu-id="352fe-114">Area:</span></span>  <br/> |<span data-ttu-id="352fe-115">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="352fe-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="352fe-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="352fe-116">Remarks</span></span>

<span data-ttu-id="352fe-117">Para establecer el valor de esta propiedad, los clientes de extensiones multipropósito de mensaje de Internet (MIME) deben escribir un campo de encabezado Accept-Language con el valor deseado.</span><span class="sxs-lookup"><span data-stu-id="352fe-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients should write an Accept-Language header field with the desired value.</span></span> <span data-ttu-id="352fe-118">Los clientes MIME pueden escribir un campo de encabezado X-Accept-Language en su lugar.</span><span class="sxs-lookup"><span data-stu-id="352fe-118">MIME clients may write an X-Accept-Language header field instead.</span></span> <span data-ttu-id="352fe-119">Lectores MIME deben copiar el valor de cualquier campo de encabezado para el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="352fe-119">MIME readers should copy the value of either header field to the value of this property.</span></span> <span data-ttu-id="352fe-120">Si ambos campos de encabezado están presentes, lectores MIME deben usar el campo de encabezado Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="352fe-120">If both header fields are present, MIME readers should use the Accept-Language header field.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="352fe-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="352fe-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="352fe-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="352fe-122">Protocol specifications</span></span>

<span data-ttu-id="352fe-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="352fe-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="352fe-124">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="352fe-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="352fe-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="352fe-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="352fe-126">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="352fe-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="352fe-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="352fe-127">Header files</span></span>

<span data-ttu-id="352fe-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="352fe-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="352fe-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="352fe-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="352fe-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="352fe-130">See also</span></span>



[<span data-ttu-id="352fe-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="352fe-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="352fe-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="352fe-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="352fe-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="352fe-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="352fe-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="352fe-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

