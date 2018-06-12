---
title: Propiedad canónico PidTagAttachMimeTag
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 6f65d67903fa9ebb255345f8666cd53de5512cab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819245"
---
# <a name="pidtagattachmimetag-canonical-property"></a><span data-ttu-id="581a6-103">Propiedad canónico PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="581a6-103">PidTagAttachMimeTag Canonical Property</span></span>

  
  
<span data-ttu-id="581a6-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="581a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="581a6-105">Contiene información de formato sobre datos adjuntos de extensiones multipropósito de correo Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="581a6-105">Contains formatting information about a Multipurpose Internet Mail Extensions (MIME) attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="581a6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="581a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="581a6-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span><span class="sxs-lookup"><span data-stu-id="581a6-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span></span>  <br/> |
|<span data-ttu-id="581a6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="581a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="581a6-109">0x370E</span><span class="sxs-lookup"><span data-stu-id="581a6-109">0x370E</span></span>  <br/> |
|<span data-ttu-id="581a6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="581a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="581a6-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="581a6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="581a6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="581a6-112">Area:</span></span>  <br/> |<span data-ttu-id="581a6-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="581a6-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="581a6-114">Notas</span><span class="sxs-lookup"><span data-stu-id="581a6-114">Remarks</span></span>

<span data-ttu-id="581a6-115">Si la propiedad **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) contiene el valor **OID_MIMETAG**, el proveedor de transporte debe tener un aspecto en estas propiedades para determinar cómo se aplica formato a los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="581a6-115">If the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property contains the value **OID_MIMETAG**, the transport provider should look at these properties to determine how the attachment is formatted.</span></span> 
  
<span data-ttu-id="581a6-116">Estas propiedades se copian desde el parámetro de tipo de contenido del encabezado MIME entrante.</span><span class="sxs-lookup"><span data-stu-id="581a6-116">These properties are copied from the Content-type parameter of the inbound MIME header.</span></span> <span data-ttu-id="581a6-117">La composición de la cadena se define en el documento RFC 1521.</span><span class="sxs-lookup"><span data-stu-id="581a6-117">The composition of the string is defined in the RFC 1521 document.</span></span> <span data-ttu-id="581a6-118">El formato es tipo/subtipo, como aplicación/binario o texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="581a6-118">The format is type/subtype, such as application/binary or text/plain.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="581a6-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="581a6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="581a6-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="581a6-120">Protocol specifications</span></span>

<span data-ttu-id="581a6-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="581a6-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="581a6-122">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="581a6-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="581a6-123">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="581a6-123">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="581a6-124">Especifica las propiedades de mensajes codificados con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="581a6-124">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="581a6-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="581a6-125">Header files</span></span>

<span data-ttu-id="581a6-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="581a6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="581a6-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="581a6-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="581a6-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="581a6-128">Mapitags.h</span></span>
  
> <span data-ttu-id="581a6-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="581a6-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="581a6-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="581a6-130">See also</span></span>



[<span data-ttu-id="581a6-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="581a6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="581a6-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="581a6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="581a6-133">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="581a6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="581a6-134">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="581a6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

