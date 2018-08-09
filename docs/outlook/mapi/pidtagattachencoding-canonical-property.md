---
title: Propiedad canónica PidTagAttachEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cdeb432e20f2779bbb625566108551748b48a01f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819234"
---
# <a name="pidtagattachencoding-canonical-property"></a><span data-ttu-id="0196d-103">Propiedad canónica PidTagAttachEncoding</span><span class="sxs-lookup"><span data-stu-id="0196d-103">PidTagAttachEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="0196d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0196d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0196d-105">Contiene un identificador de objeto ASN.1 que especifica la codificación de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0196d-105">Contains an ASN.1 object identifier that specifies the encoding for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0196d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0196d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0196d-107">PR_ATTACH_ENCODING</span><span class="sxs-lookup"><span data-stu-id="0196d-107">PR_ATTACH_ENCODING</span></span>  <br/> |
|<span data-ttu-id="0196d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0196d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0196d-109">0x3702</span><span class="sxs-lookup"><span data-stu-id="0196d-109">0x3702</span></span>  <br/> |
|<span data-ttu-id="0196d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0196d-110">Data type:</span></span>  <br/> |<span data-ttu-id="0196d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0196d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0196d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0196d-112">Area:</span></span>  <br/> |<span data-ttu-id="0196d-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="0196d-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0196d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0196d-114">Remarks</span></span>

<span data-ttu-id="0196d-115">Esta propiedad identifica el algoritmo utilizado para transformar los datos en un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="0196d-115">This property identifies the algorithm used to transform the data in an attachment.</span></span>
  
 <span data-ttu-id="0196d-116">**Nota** No se deben confundir el **PR_ATTACH_ENCODING** y las propiedades de **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0196d-116">**Note** The **PR_ATTACH_ENCODING** and **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) properties should not be confused.</span></span> <span data-ttu-id="0196d-117">No están emparejados o relacionados con.</span><span class="sxs-lookup"><span data-stu-id="0196d-117">They are not paired or related.</span></span> <span data-ttu-id="0196d-118">**PR_ATTACH_TAG** identifica la aplicación que generó originalmente los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0196d-118">**PR_ATTACH_TAG** identifies the application that originally generated the attachment.</span></span> <span data-ttu-id="0196d-119">"Objeto" tiene un significado mucho más general en el identificador de objeto de términos y en X.400, que en la programación orientada a objetos.</span><span class="sxs-lookup"><span data-stu-id="0196d-119">"Object" has a much more general meaning in the term object identifier, and in X.400, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="0196d-120">Los identificadores de objeto de ejemplo y sintaxis de identificador de objeto se definen en el MAPIOID. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="0196d-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="0196d-121">Los valores de **PR_ATTACH_ENCODING** no se limitan a los definidos en MAPIOID. H.</span><span class="sxs-lookup"><span data-stu-id="0196d-121">Values for **PR_ATTACH_ENCODING** are not limited to those defined in MAPIOID.H.</span></span> <span data-ttu-id="0196d-122">Por ejemplo, archivos de Macintosh adjuntos pueden usar un identificador como MacBinary.</span><span class="sxs-lookup"><span data-stu-id="0196d-122">For example, attached Macintosh files can use an identifier such as MacBinary.</span></span> 
  
<span data-ttu-id="0196d-123">Para obtener información detallada sobre estos identificadores de objetos, vea la documentación en ASN.1, X.208 y X.209.</span><span class="sxs-lookup"><span data-stu-id="0196d-123">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="0196d-124">El identificador de objeto se encuentra en el elemento de referencia de la aplicación del entorno FTBP (elementos de cuerpo de transferencia de archivo).</span><span class="sxs-lookup"><span data-stu-id="0196d-124">The object identifier is found in the application-reference element of the FTBP (File Transfer Body Part) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0196d-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0196d-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0196d-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0196d-126">Protocol specifications</span></span>

<span data-ttu-id="0196d-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0196d-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0196d-128">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0196d-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0196d-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0196d-129">Header files</span></span>

<span data-ttu-id="0196d-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0196d-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="0196d-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0196d-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="0196d-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0196d-132">Mapitags.h</span></span>
  
> <span data-ttu-id="0196d-133">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0196d-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0196d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="0196d-134">See also</span></span>



[<span data-ttu-id="0196d-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0196d-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0196d-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0196d-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0196d-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0196d-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0196d-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="0196d-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

