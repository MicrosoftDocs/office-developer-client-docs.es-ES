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
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316516"
---
# <a name="pidtagaccess-canonical-property"></a><span data-ttu-id="2a80e-103">Propiedad canónica PidTagAccess</span><span class="sxs-lookup"><span data-stu-id="2a80e-103">PidTagAccess Canonical Property</span></span>

  
  
<span data-ttu-id="2a80e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a80e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a80e-105">Contiene una máscara de bits de marcas que indica las operaciones que están disponibles para el cliente para el objeto.</span><span class="sxs-lookup"><span data-stu-id="2a80e-105">Contains a bitmask of flags indicating the operations that are available to the client for the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a80e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2a80e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2a80e-107">PR_ACCESS</span><span class="sxs-lookup"><span data-stu-id="2a80e-107">PR_ACCESS</span></span>  <br/> |
|<span data-ttu-id="2a80e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2a80e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2a80e-109">0x0FF4</span><span class="sxs-lookup"><span data-stu-id="2a80e-109">0x0FF4</span></span>  <br/> |
|<span data-ttu-id="2a80e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2a80e-110">Data type:</span></span>  <br/> |<span data-ttu-id="2a80e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2a80e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2a80e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2a80e-112">Area:</span></span>  <br/> |<span data-ttu-id="2a80e-113">Propiedades del control de acceso</span><span class="sxs-lookup"><span data-stu-id="2a80e-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a80e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2a80e-114">Remarks</span></span>

<span data-ttu-id="2a80e-115">Esta propiedad es de solo lectura para el cliente.</span><span class="sxs-lookup"><span data-stu-id="2a80e-115">This property is read-only for the client.</span></span> <span data-ttu-id="2a80e-116">Debe ser un or bit a **bit** de cero o más valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2a80e-116">It must be a bitwise **OR** of zero or more values from the following table.</span></span> 
  
|<span data-ttu-id="2a80e-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="2a80e-117">**Name**</span></span>|<span data-ttu-id="2a80e-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2a80e-118">**Value**</span></span>|<span data-ttu-id="2a80e-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a80e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2a80e-120">MAPI_ACCESS_MODIFY</span><span class="sxs-lookup"><span data-stu-id="2a80e-120">MAPI_ACCESS_MODIFY</span></span>  <br/> |<span data-ttu-id="2a80e-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2a80e-121">0x00000001</span></span>  <br/> |<span data-ttu-id="2a80e-122">Escritura</span><span class="sxs-lookup"><span data-stu-id="2a80e-122">Write</span></span>  <br/> |
|<span data-ttu-id="2a80e-123">MAPI_ACCESS_READ</span><span class="sxs-lookup"><span data-stu-id="2a80e-123">MAPI_ACCESS_READ</span></span>  <br/> |<span data-ttu-id="2a80e-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2a80e-124">0x00000002</span></span>  <br/> |<span data-ttu-id="2a80e-125">Lectura</span><span class="sxs-lookup"><span data-stu-id="2a80e-125">Read</span></span>  <br/> |
|<span data-ttu-id="2a80e-126">MAPI_ACCESS_DELETE</span><span class="sxs-lookup"><span data-stu-id="2a80e-126">MAPI_ACCESS_DELETE</span></span>  <br/> |<span data-ttu-id="2a80e-127">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2a80e-127">0x00000004</span></span>  <br/> |<span data-ttu-id="2a80e-128">Eliminar</span><span class="sxs-lookup"><span data-stu-id="2a80e-128">Delete</span></span>  <br/> |
|<span data-ttu-id="2a80e-129">MAPI_ACCESS_CREATE_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="2a80e-129">MAPI_ACCESS_CREATE_HIERARCHY</span></span>  <br/> |<span data-ttu-id="2a80e-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2a80e-130">0x00000008</span></span>  <br/> |<span data-ttu-id="2a80e-131">Crear subcarpetas en la jerarquía de carpetas</span><span class="sxs-lookup"><span data-stu-id="2a80e-131">Create subfolders in the folder hierarchy</span></span>  <br/> |
|<span data-ttu-id="2a80e-132">MAPI_ACCESS_CREATE_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="2a80e-132">MAPI_ACCESS_CREATE_CONTENTS</span></span>  <br/> |<span data-ttu-id="2a80e-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2a80e-133">0x00000010</span></span>  <br/> |<span data-ttu-id="2a80e-134">Crear mensajes de contenido</span><span class="sxs-lookup"><span data-stu-id="2a80e-134">Create content messages</span></span>  <br/> |
|<span data-ttu-id="2a80e-135">MAPI_ACCESS_CREATE_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="2a80e-135">MAPI_ACCESS_CREATE_ASSOCIATED</span></span>  <br/> |<span data-ttu-id="2a80e-136">0x00000020</span><span class="sxs-lookup"><span data-stu-id="2a80e-136">0x00000020</span></span>  <br/> |<span data-ttu-id="2a80e-137">Crear mensajes de contenido asociados</span><span class="sxs-lookup"><span data-stu-id="2a80e-137">Create associated content messages</span></span>  <br/> |
   
<span data-ttu-id="2a80e-138">Las MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY y MAPI_ACCESS_READ se encuentran en objetos de carpeta y mensaje y en la columna **PR_ACCESS** en tablas de contenido y tablas de contenido asociadas.</span><span class="sxs-lookup"><span data-stu-id="2a80e-138">The MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY, and MAPI_ACCESS_READ flags are found on folder and message objects and in the **PR_ACCESS** column in contents tables and associated contents tables.</span></span> <span data-ttu-id="2a80e-139">Las MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS y MAPI_ACCESS_CREATE_HIERARCHY se encuentran únicamente en objetos de carpeta.</span><span class="sxs-lookup"><span data-stu-id="2a80e-139">The MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS, and MAPI_ACCESS_CREATE_HIERARCHY flags are found on folder objects only.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2a80e-140">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a80e-140">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2a80e-141">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="2a80e-141">Protocol specifications</span></span>

<span data-ttu-id="2a80e-142">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a80e-142">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a80e-143">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="2a80e-143">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2a80e-144">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a80e-144">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a80e-145">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="2a80e-145">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2a80e-146">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2a80e-146">Header files</span></span>

<span data-ttu-id="2a80e-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2a80e-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="2a80e-148">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2a80e-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="2a80e-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2a80e-149">Mapitags.h</span></span>
  
> <span data-ttu-id="2a80e-150">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="2a80e-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a80e-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a80e-151">See also</span></span>



[<span data-ttu-id="2a80e-152">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2a80e-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2a80e-153">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2a80e-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2a80e-154">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2a80e-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2a80e-155">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2a80e-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

