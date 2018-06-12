---
title: Propiedad canónico PidTagParentEntryId
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: ba30514df028805135e9e31e7214ca336b1b3f85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819918"
---
# <a name="pidtagparententryid-canonical-property"></a><span data-ttu-id="45b62-103">Propiedad canónico PidTagParentEntryId</span><span class="sxs-lookup"><span data-stu-id="45b62-103">PidTagParentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="45b62-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45b62-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45b62-105">Contiene el identificador de entrada de la carpeta que contiene una carpeta o mensaje.</span><span class="sxs-lookup"><span data-stu-id="45b62-105">Contains the entry identifier of the folder that contains a folder or message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45b62-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="45b62-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45b62-107">PR_PARENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="45b62-107">PR_PARENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="45b62-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="45b62-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45b62-109">0x0E09</span><span class="sxs-lookup"><span data-stu-id="45b62-109">0x0E09</span></span>  <br/> |
|<span data-ttu-id="45b62-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="45b62-110">Data type:</span></span>  <br/> |<span data-ttu-id="45b62-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="45b62-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="45b62-112">Área:</span><span class="sxs-lookup"><span data-stu-id="45b62-112">Area:</span></span>  <br/> |<span data-ttu-id="45b62-113">Propiedades de Id.</span><span class="sxs-lookup"><span data-stu-id="45b62-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45b62-114">Notas</span><span class="sxs-lookup"><span data-stu-id="45b62-114">Remarks</span></span>

<span data-ttu-id="45b62-115">Esta propiedad se calcula mediante los almacenes de mensajes para todos los mensajes y carpetas.</span><span class="sxs-lookup"><span data-stu-id="45b62-115">This property is computed by message stores for all folders and messages.</span></span>
  
<span data-ttu-id="45b62-116">Para una carpeta raíz del almacén de mensajes, esta propiedad contiene el identificador de entrada de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="45b62-116">For a message store root folder, this property contains the folder's own entry identifier.</span></span>
  
 <span data-ttu-id="45b62-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) y esta propiedad no están relacionados entre sí.</span><span class="sxs-lookup"><span data-stu-id="45b62-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) and this property are not related to each other.</span></span> <span data-ttu-id="45b62-118">Pertenecieran a contextos totalmente diferentes.</span><span class="sxs-lookup"><span data-stu-id="45b62-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45b62-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="45b62-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45b62-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="45b62-120">Protocol specifications</span></span>

<span data-ttu-id="45b62-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45b62-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45b62-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="45b62-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45b62-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45b62-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45b62-124">Define las estructuras de datos básicos que se usan en las operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="45b62-124">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="45b62-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45b62-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45b62-126">Controla las operaciones de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="45b62-126">Handles folder operations.</span></span>
    
<span data-ttu-id="45b62-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45b62-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45b62-128">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="45b62-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="45b62-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45b62-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45b62-130">Permite la manipulación de las listas Permitir o bloquear y la determinación de los mensajes de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="45b62-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="45b62-131">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45b62-131">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45b62-132">Especifica las propiedades y operaciones para la creación y la ubicación de las carpetas especiales en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="45b62-132">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="45b62-133">[[MS-OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45b62-133">[[MS-OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45b62-134">Especifica el método de entrega de datos (OAB) de la libreta de direcciones sin conexión de servidor a cliente.</span><span class="sxs-lookup"><span data-stu-id="45b62-134">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45b62-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="45b62-135">Header files</span></span>

<span data-ttu-id="45b62-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45b62-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="45b62-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="45b62-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="45b62-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45b62-138">Mapitags.h</span></span>
  
> <span data-ttu-id="45b62-139">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="45b62-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45b62-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="45b62-140">See also</span></span>



[<span data-ttu-id="45b62-141">Propiedad canónico PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="45b62-141">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="45b62-142">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="45b62-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45b62-143">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="45b62-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45b62-144">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="45b62-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45b62-145">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="45b62-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

