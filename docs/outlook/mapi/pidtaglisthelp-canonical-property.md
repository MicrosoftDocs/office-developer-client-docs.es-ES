---
title: Propiedad canónica PidTagListHelp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListHelp
api_type:
- HeaderDef
ms.assetid: 403324b8-c992-4823-aa0f-0414b283debc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7a9a5d090babce8105fab43bf8401448373777cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819711"
---
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="ecd4e-103">Propiedad canónica PidTagListHelp</span><span class="sxs-lookup"><span data-stu-id="ecd4e-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="ecd4e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ecd4e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ecd4e-105">Contiene el valor del campo de encabezado de Ayuda de la lista de un mensaje de extensiones multipropósito de correo Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="ecd4e-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ecd4e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ecd4e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ecd4e-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="ecd4e-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="ecd4e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ecd4e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ecd4e-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="ecd4e-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="ecd4e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ecd4e-110">Data type:</span></span>  <br/> |<span data-ttu-id="ecd4e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ecd4e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ecd4e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ecd4e-112">Area:</span></span>  <br/> |<span data-ttu-id="ecd4e-113">Varios</span><span class="sxs-lookup"><span data-stu-id="ecd4e-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecd4e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ecd4e-114">Remarks</span></span>

<span data-ttu-id="ecd4e-115">Para generar un campo de encabezado de Ayuda de la lista, los clientes deben establecer el valor de **PR_LIST_HELP** o una propiedad asociada en el valor deseado.</span><span class="sxs-lookup"><span data-stu-id="ecd4e-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="ecd4e-116">Los escritores MIME deben copiar este valor en el campo de encabezado de Ayuda de la lista.</span><span class="sxs-lookup"><span data-stu-id="ecd4e-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="ecd4e-117">Para establecer el valor de estas propiedades relacionadas con el servidor de lista, los clientes MIME deben escribir los campos de encabezado tal como se especifica en la siguiente tabla:</span><span class="sxs-lookup"><span data-stu-id="ecd4e-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="ecd4e-118">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="ecd4e-118">**Property**</span></span>|<span data-ttu-id="ecd4e-119">**Nombre de campo de encabezado preferido**</span><span class="sxs-lookup"><span data-stu-id="ecd4e-119">**Preferred header field name**</span></span>|<span data-ttu-id="ecd4e-120">**Nombre de campo de encabezado alternativo**</span><span class="sxs-lookup"><span data-stu-id="ecd4e-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ecd4e-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="ecd4e-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="ecd4e-122">Ayuda de la lista</span><span class="sxs-lookup"><span data-stu-id="ecd4e-122">List-Help</span></span>  <br/> |<span data-ttu-id="ecd4e-123">X-lista-Help</span><span class="sxs-lookup"><span data-stu-id="ecd4e-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ecd4e-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ecd4e-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ecd4e-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="ecd4e-125">Protocol specifications</span></span>

<span data-ttu-id="ecd4e-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecd4e-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecd4e-127">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ecd4e-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ecd4e-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecd4e-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecd4e-129">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ecd4e-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ecd4e-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ecd4e-130">Header files</span></span>

<span data-ttu-id="ecd4e-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecd4e-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="ecd4e-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ecd4e-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="ecd4e-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ecd4e-133">Mapitags.h</span></span>
  
> <span data-ttu-id="ecd4e-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ecd4e-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ecd4e-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecd4e-135">See also</span></span>



[<span data-ttu-id="ecd4e-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ecd4e-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ecd4e-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="ecd4e-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ecd4e-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ecd4e-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ecd4e-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="ecd4e-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

