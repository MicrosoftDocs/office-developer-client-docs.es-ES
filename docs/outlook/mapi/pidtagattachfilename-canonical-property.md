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
# <a name="pidtagattachfilename-canonical-property"></a><span data-ttu-id="11fc1-103">Propiedad canónica PidTagAttachFilename</span><span class="sxs-lookup"><span data-stu-id="11fc1-103">PidTagAttachFilename Canonical Property</span></span>

  
  
<span data-ttu-id="11fc1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11fc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11fc1-105">Contiene el nombre de archivo base y la extensión de un archivo adjunto, excluyendo la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="11fc1-105">Contains an attachment's base file name and extension, excluding path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11fc1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="11fc1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11fc1-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="11fc1-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="11fc1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="11fc1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="11fc1-109">0x3704</span><span class="sxs-lookup"><span data-stu-id="11fc1-109">0x3704</span></span>  <br/> |
|<span data-ttu-id="11fc1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="11fc1-110">Data type:</span></span>  <br/> |<span data-ttu-id="11fc1-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="11fc1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="11fc1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="11fc1-112">Area:</span></span>  <br/> |<span data-ttu-id="11fc1-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="11fc1-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11fc1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="11fc1-114">Remarks</span></span>

<span data-ttu-id="11fc1-115">Se recomienda que los objetos de datos adjuntos exponan estas propiedades que pertenecen a los valores **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, ATTACH_BY_REF_RESOLVE y **ATTACH_BY_REF_ONLY** de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)). </span><span class="sxs-lookup"><span data-stu-id="11fc1-115">It is recommended that attachment objects expose these properties which pertain to the **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, and **ATTACH_BY_REF_ONLY** values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="11fc1-116">**PR_ATTACH_FILENAME** y las propiedades asociadas son necesarias cuando se usa cualquiera de estos valores.</span><span class="sxs-lookup"><span data-stu-id="11fc1-116">**PR_ATTACH_FILENAME** and associated properties are required when any of these values is used.</span></span> 
  
<span data-ttu-id="11fc1-117">Estas propiedades se pueden usar como un nombre de archivo sugerido para guardar los datos adjuntos y para proporcionar la extensión de nombre de archivo si no se proporciona la propiedad **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="11fc1-117">These properties can be used as a suggested file name for saving the attachment and to supply the file name extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="11fc1-118">El nombre del archivo está restringido a ocho caracteres más una extensión de tres caracteres.</span><span class="sxs-lookup"><span data-stu-id="11fc1-118">The file name is restricted to eight characters plus a three-character extension.</span></span> <span data-ttu-id="11fc1-119">Para una plataforma que admita nombres de archivo largos, establezca esta propiedad y la **propiedad PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="11fc1-119">For a platform that supports long file names, set both this property and the **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="11fc1-120">MAPI solo funciona con nombres de archivo y otras cadenas que se le pasan en el juego de caracteres del American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="11fc1-120">MAPI works only with file names, and other strings passed to it, in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="11fc1-121">Las aplicaciones cliente que usan nombres de archivo en un juego de caracteres oem (fabricante de equipos originales) deben convertirlos en ANSI antes de llamar a MAPI.</span><span class="sxs-lookup"><span data-stu-id="11fc1-121">Client applications that use file names in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="11fc1-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="11fc1-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="11fc1-123">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="11fc1-123">Protocol specifications</span></span>

<span data-ttu-id="11fc1-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11fc1-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11fc1-125">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="11fc1-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="11fc1-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11fc1-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11fc1-127">Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="11fc1-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="11fc1-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11fc1-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11fc1-129">Especifica las propiedades de los mensajes codificados con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="11fc1-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="11fc1-130">[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11fc1-130">[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11fc1-131">Especifica las propiedades del mensaje firmado y cifrado S/MIME.</span><span class="sxs-lookup"><span data-stu-id="11fc1-131">Specifies S/MIME signed and encrypted message properties.</span></span>
    
<span data-ttu-id="11fc1-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11fc1-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11fc1-133">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficiente.</span><span class="sxs-lookup"><span data-stu-id="11fc1-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="11fc1-134">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="11fc1-134">Header files</span></span>

<span data-ttu-id="11fc1-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11fc1-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="11fc1-136">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="11fc1-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="11fc1-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="11fc1-137">Mapitags.h</span></span>
  
> <span data-ttu-id="11fc1-138">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="11fc1-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11fc1-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="11fc1-139">See also</span></span>



[<span data-ttu-id="11fc1-140">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="11fc1-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11fc1-141">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="11fc1-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11fc1-142">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="11fc1-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11fc1-143">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="11fc1-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

