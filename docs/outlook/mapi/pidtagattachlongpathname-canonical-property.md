---
title: Propiedad canónica PidTagAttachLongPathname
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongPathname
api_type:
- HeaderDef
ms.assetid: 3262cf95-48b5-4764-a96e-d752ce35b2dc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d8fe8525cf4fc11ac17ed6d73fb5d97e4f2d003e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383110"
---
# <a name="pidtagattachlongpathname-canonical-property"></a><span data-ttu-id="81227-103">Propiedad canónica PidTagAttachLongPathname</span><span class="sxs-lookup"><span data-stu-id="81227-103">PidTagAttachLongPathname Canonical Property</span></span>

  
  
<span data-ttu-id="81227-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81227-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81227-105">Contiene la ruta de acceso larga completo y nombre de archivo de un documento adjunto.</span><span class="sxs-lookup"><span data-stu-id="81227-105">Contains an attachment's fully-qualified long path and filename.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81227-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="81227-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81227-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="81227-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="81227-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="81227-108">Identifier:</span></span>  <br/> |<span data-ttu-id="81227-109">0x370D</span><span class="sxs-lookup"><span data-stu-id="81227-109">0x370D</span></span>  <br/> |
|<span data-ttu-id="81227-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="81227-110">Data type:</span></span>  <br/> |<span data-ttu-id="81227-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="81227-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="81227-112">Área:</span><span class="sxs-lookup"><span data-stu-id="81227-112">Area:</span></span>  <br/> |<span data-ttu-id="81227-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="81227-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81227-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81227-114">Remarks</span></span>

<span data-ttu-id="81227-115">Estas propiedades son aplicables cuando se usa alguno de los valores de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) que indican datos adjuntos por referencia: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**o **ATTACH_BY _REF_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="81227-115">These properties are applicable when you use any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property's values that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="81227-116">Plataformas compatibles con nombres de archivo largos deben establecer **PR_ATTACH_LONG_PATHNAME** o propiedades asociadas y las propiedades de **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) cuando se envía y debe comprobar \*\*PR_ATTACH_LONG_PATHNAME \*\*o asociados propiedades primero al recibir.</span><span class="sxs-lookup"><span data-stu-id="81227-116">Platforms that support long filenames should set both **PR_ATTACH_LONG_PATHNAME** or associated properties and **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_PATHNAME** or associated properties first when receiving.</span></span> 
  
<span data-ttu-id="81227-117">La aplicación cliente debe establecer estas propiedades en una ruta de acceso sugerida largo y nombre de archivo que se usará si el equipo host de recibir un mensaje admite nombres de archivo largos.</span><span class="sxs-lookup"><span data-stu-id="81227-117">The client application should set these properties to a suggested long path and filename to be used if the host machine receiving a message supports long filenames.</span></span> <span data-ttu-id="81227-118">Establecer estas propiedades indica que los datos adjuntos no se incluye con el mensaje, pero está disponibles en un servidor de archivos comunes.</span><span class="sxs-lookup"><span data-stu-id="81227-118">Setting these properties indicates that the attachment data is not included with the message but is available on a common file server.</span></span> 
  
<span data-ttu-id="81227-119">A diferencia de los directorios y los nombres de archivo proporcionada por **PR_ATTACH_PATHNAME**, estos directorios y los nombres de archivo no están restringidos en una extensión de tres caracteres además de nombre de archivo o directorio de ocho caracteres.</span><span class="sxs-lookup"><span data-stu-id="81227-119">Unlike the directories and filenames provided by **PR_ATTACH_PATHNAME**, these directories and filenames are not restricted to an eight-character directory or filename plus three-character extension.</span></span> <span data-ttu-id="81227-120">En su lugar, cada nombre de archivo o directorio puede ser hasta 256 caracteres long, incluidos el nombre, la extensión y el período de separador.</span><span class="sxs-lookup"><span data-stu-id="81227-120">Instead, each directory or filename can be up to 256 characters long, including the name, extension, and separator period.</span></span> <span data-ttu-id="81227-121">Sin embargo, la ruta de acceso global está limitado a 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="81227-121">However, the overall path is limited to 256 characters.</span></span> 
  
<span data-ttu-id="81227-122">Los clientes deben usar una convención de nomenclatura universal (UNC) en la mayoría de los casos cuando el archivo se comparte y debe usar una ruta de acceso absoluta cuando el archivo es local.</span><span class="sxs-lookup"><span data-stu-id="81227-122">Clients should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="81227-123">MAPI sólo funciona con las rutas de acceso y conjunto de caracteres de los nombres de archivo en el ANSI.</span><span class="sxs-lookup"><span data-stu-id="81227-123">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="81227-124">Las aplicaciones de cliente que usan nombres de archivo y rutas de acceso en un juego de caracteres OEM deben convertirlos a ANSI antes de llamar a MAPI.</span><span class="sxs-lookup"><span data-stu-id="81227-124">Client applications that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="81227-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="81227-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="81227-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="81227-126">Protocol specifications</span></span>

<span data-ttu-id="81227-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81227-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81227-128">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="81227-128">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="81227-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81227-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81227-130">Especifica las propiedades de mensajes codificados con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="81227-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="81227-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="81227-131">Header files</span></span>

<span data-ttu-id="81227-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81227-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="81227-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="81227-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="81227-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="81227-134">Mapitags.h</span></span>
  
> <span data-ttu-id="81227-135">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="81227-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81227-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="81227-136">See also</span></span>



[<span data-ttu-id="81227-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="81227-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81227-138">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="81227-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81227-139">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="81227-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81227-140">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="81227-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

