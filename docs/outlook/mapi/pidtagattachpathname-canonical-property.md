---
title: Propiedad canónica PidTagAttachPathname
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPathname
api_type:
- HeaderDef
ms.assetid: e19c7cd1-7c56-4f63-8736-d6971c7c5f4d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b7e0c174f0b31522cffbb4761ab64a50267874be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819244"
---
# <a name="pidtagattachpathname-canonical-property"></a><span data-ttu-id="ed7c5-103">Propiedad canónica PidTagAttachPathname</span><span class="sxs-lookup"><span data-stu-id="ed7c5-103">PidTagAttachPathname Canonical Property</span></span>

  
  
<span data-ttu-id="ed7c5-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ed7c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ed7c5-105">Contiene la ruta de acceso completa y el nombre de archivo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ed7c5-105">Contains an attachment's fully-qualified path and filename.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed7c5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ed7c5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed7c5-107">PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="ed7c5-107">PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="ed7c5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ed7c5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ed7c5-109">0x3708</span><span class="sxs-lookup"><span data-stu-id="ed7c5-109">0x3708</span></span>  <br/> |
|<span data-ttu-id="ed7c5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ed7c5-110">Data type:</span></span>  <br/> |<span data-ttu-id="ed7c5-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ed7c5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ed7c5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ed7c5-112">Area:</span></span>  <br/> |<span data-ttu-id="ed7c5-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="ed7c5-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed7c5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ed7c5-114">Remarks</span></span>

<span data-ttu-id="ed7c5-115">Se recomienda que los datos adjuntos subobjetos exponen estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ed7c5-115">It is recommended that attachment subobjects expose these properties.</span></span> <span data-ttu-id="ed7c5-116">Establecerlas indica que los datos adjuntos no se incluye con el mensaje, pero está disponibles en un servidor de archivos comunes.</span><span class="sxs-lookup"><span data-stu-id="ed7c5-116">Setting them indicates that the attachment data is not included with the message but is available on a common file server.</span></span> <span data-ttu-id="ed7c5-117">Estas propiedades son necesarias en combinación con cualquiera de las marcas de **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) que indican datos adjuntos por referencia: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**o **ATTACH_BY_REF_ SÓLO**.</span><span class="sxs-lookup"><span data-stu-id="ed7c5-117">These properties are required in conjunction with any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) flags that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> 
  
<span data-ttu-id="ed7c5-118">Cada nombre de archivo o directorio está restringida a un nombre de ocho caracteres más una extensión de tres caracteres.</span><span class="sxs-lookup"><span data-stu-id="ed7c5-118">Each directory or filename is restricted to an eight-character name plus a three-character extension.</span></span> <span data-ttu-id="ed7c5-119">La ruta de acceso global está restringido a 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ed7c5-119">The overall path is restricted to 256 characters.</span></span> <span data-ttu-id="ed7c5-120">Para una plataforma que admite nombres de archivo largos, establecer estas propiedades y la **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ed7c5-120">For a platform that supports long filenames, set both these properties and **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)).</span></span> 
  
<span data-ttu-id="ed7c5-121">Aplicaciones cliente deben usar una convención de nomenclatura universal (UNC) en la mayoría de los casos, cuando el archivo se comparte y debe usar una ruta de acceso absoluta cuando el archivo es local.</span><span class="sxs-lookup"><span data-stu-id="ed7c5-121">Client applications should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="ed7c5-122">MAPI sólo funciona con las rutas de acceso y conjunto de caracteres de los nombres de archivo en el ANSI.</span><span class="sxs-lookup"><span data-stu-id="ed7c5-122">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="ed7c5-123">Los clientes que usan nombres de archivo y rutas de acceso en un juego de caracteres OEM deben convertirlos a ANSI antes de llamar a MAPI.</span><span class="sxs-lookup"><span data-stu-id="ed7c5-123">Clients that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ed7c5-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed7c5-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ed7c5-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="ed7c5-125">Protocol specifications</span></span>

<span data-ttu-id="ed7c5-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed7c5-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed7c5-127">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ed7c5-127">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="ed7c5-128">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed7c5-128">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed7c5-129">Especifica las propiedades de mensajes codificados con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="ed7c5-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ed7c5-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ed7c5-130">Header files</span></span>

<span data-ttu-id="ed7c5-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed7c5-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed7c5-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ed7c5-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="ed7c5-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ed7c5-133">Mapitags.h</span></span>
  
> <span data-ttu-id="ed7c5-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ed7c5-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed7c5-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed7c5-135">See also</span></span>



[<span data-ttu-id="ed7c5-136">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="ed7c5-136">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)
  
[<span data-ttu-id="ed7c5-137">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="ed7c5-137">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)


[<span data-ttu-id="ed7c5-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ed7c5-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed7c5-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="ed7c5-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed7c5-140">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ed7c5-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed7c5-141">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="ed7c5-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

