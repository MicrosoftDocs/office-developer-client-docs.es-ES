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
ms.openlocfilehash: dc4a784b3a3f3792622fca2d04f5bb4504a98b54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565371"
---
# <a name="pidtagaccess-canonical-property"></a><span data-ttu-id="4a5d1-103">Propiedad canónica PidTagAccess</span><span class="sxs-lookup"><span data-stu-id="4a5d1-103">PidTagAccess Canonical Property</span></span>

  
  
<span data-ttu-id="4a5d1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a5d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a5d1-105">Contiene una máscara de bits de marcadores que indica las operaciones que están disponibles para el cliente para el objeto.</span><span class="sxs-lookup"><span data-stu-id="4a5d1-105">Contains a bitmask of flags indicating the operations that are available to the client for the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a5d1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4a5d1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a5d1-107">PR_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4a5d1-107">PR_ACCESS</span></span>  <br/> |
|<span data-ttu-id="4a5d1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4a5d1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a5d1-109">0x0FF4</span><span class="sxs-lookup"><span data-stu-id="4a5d1-109">0x0FF4</span></span>  <br/> |
|<span data-ttu-id="4a5d1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4a5d1-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a5d1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4a5d1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4a5d1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4a5d1-112">Area:</span></span>  <br/> |<span data-ttu-id="4a5d1-113">Propiedades de Control de acceso</span><span class="sxs-lookup"><span data-stu-id="4a5d1-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a5d1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a5d1-114">Remarks</span></span>

<span data-ttu-id="4a5d1-115">Esta propiedad es de sólo lectura para el cliente.</span><span class="sxs-lookup"><span data-stu-id="4a5d1-115">This property is read-only for the client.</span></span> <span data-ttu-id="4a5d1-116">Debe ser un bit a bit **o** de cero o más valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4a5d1-116">It must be a bitwise **OR** of zero or more values from the following table.</span></span> 
  
|<span data-ttu-id="4a5d1-117">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="4a5d1-117">**Name**</span></span>|<span data-ttu-id="4a5d1-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4a5d1-118">**Value**</span></span>|<span data-ttu-id="4a5d1-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4a5d1-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4a5d1-120">MAPI_ACCESS_MODIFY</span><span class="sxs-lookup"><span data-stu-id="4a5d1-120">MAPI_ACCESS_MODIFY</span></span>  <br/> |<span data-ttu-id="4a5d1-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4a5d1-121">0x00000001</span></span>  <br/> |<span data-ttu-id="4a5d1-122">Write</span><span class="sxs-lookup"><span data-stu-id="4a5d1-122">Write</span></span>  <br/> |
|<span data-ttu-id="4a5d1-123">MAPI_ACCESS_READ</span><span class="sxs-lookup"><span data-stu-id="4a5d1-123">MAPI_ACCESS_READ</span></span>  <br/> |<span data-ttu-id="4a5d1-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4a5d1-124">0x00000002</span></span>  <br/> |<span data-ttu-id="4a5d1-125">Read</span><span class="sxs-lookup"><span data-stu-id="4a5d1-125">Read</span></span>  <br/> |
|<span data-ttu-id="4a5d1-126">MAPI_ACCESS_DELETE</span><span class="sxs-lookup"><span data-stu-id="4a5d1-126">MAPI_ACCESS_DELETE</span></span>  <br/> |<span data-ttu-id="4a5d1-127">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="4a5d1-127">0x00000004</span></span>  <br/> |<span data-ttu-id="4a5d1-128">Delete</span><span class="sxs-lookup"><span data-stu-id="4a5d1-128">Delete</span></span>  <br/> |
|<span data-ttu-id="4a5d1-129">MAPI_ACCESS_CREATE_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="4a5d1-129">MAPI_ACCESS_CREATE_HIERARCHY</span></span>  <br/> |<span data-ttu-id="4a5d1-130">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="4a5d1-130">0x00000008</span></span>  <br/> |<span data-ttu-id="4a5d1-131">Crear subcarpetas en la jerarquía de carpetas</span><span class="sxs-lookup"><span data-stu-id="4a5d1-131">Create subfolders in the folder hierarchy</span></span>  <br/> |
|<span data-ttu-id="4a5d1-132">MAPI_ACCESS_CREATE_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="4a5d1-132">MAPI_ACCESS_CREATE_CONTENTS</span></span>  <br/> |<span data-ttu-id="4a5d1-133">0 x 00000010</span><span class="sxs-lookup"><span data-stu-id="4a5d1-133">0x00000010</span></span>  <br/> |<span data-ttu-id="4a5d1-134">Crear mensajes de contenido</span><span class="sxs-lookup"><span data-stu-id="4a5d1-134">Create content messages</span></span>  <br/> |
|<span data-ttu-id="4a5d1-135">MAPI_ACCESS_CREATE_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="4a5d1-135">MAPI_ACCESS_CREATE_ASSOCIATED</span></span>  <br/> |<span data-ttu-id="4a5d1-136">0 x 00000020</span><span class="sxs-lookup"><span data-stu-id="4a5d1-136">0x00000020</span></span>  <br/> |<span data-ttu-id="4a5d1-137">Crear mensajes de contenido asociados</span><span class="sxs-lookup"><span data-stu-id="4a5d1-137">Create associated content messages</span></span>  <br/> |
   
<span data-ttu-id="4a5d1-138">Los indicadores MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY y MAPI_ACCESS_READ se encuentran en la carpeta y los objetos de mensaje y en la columna **PR_ACCESS** en tablas de contenido y las tablas de contenido asociada.</span><span class="sxs-lookup"><span data-stu-id="4a5d1-138">The MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY, and MAPI_ACCESS_READ flags are found on folder and message objects and in the **PR_ACCESS** column in contents tables and associated contents tables.</span></span> <span data-ttu-id="4a5d1-139">Los indicadores MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS y MAPI_ACCESS_CREATE_HIERARCHY se encuentran en los objetos de carpeta sólo.</span><span class="sxs-lookup"><span data-stu-id="4a5d1-139">The MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS, and MAPI_ACCESS_CREATE_HIERARCHY flags are found on folder objects only.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4a5d1-140">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a5d1-140">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a5d1-141">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="4a5d1-141">Protocol specifications</span></span>

<span data-ttu-id="4a5d1-142">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a5d1-142">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a5d1-143">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4a5d1-143">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a5d1-144">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a5d1-144">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a5d1-145">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4a5d1-145">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a5d1-146">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4a5d1-146">Header files</span></span>

<span data-ttu-id="4a5d1-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a5d1-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a5d1-148">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4a5d1-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a5d1-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4a5d1-149">Mapitags.h</span></span>
  
> <span data-ttu-id="4a5d1-150">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="4a5d1-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a5d1-151">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="4a5d1-151">See also</span></span>



[<span data-ttu-id="4a5d1-152">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4a5d1-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a5d1-153">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4a5d1-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a5d1-154">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4a5d1-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a5d1-155">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="4a5d1-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

