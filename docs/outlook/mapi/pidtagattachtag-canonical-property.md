---
title: Propiedad canónico PidTagAttachTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTag
api_type:
- HeaderDef
ms.assetid: 3d223809-b697-47c6-bc3c-2206aff7ad33
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: d8d8d32bddb98e0ac180b0898478c67297980492
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819271"
---
# <a name="pidtagattachtag-canonical-property"></a><span data-ttu-id="b9012-103">Propiedad canónico PidTagAttachTag</span><span class="sxs-lookup"><span data-stu-id="b9012-103">PidTagAttachTag Canonical Property</span></span>

  
  
<span data-ttu-id="b9012-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b9012-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b9012-105">Contiene un identificador de objeto ASN.1 que especifica la aplicación que suministró un dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="b9012-105">Contains an ASN.1 object identifier specifying the application that supplied an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b9012-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b9012-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b9012-107">PR_ATTACH_TAG</span><span class="sxs-lookup"><span data-stu-id="b9012-107">PR_ATTACH_TAG</span></span>  <br/> |
|<span data-ttu-id="b9012-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b9012-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b9012-109">0x370A</span><span class="sxs-lookup"><span data-stu-id="b9012-109">0x370A</span></span>  <br/> |
|<span data-ttu-id="b9012-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b9012-110">Data type:</span></span>  <br/> |<span data-ttu-id="b9012-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b9012-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b9012-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b9012-112">Area:</span></span>  <br/> |<span data-ttu-id="b9012-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="b9012-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9012-114">Notas</span><span class="sxs-lookup"><span data-stu-id="b9012-114">Remarks</span></span>

<span data-ttu-id="b9012-115">Esta propiedad identifica la aplicación que generó originalmente los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="b9012-115">This property identifies the application that originally generated the attachment.</span></span>
  
 <span data-ttu-id="b9012-116">**Nota** No se deben confundir las propiedades **PR_ATTACH_TAG** y **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b9012-116">**Note** The **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) and **PR_ATTACH_TAG** properties should not be confused.</span></span> <span data-ttu-id="b9012-117">No están emparejados o relacionados con.</span><span class="sxs-lookup"><span data-stu-id="b9012-117">They are not paired or related.</span></span> <span data-ttu-id="b9012-118">**PR_ATTACH_ENCODING** identifica el algoritmo utilizado para transformar los datos en un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="b9012-118">**PR_ATTACH_ENCODING** identifies the algorithm used to transform the data in an attachment.</span></span> <span data-ttu-id="b9012-119">"Objeto" tiene un significado mucho más general en el identificador de objeto de términos y en el uso X.400, que en la programación orientada a objetos.</span><span class="sxs-lookup"><span data-stu-id="b9012-119">"Object" has a much more general meaning in the term object identifier, and in X.400 usage, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="b9012-120">Los identificadores de objeto de ejemplo y sintaxis de identificador de objeto se definen en el MAPIOID. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="b9012-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="b9012-121">Los valores de **PR_ATTACH_TAG** no se limitan a los definidos en MAPIOID. H.</span><span class="sxs-lookup"><span data-stu-id="b9012-121">Values for **PR_ATTACH_TAG** are not limited to those defined in MAPIOID.H.</span></span> 
  
<span data-ttu-id="b9012-122">Para obtener información detallada sobre estos identificadores de objetos, vea la documentación en ASN.1, X.208 y X.209.</span><span class="sxs-lookup"><span data-stu-id="b9012-122">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="b9012-123">El identificador de objeto se encuentra en el elemento de referencia de la aplicación del entorno de parte de cuerpo de transferencia de archivo (FTBP).</span><span class="sxs-lookup"><span data-stu-id="b9012-123">The object identifier is found in the application-reference element of the File Transfer Body Part (FTBP) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b9012-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b9012-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b9012-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b9012-125">Protocol specifications</span></span>

<span data-ttu-id="b9012-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9012-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9012-127">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="b9012-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b9012-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b9012-128">Header files</span></span>

<span data-ttu-id="b9012-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b9012-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="b9012-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b9012-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="b9012-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b9012-131">Mapitags.h</span></span>
  
> <span data-ttu-id="b9012-132">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="b9012-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b9012-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="b9012-133">See also</span></span>



[<span data-ttu-id="b9012-134">Propiedad canónico PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="b9012-134">PidTagAttachMimeTag Canonical Property</span></span>](pidtagattachmimetag-canonical-property.md)


[<span data-ttu-id="b9012-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b9012-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b9012-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b9012-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b9012-137">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="b9012-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b9012-138">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b9012-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

