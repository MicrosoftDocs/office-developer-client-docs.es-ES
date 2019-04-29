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
ms.openlocfilehash: db19c3908c419b98b8deb71e2a86d0aa6eebe240
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438102"
---
# <a name="ssortorderset"></a><span data-ttu-id="df683-103">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="df683-103">SSortOrderSet</span></span>

  
  
<span data-ttu-id="df683-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df683-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df683-105">Define una colección de claves de ordenación para una tabla que se usa para la ordenación estándar o clasificada.</span><span class="sxs-lookup"><span data-stu-id="df683-105">Defines a collection of sort keys for a table that is used for standard or categorized sorting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="df683-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="df683-106">Header file:</span></span>  <br/> |<span data-ttu-id="df683-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="df683-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="df683-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="df683-108">Related macros:</span></span>  <br/> |<span data-ttu-id="df683-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span><span class="sxs-lookup"><span data-stu-id="df683-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span></span> <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a><span data-ttu-id="df683-110">Members</span><span class="sxs-lookup"><span data-stu-id="df683-110">Members</span></span>

 <span data-ttu-id="df683-111">**cSorts**</span><span class="sxs-lookup"><span data-stu-id="df683-111">**cSorts**</span></span>
  
> <span data-ttu-id="df683-112">Número de estructuras [SSortOrder](ssortorder.md) incluidas en el miembro **unaordenación** .</span><span class="sxs-lookup"><span data-stu-id="df683-112">Count of [SSortOrder](ssortorder.md) structures that are included in the **aSort** member.</span></span> 
    
 <span data-ttu-id="df683-113">**cCategories**</span><span class="sxs-lookup"><span data-stu-id="df683-113">**cCategories**</span></span>
  
> <span data-ttu-id="df683-114">Número de columnas que se designan como columnas de categoría.</span><span class="sxs-lookup"><span data-stu-id="df683-114">Count of columns that are designated as category columns.</span></span> <span data-ttu-id="df683-115">Los valores posibles van desde cero, que indica una ordenación no clasificada o estándar, al número indicado por el miembro **cSorts** .</span><span class="sxs-lookup"><span data-stu-id="df683-115">Possible values range from zero, which indicates a non-categorized or standard sort, to the number indicated by the **cSorts** member.</span></span> 
    
 <span data-ttu-id="df683-116">**cExpanded**</span><span class="sxs-lookup"><span data-stu-id="df683-116">**cExpanded**</span></span>
  
> <span data-ttu-id="df683-117">Número de categorías que se inician en un estado expandido, donde todas las filas que se aplican a la categoría están visibles en la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="df683-117">Count of categories that start in an expanded state, where all of the rows that apply to the category are visible in the table view.</span></span> <span data-ttu-id="df683-118">Los valores posibles oscilan entre 0 y el número indicado por **cCategories**.</span><span class="sxs-lookup"><span data-stu-id="df683-118">Possible values range from 0 to the number indicated by **cCategories**.</span></span>
    
 <span data-ttu-id="df683-119">**Unaordenación**</span><span class="sxs-lookup"><span data-stu-id="df683-119">**aSort**</span></span>
  
> <span data-ttu-id="df683-120">Matriz de estructuras **SSortOrder** , cada una de las cuales define un criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="df683-120">Array of **SSortOrder** structures, each defining a sort order.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="df683-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="df683-121">Remarks</span></span>

<span data-ttu-id="df683-122">Se usa una estructura **SSortOrderSet** para definir varios criterios de ordenación para la ordenación estándar y por categorías.</span><span class="sxs-lookup"><span data-stu-id="df683-122">A **SSortOrderSet** structure is used for defining multiple sort orders for standard and categorized sorting.</span></span> 
  
