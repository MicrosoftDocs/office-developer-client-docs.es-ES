---
title: Propiedad canónica PidTagExtendedFolderFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedFolderFlags
api_type:
- HeaderDef
ms.assetid: e0c04f98-3d66-4ab5-ba05-69f9df539fcf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fe14f6ca101e6a546f99989ecc87b0c516ee5df4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316355"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a><span data-ttu-id="3f262-103">Propiedad canónica PidTagExtendedFolderFlags</span><span class="sxs-lookup"><span data-stu-id="3f262-103">PidTagExtendedFolderFlags Canonical Property</span></span>
 
<span data-ttu-id="3f262-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f262-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f262-105">Contiene marcas extendidas acerca de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="3f262-105">Contains extended flags about a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3f262-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3f262-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3f262-107">PR_EXTENDED_FOLDER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="3f262-107">PR_EXTENDED_FOLDER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="3f262-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3f262-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3f262-109">0x36DA</span><span class="sxs-lookup"><span data-stu-id="3f262-109">0x36DA</span></span>  <br/> |
|<span data-ttu-id="3f262-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3f262-110">Data type:</span></span>  <br/> |<span data-ttu-id="3f262-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3f262-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3f262-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3f262-112">Area:</span></span>  <br/> |<span data-ttu-id="3f262-113">Contenedor MAPI</span><span class="sxs-lookup"><span data-stu-id="3f262-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f262-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3f262-114">Remarks</span></span>

<span data-ttu-id="3f262-115">Esta propiedad es una secuencia binaria que contiene sub-propiedades codificadas para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="3f262-115">This property is a binary stream that contains encoded sub-properties for the folder.</span></span> <span data-ttu-id="3f262-116">Tiene el formato de una serie de sub elementos de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="3f262-116">It is formatted as a series of variable length sub items.</span></span> <span data-ttu-id="3f262-117">Los primeros 8 bits del sub elemento son un campo id., que indica qué tipo de marca representa el sub elemento.</span><span class="sxs-lookup"><span data-stu-id="3f262-117">The first 8 bits of the sub item is an ID field, which indicates what kind of flag the sub item represents.</span></span> <span data-ttu-id="3f262-118">Los segundos 8 bits son el número de bytes de datos siguientes.</span><span class="sxs-lookup"><span data-stu-id="3f262-118">The second 8 bits is the number of bytes of data that follow.</span></span>
  
<span data-ttu-id="3f262-119">Entre los posibles valores de id. se incluyen:</span><span class="sxs-lookup"><span data-stu-id="3f262-119">Possible ID values include:</span></span>
  
- <span data-ttu-id="3f262-120">Invalid</span><span class="sxs-lookup"><span data-stu-id="3f262-120">Invalid</span></span>
    
   <span data-ttu-id="3f262-121">No usar este valor</span><span class="sxs-lookup"><span data-stu-id="3f262-121">Do not use this value</span></span>
    
- <span data-ttu-id="3f262-122">ExtendedFlags</span><span class="sxs-lookup"><span data-stu-id="3f262-122">ExtendedFlags</span></span>
    
   <span data-ttu-id="3f262-123">Los datos son un valor de cuatro bytes con el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="3f262-123">The data is a four byte value formatted as:</span></span>
    
   |<span data-ttu-id="3f262-124">**Bits**</span><span class="sxs-lookup"><span data-stu-id="3f262-124">**Bits**</span></span>|<span data-ttu-id="3f262-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f262-125">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="3f262-126">0-1</span><span class="sxs-lookup"><span data-stu-id="3f262-126">0-1</span></span>  <br/> |<span data-ttu-id="3f262-127">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3f262-127">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="3f262-128">2</span><span class="sxs-lookup"><span data-stu-id="3f262-128">2</span></span>  <br/> |<span data-ttu-id="3f262-129">Se establece en 0 si la aplicación debe mostrar una descripción de directiva.</span><span class="sxs-lookup"><span data-stu-id="3f262-129">Set to 0 if the application should show a policy description.</span></span>  <br/> |
   |<span data-ttu-id="3f262-130">3-5</span><span class="sxs-lookup"><span data-stu-id="3f262-130">3-5</span></span>  <br/> |<span data-ttu-id="3f262-131">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3f262-131">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="3f262-132">6-7</span><span class="sxs-lookup"><span data-stu-id="3f262-132">6-7</span></span>  <br/> |<span data-ttu-id="3f262-133">Controla la visualización del número de mensajes de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="3f262-133">Controls the display of the number of messages in the folder.</span></span>  <br/> <span data-ttu-id="3f262-134">0: usar la configuración predeterminada</span><span class="sxs-lookup"><span data-stu-id="3f262-134">0 - Use the default setting</span></span>  <br/> <span data-ttu-id="3f262-135">1: usar el número de mensajes no leídos</span><span class="sxs-lookup"><span data-stu-id="3f262-135">1 - Use the number of unread messages</span></span>  <br/> <span data-ttu-id="3f262-136">3: usar el número total de mensajes</span><span class="sxs-lookup"><span data-stu-id="3f262-136">3 - Use the total number of messages</span></span>  <br/> |
   |<span data-ttu-id="3f262-137">8-31</span><span class="sxs-lookup"><span data-stu-id="3f262-137">8-31</span></span>  <br/> |<span data-ttu-id="3f262-138">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3f262-138">Reserved.</span></span>  <br/> |
   
