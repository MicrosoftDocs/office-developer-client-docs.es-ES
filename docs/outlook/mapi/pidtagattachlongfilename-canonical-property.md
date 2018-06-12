---
title: Propiedad canónico PidTagAttachLongFilename
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 0debee5d480c4ea0c0a8fb4b54d9fa5d92a45987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819229"
---
# <a name="pidtagattachlongfilename-canonical-property"></a><span data-ttu-id="f0b54-103">Propiedad canónico PidTagAttachLongFilename</span><span class="sxs-lookup"><span data-stu-id="f0b54-103">PidTagAttachLongFilename Canonical Property</span></span>

  
  
<span data-ttu-id="f0b54-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f0b54-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f0b54-105">Contiene el nombre de archivo largo y la extensión, excluyendo la ruta de acceso de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="f0b54-105">Contains an attachment's long filename and extension, excluding path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f0b54-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f0b54-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f0b54-107">PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="f0b54-107">PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="f0b54-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f0b54-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f0b54-109">0x3707</span><span class="sxs-lookup"><span data-stu-id="f0b54-109">0x3707</span></span>  <br/> |
|<span data-ttu-id="f0b54-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f0b54-110">Data type:</span></span>  <br/> |<span data-ttu-id="f0b54-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f0b54-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f0b54-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f0b54-112">Area:</span></span>  <br/> |<span data-ttu-id="f0b54-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="f0b54-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0b54-114">Notas</span><span class="sxs-lookup"><span data-stu-id="f0b54-114">Remarks</span></span>

<span data-ttu-id="f0b54-115">Estas propiedades corresponden a los valores ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE y ATTACH_BY_REF_ONLY de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f0b54-115">These properties pertain to the ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, and ATTACH_BY_REF_ONLY values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="f0b54-116">Plataformas compatibles con nombres de archivo largos deben establecer las propiedades de **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) y **PR_ATTACH_LONG_FILENAME** al enviar y debe comprobar **PR_ATTACH_LONG_FILENAME** en primer lugar cuando recibir.</span><span class="sxs-lookup"><span data-stu-id="f0b54-116">Platforms that support long filenames should set both the **PR_ATTACH_LONG_FILENAME** and **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_FILENAME** first when receiving.</span></span> 
  
<span data-ttu-id="f0b54-117">La aplicación cliente debe establecer esta propiedad para un nombre de archivo largo sugerido que se usará si el equipo host de recibir un mensaje admite nombres de archivo largos.</span><span class="sxs-lookup"><span data-stu-id="f0b54-117">The client application should set this property to a suggested long filename to be used if the host computer receiving a message supports long filenames.</span></span> <span data-ttu-id="f0b54-118">**PR_ATTACH_LONG_FILENAME** se puede usar como un nombre de archivo para guardar los datos adjuntos y para proporcionar la extensión de nombre de archivo si no se proporciona la propiedad **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f0b54-118">**PR_ATTACH_LONG_FILENAME** can be used as a filename for saving the attachment, and to supply the filename extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="f0b54-119">A diferencia de nombre de archivo proporcionado por **PR_ATTACH_FILENAME**, este nombre no está limitado a un nombre de archivo de ocho caracteres más una extensión de tres caracteres.</span><span class="sxs-lookup"><span data-stu-id="f0b54-119">Unlike the filename provided by **PR_ATTACH_FILENAME**, this name is not restricted to an eight-character filename plus a three-character extension.</span></span> <span data-ttu-id="f0b54-120">En su lugar, puede ser hasta 256 caracteres long, incluido el nombre de archivo, la extensión y el separador de punto.</span><span class="sxs-lookup"><span data-stu-id="f0b54-120">Instead, it can be up to 256 characters long, including the filename, extension, and separator period.</span></span> 
  
<span data-ttu-id="f0b54-121">MAPI sólo funciona con los nombres de archivo en el juego de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="f0b54-121">MAPI works only with filenames in the ANSI character set.</span></span> <span data-ttu-id="f0b54-122">Las aplicaciones de cliente que usan nombres de archivo en un juego de caracteres OEM deben convertirlos a ANSI antes de llamar a MAPI.</span><span class="sxs-lookup"><span data-stu-id="f0b54-122">Client applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f0b54-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f0b54-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f0b54-124">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f0b54-124">Protocol specifications</span></span>

<span data-ttu-id="f0b54-125">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0b54-125">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0b54-126">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="f0b54-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="f0b54-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0b54-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0b54-128">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f0b54-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="f0b54-129">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0b54-129">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0b54-130">Especifica las propiedades de mensajes codificados con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="f0b54-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="f0b54-131">[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0b54-131">[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0b54-132">Especifica las propiedades y operaciones que se permiten para que representa los mensajes de fax y correo de voz.</span><span class="sxs-lookup"><span data-stu-id="f0b54-132">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f0b54-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f0b54-133">Header files</span></span>

<span data-ttu-id="f0b54-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f0b54-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="f0b54-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f0b54-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="f0b54-136">Mmapitags.h</span><span class="sxs-lookup"><span data-stu-id="f0b54-136">Mmapitags.h</span></span>
  
> <span data-ttu-id="f0b54-137">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f0b54-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f0b54-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="f0b54-138">See also</span></span>



[<span data-ttu-id="f0b54-139">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f0b54-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f0b54-140">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f0b54-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f0b54-141">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="f0b54-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f0b54-142">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f0b54-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

