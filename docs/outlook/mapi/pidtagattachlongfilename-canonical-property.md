---
title: Propiedad canónica PidTagAttachLongFilename
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongFilename
api_type:
- HeaderDef
ms.assetid: 83b69e8f-0b5a-4992-b5b8-160d3bdfa22a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 45b6b3fb0c67d854fddf3773c06cef7b36f54992
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339329"
---
# <a name="pidtagattachlongfilename-canonical-property"></a><span data-ttu-id="250db-103">Propiedad canónica PidTagAttachLongFilename</span><span class="sxs-lookup"><span data-stu-id="250db-103">PidTagAttachLongFilename Canonical Property</span></span>

  
  
<span data-ttu-id="250db-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="250db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="250db-105">Contiene el nombre de archivo largo y la extensión de un archivo adjunto, excluyendo la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="250db-105">Contains an attachment's long filename and extension, excluding path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="250db-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="250db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="250db-107">PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="250db-107">PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="250db-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="250db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="250db-109">0x3707</span><span class="sxs-lookup"><span data-stu-id="250db-109">0x3707</span></span>  <br/> |
|<span data-ttu-id="250db-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="250db-110">Data type:</span></span>  <br/> |<span data-ttu-id="250db-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="250db-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="250db-112">Área:</span><span class="sxs-lookup"><span data-stu-id="250db-112">Area:</span></span>  <br/> |<span data-ttu-id="250db-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="250db-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="250db-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="250db-114">Remarks</span></span>

<span data-ttu-id="250db-115">Estas propiedades pertenecen a los valores ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE y ATTACH_BY_REF_ONLY de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="250db-115">These properties pertain to the ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, and ATTACH_BY_REF_ONLY values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="250db-116">Las plataformas que admiten nombres de archivo largos deben establecer las propiedades **PR_ATTACH_LONG_FILENAME** y **PR_ATTACH_FILENAME** (  [PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) al enviar y deben comprobar PR_ATTACH_LONG_FILENAME primero al recibir.</span><span class="sxs-lookup"><span data-stu-id="250db-116">Platforms that support long filenames should set both the **PR_ATTACH_LONG_FILENAME** and **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_FILENAME** first when receiving.</span></span> 
  
<span data-ttu-id="250db-117">La aplicación cliente debe establecer esta propiedad en un nombre de archivo largo sugerido que se usará si el equipo host que recibe un mensaje admite nombres de archivo largos.</span><span class="sxs-lookup"><span data-stu-id="250db-117">The client application should set this property to a suggested long filename to be used if the host computer receiving a message supports long filenames.</span></span> <span data-ttu-id="250db-118">**PR_ATTACH_LONG_FILENAME** puede usarse como nombre de archivo para guardar los datos adjuntos y para proporcionar la extensión de nombre de archivo si no se proporciona la propiedad **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="250db-118">**PR_ATTACH_LONG_FILENAME** can be used as a filename for saving the attachment, and to supply the filename extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="250db-119">A diferencia del nombre de **archivo PR_ATTACH_FILENAME**, este nombre no está restringido a un nombre de archivo de ocho caracteres más una extensión de tres caracteres.</span><span class="sxs-lookup"><span data-stu-id="250db-119">Unlike the filename provided by **PR_ATTACH_FILENAME**, this name is not restricted to an eight-character filename plus a three-character extension.</span></span> <span data-ttu-id="250db-120">En su lugar, puede tener hasta 256 caracteres, incluidos el nombre de archivo, la extensión y el punto separador.</span><span class="sxs-lookup"><span data-stu-id="250db-120">Instead, it can be up to 256 characters long, including the filename, extension, and separator period.</span></span> 
  
<span data-ttu-id="250db-121">MAPI solo funciona con nombres de archivo en el juego de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="250db-121">MAPI works only with filenames in the ANSI character set.</span></span> <span data-ttu-id="250db-122">Las aplicaciones cliente que usan nombres de archivo en un juego de caracteres OEM deben convertirlos en ANSI antes de llamar a MAPI.</span><span class="sxs-lookup"><span data-stu-id="250db-122">Client applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="250db-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="250db-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="250db-124">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="250db-124">Protocol specifications</span></span>

<span data-ttu-id="250db-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="250db-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="250db-126">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="250db-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="250db-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="250db-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="250db-128">Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="250db-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="250db-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="250db-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="250db-130">Especifica las propiedades de los mensajes codificados con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="250db-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="250db-131">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="250db-131">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="250db-132">Especifica las propiedades y las operaciones permitidas para representar mensajes de correo de voz y fax.</span><span class="sxs-lookup"><span data-stu-id="250db-132">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="250db-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="250db-133">Header files</span></span>

<span data-ttu-id="250db-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="250db-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="250db-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="250db-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="250db-136">Mmapitags.h</span><span class="sxs-lookup"><span data-stu-id="250db-136">Mmapitags.h</span></span>
  
> <span data-ttu-id="250db-137">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="250db-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="250db-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="250db-138">See also</span></span>



[<span data-ttu-id="250db-139">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="250db-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="250db-140">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="250db-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="250db-141">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="250db-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="250db-142">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="250db-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

