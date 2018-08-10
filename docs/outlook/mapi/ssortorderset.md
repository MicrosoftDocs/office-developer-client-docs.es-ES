---
title: SSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrderSet
api_type:
- COM
ms.assetid: e7f9be6a-92e7-44a8-93ee-b087713a31df
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1604c4a1a0d1bf4008595b0d150b4f7eb3d1c2ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820756"
---
# <a name="ssortorderset"></a><span data-ttu-id="e4218-103">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="e4218-103">SSortOrderSet</span></span>

  
  
<span data-ttu-id="e4218-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4218-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e4218-105">Define una colección de claves de ordenación para una tabla que se usa para la ordenación por categorías o estándar.</span><span class="sxs-lookup"><span data-stu-id="e4218-105">Defines a collection of sort keys for a table that is used for standard or categorized sorting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e4218-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e4218-106">Header file:</span></span>  <br/> |<span data-ttu-id="e4218-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e4218-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e4218-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="e4218-108">Related macros:</span></span>  <br/> |<span data-ttu-id="e4218-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span><span class="sxs-lookup"><span data-stu-id="e4218-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span></span> <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a><span data-ttu-id="e4218-110">Members</span><span class="sxs-lookup"><span data-stu-id="e4218-110">Members</span></span>

 <span data-ttu-id="e4218-111">**cSorts**</span><span class="sxs-lookup"><span data-stu-id="e4218-111">**cSorts**</span></span>
  
> <span data-ttu-id="e4218-112">Recuento de las estructuras de [SSortOrder](ssortorder.md) que se incluyen en el miembro **aSort** .</span><span class="sxs-lookup"><span data-stu-id="e4218-112">Count of [SSortOrder](ssortorder.md) structures that are included in the **aSort** member.</span></span> 
    
 <span data-ttu-id="e4218-113">**cCategories**</span><span class="sxs-lookup"><span data-stu-id="e4218-113">**cCategories**</span></span>
  
> <span data-ttu-id="e4218-114">Número de columnas que se designan como columnas de la categoría.</span><span class="sxs-lookup"><span data-stu-id="e4218-114">Count of columns that are designated as category columns.</span></span> <span data-ttu-id="e4218-115">Intervalo de valores posibles desde cero, lo que indica a una ordenación que no sean clasificar o estándar, con el número indicado por el miembro **cSorts** .</span><span class="sxs-lookup"><span data-stu-id="e4218-115">Possible values range from zero, which indicates a non-categorized or standard sort, to the number indicated by the **cSorts** member.</span></span> 
    
 <span data-ttu-id="e4218-116">**cExpanded**</span><span class="sxs-lookup"><span data-stu-id="e4218-116">**cExpanded**</span></span>
  
> <span data-ttu-id="e4218-117">Número de categorías que se inician en un estado expandido, donde todas las filas que se aplican a la categoría son visibles en la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="e4218-117">Count of categories that start in an expanded state, where all of the rows that apply to the category are visible in the table view.</span></span> <span data-ttu-id="e4218-118">Intervalo de valores posibles entre 0 y el número indicado por **cCategories**.</span><span class="sxs-lookup"><span data-stu-id="e4218-118">Possible values range from 0 to the number indicated by **cCategories**.</span></span>
    
 <span data-ttu-id="e4218-119">**aSort**</span><span class="sxs-lookup"><span data-stu-id="e4218-119">**aSort**</span></span>
  
> <span data-ttu-id="e4218-120">Matriz de estructuras **SSortOrder** , cada definición de un criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="e4218-120">Array of **SSortOrder** structures, each defining a sort order.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e4218-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e4218-121">Remarks</span></span>

<span data-ttu-id="e4218-122">Una estructura **SSortOrderSet** se usa para definir varios criterios de ordenación para la ordenación estándar y organizados por categorías.</span><span class="sxs-lookup"><span data-stu-id="e4218-122">A **SSortOrderSet** structure is used for defining multiple sort orders for standard and categorized sorting.</span></span> 
  
