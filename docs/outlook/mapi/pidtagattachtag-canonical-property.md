---
title: Propiedad canónica PidTagAttachTag
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5a908b3543dff5cf011c9bd4d5d05b3a07004ead
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400456"
---
# <a name="pidtagattachtag-canonical-property"></a><span data-ttu-id="08a4b-103">Propiedad canónica PidTagAttachTag</span><span class="sxs-lookup"><span data-stu-id="08a4b-103">PidTagAttachTag Canonical Property</span></span>

  
  
<span data-ttu-id="08a4b-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08a4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08a4b-105">Contiene un identificador de objeto ASN.1 que especifica la aplicación que suministró un dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="08a4b-105">Contains an ASN.1 object identifier specifying the application that supplied an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08a4b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="08a4b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08a4b-107">PR_ATTACH_TAG</span><span class="sxs-lookup"><span data-stu-id="08a4b-107">PR_ATTACH_TAG</span></span>  <br/> |
|<span data-ttu-id="08a4b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="08a4b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08a4b-109">0x370A</span><span class="sxs-lookup"><span data-stu-id="08a4b-109">0x370A</span></span>  <br/> |
|<span data-ttu-id="08a4b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="08a4b-110">Data type:</span></span>  <br/> |<span data-ttu-id="08a4b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="08a4b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="08a4b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="08a4b-112">Area:</span></span>  <br/> |<span data-ttu-id="08a4b-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="08a4b-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08a4b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="08a4b-114">Remarks</span></span>

<span data-ttu-id="08a4b-115">Esta propiedad identifica la aplicación que generó originalmente los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="08a4b-115">This property identifies the application that originally generated the attachment.</span></span>
  
 <span data-ttu-id="08a4b-116">**Nota** No se deben confundir las propiedades **PR_ATTACH_TAG** y **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="08a4b-116">**Note** The **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) and **PR_ATTACH_TAG** properties should not be confused.</span></span> <span data-ttu-id="08a4b-117">No están emparejados o relacionados con.</span><span class="sxs-lookup"><span data-stu-id="08a4b-117">They are not paired or related.</span></span> <span data-ttu-id="08a4b-118">**PR_ATTACH_ENCODING** identifica el algoritmo utilizado para transformar los datos en un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="08a4b-118">**PR_ATTACH_ENCODING** identifies the algorithm used to transform the data in an attachment.</span></span> <span data-ttu-id="08a4b-119">"Objeto" tiene un significado mucho más general en el identificador de objeto de términos y en el uso X.400, que en la programación orientada a objetos.</span><span class="sxs-lookup"><span data-stu-id="08a4b-119">"Object" has a much more general meaning in the term object identifier, and in X.400 usage, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="08a4b-120">Los identificadores de objeto de ejemplo y sintaxis de identificador de objeto se definen en el MAPIOID. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="08a4b-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="08a4b-121">Los valores de **PR_ATTACH_TAG** no se limitan a los definidos en MAPIOID. H.</span><span class="sxs-lookup"><span data-stu-id="08a4b-121">Values for **PR_ATTACH_TAG** are not limited to those defined in MAPIOID.H.</span></span> 
  
<span data-ttu-id="08a4b-122">Para obtener información detallada sobre estos identificadores de objetos, vea la documentación en ASN.1, X.208 y X.209.</span><span class="sxs-lookup"><span data-stu-id="08a4b-122">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="08a4b-123">El identificador de objeto se encuentra en el elemento de referencia de la aplicación del entorno de parte de cuerpo de transferencia de archivo (FTBP).</span><span class="sxs-lookup"><span data-stu-id="08a4b-123">The object identifier is found in the application-reference element of the File Transfer Body Part (FTBP) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="08a4b-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="08a4b-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08a4b-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="08a4b-125">Protocol specifications</span></span>

<span data-ttu-id="08a4b-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08a4b-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08a4b-127">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="08a4b-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08a4b-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="08a4b-128">Header files</span></span>

<span data-ttu-id="08a4b-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08a4b-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="08a4b-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="08a4b-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="08a4b-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="08a4b-131">Mapitags.h</span></span>
  
> <span data-ttu-id="08a4b-132">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="08a4b-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08a4b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="08a4b-133">See also</span></span>



[<span data-ttu-id="08a4b-134">Propiedad canónica PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="08a4b-134">PidTagAttachMimeTag Canonical Property</span></span>](pidtagattachmimetag-canonical-property.md)


[<span data-ttu-id="08a4b-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="08a4b-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08a4b-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="08a4b-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08a4b-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="08a4b-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08a4b-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="08a4b-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

