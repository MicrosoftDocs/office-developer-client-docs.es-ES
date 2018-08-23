---
title: IMAPITableSortTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SortTable
api_type:
- COM
ms.assetid: ff5f78ac-06cf-46fb-93da-5f4a3a5d1b22
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: efeff92f1a21d076c1ee58b82ad3ab25797df014
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592307"
---
# <a name="imapitablesorttable"></a><span data-ttu-id="4b8e9-103">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="4b8e9-103">IMAPITable::SortTable</span></span>

<span data-ttu-id="4b8e9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b8e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b8e9-105">El método **SortTable** ordena las filas de la tabla, según la ordenación criterios.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-105">The **IMAPITable::SortTable** method orders the rows of the table, depending on sort criteria.</span></span> 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4b8e9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b8e9-106">Parameters</span></span>

<span data-ttu-id="4b8e9-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="4b8e9-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="4b8e9-108">[entrada] Puntero a una estructura [SSortOrderSet](ssortorderset.md) que contiene los criterios de ordenación que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-108">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the sort criteria to apply.</span></span> <span data-ttu-id="4b8e9-109">Pasando una estructura **SSortOrderSet** que contiene cero columnas indica que no dispone de la tabla que se deben ordenar en un orden determinado.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-109">Passing an **SSortOrderSet** structure that contains zero columns indicates that the table does not have to be sorted in any particular order.</span></span> 
    
<span data-ttu-id="4b8e9-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4b8e9-110">_ulFlags_</span></span>
  
> <span data-ttu-id="4b8e9-111">[entrada] Máscara de bits de indicadores que controla la sincronización de la operación de **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="4b8e9-111">[in] Bitmask of flags that controls the timing of the **IMAPITable::SortTable** operation.</span></span> <span data-ttu-id="4b8e9-112">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="4b8e9-112">The following flags can be set:</span></span> 
    
<span data-ttu-id="4b8e9-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="4b8e9-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="4b8e9-114">Inicia la operación de forma asincrónica y devuelve antes de completar la operación.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-114">Starts the operation asynchronously and returns before the operation is complete.</span></span>
    
<span data-ttu-id="4b8e9-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="4b8e9-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="4b8e9-116">Aplaza la finalización de la ordenación hasta que los datos de la tabla están necesarios.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-116">Defers the completion of the sort until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4b8e9-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b8e9-117">Return value</span></span>

<span data-ttu-id="4b8e9-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="4b8e9-118">S_OK</span></span> 
  
> <span data-ttu-id="4b8e9-119">La operación de ordenación fue correcta.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-119">The sort operation was successful.</span></span>
    
<span data-ttu-id="4b8e9-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="4b8e9-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="4b8e9-121">Otra operación está en curso que impide que la operación de ordenación de inicio.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-121">Another operation is in progress that prevents the sort operation from starting.</span></span> <span data-ttu-id="4b8e9-122">Debe ser permite la operación en curso para llevar a cabo o se debe detener.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="4b8e9-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4b8e9-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4b8e9-124">La tabla no es compatible con el tipo de ordenación solicitado.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-124">The table does not support the type of sorting requested.</span></span>
    
