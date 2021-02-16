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
ms.openlocfilehash: f16ba9164d55fdb7bd688d4068f99dc4407e5413
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432369"
---
# <a name="imapitablesorttable"></a><span data-ttu-id="3d198-103">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="3d198-103">IMAPITable::SortTable</span></span>

<span data-ttu-id="3d198-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d198-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d198-105">El **método IMAPITable::SortTable** ordena las filas de la tabla, según los criterios de ordenación.</span><span class="sxs-lookup"><span data-stu-id="3d198-105">The **IMAPITable::SortTable** method orders the rows of the table, depending on sort criteria.</span></span> 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3d198-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d198-106">Parameters</span></span>

<span data-ttu-id="3d198-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="3d198-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="3d198-108">[entrada] Puntero a una [estructura SSortOrderSet](ssortorderset.md) que contiene los criterios de ordenación que se aplicarán.</span><span class="sxs-lookup"><span data-stu-id="3d198-108">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the sort criteria to apply.</span></span> <span data-ttu-id="3d198-109">Pasar una **estructura SSortOrderSet** que contiene cero columnas indica que no es necesario ordenar la tabla en ningún orden determinado.</span><span class="sxs-lookup"><span data-stu-id="3d198-109">Passing an **SSortOrderSet** structure that contains zero columns indicates that the table does not have to be sorted in any particular order.</span></span> 
    
<span data-ttu-id="3d198-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3d198-110">_ulFlags_</span></span>
  
> <span data-ttu-id="3d198-111">[entrada] Máscara de bits de marcas que controla el tiempo de la **operación IMAPITable::SortTable.**</span><span class="sxs-lookup"><span data-stu-id="3d198-111">[in] Bitmask of flags that controls the timing of the **IMAPITable::SortTable** operation.</span></span> <span data-ttu-id="3d198-112">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="3d198-112">The following flags can be set:</span></span> 
    
<span data-ttu-id="3d198-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="3d198-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="3d198-114">Inicia la operación de forma asincrónica y vuelve antes de que finalice la operación.</span><span class="sxs-lookup"><span data-stu-id="3d198-114">Starts the operation asynchronously and returns before the operation is complete.</span></span>
    
<span data-ttu-id="3d198-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="3d198-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="3d198-116">Aplaza la finalización de la ordenación hasta que se requieran los datos de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3d198-116">Defers the completion of the sort until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3d198-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d198-117">Return value</span></span>

<span data-ttu-id="3d198-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="3d198-118">S_OK</span></span> 
  
> <span data-ttu-id="3d198-119">La operación de ordenación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3d198-119">The sort operation was successful.</span></span>
    
<span data-ttu-id="3d198-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="3d198-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="3d198-121">Hay otra operación en curso que impide que se inicie la operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="3d198-121">Another operation is in progress that prevents the sort operation from starting.</span></span> <span data-ttu-id="3d198-122">La operación en curso debe poder completarse o debe detenerse.</span><span class="sxs-lookup"><span data-stu-id="3d198-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="3d198-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="3d198-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="3d198-124">La tabla no admite el tipo de ordenación solicitada.</span><span class="sxs-lookup"><span data-stu-id="3d198-124">The table does not support the type of sorting requested.</span></span>
    
