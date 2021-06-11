---
title: Propiedad canónica PidTagListSubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bee11c495d7f1ef21f9af70e6aa89f8c0d0f78b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279660"
---
# <a name="pidtaglistsubscribe-canonical-property"></a><span data-ttu-id="2eec4-103">Propiedad canónica PidTagListSubscribe</span><span class="sxs-lookup"><span data-stu-id="2eec4-103">PidTagListSubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="2eec4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2eec4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2eec4-105">Contiene el valor del campo de encabezado de un mensaje Multipurpose Internet Mail Extensions (MIME List-Subscribe).</span><span class="sxs-lookup"><span data-stu-id="2eec4-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Subscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2eec4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2eec4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2eec4-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="2eec4-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="2eec4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2eec4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2eec4-109">0x1044</span><span class="sxs-lookup"><span data-stu-id="2eec4-109">0x1044</span></span>  <br/> |
|<span data-ttu-id="2eec4-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2eec4-110">Data type:</span></span>  <br/> |<span data-ttu-id="2eec4-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2eec4-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2eec4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2eec4-112">Area:</span></span>  <br/> |<span data-ttu-id="2eec4-113">Varios</span><span class="sxs-lookup"><span data-stu-id="2eec4-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2eec4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2eec4-114">Remarks</span></span>

<span data-ttu-id="2eec4-115">Para generar un List-Subscribe de encabezado, los clientes deben establecer el valor de estas propiedades en el valor deseado.</span><span class="sxs-lookup"><span data-stu-id="2eec4-115">To generate a List-Subscribe header field, clients must set the value of these properties to the desired value.</span></span> <span data-ttu-id="2eec4-116">Los escritores MIME deben copiar el valor de estas propiedades en el List-Subscribe de encabezado.</span><span class="sxs-lookup"><span data-stu-id="2eec4-116">MIME writers must copy the value of these properties to the List-Subscribe header field.</span></span>
  
<span data-ttu-id="2eec4-117">Para establecer el valor de propiedades relacionadas con el servidor como estas, los clientes MIME deben escribir los campos de encabezado como se especifica en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2eec4-117">To set the value of server-related properties like these, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="2eec4-118">**Property**</span><span class="sxs-lookup"><span data-stu-id="2eec4-118">**Property**</span></span>|<span data-ttu-id="2eec4-119">**Nombre de campo de encabezado preferido**</span><span class="sxs-lookup"><span data-stu-id="2eec4-119">**Preferred header field name**</span></span>|<span data-ttu-id="2eec4-120">**Nombre de campo de encabezado alternativo**</span><span class="sxs-lookup"><span data-stu-id="2eec4-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2eec4-121">**PidTagListSubscribe**</span><span class="sxs-lookup"><span data-stu-id="2eec4-121">**PidTagListSubscribe**</span></span> <br/> |<span data-ttu-id="2eec4-122">List-Subscribe</span><span class="sxs-lookup"><span data-stu-id="2eec4-122">List-Subscribe</span></span>  <br/> |<span data-ttu-id="2eec4-123">X-List-Subscribe</span><span class="sxs-lookup"><span data-stu-id="2eec4-123">X-List-Subscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2eec4-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2eec4-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2eec4-125">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="2eec4-125">Protocol specifications</span></span>

<span data-ttu-id="2eec4-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2eec4-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2eec4-127">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="2eec4-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2eec4-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2eec4-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2eec4-129">Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="2eec4-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2eec4-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2eec4-130">Header files</span></span>

<span data-ttu-id="2eec4-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2eec4-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="2eec4-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2eec4-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="2eec4-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2eec4-133">Mapitags.h</span></span>
  
> <span data-ttu-id="2eec4-134">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2eec4-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2eec4-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="2eec4-135">See also</span></span>



[<span data-ttu-id="2eec4-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2eec4-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2eec4-137">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2eec4-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2eec4-138">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2eec4-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2eec4-139">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2eec4-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

