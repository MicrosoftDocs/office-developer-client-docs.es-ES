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
ms.openlocfilehash: f05fa0816db3b412329372ad392c673c240eb59e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327247"
---
# <a name="pidtagattachmimetag-canonical-property"></a><span data-ttu-id="4d6a4-103">Propiedad canónica PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="4d6a4-103">PidTagAttachMimeTag Canonical Property</span></span>

  
  
<span data-ttu-id="4d6a4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d6a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d6a4-105">Contiene información de formato sobre los datos adjuntos de extensiones multipropósito al correo de Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="4d6a4-105">Contains formatting information about a Multipurpose Internet Mail Extensions (MIME) attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4d6a4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4d6a4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d6a4-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span><span class="sxs-lookup"><span data-stu-id="4d6a4-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span></span>  <br/> |
|<span data-ttu-id="4d6a4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4d6a4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4d6a4-109">0x370E</span><span class="sxs-lookup"><span data-stu-id="4d6a4-109">0x370E</span></span>  <br/> |
|<span data-ttu-id="4d6a4-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4d6a4-110">Data type:</span></span>  <br/> |<span data-ttu-id="4d6a4-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4d6a4-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4d6a4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4d6a4-112">Area:</span></span>  <br/> |<span data-ttu-id="4d6a4-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="4d6a4-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d6a4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d6a4-114">Remarks</span></span>

<span data-ttu-id="4d6a4-115">Si la **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) contiene el valor **OID_MIMETAG**, el proveedor de transporte debe buscar estas propiedades para determinar cómo se formatearán los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-115">If the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property contains the value **OID_MIMETAG**, the transport provider should look at these properties to determine how the attachment is formatted.</span></span> 
  
<span data-ttu-id="4d6a4-116">Estas propiedades se copian del parámetro content-type del encabezado MIME entrante.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-116">These properties are copied from the Content-type parameter of the inbound MIME header.</span></span> <span data-ttu-id="4d6a4-117">La composición de la cadena se define en el documento RFC 1521.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-117">The composition of the string is defined in the RFC 1521 document.</span></span> <span data-ttu-id="4d6a4-118">El formato es tipo/subtipo, como aplicación/binario o texto/sin formato.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-118">The format is type/subtype, such as application/binary or text/plain.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4d6a4-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d6a4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4d6a4-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="4d6a4-120">Protocol specifications</span></span>

<span data-ttu-id="4d6a4-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d6a4-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d6a4-122">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="4d6a4-123">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d6a4-123">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d6a4-124">Especifica las propiedades de los mensajes codificados con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-124">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4d6a4-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4d6a4-125">Header files</span></span>

<span data-ttu-id="4d6a4-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4d6a4-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d6a4-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="4d6a4-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4d6a4-128">Mapitags.h</span></span>
  
> <span data-ttu-id="4d6a4-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4d6a4-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d6a4-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4d6a4-130">See also</span></span>



[<span data-ttu-id="4d6a4-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4d6a4-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d6a4-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="4d6a4-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d6a4-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4d6a4-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d6a4-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4d6a4-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

