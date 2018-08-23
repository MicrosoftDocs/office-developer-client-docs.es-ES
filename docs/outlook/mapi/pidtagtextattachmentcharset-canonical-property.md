---
title: Propiedad canónica PidTagTextAttachmentCharset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTextAttachmentCharset
api_type:
- COM
ms.assetid: d347c949-d0c3-4a36-8447-3fa01111cdc1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cec34819cfa2c6e790f8808eb5bab70412f286b5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591432"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="8bf18-103">Propiedad canónica PidTagTextAttachmentCharset</span><span class="sxs-lookup"><span data-stu-id="8bf18-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="8bf18-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bf18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bf18-105">Contiene el valor de conjunto de caracteres de un mensaje de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="8bf18-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8bf18-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8bf18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8bf18-107">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8bf18-107">None</span></span>  <br/> |
|<span data-ttu-id="8bf18-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8bf18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8bf18-109">0x371B</span><span class="sxs-lookup"><span data-stu-id="8bf18-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="8bf18-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8bf18-110">Data type:</span></span>  <br/> |<span data-ttu-id="8bf18-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8bf18-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8bf18-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8bf18-112">Area:</span></span>  <br/> |<span data-ttu-id="8bf18-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="8bf18-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8bf18-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8bf18-114">Remarks</span></span>

<span data-ttu-id="8bf18-115">Los datos de esta propiedad se derivarán de un campo de encabezado Content-Type MIME que comienza por "texto /", si un parámetro "charset" está presente.</span><span class="sxs-lookup"><span data-stu-id="8bf18-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8bf18-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8bf18-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8bf18-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8bf18-117">Protocol specifications</span></span>

<span data-ttu-id="8bf18-118">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bf18-118">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bf18-119">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8bf18-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8bf18-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8bf18-120">Header files</span></span>

<span data-ttu-id="8bf18-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8bf18-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="8bf18-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8bf18-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="8bf18-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8bf18-123">Mapitags.h</span></span>
  
> <span data-ttu-id="8bf18-124">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8bf18-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8bf18-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8bf18-125">See also</span></span>



[<span data-ttu-id="8bf18-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8bf18-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8bf18-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="8bf18-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8bf18-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8bf18-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8bf18-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="8bf18-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

