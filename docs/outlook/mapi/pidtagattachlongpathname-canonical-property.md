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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339371"
---
# <a name="pidtagattachlongpathname-canonical-property"></a><span data-ttu-id="42907-103">Propiedad canónica PidTagAttachLongPathname</span><span class="sxs-lookup"><span data-stu-id="42907-103">PidTagAttachLongPathname Canonical Property</span></span>

  
  
<span data-ttu-id="42907-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42907-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42907-105">Contiene el nombre de archivo y la ruta de acceso completos completos de un archivo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="42907-105">Contains an attachment's fully-qualified long path and filename.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42907-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="42907-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="42907-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="42907-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="42907-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="42907-108">Identifier:</span></span>  <br/> |<span data-ttu-id="42907-109">0x370D</span><span class="sxs-lookup"><span data-stu-id="42907-109">0x370D</span></span>  <br/> |
|<span data-ttu-id="42907-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="42907-110">Data type:</span></span>  <br/> |<span data-ttu-id="42907-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="42907-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="42907-112">Área:</span><span class="sxs-lookup"><span data-stu-id="42907-112">Area:</span></span>  <br/> |<span data-ttu-id="42907-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="42907-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42907-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="42907-114">Remarks</span></span>

<span data-ttu-id="42907-115">Estas propiedades se aplican cuando se usa cualquiera de los valores de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) que indican datos adjuntos por referencia: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**o **ATTACH_BY _REF_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="42907-115">These properties are applicable when you use any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property's values that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="42907-116">Las plataformas que admiten nombres de archivo largos deben establecer las propiedades **PR_ATTACH_LONG_PATHNAME** o asociadas y **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) al enviar y deben comprobar \*\*PR_ATTACH_LONG_PATHNAME \*\*o las propiedades asociadas en primer lugar al recibir.</span><span class="sxs-lookup"><span data-stu-id="42907-116">Platforms that support long filenames should set both **PR_ATTACH_LONG_PATHNAME** or associated properties and **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_PATHNAME** or associated properties first when receiving.</span></span> 
  
<span data-ttu-id="42907-117">La aplicación cliente debe establecer estas propiedades en una ruta de acceso larga y un nombre de archivo sugeridos que se usarán si el equipo host que recibe un mensaje admite nombres de archivo largos.</span><span class="sxs-lookup"><span data-stu-id="42907-117">The client application should set these properties to a suggested long path and filename to be used if the host machine receiving a message supports long filenames.</span></span> <span data-ttu-id="42907-118">La configuración de estas propiedades indica que los datos adjuntos no se incluyen en el mensaje, pero que están disponibles en un servidor de archivos común.</span><span class="sxs-lookup"><span data-stu-id="42907-118">Setting these properties indicates that the attachment data is not included with the message but is available on a common file server.</span></span> 
  
<span data-ttu-id="42907-119">A diferencia de los directorios y los nombres de archivo proporcionados por **PR_ATTACH_PATHNAME**, estos directorios y nombres de archivo no están restringidos a un directorio de ocho caracteres o un nombre de archivo más una extensión de tres caracteres.</span><span class="sxs-lookup"><span data-stu-id="42907-119">Unlike the directories and filenames provided by **PR_ATTACH_PATHNAME**, these directories and filenames are not restricted to an eight-character directory or filename plus three-character extension.</span></span> <span data-ttu-id="42907-120">En su lugar, cada directorio o nombre de archivo puede tener hasta 256 caracteres, como el nombre, la extensión y el período separador.</span><span class="sxs-lookup"><span data-stu-id="42907-120">Instead, each directory or filename can be up to 256 characters long, including the name, extension, and separator period.</span></span> <span data-ttu-id="42907-121">Sin embargo, la ruta de acceso general está limitada a 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="42907-121">However, the overall path is limited to 256 characters.</span></span> 
  
<span data-ttu-id="42907-122">Los clientes deben usar una Convención de nomenclatura universal (UNC) en la mayoría de los casos cuando se comparte el archivo y deben usar una ruta de acceso absoluta cuando el archivo es local.</span><span class="sxs-lookup"><span data-stu-id="42907-122">Clients should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="42907-123">MAPI solo funciona con los nombres de archivo y las rutas del juego de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="42907-123">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="42907-124">Las aplicaciones cliente que usan rutas de acceso y nombres de archivo en un conjunto de caracteres OEM deben convertirlas a ANSI antes de llamar a MAPI.</span><span class="sxs-lookup"><span data-stu-id="42907-124">Client applications that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="42907-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="42907-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="42907-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="42907-126">Protocol specifications</span></span>

<span data-ttu-id="42907-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42907-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42907-128">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="42907-128">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="42907-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42907-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42907-130">Especifica las propiedades de los mensajes codificados con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="42907-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="42907-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="42907-131">Header files</span></span>

<span data-ttu-id="42907-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="42907-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="42907-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="42907-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="42907-134">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="42907-134">Mapitags.h</span></span>
  
> <span data-ttu-id="42907-135">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="42907-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="42907-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="42907-136">See also</span></span>



[<span data-ttu-id="42907-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="42907-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="42907-138">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="42907-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="42907-139">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="42907-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="42907-140">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="42907-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

