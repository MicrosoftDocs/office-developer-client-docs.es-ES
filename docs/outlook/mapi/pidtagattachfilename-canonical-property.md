---
title: Propiedad canónica PidTagAttachFilename
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFilename
api_type:
- HeaderDef
ms.assetid: cbf34dd6-7733-47f6-9c41-9d82656ca9dc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f5dcf90e8224f1bf2e96042a7344109293cc2c3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319225"
---
# <a name="pidtagattachfilename-canonical-property"></a><span data-ttu-id="52d24-103">Propiedad canónica PidTagAttachFilename</span><span class="sxs-lookup"><span data-stu-id="52d24-103">PidTagAttachFilename Canonical Property</span></span>

  
  
<span data-ttu-id="52d24-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52d24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52d24-105">Contiene el nombre y la extensión del archivo base de datos adjuntos, excepto la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="52d24-105">Contains an attachment's base file name and extension, excluding path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52d24-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="52d24-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52d24-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="52d24-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="52d24-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="52d24-108">Identifier:</span></span>  <br/> |<span data-ttu-id="52d24-109">0x3704</span><span class="sxs-lookup"><span data-stu-id="52d24-109">0x3704</span></span>  <br/> |
|<span data-ttu-id="52d24-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="52d24-110">Data type:</span></span>  <br/> |<span data-ttu-id="52d24-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="52d24-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="52d24-112">Área:</span><span class="sxs-lookup"><span data-stu-id="52d24-112">Area:</span></span>  <br/> |<span data-ttu-id="52d24-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="52d24-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52d24-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52d24-114">Remarks</span></span>

<span data-ttu-id="52d24-115">Se recomienda que los objetos Attachment expongan estas propiedades que pertenecen a los valores **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**y **ATTACH_BY_REF_ONLY** de la **PR_ATTACH_METHOD** Propiedad ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="52d24-115">It is recommended that attachment objects expose these properties which pertain to the **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, and **ATTACH_BY_REF_ONLY** values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="52d24-116">**PR_ATTACH_FILENAME** y las propiedades asociadas son necesarias cuando se usa cualquiera de estos valores.</span><span class="sxs-lookup"><span data-stu-id="52d24-116">**PR_ATTACH_FILENAME** and associated properties are required when any of these values is used.</span></span> 
  
<span data-ttu-id="52d24-117">Estas propiedades se pueden usar como un nombre de archivo sugerido para guardar los datos adjuntos y para proporcionar la extensión del nombre de archivo si no se proporciona la propiedad **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="52d24-117">These properties can be used as a suggested file name for saving the attachment and to supply the file name extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="52d24-118">El nombre de archivo está restringido a ocho caracteres más una extensión de tres caracteres.</span><span class="sxs-lookup"><span data-stu-id="52d24-118">The file name is restricted to eight characters plus a three-character extension.</span></span> <span data-ttu-id="52d24-119">Para una plataforma que admite nombres de archivo largos, establezca esta propiedad y la propiedad **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="52d24-119">For a platform that supports long file names, set both this property and the **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="52d24-120">MAPI solo funciona con los nombres de archivo y otras cadenas que se le pasan, en el juego de caracteres ANSI (American National Standards Institute).</span><span class="sxs-lookup"><span data-stu-id="52d24-120">MAPI works only with file names, and other strings passed to it, in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="52d24-121">Las aplicaciones cliente que usan nombres de archivo en un conjunto de caracteres OEM (fabricante de equipos originales) deben convertirlos a ANSI antes de llamar a MAPI.</span><span class="sxs-lookup"><span data-stu-id="52d24-121">Client applications that use file names in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="52d24-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="52d24-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="52d24-123">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="52d24-123">Protocol specifications</span></span>

<span data-ttu-id="52d24-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52d24-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52d24-125">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="52d24-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="52d24-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52d24-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52d24-127">Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="52d24-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="52d24-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52d24-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52d24-129">Especifica las propiedades de los mensajes codificados con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="52d24-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="52d24-130">[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52d24-130">[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52d24-131">Especifica las propiedades de los mensajes firmados y cifrados S/MIME.</span><span class="sxs-lookup"><span data-stu-id="52d24-131">Specifies S/MIME signed and encrypted message properties.</span></span>
    
<span data-ttu-id="52d24-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52d24-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52d24-133">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="52d24-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="52d24-134">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="52d24-134">Header files</span></span>

<span data-ttu-id="52d24-135">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="52d24-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="52d24-136">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="52d24-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="52d24-137">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="52d24-137">Mapitags.h</span></span>
  
> <span data-ttu-id="52d24-138">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="52d24-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52d24-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="52d24-139">See also</span></span>



[<span data-ttu-id="52d24-140">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="52d24-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52d24-141">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="52d24-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52d24-142">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="52d24-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52d24-143">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="52d24-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

