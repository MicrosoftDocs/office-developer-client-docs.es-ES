---
title: Propiedad canónica PidTagContainerFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c9c446097213e5b743a47ec32db17ec0afe63b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357550"
---
# <a name="pidtagcontainerflags-canonical-property"></a><span data-ttu-id="ffd85-103">Propiedad canónica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="ffd85-103">PidTagContainerFlags Canonical Property</span></span>

  
  
<span data-ttu-id="ffd85-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffd85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffd85-105">Contiene una máscara de bits de marcas que describen las capacidades de un contenedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="ffd85-105">Contains a bitmask of flags describing capabilities of an address book container.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ffd85-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ffd85-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ffd85-107">PR_CONTAINER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ffd85-107">PR_CONTAINER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="ffd85-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ffd85-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ffd85-109">0x3600</span><span class="sxs-lookup"><span data-stu-id="ffd85-109">0x3600</span></span>  <br/> |
|<span data-ttu-id="ffd85-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ffd85-110">Data type:</span></span>  <br/> |<span data-ttu-id="ffd85-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ffd85-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ffd85-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ffd85-112">Area:</span></span>  <br/> |<span data-ttu-id="ffd85-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="ffd85-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffd85-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ffd85-114">Remarks</span></span>

<span data-ttu-id="ffd85-115">Se pueden establecer una o varias de las siguientes marcas para la máscara de bits:</span><span class="sxs-lookup"><span data-stu-id="ffd85-115">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="ffd85-116">AB_FIND_ON_OPEN</span><span class="sxs-lookup"><span data-stu-id="ffd85-116">AB_FIND_ON_OPEN</span></span> 
  
> <span data-ttu-id="ffd85-117">Muestra un cuadro de diálogo para solicitar una restricción antes de mostrar cualquier contenido del contenedor.</span><span class="sxs-lookup"><span data-stu-id="ffd85-117">Displays a dialog box to request a restriction before displaying any contents of the container.</span></span> 
    
<span data-ttu-id="ffd85-118">AB_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="ffd85-118">AB_MODIFIABLE</span></span> 
  
> <span data-ttu-id="ffd85-119">Las entradas se pueden agregar y quitar del contenedor.</span><span class="sxs-lookup"><span data-stu-id="ffd85-119">Entries can be added to and removed from the container.</span></span> <span data-ttu-id="ffd85-120">Esta marca no indica si se pueden modificar las entradas del contenedor.</span><span class="sxs-lookup"><span data-stu-id="ffd85-120">This flag does not indicate whether any entries in the container can be modified.</span></span>
    
<span data-ttu-id="ffd85-121">AB_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="ffd85-121">AB_RECIPIENTS</span></span> 
  
> <span data-ttu-id="ffd85-122">El contenedor puede contener destinatarios.</span><span class="sxs-lookup"><span data-stu-id="ffd85-122">The container can hold recipients.</span></span> <span data-ttu-id="ffd85-123">Esta marca no indica si los destinatarios están realmente presentes en el contenedor o si se pueden agregar o quitar.</span><span class="sxs-lookup"><span data-stu-id="ffd85-123">This flag does not indicate whether any recipients are actually present in the container, or whether they can be added or removed.</span></span> 
    
<span data-ttu-id="ffd85-124">AB_SUBCONTAINERS</span><span class="sxs-lookup"><span data-stu-id="ffd85-124">AB_SUBCONTAINERS</span></span> 
  
