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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 7cb511c7a021c4e65214acc7efa785be0e02ffc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820753"
---
# <a name="ssortorder"></a><span data-ttu-id="74141-103">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="74141-103">SSortOrder</span></span>
 
<span data-ttu-id="74141-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="74141-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="74141-105">Define cómo se ordenan las filas de una tabla, ¿qué columna para usar como el criterio de ordenación y la dirección de la ordenación.</span><span class="sxs-lookup"><span data-stu-id="74141-105">Defines how to sort the rows of a table, what column to use as the sort key, and the direction of the sort.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74141-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="74141-106">Header file:</span></span>  <br/> |<span data-ttu-id="74141-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74141-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a><span data-ttu-id="74141-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="74141-108">Members</span></span>

<span data-ttu-id="74141-109">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="74141-109">**ulPropTag**</span></span>
  
> <span data-ttu-id="74141-110">Etiqueta de la propiedad que identifica el criterio de ordenación clave o, para una ordenación por categorías, la columna categoría.</span><span class="sxs-lookup"><span data-stu-id="74141-110">Property tag identifying the sort key or, for a categorized sort, the category column.</span></span>
    
<span data-ttu-id="74141-111">**ulOrder**</span><span class="sxs-lookup"><span data-stu-id="74141-111">**ulOrder**</span></span>
  
> <span data-ttu-id="74141-112">El orden en que los datos están que se deben ordenar.</span><span class="sxs-lookup"><span data-stu-id="74141-112">The order in which the data is to be sorted.</span></span> <span data-ttu-id="74141-113">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="74141-113">Possible values are as follow:</span></span>
    
  - <span data-ttu-id="74141-114">TABLE_SORT_ASCEND: La tabla se debe ordenar en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="74141-114">TABLE_SORT_ASCEND: The table should be sorted in ascending order.</span></span>
      
  - <span data-ttu-id="74141-115">TABLE_SORT_COMBINE: La operación de ordenación debe crear una categoría que combina la propiedad identificada como la columna de clave de ordenación en el miembro **ulPropTag** con la columna de clave de ordenación especificada en la estructura de **SSortOrder** anterior.</span><span class="sxs-lookup"><span data-stu-id="74141-115">TABLE_SORT_COMBINE: The sort operation should create a category that combines the property identified as the sort key column in the **ulPropTag** member with the sort key column specified in the previous **SSortOrder** structure.</span></span> 
      
    <span data-ttu-id="74141-116">Sólo se puede usar TABLE_SORT_COMBINE cuando se utiliza la estructura **SSortOrder** como una entrada en una estructura de [SSortOrderSet](ssortorderset.md) para especificar varios criterios de ordenación para una ordenación por categorías.</span><span class="sxs-lookup"><span data-stu-id="74141-116">TABLE_SORT_COMBINE can only be used when the **SSortOrder** structure is being used as an entry in an [SSortOrderSet](ssortorderset.md) structure to specify multiple sort orders for a categorized sort.</span></span> <span data-ttu-id="74141-117">TABLE_SORT_COMBINE no se puede usar en la primera estructura **SSortOrder** en una estructura **SSortOrderSet** .</span><span class="sxs-lookup"><span data-stu-id="74141-117">TABLE_SORT_COMBINE cannot be used in the first **SSortOrder** structure in an **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="74141-118">TABLE_SORT_DESCEND: La tabla se debe ordenar en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="74141-118">TABLE_SORT_DESCEND: The table should be sorted in descending order.</span></span>
      
  - <span data-ttu-id="74141-119">TABLE_SORT_CATEG_MAX: Se debe ordenar la tabla en el valor máximo del miembro **ulPropTag** para las filas de datos en las categorías especificadas por el criterio de ordenación anterior en la estructura **SSortOrderSet** .</span><span class="sxs-lookup"><span data-stu-id="74141-119">TABLE_SORT_CATEG_MAX: The table should be sorted on the maximum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="74141-120">TABLE_SORT_CATEG_MIN: En el valor mínimo del miembro **ulPropTag** para las filas de datos en las categorías especificadas por el criterio de ordenación anterior en la estructura de **SSortOrderSet** en la que se debe ordenar la tabla.</span><span class="sxs-lookup"><span data-stu-id="74141-120">TABLE_SORT_CATEG_MIN: The table should be sorted on the minimum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the in **SSortOrderSet** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="74141-121">Notas</span><span class="sxs-lookup"><span data-stu-id="74141-121">Remarks</span></span>

<span data-ttu-id="74141-122">Una estructura de **SSortOrder** se usa para describir cómo se realiza una operación de ordenación estándar o una operación de ordenación por categorías.</span><span class="sxs-lookup"><span data-stu-id="74141-122">An **SSortOrder** structure is used to describe how to perform either a standard sort operation or a categorized sort operation.</span></span> <span data-ttu-id="74141-123">Estructuras **SSortOrder** normalmente se combinan en una estructura **SSortOrderSet** para describir varios criterios de ordenación y las instrucciones de activación.</span><span class="sxs-lookup"><span data-stu-id="74141-123">**SSortOrder** structures are typically combined into an **SSortOrderSet** structure to describe multiple sort keys and directions.</span></span> <span data-ttu-id="74141-124">Estructuras de **SSortOrderSet** se usan en los métodos de interfaz y las funciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="74141-124">**SSortOrderSet** structures are used in the following functions and interface methods:</span></span> 
  
- [<span data-ttu-id="74141-125">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="74141-125">ITableData::HrGetView</span></span>](itabledata-hrgetview.md)
    
- [<span data-ttu-id="74141-126">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="74141-126">IMAPIFolder::SaveContentsSort</span></span>](imapifolder-savecontentssort.md)
    
