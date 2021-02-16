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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327855"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a><span data-ttu-id="d34db-103">Propiedad canónica PidTagIpmTaskEntryId</span><span class="sxs-lookup"><span data-stu-id="d34db-103">PidTagIpmTaskEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="d34db-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d34db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d34db-105">Contiene el **EntryID de** la carpeta Tareas de Outlook.</span><span class="sxs-lookup"><span data-stu-id="d34db-105">Contains the **EntryID** of the Outlook Tasks folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d34db-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d34db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d34db-107">PR_IPM_TASK_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d34db-107">PR_IPM_TASK_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="d34db-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d34db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d34db-109">0x36D4</span><span class="sxs-lookup"><span data-stu-id="d34db-109">0x36D4</span></span>  <br/> |
|<span data-ttu-id="d34db-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d34db-110">Data type:</span></span>  <br/> |<span data-ttu-id="d34db-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d34db-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d34db-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d34db-112">Area:</span></span>  <br/> |<span data-ttu-id="d34db-113">Folder</span><span class="sxs-lookup"><span data-stu-id="d34db-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d34db-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d34db-114">Remarks</span></span>

<span data-ttu-id="d34db-115">Esta propiedad se lee o escribe mediante el protocolo Property y Stream Object.</span><span class="sxs-lookup"><span data-stu-id="d34db-115">This property is read or written by using the Property and Stream Object protocol.</span></span> <span data-ttu-id="d34db-116">Se lee y se escribe en la bandeja de entrada o en la carpeta raíz.</span><span class="sxs-lookup"><span data-stu-id="d34db-116">It is read from and written to the Inbox or Root folder.</span></span> <span data-ttu-id="d34db-117">La implementación debe usar la carpeta Bandeja de entrada cuando el almacén es el del usuario de mensajería principal y debe usar la carpeta raíz cuando el almacén es el de un usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="d34db-117">The implementation must use the Inbox folder when the store is that of the primary messaging user, and it must use the Root folder when the store is that of a delegate user.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d34db-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d34db-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d34db-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="d34db-119">Protocol specifications</span></span>

<span data-ttu-id="d34db-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d34db-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d34db-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="d34db-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d34db-122">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d34db-122">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d34db-123">Especifica las propiedades y las operaciones para crear y buscar las carpetas especiales en un buzón.</span><span class="sxs-lookup"><span data-stu-id="d34db-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="d34db-124">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d34db-124">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d34db-125">Especifica métodos para conectar y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="d34db-125">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d34db-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d34db-126">Header files</span></span>

<span data-ttu-id="d34db-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d34db-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="d34db-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d34db-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="d34db-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d34db-129">Mapitags.h</span></span>
  
> <span data-ttu-id="d34db-130">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d34db-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d34db-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d34db-131">See also</span></span>



[<span data-ttu-id="d34db-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d34db-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d34db-133">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="d34db-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d34db-134">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d34db-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d34db-135">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="d34db-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

