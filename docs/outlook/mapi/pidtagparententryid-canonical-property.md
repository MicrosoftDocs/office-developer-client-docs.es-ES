---
title: Propiedad canónica PidTagParentEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentEntryId
api_type:
- COM
ms.assetid: 55e08ace-493c-4246-8ebf-c304f4abc56a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 65f5e6c5da88267ec2e63d0acf3ef6f8e10c893b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348233"
---
# <a name="pidtagparententryid-canonical-property"></a><span data-ttu-id="cf3d7-103">Propiedad canónica PidTagParentEntryId</span><span class="sxs-lookup"><span data-stu-id="cf3d7-103">PidTagParentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="cf3d7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf3d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf3d7-105">Contiene el identificador de entrada de la carpeta que contiene una carpeta o un mensaje.</span><span class="sxs-lookup"><span data-stu-id="cf3d7-105">Contains the entry identifier of the folder that contains a folder or message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cf3d7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cf3d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cf3d7-107">PR_PARENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cf3d7-107">PR_PARENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="cf3d7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cf3d7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cf3d7-109">0x0E09</span><span class="sxs-lookup"><span data-stu-id="cf3d7-109">0x0E09</span></span>  <br/> |
|<span data-ttu-id="cf3d7-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cf3d7-110">Data type:</span></span>  <br/> |<span data-ttu-id="cf3d7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cf3d7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cf3d7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cf3d7-112">Area:</span></span>  <br/> |<span data-ttu-id="cf3d7-113">Propiedades de identificador</span><span class="sxs-lookup"><span data-stu-id="cf3d7-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf3d7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cf3d7-114">Remarks</span></span>

<span data-ttu-id="cf3d7-115">Los almacenes de mensajes calculan esta propiedad para todas las carpetas y los mensajes.</span><span class="sxs-lookup"><span data-stu-id="cf3d7-115">This property is computed by message stores for all folders and messages.</span></span>
  
<span data-ttu-id="cf3d7-116">Para una carpeta raíz del almacén de mensajes, esta propiedad contiene el identificador de entrada propio de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="cf3d7-116">For a message store root folder, this property contains the folder's own entry identifier.</span></span>
  
 <span data-ttu-id="cf3d7-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) y esta propiedad no están relacionadas entre sí.</span><span class="sxs-lookup"><span data-stu-id="cf3d7-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) and this property are not related to each other.</span></span> <span data-ttu-id="cf3d7-118">Pertenecen a contextos completamente diferentes.</span><span class="sxs-lookup"><span data-stu-id="cf3d7-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cf3d7-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf3d7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cf3d7-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="cf3d7-120">Protocol specifications</span></span>

<span data-ttu-id="cf3d7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf3d7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf3d7-122">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="cf3d7-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cf3d7-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf3d7-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf3d7-124">Define las estructuras de datos básicas que se usan en las operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="cf3d7-124">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="cf3d7-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf3d7-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf3d7-126">Controla las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="cf3d7-126">Handles folder operations.</span></span>
    
<span data-ttu-id="cf3d7-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf3d7-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf3d7-128">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="cf3d7-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="cf3d7-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf3d7-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf3d7-130">Habilita el control de las listas de permitidos y bloqueados y la determinación de los mensajes de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="cf3d7-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="cf3d7-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf3d7-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf3d7-132">Especifica las propiedades y operaciones para crear y ubicar las carpetas especiales en un buzón.</span><span class="sxs-lookup"><span data-stu-id="cf3d7-132">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="cf3d7-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf3d7-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf3d7-134">Especifica el método de entrega de datos de la libreta de direcciones sin conexión del servidor al cliente.</span><span class="sxs-lookup"><span data-stu-id="cf3d7-134">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cf3d7-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cf3d7-135">Header files</span></span>

<span data-ttu-id="cf3d7-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cf3d7-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="cf3d7-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cf3d7-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="cf3d7-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="cf3d7-138">Mapitags.h</span></span>
  
> <span data-ttu-id="cf3d7-139">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="cf3d7-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cf3d7-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf3d7-140">See also</span></span>



[<span data-ttu-id="cf3d7-141">Propiedad canónica PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="cf3d7-141">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="cf3d7-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cf3d7-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cf3d7-143">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="cf3d7-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cf3d7-144">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cf3d7-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cf3d7-145">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="cf3d7-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