<span data-ttu-id="3d198-125">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="3d198-125">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="3d198-126">La tabla no puede realizar la operación porque el criterio de ordenación determinado al que apunta el parámetro  _lpSortCriteria_ es demasiado complejo.</span><span class="sxs-lookup"><span data-stu-id="3d198-126">The table cannot perform the operation because the particular sort criteria pointed to by the  _lpSortCriteria_ parameter is too complex.</span></span> <span data-ttu-id="3d198-127">**SortTable** puede devolver MAPI_E_TOO_COMPLEX en las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="3d198-127">**SortTable** can return MAPI_E_TOO_COMPLEX under the following conditions.</span></span> 
    
   - <span data-ttu-id="3d198-128">Se solicita una operación de ordenación para una columna de propiedad que la implementación no puede ordenar.</span><span class="sxs-lookup"><span data-stu-id="3d198-128">A sort operation is requested for a property column that the implementation cannot sort.</span></span>
    
   - <span data-ttu-id="3d198-129">La implementación no admite el criterio de ordenación solicitado en el **miembro ulOrder** de la **estructura SSortOrderSet.**</span><span class="sxs-lookup"><span data-stu-id="3d198-129">The implementation does not support the sort order requested in the **ulOrder** member of the **SSortOrderSet** structure.</span></span> 
    
   - <span data-ttu-id="3d198-130">El número de columnas que se va a ordenar, como se especifica en el miembro **cSorts** en **SSortOrderSet**, es mayor de lo que puede controlar la implementación.</span><span class="sxs-lookup"><span data-stu-id="3d198-130">The number of columns to be sorted, as specified in the **cSorts** member in **SSortOrderSet**, is larger than the implementation can handle.</span></span>
    
   - <span data-ttu-id="3d198-131">Se solicita una operación de ordenación, como se indica mediante una etiqueta de propiedad en **SSortOrderSet**, basada en una propiedad que no está en el conjunto disponible o activo y la implementación no admite la ordenación de propiedades que no están en el conjunto disponible.</span><span class="sxs-lookup"><span data-stu-id="3d198-131">A sort operation is requested, as indicated by a property tag in **SSortOrderSet**, based on a property that is not in the available or active set and the implementation does not support sorting on properties not in the available set.</span></span>
    
   - <span data-ttu-id="3d198-132">Una propiedad se especifica varias veces en un conjunto de criterio de ordenación, como indican varias instancias de la misma etiqueta de propiedad, y la implementación no puede realizar dicha operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="3d198-132">One property is specified multiple times in a sort order set, as indicated by multiple instances of the same property tag, and the implementation cannot perform such a sort operation.</span></span>
    
   - <span data-ttu-id="3d198-133">Se solicita una operación de ordenación basada en columnas de propiedad multivalor mediante MVI_FLAG y la implementación no admite la ordenación de propiedades multivalor.</span><span class="sxs-lookup"><span data-stu-id="3d198-133">A sort operation based on multivalued property columns is requested using MVI_FLAG and the implementation does not support sorting on multivalued properties.</span></span> 
    
   - <span data-ttu-id="3d198-134">Una etiqueta de propiedad para una propiedad en **SSortOrderSet** especifica una propiedad o tipo que la implementación no admite.</span><span class="sxs-lookup"><span data-stu-id="3d198-134">A property tag for a property in **SSortOrderSet** specifies a property or type that the implementation does not support.</span></span> 
    
   - <span data-ttu-id="3d198-135">Una operación de ordenación que no sea una que continúe a través de la tabla desde la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) se especifica sólo para una tabla de datos adjuntos que admite este tipo de ordenación.</span><span class="sxs-lookup"><span data-stu-id="3d198-135">A sort operation other than one that proceeds through the table from the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property forward is specified only for an attachment table that supports this type of sorting.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3d198-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3d198-136">Remarks</span></span>

<span data-ttu-id="3d198-137">El **método IMAPITable::SortTable** ordena las filas de una vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="3d198-137">The **IMAPITable::SortTable** method orders the rows in a table view.</span></span> <span data-ttu-id="3d198-138">Mientras que algunas tablas admiten la ordenación estándar y por categorías en varias columnas de clave de ordenación, otras tablas son más limitadas en su compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="3d198-138">Whereas some tables support both standard and categorized sorting on various sort key columns, other tables are more limited in their support.</span></span> <span data-ttu-id="3d198-139">Normalmente, los proveedores de libretas de direcciones no admiten la ordenación de tablas.</span><span class="sxs-lookup"><span data-stu-id="3d198-139">Address book providers ordinarily do not support table sorting.</span></span> <span data-ttu-id="3d198-140">Los proveedores de almacenamiento de mensajes normalmente admiten la ordenación en la medida en que mantienen el criterio de ordenación de las carpetas que se produce cuando se ordena una tabla completa (una tabla sin restricciones).</span><span class="sxs-lookup"><span data-stu-id="3d198-140">Message store providers usually support sorting to the extent that they keep the sort order of folders that results when a full table (a table without restrictions) is sorted.</span></span> 
  
<span data-ttu-id="3d198-141">Algunas tablas permiten ordenar en cualquier columna de tabla.</span><span class="sxs-lookup"><span data-stu-id="3d198-141">Some tables allow sorting to be done on any table column.</span></span> <span data-ttu-id="3d198-142">Otras tablas no lo hacen; las columnas que no se incluyen en la vista de tabla no se ven afectadas por una **llamada a SortTable.**</span><span class="sxs-lookup"><span data-stu-id="3d198-142">Other tables do not; columns not included in the table view are unaffected by a **SortTable** call.</span></span> <span data-ttu-id="3d198-143">Algunas tablas requieren que las claves de ordenación se puedan crear solo con columnas del conjunto de columnas actual de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3d198-143">Some tables require that sort keys be built only with columns in the table's current column set.</span></span> 
  