<span data-ttu-id="4b8e9-125">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="4b8e9-125">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="4b8e9-126">La tabla no puede realizar la operación porque el criterio de ordenación determinado indicado por el parámetro _lpSortCriteria_ es demasiado compleja.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-126">The table cannot perform the operation because the particular sort criteria pointed to by the  _lpSortCriteria_ parameter is too complex.</span></span> <span data-ttu-id="4b8e9-127">**SortTable** puede devolver MAPI_E_TOO_COMPLEX en las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-127">**SortTable** can return MAPI_E_TOO_COMPLEX under the following conditions.</span></span> 
    
   - <span data-ttu-id="4b8e9-128">Se solicita una operación de ordenación para una columna de propiedad que no se puede ordenar la implementación.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-128">A sort operation is requested for a property column that the implementation cannot sort.</span></span>
    
   - <span data-ttu-id="4b8e9-129">La implementación no es compatible con el criterio de ordenación solicitado en el miembro **ulOrder** de la estructura **SSortOrderSet** .</span><span class="sxs-lookup"><span data-stu-id="4b8e9-129">The implementation does not support the sort order requested in the **ulOrder** member of the **SSortOrderSet** structure.</span></span> 
    
   - <span data-ttu-id="4b8e9-130">El número de columnas que se deben ordenar, tal como se especifica en el miembro **cSorts** en **SSortOrderSet**, es mayor que la implementación puede tratar.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-130">The number of columns to be sorted, as specified in the **cSorts** member in **SSortOrderSet**, is larger than the implementation can handle.</span></span>
    
   - <span data-ttu-id="4b8e9-131">Se solicita una operación de ordenación, indicada por una etiqueta de propiedad en **SSortOrderSet**, en función de una propiedad que no está en el conjunto disponible o activo y la implementación no admite la ordenación en las propiedades no en el conjunto disponible.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-131">A sort operation is requested, as indicated by a property tag in **SSortOrderSet**, based on a property that is not in the available or active set and the implementation does not support sorting on properties not in the available set.</span></span>
    
   - <span data-ttu-id="4b8e9-132">Una propiedad se especifica varias veces en un conjunto de criterio de ordenación, como se indica en varias instancias de la misma etiqueta de propiedad, y la implementación no puede realizar como una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-132">One property is specified multiple times in a sort order set, as indicated by multiple instances of the same property tag, and the implementation cannot perform such a sort operation.</span></span>
    
   - <span data-ttu-id="4b8e9-133">Se solicita una operación de ordenación en función de las columnas de propiedad multivalor con MVI_FLAG y la implementación no admite la ordenación en las propiedades multivalores.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-133">A sort operation based on multivalued property columns is requested using MVI_FLAG and the implementation does not support sorting on multivalued properties.</span></span> 
    
   - <span data-ttu-id="4b8e9-134">Una etiqueta de propiedad para una propiedad en **SSortOrderSet** especifica una propiedad o un tipo que no es compatible con la implementación.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-134">A property tag for a property in **SSortOrderSet** specifies a property or type that the implementation does not support.</span></span> 
    
   - <span data-ttu-id="4b8e9-135">Una operación de ordenación distinto del que se realiza a través de la tabla de la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) desviar sólo se especifica para una tabla de datos adjuntos que admite este tipo de ordenación.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-135">A sort operation other than one that proceeds through the table from the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property forward is specified only for an attachment table that supports this type of sorting.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b8e9-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b8e9-136">Remarks</span></span>

<span data-ttu-id="4b8e9-137">El método **SortTable** pedidos las filas en una vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-137">The **IMAPITable::SortTable** method orders the rows in a table view.</span></span> <span data-ttu-id="4b8e9-138">Mientras que algunas tablas admiten la ordenación estándar y ordenadas por categorías en varias columnas de clave de ordenación, otras tablas son más limitados en las admite.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-138">Whereas some tables support both standard and categorized sorting on various sort key columns, other tables are more limited in their support.</span></span> <span data-ttu-id="4b8e9-139">Los proveedores de la libreta de direcciones normalmente no admiten la ordenación de tablas.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-139">Address book providers ordinarily do not support table sorting.</span></span> <span data-ttu-id="4b8e9-140">Los proveedores de almacén de mensajes normalmente admiten la ordenación en la medida en que mantienen el criterio de ordenación de las carpetas que se produce cuando se ordena una tabla completa (una tabla sin restricciones).</span><span class="sxs-lookup"><span data-stu-id="4b8e9-140">Message store providers usually support sorting to the extent that they keep the sort order of folders that results when a full table (a table without restrictions) is sorted.</span></span> 
  
<span data-ttu-id="4b8e9-141">Algunas tablas permiten ordenación que debe realizarse en cualquier columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-141">Some tables allow sorting to be done on any table column.</span></span> <span data-ttu-id="4b8e9-142">Otras tablas no; las columnas no incluidas en la vista de tabla no se ven afectadas por una llamada de **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="4b8e9-142">Other tables do not; columns not included in the table view are unaffected by a **SortTable** call.</span></span> <span data-ttu-id="4b8e9-143">Algunas tablas requieren que las claves de ordenación se generan sólo con columnas en el conjunto actual de columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-143">Some tables require that sort keys be built only with columns in the table's current column set.</span></span> 
  
