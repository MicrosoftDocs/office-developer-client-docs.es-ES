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
ms.openlocfilehash: 4a4d3c940539c23be8ec212cb85e3dd4f3a04aab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819499"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a><span data-ttu-id="1b7a6-103">Propiedad canónica PidTagExtendedFolderFlags</span><span class="sxs-lookup"><span data-stu-id="1b7a6-103">PidTagExtendedFolderFlags Canonical Property</span></span>
 
<span data-ttu-id="1b7a6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b7a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b7a6-105">Contiene indicadores extendidas acerca de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-105">Contains extended flags about a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b7a6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1b7a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b7a6-107">PR_EXTENDED_FOLDER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="1b7a6-107">PR_EXTENDED_FOLDER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="1b7a6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1b7a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1b7a6-109">0x36DA</span><span class="sxs-lookup"><span data-stu-id="1b7a6-109">0x36DA</span></span>  <br/> |
|<span data-ttu-id="1b7a6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1b7a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="1b7a6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1b7a6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1b7a6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1b7a6-112">Area:</span></span>  <br/> |<span data-ttu-id="1b7a6-113">Contenedor MAPI</span><span class="sxs-lookup"><span data-stu-id="1b7a6-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b7a6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1b7a6-114">Remarks</span></span>

<span data-ttu-id="1b7a6-115">Esta propiedad es una secuencia binaria que contiene propiedades de subcaracterística codificadas para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-115">This property is a binary stream that contains encoded sub-properties for the folder.</span></span> <span data-ttu-id="1b7a6-116">Si tiene un formato como una serie de elementos de sub de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-116">It is formatted as a series of variable length sub items.</span></span> <span data-ttu-id="1b7a6-117">Los primeros 8 bits del elemento sub es un campo de identificador, lo que indica el tipo de marca que representa el elemento sub.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-117">The first 8 bits of the sub item is an ID field, which indicates what kind of flag the sub item represents.</span></span> <span data-ttu-id="1b7a6-118">La segundos 8 bits es el número de bytes de datos que le siguen.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-118">The second 8 bits is the number of bytes of data that follow.</span></span>
  
<span data-ttu-id="1b7a6-119">Los valores de identificador posibles son:</span><span class="sxs-lookup"><span data-stu-id="1b7a6-119">Possible ID values include:</span></span>
  
- <span data-ttu-id="1b7a6-120">Invalid</span><span class="sxs-lookup"><span data-stu-id="1b7a6-120">Invalid</span></span>
    
   <span data-ttu-id="1b7a6-121">No utilice este valor</span><span class="sxs-lookup"><span data-stu-id="1b7a6-121">Do not use this value</span></span>
    
- <span data-ttu-id="1b7a6-122">ExtendedFlags</span><span class="sxs-lookup"><span data-stu-id="1b7a6-122">ExtendedFlags</span></span>
    
   <span data-ttu-id="1b7a6-123">Los datos están un valor de cuatro bytes con formato como:</span><span class="sxs-lookup"><span data-stu-id="1b7a6-123">The data is a four byte value formatted as:</span></span>
    
   |<span data-ttu-id="1b7a6-124">**Bits**</span><span class="sxs-lookup"><span data-stu-id="1b7a6-124">**Bits**</span></span>|<span data-ttu-id="1b7a6-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1b7a6-125">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="1b7a6-126">0-1</span><span class="sxs-lookup"><span data-stu-id="1b7a6-126">0-1</span></span>  <br/> |<span data-ttu-id="1b7a6-127">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-127">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="1b7a6-128">2</span><span class="sxs-lookup"><span data-stu-id="1b7a6-128">2</span></span>  <br/> |<span data-ttu-id="1b7a6-129">Se establece en 0 si la aplicación debe mostrar una descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-129">Set to 0 if the application should show a policy description.</span></span>  <br/> |
   |<span data-ttu-id="1b7a6-130">3-5</span><span class="sxs-lookup"><span data-stu-id="1b7a6-130">3-5</span></span>  <br/> |<span data-ttu-id="1b7a6-131">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-131">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="1b7a6-132">6-7</span><span class="sxs-lookup"><span data-stu-id="1b7a6-132">6-7</span></span>  <br/> |<span data-ttu-id="1b7a6-133">Controla la visualización del número de mensajes en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-133">Controls the display of the number of messages in the folder.</span></span>  <br/> <span data-ttu-id="1b7a6-134">0 - utilizar la configuración predeterminada</span><span class="sxs-lookup"><span data-stu-id="1b7a6-134">0 - Use the default setting</span></span>  <br/> <span data-ttu-id="1b7a6-135">1: usar el número de mensajes no leídos</span><span class="sxs-lookup"><span data-stu-id="1b7a6-135">1 - Use the number of unread messages</span></span>  <br/> <span data-ttu-id="1b7a6-136">3 - usar el número total de mensajes</span><span class="sxs-lookup"><span data-stu-id="1b7a6-136">3 - Use the total number of messages</span></span>  <br/> |
   |<span data-ttu-id="1b7a6-137">8-31</span><span class="sxs-lookup"><span data-stu-id="1b7a6-137">8-31</span></span>  <br/> |<span data-ttu-id="1b7a6-138">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-138">Reserved.</span></span>  <br/> |
   