> <span data-ttu-id="ffd85-125">El contenedor puede contener contenedores secundarios.</span><span class="sxs-lookup"><span data-stu-id="ffd85-125">The container can hold child containers.</span></span> <span data-ttu-id="ffd85-126">Esta marca no indica si hay subcontenedores realmente presentes en el contenedor ni si se pueden agregar o quitar.</span><span class="sxs-lookup"><span data-stu-id="ffd85-126">This flag does not indicate whether any subcontainers are actually present in the container, nor whether they can be added or removed.</span></span> <span data-ttu-id="ffd85-127">AB_SUBCONTAINERS debe establecerse para que el contenedor admita [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span><span class="sxs-lookup"><span data-stu-id="ffd85-127">AB_SUBCONTAINERS must be set for the container to support [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span></span> 
    
<span data-ttu-id="ffd85-128">AB_UNMODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="ffd85-128">AB_UNMODIFIABLE</span></span> 
  
> <span data-ttu-id="ffd85-129">Las entradas no se pueden agregar ni quitar del contenedor.</span><span class="sxs-lookup"><span data-stu-id="ffd85-129">Entries cannot be added to or removed from the container.</span></span> <span data-ttu-id="ffd85-130">Esta marca no indica si se pueden modificar las entradas del contenedor.</span><span class="sxs-lookup"><span data-stu-id="ffd85-130">This flag does not indicate whether any entries in the container can be modified.</span></span> 
    
<span data-ttu-id="ffd85-131">El AB_FIND_ON_OPEN marca es muy recomendable para contenedores usados con servicios en línea o con conexiones lentas a servidores.</span><span class="sxs-lookup"><span data-stu-id="ffd85-131">The AB_FIND_ON_OPEN flag is highly recommended for containers used with online services or with slow connections to servers.</span></span> <span data-ttu-id="ffd85-132">Cuando se abre un contenedor que AB_FIND_ON_OPEN,  se presenta un cuadro de diálogo Buscar al usuario para restringir los usuarios de mensajería mostrados.</span><span class="sxs-lookup"><span data-stu-id="ffd85-132">When a container is opened that has AB_FIND_ON_OPEN set, a **Find** dialog box is presented to the user to restrict the displayed messaging users.</span></span> <span data-ttu-id="ffd85-133">Incluso una especificación parcial que limita los usuarios de mensajería puede acelerar considerablemente una presentación del contenido.</span><span class="sxs-lookup"><span data-stu-id="ffd85-133">Even a partial specification limiting the messaging users can dramatically speed up a display of the contents.</span></span> 
  
<span data-ttu-id="ffd85-134">Debe establecerse AB_MODIFIABLE o AB_UNMODIFIABLE marca.</span><span class="sxs-lookup"><span data-stu-id="ffd85-134">Either the AB_MODIFIABLE or AB_UNMODIFIABLE flag must be set.</span></span> <span data-ttu-id="ffd85-135">Ambas marcas se pueden establecer para indicar que el contenedor no sabe si se puede modificar o no, por ejemplo, si la modificación depende de los derechos de acceso del usuario.</span><span class="sxs-lookup"><span data-stu-id="ffd85-135">Both flags can be set to indicate that the container does not know whether it can be modified or not, for example if modification depends on the user's access rights.</span></span> <span data-ttu-id="ffd85-136">En este caso, una aplicación cliente debe intentar una llamada y examinar el código devuelto para determinar las capacidades del contenedor.</span><span class="sxs-lookup"><span data-stu-id="ffd85-136">In this case, a client application must attempt a call and examine the return code to determine the container's capabilities.</span></span> <span data-ttu-id="ffd85-137">Normalmente, un cliente comienza examinando AB_MODIFIABLE.</span><span class="sxs-lookup"><span data-stu-id="ffd85-137">A client typically starts by examining AB_MODIFIABLE.</span></span> <span data-ttu-id="ffd85-138">Si se establece, el cliente realiza una llamada que intenta modificar el contenedor y comprueba el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="ffd85-138">If it is set, the client makes a call that attempts to modify the container and checks the return value.</span></span> 
  
<span data-ttu-id="ffd85-139">La AB_MODIFIABLE no indica qué tipos de entradas se pueden agregar al contenedor.</span><span class="sxs-lookup"><span data-stu-id="ffd85-139">The AB_MODIFIABLE flag does not indicate what types of entries can be added to the container.</span></span> <span data-ttu-id="ffd85-140">Para determinar esto, el cliente debe usar el método [OpenProperty](imapiprop-openproperty.md) adecuado para abrir la propiedad PR_CREATE_TEMPLATES **(** [PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) del contenedor.</span><span class="sxs-lookup"><span data-stu-id="ffd85-140">To determine this, the client should use the appropriate [OpenProperty](imapiprop-openproperty.md) method to open the container's **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="ffd85-141">Abrir **PR_CREATE_TEMPLATES** hace que se devuelva la tabla de uso único del contenedor, enumerando los tipos de entradas que se pueden crear en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="ffd85-141">Opening **PR_CREATE_TEMPLATES** causes the container's one-off table to be returned, listing the kinds of entries that can be created in the container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ffd85-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ffd85-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ffd85-143">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="ffd85-143">Protocol specifications</span></span>

<span data-ttu-id="ffd85-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffd85-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffd85-145">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="ffd85-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ffd85-146">[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffd85-146">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffd85-147">Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="ffd85-147">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="ffd85-148">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffd85-148">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffd85-149">Controla las comunicaciones de un cliente con un servidor de interfaz de proveedor de servicios de nombres (NSPI).</span><span class="sxs-lookup"><span data-stu-id="ffd85-149">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ffd85-150">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ffd85-150">Header files</span></span>

<span data-ttu-id="ffd85-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ffd85-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="ffd85-152">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ffd85-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="ffd85-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ffd85-153">Mapitags.h</span></span>
  
> <span data-ttu-id="ffd85-154">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="ffd85-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ffd85-155">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ffd85-155">See also</span></span>



[<span data-ttu-id="ffd85-156">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ffd85-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ffd85-157">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="ffd85-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ffd85-158">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ffd85-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ffd85-159">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ffd85-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