<span data-ttu-id="df683-123">Cada estructura **SSortOrderSet** contiene al menos una estructura **SSortOrder** que define la dirección de la ordenación y la columna que se utilizará como clave de ordenación.</span><span class="sxs-lookup"><span data-stu-id="df683-123">Each **SSortOrderSet** structure contains at least one **SSortOrder** structure defining the direction of the sort and the column that will be used as the sort key.</span></span> <span data-ttu-id="df683-124">Para la ordenación por categorías, esta columna se usa como categoría.</span><span class="sxs-lookup"><span data-stu-id="df683-124">For categorized sorting, this column is used as the category.</span></span> <span data-ttu-id="df683-125">Cuando el valor del miembro **cSorts** supera el valor del miembro **cCategories** , hay más claves de ordenación que categorías y se crean categorías a partir de las columnas que aparecen primero en la matriz **SSortOrder** .</span><span class="sxs-lookup"><span data-stu-id="df683-125">When the value of the **cSorts** member exceeds the value of the **cCategories** member, there are more sort keys than categories, and categories are created from the columns that appear first in the **SSortOrder** array.</span></span> 
  
<span data-ttu-id="df683-126">Por ejemplo, si **cSorts** se establece en 3 y **cCategories** se establece en 2, las columnas descritas por el miembro **ulPropTag** de las dos primeras entradas de la matriz **SSortOrder** se usan como columnas Category.</span><span class="sxs-lookup"><span data-stu-id="df683-126">For example, if **cSorts** is set to 3 and **cCategories** is set to 2, the columns described by the **ulPropTag** member of the first two entries in the **SSortOrder** array are used as the category columns.</span></span> <span data-ttu-id="df683-127">La primera entrada sirve como grupo de categorías de nivel superior; segunda entrada de la agrupación secundaria.</span><span class="sxs-lookup"><span data-stu-id="df683-127">The first entry serves as the top-level category grouping; the second entry as the secondary grouping.</span></span> <span data-ttu-id="df683-128">Todas las filas que coinciden con las dos columnas Category se ordenan mediante el criterio de ordenación definido en la tercera entrada.</span><span class="sxs-lookup"><span data-stu-id="df683-128">All of the rows that match the two category columns are sorted by using the sort key defined in the third entry.</span></span> 
  
<span data-ttu-id="df683-129">El miembro **cExpanded** especifica el número de categorías que se han expandido por primera vez.</span><span class="sxs-lookup"><span data-stu-id="df683-129">The **cExpanded** member specifies the number of categories that are at first expanded.</span></span> <span data-ttu-id="df683-130">Cuando hay varias categorías, la implementación de la tabla comienza con la primera columna que se va a designar como categoría y sigue en orden secuencial con las columnas de categoría siguientes hasta que se haya superado el número de **cCategories** .</span><span class="sxs-lookup"><span data-stu-id="df683-130">When there are multiple categories, the table implementation starts with the first column to be designated as a category and continues in sequential order with the subsequent category columns until the number of **cCategories** has been exceeded.</span></span> <span data-ttu-id="df683-131">Si hay más columnas de categorías que las columnas expandidas, las columnas de categoría están contraídas.</span><span class="sxs-lookup"><span data-stu-id="df683-131">If there are more category columns than there are expanded columns, the category columns are collapsed.</span></span> <span data-ttu-id="df683-132">Si **cExpanded** es igual a cero, sólo la fila de título de nivel superior estará disponible para el usuario de la tabla para la visualización.</span><span class="sxs-lookup"><span data-stu-id="df683-132">If **cExpanded** is equal to zero, only the top level heading row is available to the table user for display.</span></span> <span data-ttu-id="df683-133">Si **cExpanded** es igual a uno menos que el número de categorías, todas las filas de título y ninguna de las filas de hoja estarán disponibles.</span><span class="sxs-lookup"><span data-stu-id="df683-133">If **cExpanded** is equal to one less than the number of categories, then all of the heading rows and none of the leaf rows are available.</span></span> <span data-ttu-id="df683-134">Si **cExpanded** es igual al número de categorías, la tabla se expande completamente.</span><span class="sxs-lookup"><span data-stu-id="df683-134">If **cExpanded** is equal to the number of categories, then the table is fully expanded.</span></span> 
  
<span data-ttu-id="df683-135">Para obtener más información acerca de la ordenación estándar y clasificada, vea [ordenar y categorizar](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="df683-135">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="df683-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="df683-136">See also</span></span>



[<span data-ttu-id="df683-137">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="df683-137">SSortOrder</span></span>](ssortorder.md)
  
[<span data-ttu-id="df683-138">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="df683-138">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="df683-139">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="df683-139">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)


[<span data-ttu-id="df683-140">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="df683-140">MAPI Structures</span></span>](mapi-structures.md)

