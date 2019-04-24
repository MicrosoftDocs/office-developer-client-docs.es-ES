---
title: Ordenación y categorización
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Última modificación: 8 de noviembre de 2011'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344509"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="b8cf5-103">Ordenación y categorización</span><span class="sxs-lookup"><span data-stu-id="b8cf5-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="b8cf5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8cf5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8cf5-105">Ordenar una tabla coloca las filas en un orden que tiene sentido para su visor.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="b8cf5-106">Por ejemplo, un visor puede preferir ver la tabla de contenido de una carpeta ordenada por asunto del mensaje, de modo que todos los subprocesos de una conversación estén juntos, mientras que otro usuario desea ordenar los mensajes por el nombre del remitente.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="b8cf5-107">Una tabla recién creada no está necesariamente ordenada en un orden determinado.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="b8cf5-108">Hay dos tipos de ordenación:</span><span class="sxs-lookup"><span data-stu-id="b8cf5-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="b8cf5-109">Ordenación estándar</span><span class="sxs-lookup"><span data-stu-id="b8cf5-109">Standard sorting</span></span>
    
- <span data-ttu-id="b8cf5-110">Ordenación por categorías</span><span class="sxs-lookup"><span data-stu-id="b8cf5-110">Categorized sorting</span></span> 
    
<span data-ttu-id="b8cf5-111">Con la ordenación estándar, todas las filas se muestran en una lista plana con una o más columnas como criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="b8cf5-112">Con la ordenación por categorías, las filas se muestran jerárquicamente con una o más columnas como clave de ordenación.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="b8cf5-113">Dentro de cada categoría hay una fila de encabezado especial que contiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="b8cf5-114">La columna o columnas que componen el criterio de ordenación</span><span class="sxs-lookup"><span data-stu-id="b8cf5-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="b8cf5-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8cf5-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="b8cf5-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8cf5-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="b8cf5-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8cf5-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="b8cf5-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8cf5-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="b8cf5-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8cf5-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="b8cf5-120">La sangría situada debajo de la fila de encabezado son todas las filas de la tabla que contienen columnas con valores que coinciden con la clave de ordenación.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="b8cf5-121">Estas filas se denominan filas de hoja.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="b8cf5-122">Las filas hoja contienen todas las columnas del conjunto de columnas menos las columnas clave de ordenación.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="b8cf5-123">Las tablas de contenido de las carpetas a menudo admiten la ordenación por categorías además de la ordenación estándar.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="b8cf5-124">Las tablas de contenido de los contenedores de la libreta de direcciones normalmente solo admiten la ordenación estándar.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="b8cf5-125">Una categoría puede tener dos Estados: contraído y expandido.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="b8cf5-126">Cuando una categoría está contraída, sólo la fila de título se devuelve desde [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="b8cf5-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="b8cf5-127">Cuando una categoría está en estado expandido, se devuelven todas las filas relacionadas con la categoría.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="b8cf5-128">Esto incluye la fila de encabezado y las filas de hoja.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="b8cf5-129">Cada categoría de una vista de tabla se puede expandir o contraer independientemente.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="b8cf5-130">Es decir, no todas las categorías deben estar en el mismo estado al mismo tiempo; algunas categorías pueden estar contraídas mientras que otras se expanden.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="b8cf5-131">El usuario de una tabla clasificada decide cómo se muestra.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="b8cf5-132">Una opción común es usar un control proporcionado en el SDK de Windows denominado el control TreeView.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="b8cf5-133">Los controles TreeView son cuadros de lista que admiten información en una estructura de tipo árbol.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="b8cf5-134">Las filas de título de las categorías con el estado expandido se marcan con un signo menos mientras que las filas de título de las categorías del estado contraído se marcan con un signo más.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="b8cf5-135">Las categorías expandidas se muestran con las filas hoja con sangría debajo de las filas de título.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="b8cf5-136">Para contraer y expandir una categoría, una aplicación cliente o un proveedor de servicios utiliza los siguientes métodos [IMAPITable: IUnknown](imapitableiunknown.md) :</span><span class="sxs-lookup"><span data-stu-id="b8cf5-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="b8cf5-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="b8cf5-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="b8cf5-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="b8cf5-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="b8cf5-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="b8cf5-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="b8cf5-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="b8cf5-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="b8cf5-141">Para obtener más información acerca de la ordenación de los subprocesos de una conversación, vea los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="b8cf5-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="b8cf5-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="b8cf5-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="b8cf5-143">Propiedad canónica PidTagSubject</span><span class="sxs-lookup"><span data-stu-id="b8cf5-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="b8cf5-144">Propiedad canónica PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="b8cf5-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="b8cf5-145">Propiedad canónica PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="b8cf5-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="b8cf5-146">Propiedad canónica PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="b8cf5-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="b8cf5-147">Propiedad canónica PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="b8cf5-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="b8cf5-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="b8cf5-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="b8cf5-149">Ordenar tablas después de establecer las columnas y restricciones</span><span class="sxs-lookup"><span data-stu-id="b8cf5-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="b8cf5-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8cf5-150">See also</span></span>



[<span data-ttu-id="b8cf5-151">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="b8cf5-151">MAPI Tables</span></span>](mapi-tables.md)

