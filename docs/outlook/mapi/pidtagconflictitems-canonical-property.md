---
title: Propiedad canónico PidTagConflictItems
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 61176ec6f9ff00fa5a38a2b385cb5281fa40961e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819297"
---
# <a name="pidtagconflictitems-canonical-property"></a><span data-ttu-id="94a91-103">Propiedad canónico PidTagConflictItems</span><span class="sxs-lookup"><span data-stu-id="94a91-103">PidTagConflictItems Canonical Property</span></span>

  
  
<span data-ttu-id="94a91-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="94a91-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="94a91-105">Contiene la entrada de uno o varios identificadores de elementos que han participado en una resolución automática de conflictos.</span><span class="sxs-lookup"><span data-stu-id="94a91-105">Contains one or more entry IDs of items that have been involved in an automatic conflict resolution.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="94a91-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="94a91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94a91-107">PR_CONFLICT_ITEMS</span><span class="sxs-lookup"><span data-stu-id="94a91-107">PR_CONFLICT_ITEMS</span></span>  <br/> |
|<span data-ttu-id="94a91-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="94a91-108">Identifier:</span></span>  <br/> |<span data-ttu-id="94a91-109">0x1098</span><span class="sxs-lookup"><span data-stu-id="94a91-109">0x1098</span></span>  <br/> |
|<span data-ttu-id="94a91-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="94a91-110">Property type:</span></span>  <br/> |<span data-ttu-id="94a91-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="94a91-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="94a91-112">Área:</span><span class="sxs-lookup"><span data-stu-id="94a91-112">Area:</span></span>  <br/> |<span data-ttu-id="94a91-113">ICS</span><span class="sxs-lookup"><span data-stu-id="94a91-113">ICS</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94a91-114">Notas</span><span class="sxs-lookup"><span data-stu-id="94a91-114">Remarks</span></span>

<span data-ttu-id="94a91-115">Los tipos de elementos estándar de Microsoft Outlook que admiten la resolución de conflictos automática incluyen los siguientes tipos de elemento estándar: elementos de cita, elementos de contactos, los elementos del diario, elementos de correo, convocatorias de reunión, elementos de notas rápidas y elementos de tarea.</span><span class="sxs-lookup"><span data-stu-id="94a91-115">The types of standard Microsoft Outlook items that support automatic conflict resolution include the following standard item types: appointment items, contact items, journal items, mail items, meeting items, sticky note items, and task items.</span></span> <span data-ttu-id="94a91-116">Un elemento que pertenecen a una clase de mensaje que se deriva de uno de estos tipos de elementos estándar también es compatible con la resolución de conflictos automática.</span><span class="sxs-lookup"><span data-stu-id="94a91-116">An item belonging to a message class that derives from one of these standard item types also supports automatic conflict resolution.</span></span> <span data-ttu-id="94a91-117">En Microsoft Outlook 2003 y Microsoft Office Outlook 2007, cuando Outlook sincroniza los elementos y se considera que existe la posibilidad de que la copia resultante no puede contener todos los datos esenciales, Outlook almacena las copias en conflicto en los **conflictos** carpeta, bajo la carpeta **Problemas de sincronización** .</span><span class="sxs-lookup"><span data-stu-id="94a91-117">In Microsoft Outlook 2003 and Microsoft Office Outlook 2007, when Outlook synchronizes items and considers that there is a possibility that the resultant copy may not contain all essential data, Outlook stores the conflicting copies in the **Conflicts** folder, under the **Sync Issues** folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="94a91-118">**Problemas de sincronización** y sus subcarpetas están ocultos hasta que haga clic en **Lista de carpetas** en el menú **Ir** .</span><span class="sxs-lookup"><span data-stu-id="94a91-118">**Sync Issues** and its subfolders are hidden until you click **Folder List** on the **Go** menu.</span></span> 
  
<span data-ttu-id="94a91-119">Un elemento expone la propiedad **PR_CONFLICT_ITEMS** si es uno de los tipos de elemento que admiten la resolución de conflictos automática, se obtuvo en una resolución de conflictos o se ha puesto en la carpeta **conflictos** debido a una resolución de conflictos.</span><span class="sxs-lookup"><span data-stu-id="94a91-119">An item exposes the **PR_CONFLICT_ITEMS** property if it is one of the item types that support automatic conflict resolution, has won in a conflict resolution, or was placed in the **Conflicts** folder because of a conflict resolution.</span></span> <span data-ttu-id="94a91-120">La carpeta en la que se coloca el elemento determina el contenido de **PR_CONFLICT_ITEMS**.</span><span class="sxs-lookup"><span data-stu-id="94a91-120">The folder in which the item is placed determines the content of **PR_CONFLICT_ITEMS**.</span></span> <span data-ttu-id="94a91-121">Si el elemento se encuentra en alguna carpeta que no sea la carpeta **conflictos** y el elemento expone la propiedad **PR_CONFLICT_ITEMS** , el elemento debe ha obtenido la resolución de conflictos y **PR_CONFLICT_ITEMS** va a contener uno o varios identificadores de entrada de los elementos que se perdió en la resolución de conflictos.</span><span class="sxs-lookup"><span data-stu-id="94a91-121">If the item is located in some folder other than the **Conflicts** folder, and the item exposes the **PR_CONFLICT_ITEMS** property, the item must have won the conflict resolution, and **PR_CONFLICT_ITEMS** would contain one or more entry IDs of those items that lost in the conflict resolution.</span></span> <span data-ttu-id="94a91-122">Si el elemento se encuentra en la carpeta **conflictos** y el elemento expone la propiedad **PR_CONFLICT_ITEMS** , este elemento debe ha perdido la resolución de conflictos y **PR_CONFLICT_ITEMS** va a contener el identificador de entrada del elemento que obtuvo en el conflicto resolución.</span><span class="sxs-lookup"><span data-stu-id="94a91-122">If the item is located in the **Conflicts** folder and the item exposes the **PR_CONFLICT_ITEMS** property, this item must have lost the conflict resolution, and **PR_CONFLICT_ITEMS** would contain the entry ID of the item that won in the conflict resolution.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="94a91-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="94a91-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="94a91-124">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="94a91-124">Protocol specifications</span></span>

<span data-ttu-id="94a91-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94a91-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94a91-126">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="94a91-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="94a91-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94a91-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94a91-128">Controla la sincronización de datos de objeto mensajería entre un servidor y un cliente.</span><span class="sxs-lookup"><span data-stu-id="94a91-128">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="94a91-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="94a91-129">Header files</span></span>

<span data-ttu-id="94a91-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="94a91-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="94a91-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="94a91-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="94a91-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="94a91-132">Mapitags.h</span></span>
  
> <span data-ttu-id="94a91-133">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="94a91-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94a91-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="94a91-134">See also</span></span>



[<span data-ttu-id="94a91-135">Acerca de las adiciones de MAPI</span><span class="sxs-lookup"><span data-stu-id="94a91-135">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="94a91-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="94a91-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94a91-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="94a91-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94a91-138">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="94a91-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94a91-139">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="94a91-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

