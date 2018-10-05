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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389606"
---
# <a name="pidtaglistsubscribe-canonical-property"></a><span data-ttu-id="66809-103">Propiedad canónica PidTagListSubscribe</span><span class="sxs-lookup"><span data-stu-id="66809-103">PidTagListSubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="66809-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66809-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66809-105">Contiene el valor del campo de encabezado de suscribirse a la lista de un mensaje de extensiones multipropósito de correo Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="66809-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Subscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="66809-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="66809-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66809-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="66809-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="66809-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="66809-108">Identifier:</span></span>  <br/> |<span data-ttu-id="66809-109">0x1044</span><span class="sxs-lookup"><span data-stu-id="66809-109">0x1044</span></span>  <br/> |
|<span data-ttu-id="66809-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="66809-110">Data type:</span></span>  <br/> |<span data-ttu-id="66809-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="66809-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="66809-112">Área:</span><span class="sxs-lookup"><span data-stu-id="66809-112">Area:</span></span>  <br/> |<span data-ttu-id="66809-113">Varios</span><span class="sxs-lookup"><span data-stu-id="66809-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66809-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="66809-114">Remarks</span></span>

<span data-ttu-id="66809-115">Para generar un campo de encabezado suscribirse a la lista, los clientes deben establecer el valor de estas propiedades en el valor deseado.</span><span class="sxs-lookup"><span data-stu-id="66809-115">To generate a List-Subscribe header field, clients must set the value of these properties to the desired value.</span></span> <span data-ttu-id="66809-116">Los escritores MIME deben copiar el valor de estas propiedades en el campo de encabezado de suscribirse a la lista.</span><span class="sxs-lookup"><span data-stu-id="66809-116">MIME writers must copy the value of these properties to the List-Subscribe header field.</span></span>
  
<span data-ttu-id="66809-117">Para establecer el valor de las propiedades relacionadas con el servidor como estos, los clientes MIME deben escribir los campos de encabezado tal como se especifica en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="66809-117">To set the value of server-related properties like these, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="66809-118">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="66809-118">**Property**</span></span>|<span data-ttu-id="66809-119">**Nombre de campo de encabezado preferido**</span><span class="sxs-lookup"><span data-stu-id="66809-119">**Preferred header field name**</span></span>|<span data-ttu-id="66809-120">**Nombre de campo de encabezado alternativo**</span><span class="sxs-lookup"><span data-stu-id="66809-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="66809-121">**PidTagListSubscribe**</span><span class="sxs-lookup"><span data-stu-id="66809-121">**PidTagListSubscribe**</span></span> <br/> |<span data-ttu-id="66809-122">Suscríbase a la lista</span><span class="sxs-lookup"><span data-stu-id="66809-122">List-Subscribe</span></span>  <br/> |<span data-ttu-id="66809-123">Lista de X suscribirse</span><span class="sxs-lookup"><span data-stu-id="66809-123">X-List-Subscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="66809-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="66809-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="66809-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="66809-125">Protocol specifications</span></span>

<span data-ttu-id="66809-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66809-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66809-127">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="66809-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="66809-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66809-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66809-129">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="66809-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="66809-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="66809-130">Header files</span></span>

<span data-ttu-id="66809-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66809-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="66809-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="66809-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="66809-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="66809-133">Mapitags.h</span></span>
  
> <span data-ttu-id="66809-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="66809-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66809-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="66809-135">See also</span></span>



[<span data-ttu-id="66809-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="66809-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66809-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="66809-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66809-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="66809-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66809-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="66809-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

