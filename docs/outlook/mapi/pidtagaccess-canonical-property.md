---
title: Propiedad canónica PidTagAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 8c8a882e-62c1-4c57-8c63-ee5849f656b0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bb00d4e0e1437f9b3c13ac5e7d0a9dc4f3610d32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819170"
---
# <a name="pidtagaccess-canonical-property"></a><span data-ttu-id="08414-103">Propiedad canónica PidTagAccess</span><span class="sxs-lookup"><span data-stu-id="08414-103">PidTagAccess Canonical Property</span></span>

  
  
<span data-ttu-id="08414-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="08414-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="08414-105">Contiene una máscara de bits de marcadores que indica las operaciones que están disponibles para el cliente para el objeto.</span><span class="sxs-lookup"><span data-stu-id="08414-105">Contains a bitmask of flags indicating the operations that are available to the client for the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08414-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="08414-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08414-107">PR_ACCESS</span><span class="sxs-lookup"><span data-stu-id="08414-107">PR_ACCESS</span></span>  <br/> |
|<span data-ttu-id="08414-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="08414-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08414-109">0x0FF4</span><span class="sxs-lookup"><span data-stu-id="08414-109">0x0FF4</span></span>  <br/> |
|<span data-ttu-id="08414-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="08414-110">Data type:</span></span>  <br/> |<span data-ttu-id="08414-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="08414-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="08414-112">Área:</span><span class="sxs-lookup"><span data-stu-id="08414-112">Area:</span></span>  <br/> |<span data-ttu-id="08414-113">Propiedades de Control de acceso</span><span class="sxs-lookup"><span data-stu-id="08414-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08414-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="08414-114">Remarks</span></span>

<span data-ttu-id="08414-115">Esta propiedad es de sólo lectura para el cliente.</span><span class="sxs-lookup"><span data-stu-id="08414-115">This property is read-only for the client.</span></span> <span data-ttu-id="08414-116">Debe ser un bit a bit **o** de cero o más valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="08414-116">It must be a bitwise **OR** of zero or more values from the following table.</span></span> 
  
|<span data-ttu-id="08414-117">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="08414-117">**Name**</span></span>|<span data-ttu-id="08414-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="08414-118">**Value**</span></span>|<span data-ttu-id="08414-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="08414-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="08414-120">MAPI_ACCESS_MODIFY</span><span class="sxs-lookup"><span data-stu-id="08414-120">MAPI_ACCESS_MODIFY</span></span>  <br/> |<span data-ttu-id="08414-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="08414-121">0x00000001</span></span>  <br/> |<span data-ttu-id="08414-122">Write</span><span class="sxs-lookup"><span data-stu-id="08414-122">Write</span></span>  <br/> |
|<span data-ttu-id="08414-123">MAPI_ACCESS_READ</span><span class="sxs-lookup"><span data-stu-id="08414-123">MAPI_ACCESS_READ</span></span>  <br/> |<span data-ttu-id="08414-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="08414-124">0x00000002</span></span>  <br/> |<span data-ttu-id="08414-125">Read</span><span class="sxs-lookup"><span data-stu-id="08414-125">Read</span></span>  <br/> |
|<span data-ttu-id="08414-126">MAPI_ACCESS_DELETE</span><span class="sxs-lookup"><span data-stu-id="08414-126">MAPI_ACCESS_DELETE</span></span>  <br/> |<span data-ttu-id="08414-127">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="08414-127">0x00000004</span></span>  <br/> |<span data-ttu-id="08414-128">Delete</span><span class="sxs-lookup"><span data-stu-id="08414-128">Delete</span></span>  <br/> |
|<span data-ttu-id="08414-129">MAPI_ACCESS_CREATE_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="08414-129">MAPI_ACCESS_CREATE_HIERARCHY</span></span>  <br/> |<span data-ttu-id="08414-130">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="08414-130">0x00000008</span></span>  <br/> |<span data-ttu-id="08414-131">Crear subcarpetas en la jerarquía de carpetas</span><span class="sxs-lookup"><span data-stu-id="08414-131">Create subfolders in the folder hierarchy</span></span>  <br/> |
|<span data-ttu-id="08414-132">MAPI_ACCESS_CREATE_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="08414-132">MAPI_ACCESS_CREATE_CONTENTS</span></span>  <br/> |<span data-ttu-id="08414-133">0 x 00000010</span><span class="sxs-lookup"><span data-stu-id="08414-133">0x00000010</span></span>  <br/> |<span data-ttu-id="08414-134">Crear mensajes de contenido</span><span class="sxs-lookup"><span data-stu-id="08414-134">Create content messages</span></span>  <br/> |
|<span data-ttu-id="08414-135">MAPI_ACCESS_CREATE_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="08414-135">MAPI_ACCESS_CREATE_ASSOCIATED</span></span>  <br/> |<span data-ttu-id="08414-136">0 x 00000020</span><span class="sxs-lookup"><span data-stu-id="08414-136">0x00000020</span></span>  <br/> |<span data-ttu-id="08414-137">Crear mensajes de contenido asociados</span><span class="sxs-lookup"><span data-stu-id="08414-137">Create associated content messages</span></span>  <br/> |
   
<span data-ttu-id="08414-138">Los indicadores MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY y MAPI_ACCESS_READ se encuentran en la carpeta y los objetos de mensaje y en la columna **PR_ACCESS** en tablas de contenido y las tablas de contenido asociada.</span><span class="sxs-lookup"><span data-stu-id="08414-138">The MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY, and MAPI_ACCESS_READ flags are found on folder and message objects and in the **PR_ACCESS** column in contents tables and associated contents tables.</span></span> <span data-ttu-id="08414-139">Los indicadores MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS y MAPI_ACCESS_CREATE_HIERARCHY se encuentran en los objetos de carpeta sólo.</span><span class="sxs-lookup"><span data-stu-id="08414-139">The MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS, and MAPI_ACCESS_CREATE_HIERARCHY flags are found on folder objects only.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="08414-140">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="08414-140">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08414-141">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="08414-141">Protocol specifications</span></span>

<span data-ttu-id="08414-142">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08414-142">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08414-143">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="08414-143">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="08414-144">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08414-144">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08414-145">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="08414-145">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08414-146">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="08414-146">Header files</span></span>

<span data-ttu-id="08414-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08414-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="08414-148">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="08414-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="08414-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="08414-149">Mapitags.h</span></span>
  
> <span data-ttu-id="08414-150">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="08414-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08414-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="08414-151">See also</span></span>



[<span data-ttu-id="08414-152">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="08414-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08414-153">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="08414-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08414-154">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="08414-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08414-155">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="08414-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

