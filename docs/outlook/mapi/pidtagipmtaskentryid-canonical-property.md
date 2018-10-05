---
title: Propiedad canónica PidTagIpmTaskEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmTaskEntryId
api_type:
- HeaderDef
ms.assetid: ec8b7486-b547-4a4e-96e5-1fc825b23f3d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c3845c745dcd2c18525f147308233b94fbce70d4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400253"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a><span data-ttu-id="72494-103">Propiedad canónica PidTagIpmTaskEntryId</span><span class="sxs-lookup"><span data-stu-id="72494-103">PidTagIpmTaskEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="72494-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72494-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72494-105">Contiene la **propiedad EntryID** de la carpeta tareas de Outlook.</span><span class="sxs-lookup"><span data-stu-id="72494-105">Contains the **EntryID** of the Outlook Tasks folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72494-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="72494-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="72494-107">PR_IPM_TASK_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="72494-107">PR_IPM_TASK_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="72494-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="72494-108">Identifier:</span></span>  <br/> |<span data-ttu-id="72494-109">0x36D4</span><span class="sxs-lookup"><span data-stu-id="72494-109">0x36D4</span></span>  <br/> |
|<span data-ttu-id="72494-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="72494-110">Data type:</span></span>  <br/> |<span data-ttu-id="72494-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="72494-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="72494-112">Área:</span><span class="sxs-lookup"><span data-stu-id="72494-112">Area:</span></span>  <br/> |<span data-ttu-id="72494-113">Folder</span><span class="sxs-lookup"><span data-stu-id="72494-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72494-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="72494-114">Remarks</span></span>

<span data-ttu-id="72494-115">Esta propiedad se lee o escribe mediante el protocolo de propiedad y el objeto Stream.</span><span class="sxs-lookup"><span data-stu-id="72494-115">This property is read or written by using the Property and Stream Object protocol.</span></span> <span data-ttu-id="72494-116">Es leen y escriben en la carpeta Bandeja de entrada o raíz.</span><span class="sxs-lookup"><span data-stu-id="72494-116">It is read from and written to the Inbox or Root folder.</span></span> <span data-ttu-id="72494-117">La implementación debe utilizar la carpeta Bandeja de entrada cuando el almacén es del usuario de mensajería principal, y debe usar la carpeta raíz cuando el almacén de es de un usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="72494-117">The implementation must use the Inbox folder when the store is that of the primary messaging user, and it must use the Root folder when the store is that of a delegate user.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="72494-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="72494-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="72494-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="72494-119">Protocol specifications</span></span>

<span data-ttu-id="72494-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72494-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72494-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="72494-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="72494-122">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72494-122">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72494-123">Especifica las propiedades y operaciones para la creación y la ubicación de las carpetas especiales en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="72494-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="72494-124">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72494-124">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72494-125">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="72494-125">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="72494-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="72494-126">Header files</span></span>

<span data-ttu-id="72494-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="72494-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="72494-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="72494-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="72494-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="72494-129">Mapitags.h</span></span>
  
> <span data-ttu-id="72494-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="72494-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72494-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="72494-131">See also</span></span>



[<span data-ttu-id="72494-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="72494-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72494-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="72494-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72494-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="72494-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72494-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="72494-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