<span data-ttu-id="4b8e9-144">Una tabla puede devolver MAPI_E_NO_SUPPORT o MAPI_E_TOO_COMPLEX de **SortTable** cuando no puede completar una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-144">A table can return either MAPI_E_NO_SUPPORT or MAPI_E_TOO_COMPLEX from **SortTable** when it cannot complete a sort operation.</span></span> <span data-ttu-id="4b8e9-145">Además, no se garantiza que los proveedores de almacén para respetar el criterio de ordenación especificado para tablas de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-145">Moreover, store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="4b8e9-146">Cuando hay cero columnas en la estructura de [SSortOrderSet](ssortorderset.md) indicada por el parámetro _lpSortCriteria_ , en la tabla devuelve el conjunto actual de la columna.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-146">When there are zero columns in the [SSortOrderSet](ssortorderset.md) structure pointed to by the  _lpSortCriteria_ parameter, the table returns the current column set.</span></span> <span data-ttu-id="4b8e9-147">El criterio de ordenación actual se puede recuperar al llamar al método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) de la tabla.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-147">The current sort order can be retrieved by calling the table's [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="4b8e9-148">Todos los marcadores de una tabla se invalidan y se deben eliminar cuando se realiza una llamada a **SortTable** , y debe establecerse el marcador BOOKMARK_CURRENT que indica la posición actual del cursor, al principio de la tabla.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-148">All bookmarks for a table are invalidated and should be deleted when a call to **SortTable** is made, and the BOOKMARK_CURRENT bookmark that indicates the current cursor position, should be set to the beginning of the table.</span></span> 
  
<span data-ttu-id="4b8e9-149">Si realiza una ordenación en una columna que contiene una propiedad multivalor sin establecer el indicador MVI_FLAG, los valores de la columna se tratan como una tupla ordenada por completo.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-149">If you are sorting on a column that contains a multivalued property without the MVI_FLAG flag set, the column's values are treated as a completely ordered tuple.</span></span> <span data-ttu-id="4b8e9-150">Una comparación de dos columnas con varios valores compara los elementos de columna en orden, informes de la relación de las columnas en la primera desigualdad y devuelve la igualdad sólo si las columnas que se comparan contienen los mismos valores en el mismo orden.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-150">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality, and returns equality only if the columns being compared contain the same values in the same order.</span></span> <span data-ttu-id="4b8e9-151">Si una columna tiene menos valores que el otro, la relación conocida es un valor nulo en el otro valor.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-151">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="4b8e9-152">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="4b8e9-152">Notes to callers</span></span>

<span data-ttu-id="4b8e9-153">**SortTable** funciona de forma sincrónica a menos que establezca uno de los indicadores.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-153">**SortTable** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="4b8e9-154">Si se establece la marca TBL_BATCH, **SortTable** pospone la operación de ordenación a menos que solicitar los datos.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-154">If you set the TBL_BATCH flag, **SortTable** postpones the sort operation unless you request the data.</span></span> <span data-ttu-id="4b8e9-155">Si se establece la marca TBL_ASYNC, **SortTable** funciona de forma asincrónica, potencialmente devolver antes de la finalización de la operación.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-155">If the TBL_ASYNC flag is set, **SortTable** operates asynchronously, potentially returning before the completion of the operation.</span></span> 
  
<span data-ttu-id="4b8e9-156">Llame al método [IMAPITable::Abort](imapitable-abort.md) para detener una operación asincrónica en curso si la ordenación debe llevarse a cabo inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-156">Call the [IMAPITable::Abort](imapitable-abort.md) method to stop an asynchronous operation in progress if your sort must be done immediately.</span></span> <span data-ttu-id="4b8e9-157">Si no se puede continuar **SortTable** debido a que una o varias operaciones asincrónicas en la tabla están en curso, devuelve MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-157">If **SortTable** cannot continue because one or more asynchronous operations on the table are in progress, it returns MAPI_E_BUSY.</span></span> 
  
<span data-ttu-id="4b8e9-158">Para obtener el mejor rendimiento, llame a **SetColumns** para personalizar el conjunto de columnas de la tabla y **Restrict** para limitar el número de filas en la tabla antes de llamar a **SortTable** para llevar a cabo a la ordenación.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-158">For best performance, call **SetColumns** to customize the table's column set and **Restrict** to limit the number of rows in the table before you call **SortTable** to perform the sort.</span></span> 
  
<span data-ttu-id="4b8e9-159">Cada vez que se produce un error de **SortTable** , el criterio de ordenación que estaba en vigor antes del error todavía está en efecto.</span><span class="sxs-lookup"><span data-stu-id="4b8e9-159">Whenever **SortTable** fails, the sort order that was in effect before the failure is still in effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4b8e9-160">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="4b8e9-160">See also</span></span>

- [<span data-ttu-id="4b8e9-161">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="4b8e9-161">IMAPITable::Abort</span></span>](imapitable-abort.md)
- [<span data-ttu-id="4b8e9-162">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="4b8e9-162">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
- [<span data-ttu-id="4b8e9-163">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="4b8e9-163">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
- [<span data-ttu-id="4b8e9-164">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="4b8e9-164">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
- [<span data-ttu-id="4b8e9-165">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="4b8e9-165">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
- [<span data-ttu-id="4b8e9-166">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="4b8e9-166">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="4b8e9-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4b8e9-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