<span data-ttu-id="1b7a6-139">Artículos reservados pueden omitirse, pero deben conservarse los valores existentes.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-139">Reserved items can be ignored, but existing values must be preserved.</span></span>
    
- <span data-ttu-id="1b7a6-140">SearchFolderID</span><span class="sxs-lookup"><span data-stu-id="1b7a6-140">SearchFolderID</span></span>
    
   <span data-ttu-id="1b7a6-141">El campo de datos es un campo de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-141">The data field is a 16-byte field.</span></span> <span data-ttu-id="1b7a6-142">Cuando la aplicación crea una carpeta de búsqueda persistente, debe establecer este campo en la carpeta en el mismo valor que la **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) una propiedad binaria en el mensaje de la carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-142">When the application creates a persistent search folder, it must set this field on the folder to the same value as the **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) binary property on the Search Folder Message.</span></span>
    
- <span data-ttu-id="1b7a6-143">ToDoFolderVersion</span><span class="sxs-lookup"><span data-stu-id="1b7a6-143">ToDoFolderVersion</span></span>
    
   <span data-ttu-id="1b7a6-144">El campo de datos es un campo de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-144">The data field is a 4-byte field.</span></span> <span data-ttu-id="1b7a6-145">Cuando la aplicación crea la carpeta de búsqueda de tareas pendientes, debe establecer el valor de este campo en la carpeta para el valor entero de "little-endian" de "0x000c0000":</span><span class="sxs-lookup"><span data-stu-id="1b7a6-145">When the application creates the to-do search folder, it must set the value of this field on the folder to the little-endian integer value of" 0x000c0000":</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="1b7a6-146">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b7a6-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1b7a6-147">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1b7a6-147">Protocol specifications</span></span>

<span data-ttu-id="1b7a6-148">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b7a6-148">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b7a6-149">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1b7a6-150">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b7a6-150">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b7a6-151">Especifica la ubicación y las propiedades de datos de configuración de cliente y servidor, como las listas de categoría compartida y horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-151">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="1b7a6-152">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b7a6-152">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b7a6-153">Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-153">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1b7a6-154">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1b7a6-154">Header files</span></span>

<span data-ttu-id="1b7a6-155">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b7a6-155">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b7a6-156">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-156">Provides data type definitions.</span></span>
    
<span data-ttu-id="1b7a6-157">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1b7a6-157">Mapitags.h</span></span>
  
> <span data-ttu-id="1b7a6-158">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1b7a6-158">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b7a6-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b7a6-159">See also</span></span>

- [<span data-ttu-id="1b7a6-160">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1b7a6-160">MAPI Properties</span></span>](mapi-properties.md)
- [<span data-ttu-id="1b7a6-161">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1b7a6-161">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="1b7a6-162">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1b7a6-162">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="1b7a6-163">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="1b7a6-163">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

