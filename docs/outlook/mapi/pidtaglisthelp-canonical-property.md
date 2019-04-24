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
ms.openlocfilehash: 588747205ee3922fef7b107dc024f074a6ee527e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279632"
---
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="0aa73-103">Propiedad canónica PidTagListHelp</span><span class="sxs-lookup"><span data-stu-id="0aa73-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="0aa73-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0aa73-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0aa73-105">Contiene el valor del campo de encabezado de la ayuda de la lista de un mensaje de extensiones de correo de Internet multipropósito (MIME).</span><span class="sxs-lookup"><span data-stu-id="0aa73-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0aa73-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0aa73-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0aa73-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="0aa73-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="0aa73-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0aa73-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0aa73-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="0aa73-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="0aa73-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0aa73-110">Data type:</span></span>  <br/> |<span data-ttu-id="0aa73-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0aa73-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0aa73-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0aa73-112">Area:</span></span>  <br/> |<span data-ttu-id="0aa73-113">Varios</span><span class="sxs-lookup"><span data-stu-id="0aa73-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0aa73-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0aa73-114">Remarks</span></span>

<span data-ttu-id="0aa73-115">Para generar un campo de encabezado de la ayuda de lista, los clientes deben establecer el valor de **PR_LIST_HELP** o una propiedad asociada con el valor deseado.</span><span class="sxs-lookup"><span data-stu-id="0aa73-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="0aa73-116">Los escritores MIME deben copiar este valor en el campo de encabezado List-help.</span><span class="sxs-lookup"><span data-stu-id="0aa73-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="0aa73-117">Para establecer el valor de estas propiedades relacionadas con el servidor de listas, los clientes MIME deben escribir los campos de encabezado como se especifica en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="0aa73-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="0aa73-118">**Property**</span><span class="sxs-lookup"><span data-stu-id="0aa73-118">**Property**</span></span>|<span data-ttu-id="0aa73-119">**Nombre de campo de encabezado preferido**</span><span class="sxs-lookup"><span data-stu-id="0aa73-119">**Preferred header field name**</span></span>|<span data-ttu-id="0aa73-120">**Nombre de campo de encabezado alternativo**</span><span class="sxs-lookup"><span data-stu-id="0aa73-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0aa73-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="0aa73-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="0aa73-122">List-Help</span><span class="sxs-lookup"><span data-stu-id="0aa73-122">List-Help</span></span>  <br/> |<span data-ttu-id="0aa73-123">X-List-Help</span><span class="sxs-lookup"><span data-stu-id="0aa73-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0aa73-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0aa73-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0aa73-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0aa73-125">Protocol specifications</span></span>

<span data-ttu-id="0aa73-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0aa73-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0aa73-127">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0aa73-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0aa73-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0aa73-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0aa73-129">Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="0aa73-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0aa73-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0aa73-130">Header files</span></span>

<span data-ttu-id="0aa73-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0aa73-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="0aa73-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0aa73-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="0aa73-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0aa73-133">Mapitags.h</span></span>
  
> <span data-ttu-id="0aa73-134">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0aa73-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0aa73-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="0aa73-135">See also</span></span>



[<span data-ttu-id="0aa73-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0aa73-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0aa73-137">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="0aa73-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0aa73-138">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0aa73-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0aa73-139">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="0aa73-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

