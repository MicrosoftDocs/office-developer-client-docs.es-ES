---
title: SSortOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrder
api_type:
- COM
ms.assetid: fe181b9a-5903-4cc0-bcd5-2061b440b5b1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f9d38c90fa5795d34f78c61ce0faa5f76d8f740d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439726"
---
# <a name="ssortorder"></a><span data-ttu-id="e5e2a-103">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="e5e2a-103">SSortOrder</span></span>
 
<span data-ttu-id="e5e2a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5e2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5e2a-105">Define cómo ordenar las filas de una tabla, qué columna usar como clave de ordenación y la dirección de la ordenación.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-105">Defines how to sort the rows of a table, what column to use as the sort key, and the direction of the sort.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e5e2a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e5e2a-106">Header file:</span></span>  <br/> |<span data-ttu-id="e5e2a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e5e2a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a><span data-ttu-id="e5e2a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e5e2a-108">Members</span></span>

<span data-ttu-id="e5e2a-109">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="e5e2a-109">**ulPropTag**</span></span>
  
> <span data-ttu-id="e5e2a-110">Etiqueta de propiedad que identifica la clave de ordenación o, para una ordenación por categorías, la columna de categoría.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-110">Property tag identifying the sort key or, for a categorized sort, the category column.</span></span>
    
<span data-ttu-id="e5e2a-111">**ulOrder**</span><span class="sxs-lookup"><span data-stu-id="e5e2a-111">**ulOrder**</span></span>
  
> <span data-ttu-id="e5e2a-112">El orden en que se ordenarán los datos.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-112">The order in which the data is to be sorted.</span></span> <span data-ttu-id="e5e2a-113">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e5e2a-113">Possible values are as follow:</span></span>
    
  - <span data-ttu-id="e5e2a-114">TABLE_SORT_ASCEND: la tabla debe ordenarse en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-114">TABLE_SORT_ASCEND: The table should be sorted in ascending order.</span></span>
      
  - <span data-ttu-id="e5e2a-115">TABLE_SORT_COMBINE: la operación de ordenación debe crear una categoría que combine la propiedad identificada como columna de clave de ordenación en el miembro **ulPropTag** con la columna de clave de ordenación especificada en la estructura **anterior de SSortOrder.**</span><span class="sxs-lookup"><span data-stu-id="e5e2a-115">TABLE_SORT_COMBINE: The sort operation should create a category that combines the property identified as the sort key column in the **ulPropTag** member with the sort key column specified in the previous **SSortOrder** structure.</span></span> 
      
    <span data-ttu-id="e5e2a-116">TABLE_SORT_COMBINE sólo se puede usar cuando la estructura **SSortOrder** se usa como una entrada en una estructura [SSortOrderSet](ssortorderset.md) para especificar varios pedidos de ordenación para una ordenación por categorías.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-116">TABLE_SORT_COMBINE can only be used when the **SSortOrder** structure is being used as an entry in an [SSortOrderSet](ssortorderset.md) structure to specify multiple sort orders for a categorized sort.</span></span> <span data-ttu-id="e5e2a-117">TABLE_SORT_COMBINE se puede usar en la primera **estructura SSortOrder** de una **estructura SSortOrderSet.**</span><span class="sxs-lookup"><span data-stu-id="e5e2a-117">TABLE_SORT_COMBINE cannot be used in the first **SSortOrder** structure in an **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="e5e2a-118">TABLE_SORT_DESCEND: la tabla debe ordenarse en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-118">TABLE_SORT_DESCEND: The table should be sorted in descending order.</span></span>
      
  - <span data-ttu-id="e5e2a-119">TABLE_SORT_CATEG_MAX: la tabla debe ordenarse según el valor máximo del miembro **ulPropTag** para las filas de datos de las categorías especificadas por el criterio de ordenación anterior en la estructura **SSortOrderSet.**</span><span class="sxs-lookup"><span data-stu-id="e5e2a-119">TABLE_SORT_CATEG_MAX: The table should be sorted on the maximum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="e5e2a-120">TABLE_SORT_CATEG_MIN: la tabla debe ordenarse según el valor mínimo del miembro **ulPropTag** para las filas de datos de las categorías especificadas por el criterio de ordenación anterior en la estructura **de SSortOrderSet.**</span><span class="sxs-lookup"><span data-stu-id="e5e2a-120">TABLE_SORT_CATEG_MIN: The table should be sorted on the minimum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the in **SSortOrderSet** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e5e2a-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e5e2a-121">Remarks</span></span>

<span data-ttu-id="e5e2a-122">Una **estructura SSortOrder** se usa para describir cómo realizar una operación de ordenación estándar o una operación de ordenación categorizada.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-122">An **SSortOrder** structure is used to describe how to perform either a standard sort operation or a categorized sort operation.</span></span> <span data-ttu-id="e5e2a-123">**Las estructuras de SSortOrder** normalmente se combinan en una estructura **SSortOrderSet** para describir varias teclas de ordenación e indicaciones.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-123">**SSortOrder** structures are typically combined into an **SSortOrderSet** structure to describe multiple sort keys and directions.</span></span> <span data-ttu-id="e5e2a-124">**Las estructuras SSortOrderSet** se usan en las siguientes funciones y métodos de interfaz:</span><span class="sxs-lookup"><span data-stu-id="e5e2a-124">**SSortOrderSet** structures are used in the following functions and interface methods:</span></span> 
  
