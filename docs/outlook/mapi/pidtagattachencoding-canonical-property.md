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
ms.openlocfilehash: 4bda4783012a3a5cd50d9c0aea6a37ccd238b660
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345496"
---
# <a name="pidtagattachencoding-canonical-property"></a><span data-ttu-id="84d39-103">Propiedad canónica PidTagAttachEncoding</span><span class="sxs-lookup"><span data-stu-id="84d39-103">PidTagAttachEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="84d39-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84d39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84d39-105">Contiene un identificador de objeto ASN.1 que especifica la codificación de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="84d39-105">Contains an ASN.1 object identifier that specifies the encoding for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84d39-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="84d39-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84d39-107">PR_ATTACH_ENCODING</span><span class="sxs-lookup"><span data-stu-id="84d39-107">PR_ATTACH_ENCODING</span></span>  <br/> |
|<span data-ttu-id="84d39-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="84d39-108">Identifier:</span></span>  <br/> |<span data-ttu-id="84d39-109">0x3702</span><span class="sxs-lookup"><span data-stu-id="84d39-109">0x3702</span></span>  <br/> |
|<span data-ttu-id="84d39-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="84d39-110">Data type:</span></span>  <br/> |<span data-ttu-id="84d39-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="84d39-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="84d39-112">Área:</span><span class="sxs-lookup"><span data-stu-id="84d39-112">Area:</span></span>  <br/> |<span data-ttu-id="84d39-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="84d39-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84d39-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="84d39-114">Remarks</span></span>

<span data-ttu-id="84d39-115">Esta propiedad identifica el algoritmo usado para transformar los datos de un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="84d39-115">This property identifies the algorithm used to transform the data in an attachment.</span></span>
  
 <span data-ttu-id="84d39-116">**Nota** Las **PR_ATTACH_ENCODING** y **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) no deben confundirse.</span><span class="sxs-lookup"><span data-stu-id="84d39-116">**Note** The **PR_ATTACH_ENCODING** and **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) properties should not be confused.</span></span> <span data-ttu-id="84d39-117">No están emparejados ni relacionados.</span><span class="sxs-lookup"><span data-stu-id="84d39-117">They are not paired or related.</span></span> <span data-ttu-id="84d39-118">**PR_ATTACH_TAG** identifica la aplicación que generó originalmente los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="84d39-118">**PR_ATTACH_TAG** identifies the application that originally generated the attachment.</span></span> <span data-ttu-id="84d39-119">"Object" tiene un significado mucho más general en el identificador de objeto de término, y en X.400, que en la programación orientada a objetos.</span><span class="sxs-lookup"><span data-stu-id="84d39-119">"Object" has a much more general meaning in the term object identifier, and in X.400, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="84d39-120">La sintaxis del identificador de objeto y los identificadores de objeto de ejemplo se definen en MAPIOID. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="84d39-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="84d39-121">Los valores **PR_ATTACH_ENCODING** no se limitan a los definidos en MAPIOID.H.</span><span class="sxs-lookup"><span data-stu-id="84d39-121">Values for **PR_ATTACH_ENCODING** are not limited to those defined in MAPIOID.H.</span></span> <span data-ttu-id="84d39-122">Por ejemplo, los archivos Macintosh adjuntos pueden usar un identificador como MacBinary.</span><span class="sxs-lookup"><span data-stu-id="84d39-122">For example, attached Macintosh files can use an identifier such as MacBinary.</span></span> 
  
<span data-ttu-id="84d39-123">Para obtener información completa sobre estos identificadores de objeto, consulte la documentación de ASN.1, X.208 y X.209.</span><span class="sxs-lookup"><span data-stu-id="84d39-123">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="84d39-124">El identificador del objeto se encuentra en el elemento de referencia de aplicación del entorno FTBP (file transfer body part).</span><span class="sxs-lookup"><span data-stu-id="84d39-124">The object identifier is found in the application-reference element of the FTBP (File Transfer Body Part) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="84d39-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="84d39-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84d39-126">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="84d39-126">Protocol specifications</span></span>

<span data-ttu-id="84d39-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84d39-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84d39-128">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="84d39-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84d39-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="84d39-129">Header files</span></span>

<span data-ttu-id="84d39-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84d39-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="84d39-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="84d39-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="84d39-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="84d39-132">Mapitags.h</span></span>
  
> <span data-ttu-id="84d39-133">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="84d39-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84d39-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="84d39-134">See also</span></span>



[<span data-ttu-id="84d39-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="84d39-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84d39-136">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="84d39-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84d39-137">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="84d39-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84d39-138">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="84d39-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