<span data-ttu-id="3d198-144">Una tabla puede devolver MAPI_E_NO_SUPPORT o MAPI_E_TOO_COMPLEX de **SortTable** cuando no puede completar una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="3d198-144">A table can return either MAPI_E_NO_SUPPORT or MAPI_E_TOO_COMPLEX from **SortTable** when it cannot complete a sort operation.</span></span> <span data-ttu-id="3d198-145">Además, no se garantiza que los proveedores de almacén respetarán el conjunto de criterio de ordenación especificado para las tablas de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="3d198-145">Moreover, store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="3d198-146">Cuando hay cero columnas en la estructura [SSortOrderSet](ssortorderset.md) a las que apunta el parámetro  _lpSortCriteria,_ la tabla devuelve el conjunto de columnas actual.</span><span class="sxs-lookup"><span data-stu-id="3d198-146">When there are zero columns in the [SSortOrderSet](ssortorderset.md) structure pointed to by the  _lpSortCriteria_ parameter, the table returns the current column set.</span></span> <span data-ttu-id="3d198-147">El criterio de ordenación actual se puede recuperar llamando al método [IMAPITable::QuerySortOrder de](imapitable-querysortorder.md) la tabla.</span><span class="sxs-lookup"><span data-stu-id="3d198-147">The current sort order can be retrieved by calling the table's [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="3d198-148">Todos los marcadores de una tabla se invalidan y deben eliminarse cuando se realiza una llamada a **SortTable,** y el marcador BOOKMARK_CURRENT que indica la posición actual del cursor debe establecerse al principio de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3d198-148">All bookmarks for a table are invalidated and should be deleted when a call to **SortTable** is made, and the BOOKMARK_CURRENT bookmark that indicates the current cursor position, should be set to the beginning of the table.</span></span> 
  
<span data-ttu-id="3d198-149">Si se ordena en una columna que contiene una propiedad multivalor sin la marca MVI_FLAG establecida, los valores de la columna se tratan como una tupla completamente ordenada.</span><span class="sxs-lookup"><span data-stu-id="3d198-149">If you are sorting on a column that contains a multivalued property without the MVI_FLAG flag set, the column's values are treated as a completely ordered tuple.</span></span> <span data-ttu-id="3d198-150">Una comparación de dos columnas multivalor compara los elementos de columna en orden, informando de la relación de las columnas en la primera diferencia y devuelve la igualdad sólo si las columnas que se comparan contienen los mismos valores en el mismo orden.</span><span class="sxs-lookup"><span data-stu-id="3d198-150">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality, and returns equality only if the columns being compared contain the same values in the same order.</span></span> <span data-ttu-id="3d198-151">Si una columna tiene menos valores que la otra, la relación notificada es la de un valor nulo con el otro valor.</span><span class="sxs-lookup"><span data-stu-id="3d198-151">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="3d198-152">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="3d198-152">Notes to callers</span></span>

<span data-ttu-id="3d198-153">**SortTable** funciona de forma sincrónica a menos que establezcas una de las marcas.</span><span class="sxs-lookup"><span data-stu-id="3d198-153">**SortTable** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="3d198-154">Si establece la marca TBL_BATCH, **SortTable** pospone la operación de ordenación a menos que solicite los datos.</span><span class="sxs-lookup"><span data-stu-id="3d198-154">If you set the TBL_BATCH flag, **SortTable** postpones the sort operation unless you request the data.</span></span> <span data-ttu-id="3d198-155">Si se TBL_ASYNC marca, **SortTable** funciona de forma asincrónica, lo que puede devolverse antes de que finalice la operación.</span><span class="sxs-lookup"><span data-stu-id="3d198-155">If the TBL_ASYNC flag is set, **SortTable** operates asynchronously, potentially returning before the completion of the operation.</span></span> 
  
<span data-ttu-id="3d198-156">Llame al [método IMAPITable::Abort](imapitable-abort.md) para detener una operación asincrónica en curso si la ordenación debe realizarse inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="3d198-156">Call the [IMAPITable::Abort](imapitable-abort.md) method to stop an asynchronous operation in progress if your sort must be done immediately.</span></span> <span data-ttu-id="3d198-157">Si **SortTable** no puede continuar porque una o varias operaciones asincrónicas de la tabla están en curso, devuelve MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="3d198-157">If **SortTable** cannot continue because one or more asynchronous operations on the table are in progress, it returns MAPI_E_BUSY.</span></span> 
  
<span data-ttu-id="3d198-158">Para obtener un mejor rendimiento, llame a **SetColumns** para personalizar el conjunto de columnas de la tabla y Restrinja para limitar el número de filas de la tabla antes de llamar a  **SortTable** para realizar la ordenación.</span><span class="sxs-lookup"><span data-stu-id="3d198-158">For best performance, call **SetColumns** to customize the table's column set and **Restrict** to limit the number of rows in the table before you call **SortTable** to perform the sort.</span></span> 
  
<span data-ttu-id="3d198-159">Siempre que se produce un error en **SortTable,** el criterio de ordenación que estaba en vigor antes del error sigue en vigor.</span><span class="sxs-lookup"><span data-stu-id="3d198-159">Whenever **SortTable** fails, the sort order that was in effect before the failure is still in effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3d198-160">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3d198-160">See also</span></span>

- [<span data-ttu-id="3d198-161">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="3d198-161">IMAPITable::Abort</span></span>](imapitable-abort.md)
- [<span data-ttu-id="3d198-162">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="3d198-162">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
- [<span data-ttu-id="3d198-163">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="3d198-163">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
- [<span data-ttu-id="3d198-164">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="3d198-164">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
- [<span data-ttu-id="3d198-165">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="3d198-165">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
- [<span data-ttu-id="3d198-166">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="3d198-166">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="3d198-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3d198-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