- [<span data-ttu-id="e5e2a-125">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="e5e2a-125">ITableData::HrGetView</span></span>](itabledata-hrgetview.md)
    
- [<span data-ttu-id="e5e2a-126">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="e5e2a-126">IMAPIFolder::SaveContentsSort</span></span>](imapifolder-savecontentssort.md)
    
- [<span data-ttu-id="e5e2a-127">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="e5e2a-127">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
    
- [<span data-ttu-id="e5e2a-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="e5e2a-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="e5e2a-129">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="e5e2a-129">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
- [<span data-ttu-id="e5e2a-130">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="e5e2a-130">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="e5e2a-131">El intervalo de columnas permitidas en una tabla que se puede usar como clave de ordenación depende del proveedor.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-131">The range of allowed columns in a table that can be used as a sort key depends on the provider.</span></span> <span data-ttu-id="e5e2a-132">Las columnas que forman parte del conjunto de columnas actual siempre se pueden usar como claves de ordenación.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-132">Columns that are part of the current column set can always be used as sort keys.</span></span> <span data-ttu-id="e5e2a-133">Sin embargo, cada proveedor determina si las claves de ordenación se pueden definir mediante columnas disponibles que no están en el conjunto de columnas actual.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-133">However, each provider determines whether sort keys can be defined by using available columns that are not in the current column set.</span></span> <span data-ttu-id="e5e2a-134">Una columna disponible es una columna que se devuelve de [IMAPITable::QueryColumns](imapitable-querycolumns.md) cuando se TBL_ALL_COLUMNS marca.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-134">An available column is a column that is returned from [IMAPITable::QueryColumns](imapitable-querycolumns.md) when the TBL_ALL_COLUMNS flag is set.</span></span> 
  
<span data-ttu-id="e5e2a-135">El **miembro ulOrder** indica información de orden direccional y categorización, por ejemplo, por conversación ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), es decir, hilo de conversación, que es una serie de mensajes y respuestas.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-135">The **ulOrder** member indicates both directional order and categorization information, for example, by conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), that is, conversational thread, which is a series of messages and replies.</span></span> <span data-ttu-id="e5e2a-136">Las filas se pueden ordenar en una secuencia ascendente o descendente con todas las entradas NULL en último lugar.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-136">Rows can be sorted in either an ascending or descending sequence with all NULL entries positioned last.</span></span> 
  
<span data-ttu-id="e5e2a-137">El TABLE_SORT_COMBINE valor indica que la columna especificada en **ulPropTag** debe combinarse con la columna de categoría anterior para formar una categoría compuesta.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-137">The TABLE_SORT_COMBINE value indicates that the column specified in **ulPropTag** should be combined with the previous category column to form a composite category.</span></span> <span data-ttu-id="e5e2a-138">Es decir, en lugar de clasificar en valores únicos de columnas individuales, TABLE_SORT_COMBINE permite la categorización en valores únicos de una combinación de columnas.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-138">That is, instead of categorizing on unique values of individual columns, TABLE_SORT_COMBINE allows for categorization on unique values of a combination of columns.</span></span> <span data-ttu-id="e5e2a-139">Por ejemplo, se puede definir una sola categoría para agrupar los mensajes recibidos de un remitente determinado en un asunto determinado.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-139">For example, a single category could be defined to group messages received from a particular sender on a particular subject.</span></span> <span data-ttu-id="e5e2a-140">Establecer el valor en TABLE_SORT_COMBINE reduce el número de filas de categoría que se muestran.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-140">Setting the value to TABLE_SORT_COMBINE reduces the number of category rows that are displayed.</span></span> 
  
<span data-ttu-id="e5e2a-141">La ordenación de columnas de varios valores no es compatible universalmente con todas las implementaciones de tabla.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-141">Sorting on multi-valued columns is not universally supported by all table implementations.</span></span> <span data-ttu-id="e5e2a-142">Si se admite, aplique el MV_FLAG mediante la macro MVI_PROP a la etiqueta de propiedad en el **miembro ulPropTag** para identificar la clave de ordenación como una columna de varios valores.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-142">If supported, apply the MV_FLAG using the MVI_PROP macro to the property tag in the **ulPropTag** member to identify the sort key as a multi-valued column.</span></span> <span data-ttu-id="e5e2a-143">La ordenación en una columna de varios valores se basa en el uso de los valores individuales.</span><span class="sxs-lookup"><span data-stu-id="e5e2a-143">Sorting on a multi-valued column is based on using the individual values.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e5e2a-144">Es posible que los valores de los miembros **ulOrder** TABLE_SORT_CATEG_MAX y TABLE_SORT_CATEG_MIN no se definan en el archivo de encabezado descargable que tenga actualmente, en cuyo caso puede agregarlo al código con los siguientes valores: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span><span class="sxs-lookup"><span data-stu-id="e5e2a-144">The **ulOrder** member values TABLE_SORT_CATEG_MAX and TABLE_SORT_CATEG_MIN might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span></span>
  
<span data-ttu-id="e5e2a-145">Para obtener más información acerca de la ordenación estándar y categorizada, vea [Ordenar y categorizar.](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="e5e2a-145">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e5e2a-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e5e2a-146">See also</span></span>

- [<span data-ttu-id="e5e2a-147">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="e5e2a-147">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="e5e2a-148">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="e5e2a-148">MAPI Structures</span></span>](mapi-structures.md)