- [<span data-ttu-id="74141-127">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="74141-127">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
    
- [<span data-ttu-id="74141-128">SortTable</span><span class="sxs-lookup"><span data-stu-id="74141-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="74141-129">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="74141-129">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
- [<span data-ttu-id="74141-130">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="74141-130">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="74141-131">El rango de columnas permitidos en una tabla que se pueden usar como una clave de ordenación depende del proveedor.</span><span class="sxs-lookup"><span data-stu-id="74141-131">The range of allowed columns in a table that can be used as a sort key depends on the provider.</span></span> <span data-ttu-id="74141-132">Las columnas que forman parte del conjunto de columna actual siempre se pueden usar como claves de ordenación.</span><span class="sxs-lookup"><span data-stu-id="74141-132">Columns that are part of the current column set can always be used as sort keys.</span></span> <span data-ttu-id="74141-133">Sin embargo, cada proveedor determina si las claves de ordenación se pueden definir mediante el uso de columnas disponibles que no están en la columna actual conjunto.</span><span class="sxs-lookup"><span data-stu-id="74141-133">However, each provider determines whether sort keys can be defined by using available columns that are not in the current column set.</span></span> <span data-ttu-id="74141-134">Una columna disponible es una columna que se devuelve desde [IMAPITable::QueryColumns](imapitable-querycolumns.md) cuando se establece la marca TBL_ALL_COLUMNS.</span><span class="sxs-lookup"><span data-stu-id="74141-134">An available column is a column that is returned from [IMAPITable::QueryColumns](imapitable-querycolumns.md) when the TBL_ALL_COLUMNS flag is set.</span></span> 
  
<span data-ttu-id="74141-135">El miembro **ulOrder** indica orden direccional y la información de categorización, por ejemplo, por conversación ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), es decir, conversación subproceso, que es una serie de mensajes y respuestas.</span><span class="sxs-lookup"><span data-stu-id="74141-135">The **ulOrder** member indicates both directional order and categorization information, for example, by conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), that is, conversational thread, which is a series of messages and replies.</span></span> <span data-ttu-id="74141-136">Las filas se pueden ordenar en orden ascendente o descendente secuencia con todas las entradas NULL situadas por última vez.</span><span class="sxs-lookup"><span data-stu-id="74141-136">Rows can be sorted in either an ascending or descending sequence with all NULL entries positioned last.</span></span> 
  
<span data-ttu-id="74141-137">El valor TABLE_SORT_COMBINE indica que la columna especificada en **ulPropTag** se debe combinar con la columna de categoría anterior para formar una categoría compuesta.</span><span class="sxs-lookup"><span data-stu-id="74141-137">The TABLE_SORT_COMBINE value indicates that the column specified in **ulPropTag** should be combined with the previous category column to form a composite category.</span></span> <span data-ttu-id="74141-138">Es decir, en lugar de clasificar en valores únicos de las columnas individuales, permite TABLE_SORT_COMBINE para la categorización de valores únicos de una combinación de columnas.</span><span class="sxs-lookup"><span data-stu-id="74141-138">That is, instead of categorizing on unique values of individual columns, TABLE_SORT_COMBINE allows for categorization on unique values of a combination of columns.</span></span> <span data-ttu-id="74141-139">Por ejemplo, se podría definir una única categoría para agrupar mensajes procedentes de un remitente determinado en un tema concreto.</span><span class="sxs-lookup"><span data-stu-id="74141-139">For example, a single category could be defined to group messages received from a particular sender on a particular subject.</span></span> <span data-ttu-id="74141-140">Si se establece el valor en TABLE_SORT_COMBINE, reduce el número de filas de categoría que se muestran.</span><span class="sxs-lookup"><span data-stu-id="74141-140">Setting the value to TABLE_SORT_COMBINE reduces the number of category rows that are displayed.</span></span> 
  
<span data-ttu-id="74141-141">Todo el mundo no se admite la ordenación en columnas con varios valores por todas las implementaciones de la tabla.</span><span class="sxs-lookup"><span data-stu-id="74141-141">Sorting on multi-valued columns is not universally supported by all table implementations.</span></span> <span data-ttu-id="74141-142">Si se admite, aplicar el MV_FLAG mediante la macro MVI_PROP a la etiqueta de propiedad en el miembro **ulPropTag** para identificar el criterio de ordenación como una columna multivalor.</span><span class="sxs-lookup"><span data-stu-id="74141-142">If supported, apply the MV_FLAG using the MVI_PROP macro to the property tag in the **ulPropTag** member to identify the sort key as a multi-valued column.</span></span> <span data-ttu-id="74141-143">Ordenación en una columna multivalor se basa en el uso de los valores individuales.</span><span class="sxs-lookup"><span data-stu-id="74141-143">Sorting on a multi-valued column is based on using the individual values.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="74141-144">Los valores de miembro **ulOrder** TABLE_SORT_CATEG_MAX y TABLE_SORT_CATEG_MIN no pueden definirse en el archivo de encabezado que se pueden descargar tiene actualmente, en cuyo caso se puede agregar a su código con los siguientes valores: >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span><span class="sxs-lookup"><span data-stu-id="74141-144">The **ulOrder** member values TABLE_SORT_CATEG_MAX and TABLE_SORT_CATEG_MIN might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span></span>
  
<span data-ttu-id="74141-145">Para obtener más información acerca de la ordenación estándar y organizados por categorías, vea [Ordenar y la categorización](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="74141-145">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="74141-146">Ver también</span><span class="sxs-lookup"><span data-stu-id="74141-146">See also</span></span>

- [<span data-ttu-id="74141-147">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="74141-147">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="74141-148">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="74141-148">MAPI Structures</span></span>](mapi-structures.md)

