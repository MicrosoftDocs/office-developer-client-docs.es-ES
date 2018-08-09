---
title: Propiedad canónica PidTagAttachMimeTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMimeTag
api_type:
- HeaderDef
ms.assetid: cbc4585d-f970-4b22-ac08-d7fc91bff3d3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6f65d67903fa9ebb255345f8666cd53de5512cab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819245"
---
# <a name="pidtagattachmimetag-canonical-property"></a><span data-ttu-id="5b291-103">Propiedad canónica PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="5b291-103">PidTagAttachMimeTag Canonical Property</span></span>

  
  
<span data-ttu-id="5b291-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5b291-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5b291-105">Contiene información de formato sobre datos adjuntos de extensiones multipropósito de correo Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="5b291-105">Contains formatting information about a Multipurpose Internet Mail Extensions (MIME) attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5b291-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5b291-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b291-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span><span class="sxs-lookup"><span data-stu-id="5b291-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span></span>  <br/> |
|<span data-ttu-id="5b291-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5b291-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5b291-109">0x370E</span><span class="sxs-lookup"><span data-stu-id="5b291-109">0x370E</span></span>  <br/> |
|<span data-ttu-id="5b291-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5b291-110">Data type:</span></span>  <br/> |<span data-ttu-id="5b291-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5b291-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5b291-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5b291-112">Area:</span></span>  <br/> |<span data-ttu-id="5b291-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="5b291-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b291-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5b291-114">Remarks</span></span>

<span data-ttu-id="5b291-115">Si la propiedad **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) contiene el valor **OID_MIMETAG**, el proveedor de transporte debe tener un aspecto en estas propiedades para determinar cómo se aplica formato a los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="5b291-115">If the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property contains the value **OID_MIMETAG**, the transport provider should look at these properties to determine how the attachment is formatted.</span></span> 
  
<span data-ttu-id="5b291-116">Estas propiedades se copian desde el parámetro de tipo de contenido del encabezado MIME entrante.</span><span class="sxs-lookup"><span data-stu-id="5b291-116">These properties are copied from the Content-type parameter of the inbound MIME header.</span></span> <span data-ttu-id="5b291-117">La composición de la cadena se define en el documento RFC 1521.</span><span class="sxs-lookup"><span data-stu-id="5b291-117">The composition of the string is defined in the RFC 1521 document.</span></span> <span data-ttu-id="5b291-118">El formato es tipo/subtipo, como aplicación/binario o texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="5b291-118">The format is type/subtype, such as application/binary or text/plain.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5b291-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b291-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5b291-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5b291-120">Protocol specifications</span></span>

<span data-ttu-id="5b291-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b291-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b291-122">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="5b291-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="5b291-123">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b291-123">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b291-124">Especifica las propiedades de mensajes codificados con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="5b291-124">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5b291-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5b291-125">Header files</span></span>

<span data-ttu-id="5b291-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b291-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b291-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5b291-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="5b291-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5b291-128">Mapitags.h</span></span>
  
> <span data-ttu-id="5b291-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5b291-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b291-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b291-130">See also</span></span>



[<span data-ttu-id="5b291-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5b291-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b291-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5b291-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b291-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5b291-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b291-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5b291-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

