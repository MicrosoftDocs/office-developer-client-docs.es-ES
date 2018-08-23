---
title: Ordenar y categorización
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Última modificación: 08 de noviembre de 2011'
ms.openlocfilehash: 12668cb87f21b56cd398a7b5375f6a4b40c65829
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581534"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="801ed-103">Ordenar y categorización</span><span class="sxs-lookup"><span data-stu-id="801ed-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="801ed-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="801ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="801ed-105">Ordenar una tabla, coloca las filas en un orden que tenga sentido para su visor.</span><span class="sxs-lookup"><span data-stu-id="801ed-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="801ed-106">Por ejemplo, podría preferir un visor ver la tabla de contenido de una carpeta ordenada por asunto del mensaje de modo que todos los subprocesos de una conversación estén juntas mientras otro visor es posible que desea que los mensajes ordenados por el nombre del remitente.</span><span class="sxs-lookup"><span data-stu-id="801ed-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="801ed-107">Una tabla de la instancia recién creada no se ordena necesariamente en un orden determinado.</span><span class="sxs-lookup"><span data-stu-id="801ed-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="801ed-108">Hay dos tipos de ordenación:</span><span class="sxs-lookup"><span data-stu-id="801ed-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="801ed-109">Ordenación estándar</span><span class="sxs-lookup"><span data-stu-id="801ed-109">Standard sorting</span></span>
    
- <span data-ttu-id="801ed-110">Clasificar la ordenación</span><span class="sxs-lookup"><span data-stu-id="801ed-110">Categorized sorting</span></span> 
    
<span data-ttu-id="801ed-111">Con la ordenación estándar, todas las filas se muestran en una lista plana con una o varias columnas como un criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="801ed-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="801ed-112">Con la ordenación por categorías, las filas se muestran jerárquicamente con una o varias columnas como el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="801ed-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="801ed-113">Dentro de cada categoría, hay una fila de encabezado especial que contiene las siguientes columnas.</span><span class="sxs-lookup"><span data-stu-id="801ed-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="801ed-114">La columna o columnas que componen la clave de ordenación</span><span class="sxs-lookup"><span data-stu-id="801ed-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="801ed-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="801ed-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="801ed-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="801ed-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="801ed-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="801ed-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="801ed-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="801ed-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="801ed-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="801ed-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="801ed-120">En la fila de encabezado de sangría son todas las filas de la tabla que contienen columnas con valores que coinciden con el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="801ed-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="801ed-121">Estas filas se denominan las filas de la hoja.</span><span class="sxs-lookup"><span data-stu-id="801ed-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="801ed-122">Las filas de la hoja contienen todas las columnas en el conjunto menos las columnas de clave de ordenación de columnas.</span><span class="sxs-lookup"><span data-stu-id="801ed-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="801ed-123">Las tablas de contenido de carpetas a menudo admiten la ordenación por categorías además de ordenación estándar.</span><span class="sxs-lookup"><span data-stu-id="801ed-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="801ed-124">Normalmente, en las tablas de contenido de los contenedores de la libreta de direcciones se admiten la ordenación sólo estándar.</span><span class="sxs-lookup"><span data-stu-id="801ed-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="801ed-125">Una categoría puede tener dos estados: contraído y expandido.</span><span class="sxs-lookup"><span data-stu-id="801ed-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="801ed-126">Cuando una categoría se encuentra en el estado contraído, [IMAPITable:: QueryRows](imapitable-queryrows.md)devuelve sólo la fila de encabezado.</span><span class="sxs-lookup"><span data-stu-id="801ed-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="801ed-127">Cuando una categoría se encuentra en estado expandido, se devuelven todas las filas relacionadas con la categoría.</span><span class="sxs-lookup"><span data-stu-id="801ed-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="801ed-128">Esto incluye la fila de encabezado y las filas de la hoja.</span><span class="sxs-lookup"><span data-stu-id="801ed-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="801ed-129">Cada categoría en una vista de tabla se puede expandir o contraer de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="801ed-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="801ed-130">Es decir, deben ser no todas las categorías en el mismo estado al mismo tiempo; Algunas categorías se pueden contraer mientras que otras personas se expanden.</span><span class="sxs-lookup"><span data-stu-id="801ed-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="801ed-131">El usuario de una tabla con categorías decide cómo se muestra.</span><span class="sxs-lookup"><span data-stu-id="801ed-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="801ed-132">Una opción común consiste en usar un control proporcionado en el SDK de Windows denominado el control treeview.</span><span class="sxs-lookup"><span data-stu-id="801ed-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="801ed-133">Controles TreeView son cuadros de lista que admiten la información en una estructura de árbol.</span><span class="sxs-lookup"><span data-stu-id="801ed-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="801ed-134">Filas de encabezado para las categorías en el estado expandido se marcan con un signo menos mientras se marcan las filas de encabezado para las categorías en el estado contraído con un signo más.</span><span class="sxs-lookup"><span data-stu-id="801ed-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="801ed-135">Categorías expandidas se muestran con las filas de la hoja con sangría bajo las filas de encabezado.</span><span class="sxs-lookup"><span data-stu-id="801ed-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="801ed-136">Para contraer y expandir una categoría, una aplicación de cliente o un proveedor de servicios usa las siguientes [IMAPITable: IUnknown](imapitableiunknown.md) métodos:</span><span class="sxs-lookup"><span data-stu-id="801ed-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="801ed-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="801ed-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="801ed-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="801ed-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="801ed-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="801ed-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="801ed-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="801ed-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="801ed-141">Para obtener más información acerca de la ordenación los subprocesos de una conversación vea los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="801ed-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="801ed-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="801ed-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="801ed-143">Propiedad canónica PidTagSubject</span><span class="sxs-lookup"><span data-stu-id="801ed-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="801ed-144">Propiedad canónica PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="801ed-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="801ed-145">Propiedad canónica PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="801ed-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="801ed-146">Propiedad canónica PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="801ed-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="801ed-147">Propiedad canónica PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="801ed-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="801ed-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="801ed-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="801ed-149">Ordenar tablas después de establecer restricciones y columnas</span><span class="sxs-lookup"><span data-stu-id="801ed-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="801ed-150">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="801ed-150">See also</span></span>



[<span data-ttu-id="801ed-151">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="801ed-151">MAPI Tables</span></span>](mapi-tables.md)

