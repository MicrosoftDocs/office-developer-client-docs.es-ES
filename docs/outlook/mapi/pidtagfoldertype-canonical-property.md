---
title: Propiedad canónica PidTagFolderType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7cca884eae2111a94d87cc24a6d30542148ab845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316320"
---
# <a name="pidtagfoldertype-canonical-property"></a><span data-ttu-id="87da0-103">Propiedad canónica PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="87da0-103">PidTagFolderType Canonical Property</span></span>

  
  
<span data-ttu-id="87da0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87da0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87da0-105">Contiene una constante que indica el tipo de carpeta.</span><span class="sxs-lookup"><span data-stu-id="87da0-105">Contains a constant that indicates the folder type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87da0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="87da0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87da0-107">PR_FOLDER_TYPE</span><span class="sxs-lookup"><span data-stu-id="87da0-107">PR_FOLDER_TYPE</span></span>  <br/> |
|<span data-ttu-id="87da0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="87da0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="87da0-109">0x3601</span><span class="sxs-lookup"><span data-stu-id="87da0-109">0x3601</span></span>  <br/> |
|<span data-ttu-id="87da0-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="87da0-110">Data type:</span></span>  <br/> |<span data-ttu-id="87da0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="87da0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="87da0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="87da0-112">Area:</span></span>  <br/> |<span data-ttu-id="87da0-113">Contenedor de MAPI</span><span class="sxs-lookup"><span data-stu-id="87da0-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87da0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="87da0-114">Remarks</span></span>

<span data-ttu-id="87da0-115">Esta propiedad puede tener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="87da0-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="87da0-116">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="87da0-116">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="87da0-117">Una carpeta genérica que contiene mensajes y otras carpetas.</span><span class="sxs-lookup"><span data-stu-id="87da0-117">A generic folder that contains messages and other folders.</span></span>
    
<span data-ttu-id="87da0-118">FOLDER_ROOT</span><span class="sxs-lookup"><span data-stu-id="87da0-118">FOLDER_ROOT</span></span> 
  
> <span data-ttu-id="87da0-119">La carpeta raíz de la tabla jerarquía de carpetas, es decir, una carpeta que no tiene carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="87da0-119">The root folder of the folder hierarchy table, that is, a folder that has no parent folder.</span></span>
    
<span data-ttu-id="87da0-120">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="87da0-120">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="87da0-121">Una carpeta que contiene los resultados de una búsqueda, en forma de vínculos a mensajes que cumplen los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="87da0-121">A folder that contains the results of a search, in the form of links to messages that meet search criteria.</span></span>
    
<span data-ttu-id="87da0-122">La raíz de un almacén de mensajes no debe confundirse con la raíz del subárbol de mensaje interpersonal (IPM) de ese almacén.</span><span class="sxs-lookup"><span data-stu-id="87da0-122">The root of a message store should not be confused with the root of the interpersonal message (IPM) subtree in that store.</span></span> <span data-ttu-id="87da0-123">La carpeta raíz de la tienda, que no tiene ningún elemento primario, se obtiene llamando al método [IMsgStore:: OpenEntry](imsgstore-openentry.md) con un identificador de entrada null.</span><span class="sxs-lookup"><span data-stu-id="87da0-123">The store's root folder, which has no parent, is obtained by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with a null entry identifier.</span></span> <span data-ttu-id="87da0-124">La carpeta raíz del subárbol IPM, que tiene un elemento primario, se obtiene mediante el valor de la propiedad **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) para la llamada **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="87da0-124">The IPM subtree's root folder, which does have a parent, is obtained by using the value of the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property for the **OpenEntry** call.</span></span> 
  
<span data-ttu-id="87da0-125">MAPI solo permite una carpeta raíz por almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="87da0-125">MAPI allows only one root folder per message store.</span></span> <span data-ttu-id="87da0-126">Esta carpeta contiene mensajes y otras carpetas.</span><span class="sxs-lookup"><span data-stu-id="87da0-126">This folder contains messages and other folders.</span></span> <span data-ttu-id="87da0-127">La propiedad **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) de la carpeta raíz contiene el identificador de entrada propio de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="87da0-127">The root folder's **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property contains the folder's own entry identifier.</span></span>
  
<span data-ttu-id="87da0-128">La información de una carpeta de resultados de búsqueda se almacena principalmente en su tabla de contenido, que contiene las mismas columnas que una tabla de contenido típica, así como dos columnas adicionales que identifican la carpeta en la que se encontró cada mensaje: **PR_PARENT_DISPLAY** ([ PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (nombre para mostrar, obligatorio) y esta propiedad (identificador de entrada, opcional).</span><span class="sxs-lookup"><span data-stu-id="87da0-128">The information in a search-results folder is mainly stored in its contents table, which contains the same columns as a typical contents table, as well as two extra columns identifying the folder in which each message was found: **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (display name, required) and this property (entry identifier, optional).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="87da0-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="87da0-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="87da0-130">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="87da0-130">Protocol specifications</span></span>

<span data-ttu-id="87da0-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87da0-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87da0-132">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="87da0-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="87da0-133">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87da0-133">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87da0-134">Controla las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="87da0-134">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="87da0-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="87da0-135">Header files</span></span>

<span data-ttu-id="87da0-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="87da0-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="87da0-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="87da0-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="87da0-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="87da0-138">Mapitags.h</span></span>
  
> <span data-ttu-id="87da0-139">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="87da0-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87da0-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="87da0-140">See also</span></span>



[<span data-ttu-id="87da0-141">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="87da0-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87da0-142">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="87da0-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87da0-143">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="87da0-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87da0-144">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="87da0-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

