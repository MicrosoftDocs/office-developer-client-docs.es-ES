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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361085"
---
# <a name="pidtagattachtag-canonical-property"></a><span data-ttu-id="2ef6e-103">Propiedad canónica PidTagAttachTag</span><span class="sxs-lookup"><span data-stu-id="2ef6e-103">PidTagAttachTag Canonical Property</span></span>

  
  
<span data-ttu-id="2ef6e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ef6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ef6e-105">Contiene un identificador de objeto ASN. 1 que especifica la aplicación que suministró un dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="2ef6e-105">Contains an ASN.1 object identifier specifying the application that supplied an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2ef6e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2ef6e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ef6e-107">PR_ATTACH_TAG</span><span class="sxs-lookup"><span data-stu-id="2ef6e-107">PR_ATTACH_TAG</span></span>  <br/> |
|<span data-ttu-id="2ef6e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2ef6e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ef6e-109">0x370A</span><span class="sxs-lookup"><span data-stu-id="2ef6e-109">0x370A</span></span>  <br/> |
|<span data-ttu-id="2ef6e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2ef6e-110">Data type:</span></span>  <br/> |<span data-ttu-id="2ef6e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2ef6e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2ef6e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2ef6e-112">Area:</span></span>  <br/> |<span data-ttu-id="2ef6e-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="2ef6e-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ef6e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2ef6e-114">Remarks</span></span>

<span data-ttu-id="2ef6e-115">Esta propiedad identifica la aplicación que generó originalmente los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="2ef6e-115">This property identifies the application that originally generated the attachment.</span></span>
  
 <span data-ttu-id="2ef6e-116">**Nota:** Las propiedades **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) y **PR_ATTACH_TAG** no deben confundirse.</span><span class="sxs-lookup"><span data-stu-id="2ef6e-116">**Note** The **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) and **PR_ATTACH_TAG** properties should not be confused.</span></span> <span data-ttu-id="2ef6e-117">No están emparejados ni relacionados.</span><span class="sxs-lookup"><span data-stu-id="2ef6e-117">They are not paired or related.</span></span> <span data-ttu-id="2ef6e-118">**PR_ATTACH_ENCODING** identifica el algoritmo que se usa para transformar los datos en datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="2ef6e-118">**PR_ATTACH_ENCODING** identifies the algorithm used to transform the data in an attachment.</span></span> <span data-ttu-id="2ef6e-119">"Objeto" tiene un significado mucho más general en el identificador de objeto term y en el uso de X. 400, que en la programación orientada a objetos.</span><span class="sxs-lookup"><span data-stu-id="2ef6e-119">"Object" has a much more general meaning in the term object identifier, and in X.400 usage, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="2ef6e-120">La sintaxis del identificador de objeto y los identificadores de objeto de ejemplo se definen en MAPIOID. H archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="2ef6e-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="2ef6e-121">Los valores de **PR_ATTACH_TAG** no se limitan a los definidos en MAPIOID. H.</span><span class="sxs-lookup"><span data-stu-id="2ef6e-121">Values for **PR_ATTACH_TAG** are not limited to those defined in MAPIOID.H.</span></span> 
  
<span data-ttu-id="2ef6e-122">Para obtener información completa sobre estos identificadores de objeto, consulte la documentación de ASN. 1, X. 208 y X. 209.</span><span class="sxs-lookup"><span data-stu-id="2ef6e-122">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="2ef6e-123">El identificador de objeto se encuentra en el elemento Application-Reference del entorno de la parte del cuerpo de la transferencia de archivos (FTBP).</span><span class="sxs-lookup"><span data-stu-id="2ef6e-123">The object identifier is found in the application-reference element of the File Transfer Body Part (FTBP) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2ef6e-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ef6e-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ef6e-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="2ef6e-125">Protocol specifications</span></span>

<span data-ttu-id="2ef6e-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ef6e-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ef6e-127">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="2ef6e-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ef6e-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2ef6e-128">Header files</span></span>

<span data-ttu-id="2ef6e-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2ef6e-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ef6e-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2ef6e-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="2ef6e-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2ef6e-131">Mapitags.h</span></span>
  
> <span data-ttu-id="2ef6e-132">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2ef6e-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ef6e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ef6e-133">See also</span></span>



[<span data-ttu-id="2ef6e-134">Propiedad canónica PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="2ef6e-134">PidTagAttachMimeTag Canonical Property</span></span>](pidtagattachmimetag-canonical-property.md)


[<span data-ttu-id="2ef6e-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2ef6e-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ef6e-136">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="2ef6e-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ef6e-137">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2ef6e-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ef6e-138">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2ef6e-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