<span data-ttu-id="e4218-123">Cada estructura **SSortOrderSet** contiene al menos una estructura **SSortOrder** definir la dirección de la ordenación y la columna que se utilizará como el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="e4218-123">Each **SSortOrderSet** structure contains at least one **SSortOrder** structure defining the direction of the sort and the column that will be used as the sort key.</span></span> <span data-ttu-id="e4218-124">Para la ordenación por categorías, esta columna se usa como la categoría.</span><span class="sxs-lookup"><span data-stu-id="e4218-124">For categorized sorting, this column is used as the category.</span></span> <span data-ttu-id="e4218-125">Cuando el valor del miembro **cSorts** supera el valor del miembro **cCategories** , hay más claves de ordenación que las categorías y categorías se crean a partir de las columnas que aparecen primeros en la matriz **SSortOrder** .</span><span class="sxs-lookup"><span data-stu-id="e4218-125">When the value of the **cSorts** member exceeds the value of the **cCategories** member, there are more sort keys than categories, and categories are created from the columns that appear first in the **SSortOrder** array.</span></span> 
  
<span data-ttu-id="e4218-126">Por ejemplo, si **cSorts** se establece en 3 y **cCategories** está establecido en 2, se utilizan las columnas descritas por el miembro **ulPropTag** de las dos primeras entradas de la matriz **SSortOrder** como las columnas de la categoría.</span><span class="sxs-lookup"><span data-stu-id="e4218-126">For example, if **cSorts** is set to 3 and **cCategories** is set to 2, the columns described by the **ulPropTag** member of the first two entries in the **SSortOrder** array are used as the category columns.</span></span> <span data-ttu-id="e4218-127">La primera entrada sirve como la categoría de nivel superior de agrupación; la segunda entrada como la agrupación secundaria.</span><span class="sxs-lookup"><span data-stu-id="e4218-127">The first entry serves as the top-level category grouping; the second entry as the secondary grouping.</span></span> <span data-ttu-id="e4218-128">Todas las filas que coinciden con las columnas de dos categorías se ordenan mediante el uso de la clave de ordenación definida en la tercera entrada.</span><span class="sxs-lookup"><span data-stu-id="e4218-128">All of the rows that match the two category columns are sorted by using the sort key defined in the third entry.</span></span> 
  
<span data-ttu-id="e4218-129">El miembro **cExpanded** especifica el número de categorías que expandió en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="e4218-129">The **cExpanded** member specifies the number of categories that are at first expanded.</span></span> <span data-ttu-id="e4218-130">Cuando hay varias categorías, la implementación de la tabla comienza con la primera columna que se designarán como una categoría y continúa en orden secuencial con las columnas de la categoría subsiguientes hasta que se ha superado el número de **cCategories** .</span><span class="sxs-lookup"><span data-stu-id="e4218-130">When there are multiple categories, the table implementation starts with the first column to be designated as a category and continues in sequential order with the subsequent category columns until the number of **cCategories** has been exceeded.</span></span> <span data-ttu-id="e4218-131">Si hay más columnas de la categoría de las columnas expandida, las columnas de categoría están contraídas.</span><span class="sxs-lookup"><span data-stu-id="e4218-131">If there are more category columns than there are expanded columns, the category columns are collapsed.</span></span> <span data-ttu-id="e4218-132">Si **cExpanded** es igual a cero, está disponible para el usuario de la tabla para mostrar sólo la fila de encabezado de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="e4218-132">If **cExpanded** is equal to zero, only the top level heading row is available to the table user for display.</span></span> <span data-ttu-id="e4218-133">Si **cExpanded** es igual a uno menor que el número de categorías, a continuación, todas las filas de encabezado y ninguna de las filas de la hoja están disponible.</span><span class="sxs-lookup"><span data-stu-id="e4218-133">If **cExpanded** is equal to one less than the number of categories, then all of the heading rows and none of the leaf rows are available.</span></span> <span data-ttu-id="e4218-134">Si **cExpanded** es igual que el número de categorías, a continuación, en la tabla se expande por completo.</span><span class="sxs-lookup"><span data-stu-id="e4218-134">If **cExpanded** is equal to the number of categories, then the table is fully expanded.</span></span> 
  
<span data-ttu-id="e4218-135">Para obtener más información acerca de la ordenación estándar y organizados por categorías, vea [Ordenar y la categorización](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="e4218-135">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e4218-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4218-136">See also</span></span>



[<span data-ttu-id="e4218-137">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="e4218-137">SSortOrder</span></span>](ssortorder.md)
  
[<span data-ttu-id="e4218-138">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="e4218-138">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="e4218-139">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="e4218-139">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)


[<span data-ttu-id="e4218-140">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="e4218-140">MAPI Structures</span></span>](mapi-structures.md)