<span data-ttu-id="3f262-139">Los elementos reservados se pueden omitir, pero los valores existentes deben conservarse.</span><span class="sxs-lookup"><span data-stu-id="3f262-139">Reserved items can be ignored, but existing values must be preserved.</span></span>
    
- <span data-ttu-id="3f262-140">SearchFolderID</span><span class="sxs-lookup"><span data-stu-id="3f262-140">SearchFolderID</span></span>
    
   <span data-ttu-id="3f262-141">El campo de datos es un campo de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="3f262-141">The data field is a 16-byte field.</span></span> <span data-ttu-id="3f262-142">Cuando la aplicación crea una carpeta de búsqueda persistente, debe establecer este campo en la carpeta en el mismo valor que la propiedad binaria **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) en el mensaje de carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3f262-142">When the application creates a persistent search folder, it must set this field on the folder to the same value as the **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) binary property on the Search Folder Message.</span></span>
    
- <span data-ttu-id="3f262-143">ToDoFolderVersion</span><span class="sxs-lookup"><span data-stu-id="3f262-143">ToDoFolderVersion</span></span>
    
   <span data-ttu-id="3f262-144">El campo de datos es un campo de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="3f262-144">The data field is a 4-byte field.</span></span> <span data-ttu-id="3f262-145">Cuando la aplicación crea la carpeta de búsqueda para hacer, debe establecer el valor de este campo en la carpeta en el valor entero little-endian de" 0x000c0000":</span><span class="sxs-lookup"><span data-stu-id="3f262-145">When the application creates the to-do search folder, it must set the value of this field on the folder to the little-endian integer value of" 0x000c0000":</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="3f262-146">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3f262-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3f262-147">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="3f262-147">Protocol specifications</span></span>

<span data-ttu-id="3f262-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3f262-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3f262-149">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="3f262-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3f262-150">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3f262-150">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3f262-151">Especifica la ubicación y las propiedades de los datos de configuración de cliente y servidor, como listas de categorías compartidas y horas laborables.</span><span class="sxs-lookup"><span data-stu-id="3f262-151">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="3f262-152">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3f262-152">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3f262-153">Especifica las propiedades y las operaciones para manipular una configuración de lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3f262-153">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3f262-154">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3f262-154">Header files</span></span>

<span data-ttu-id="3f262-155">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3f262-155">Mapidefs.h</span></span>
  
> <span data-ttu-id="3f262-156">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3f262-156">Provides data type definitions.</span></span>
    
<span data-ttu-id="3f262-157">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3f262-157">Mapitags.h</span></span>
  
> <span data-ttu-id="3f262-158">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="3f262-158">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3f262-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f262-159">See also</span></span>

- [<span data-ttu-id="3f262-160">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3f262-160">MAPI Properties</span></span>](mapi-properties.md)
- [<span data-ttu-id="3f262-161">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3f262-161">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="3f262-162">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3f262-162">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="3f262-163">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="3f262-163">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

