---
title: Propiedad canónica PidTagConflictItems
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConflictItems
api_type:
- HeaderDef
ms.assetid: 0d147827-f0e2-dcc1-4427-c4a2f48ca801
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 83940d9239bc172d5fab76232f6644f0e89033b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338020"
---
# <a name="pidtagconflictitems-canonical-property"></a><span data-ttu-id="cc7c2-103">Propiedad canónica PidTagConflictItems</span><span class="sxs-lookup"><span data-stu-id="cc7c2-103">PidTagConflictItems Canonical Property</span></span>

  
  
<span data-ttu-id="cc7c2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc7c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc7c2-105">Contiene uno o más identificadores de entrada de elementos que se han implicado en una resolución automática de conflictos.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-105">Contains one or more entry IDs of items that have been involved in an automatic conflict resolution.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="cc7c2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cc7c2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc7c2-107">PR_CONFLICT_ITEMS</span><span class="sxs-lookup"><span data-stu-id="cc7c2-107">PR_CONFLICT_ITEMS</span></span>  <br/> |
|<span data-ttu-id="cc7c2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cc7c2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cc7c2-109">0x1098</span><span class="sxs-lookup"><span data-stu-id="cc7c2-109">0x1098</span></span>  <br/> |
|<span data-ttu-id="cc7c2-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="cc7c2-110">Property type:</span></span>  <br/> |<span data-ttu-id="cc7c2-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="cc7c2-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="cc7c2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cc7c2-112">Area:</span></span>  <br/> |<span data-ttu-id="cc7c2-113">ICS</span><span class="sxs-lookup"><span data-stu-id="cc7c2-113">ICS</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc7c2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc7c2-114">Remarks</span></span>

<span data-ttu-id="cc7c2-115">Los tipos de elementos estándar de Microsoft Outlook que admiten la resolución automática de conflictos incluyen los siguientes tipos de elementos estándar: elementos de cita, elementos de contacto, elementos de diario, elementos de correo, elementos de reunión, elementos de nota permanente y elementos de tareas.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-115">The types of standard Microsoft Outlook items that support automatic conflict resolution include the following standard item types: appointment items, contact items, journal items, mail items, meeting items, sticky note items, and task items.</span></span> <span data-ttu-id="cc7c2-116">Un elemento que pertenece a una clase de mensaje que deriva de uno de estos tipos de elementos estándar también admite la resolución automática de conflictos.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-116">An item belonging to a message class that derives from one of these standard item types also supports automatic conflict resolution.</span></span> <span data-ttu-id="cc7c2-117">En Microsoft Outlook 2003 y Microsoft Office Outlook 2007, cuando Outlook sincroniza elementos y considera que existe la posibilidad de que la copia resultante no contenga  todos los datos esenciales, Outlook almacena las copias en conflicto en la carpeta **Conflictos,** en la carpeta Problemas de sincronización.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-117">In Microsoft Outlook 2003 and Microsoft Office Outlook 2007, when Outlook synchronizes items and considers that there is a possibility that the resultant copy may not contain all essential data, Outlook stores the conflicting copies in the **Conflicts** folder, under the **Sync Issues** folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cc7c2-118">**Los problemas de** sincronización y sus subcarpetas están ocultos hasta que haga clic en **Lista de carpetas** en el **menú** Ir.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-118">**Sync Issues** and its subfolders are hidden until you click **Folder List** on the **Go** menu.</span></span> 
  
<span data-ttu-id="cc7c2-119">Un elemento expone la propiedad **PR_CONFLICT_ITEMS** si es uno de los tipos de elementos que admiten la resolución automática de conflictos, si ha ganado en una resolución de conflictos o se ha colocado en la carpeta Conflictos debido a una resolución de **conflictos.**</span><span class="sxs-lookup"><span data-stu-id="cc7c2-119">An item exposes the **PR_CONFLICT_ITEMS** property if it is one of the item types that support automatic conflict resolution, has won in a conflict resolution, or was placed in the **Conflicts** folder because of a conflict resolution.</span></span> <span data-ttu-id="cc7c2-120">La carpeta en la que se coloca el elemento determina el contenido de **PR_CONFLICT_ITEMS**.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-120">The folder in which the item is placed determines the content of **PR_CONFLICT_ITEMS**.</span></span> <span data-ttu-id="cc7c2-121">Si el elemento se encuentra en una carpeta que no sea la carpeta **Conflictos** y el elemento expone la propiedad **PR_CONFLICT_ITEMS,** el elemento debe haber ganado la resolución de conflictos y **PR_CONFLICT_ITEMS** contendrá uno o más identificadores de entrada de los elementos que perdieron en la resolución de conflictos.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-121">If the item is located in some folder other than the **Conflicts** folder, and the item exposes the **PR_CONFLICT_ITEMS** property, the item must have won the conflict resolution, and **PR_CONFLICT_ITEMS** would contain one or more entry IDs of those items that lost in the conflict resolution.</span></span> <span data-ttu-id="cc7c2-122">Si el elemento se encuentra en la carpeta **Conflictos** y el elemento expone la propiedad **PR_CONFLICT_ITEMS,** este elemento debe haber perdido la resolución de conflictos y **PR_CONFLICT_ITEMS** contendrá el identificador de entrada del elemento que ha ganado en la resolución de conflictos.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-122">If the item is located in the **Conflicts** folder and the item exposes the **PR_CONFLICT_ITEMS** property, this item must have lost the conflict resolution, and **PR_CONFLICT_ITEMS** would contain the entry ID of the item that won in the conflict resolution.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cc7c2-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc7c2-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cc7c2-124">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="cc7c2-124">Protocol specifications</span></span>

<span data-ttu-id="cc7c2-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc7c2-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc7c2-126">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cc7c2-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc7c2-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc7c2-128">Controla la sincronización de datos de objetos de mensajería entre un servidor y un cliente.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-128">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cc7c2-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cc7c2-129">Header files</span></span>

<span data-ttu-id="cc7c2-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cc7c2-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc7c2-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="cc7c2-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cc7c2-132">Mapitags.h</span></span>
  
> <span data-ttu-id="cc7c2-133">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="cc7c2-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc7c2-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc7c2-134">See also</span></span>



[<span data-ttu-id="cc7c2-135">Acerca de las adiciones de MAPI</span><span class="sxs-lookup"><span data-stu-id="cc7c2-135">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="cc7c2-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cc7c2-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc7c2-137">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="cc7c2-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc7c2-138">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cc7c2-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc7c2-139">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="cc7c2-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

