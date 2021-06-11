---
title: IMAPITableQueryRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryRows
api_type:
- COM
ms.assetid: f26384f1-467e-4343-92b3-0425da9d2123
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 26d6ffe66a5e7749c9d8c4e5210e9f72de808932
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416296"
---
# <a name="imapitablequeryrows"></a><span data-ttu-id="4d5e3-103">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="4d5e3-103">IMAPITable::QueryRows</span></span>

  
  
<span data-ttu-id="4d5e3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d5e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d5e3-105">Devuelve una o más filas de una tabla, comenzando en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-105">Returns one or more rows from a table, beginning at the current cursor position.</span></span>
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a><span data-ttu-id="4d5e3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4d5e3-106">Parameters</span></span>

 <span data-ttu-id="4d5e3-107">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="4d5e3-107">_lRowCount_</span></span>
  
> <span data-ttu-id="4d5e3-108">[in] Número máximo de filas que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-108">[in] Maximum number of rows to be returned.</span></span>
    
 <span data-ttu-id="4d5e3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4d5e3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="4d5e3-110">[in] Máscara de bits de marcas que controlan cómo se devuelven las filas.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-110">[in] Bitmask of flags that control how rows are returned.</span></span> <span data-ttu-id="4d5e3-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="4d5e3-111">The following flag can be set:</span></span>
    
<span data-ttu-id="4d5e3-112">TBL_NOADVANCE</span><span class="sxs-lookup"><span data-stu-id="4d5e3-112">TBL_NOADVANCE</span></span> 
  
> <span data-ttu-id="4d5e3-113">Impide que el cursor avance como resultado de la recuperación de filas.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-113">Prevents the cursor from advancing as a result of the row retrieval.</span></span> <span data-ttu-id="4d5e3-114">Si se TBL_NOADVANCE marca, el cursor apunta a la primera fila devuelta.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-114">If the TBL_NOADVANCE flag is set, the cursor points to the first row returned.</span></span> <span data-ttu-id="4d5e3-115">Si no TBL_NOADVANCE marca, el cursor apunta a la fila que sigue a la última fila devuelta.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-115">If the TBL_NOADVANCE flag is not set, the cursor points to the row following the last row returned.</span></span>
    
 <span data-ttu-id="4d5e3-116">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="4d5e3-116">_lppRows_</span></span>
  
> <span data-ttu-id="4d5e3-117">[salida] Puntero a un puntero a una [estructura SRowSet](srowset.md) que contiene las filas de tabla.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-117">[out] Pointer to a pointer to an [SRowSet](srowset.md) structure holding the table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4d5e3-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d5e3-118">Return value</span></span>

<span data-ttu-id="4d5e3-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d5e3-119">S_OK</span></span> 
  
> <span data-ttu-id="4d5e3-120">Las filas se devolvieron correctamente.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-120">The rows were successfully returned.</span></span>
    
<span data-ttu-id="4d5e3-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="4d5e3-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="4d5e3-122">Hay otra operación en curso que impide que se inicie la operación de recuperación de filas.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-122">Another operation is in progress that prevents the row retrieval operation from starting.</span></span> <span data-ttu-id="4d5e3-123">Debe permitirse completar la operación en curso o detenerse.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="4d5e3-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4d5e3-124">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="4d5e3-125">El  _parámetro IRowCount_ se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-125">The  _IRowCount_ parameter is set to zero.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4d5e3-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d5e3-126">Remarks</span></span>

<span data-ttu-id="4d5e3-127">El **método IMAPITable::QueryRows** obtiene una o más filas de datos de una tabla.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-127">The **IMAPITable::QueryRows** method gets one or more rows of data from a table.</span></span> <span data-ttu-id="4d5e3-128">El valor del parámetro  _IRowCount_ afecta al punto inicial de la recuperación.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-128">The value of the  _IRowCount_ parameter affects the starting point for the retrieval.</span></span> <span data-ttu-id="4d5e3-129">Si  _IRowCount_ es positivo, las filas se leen en una dirección hacia delante, comenzando en la posición actual.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-129">If  _IRowCount_ is positive, rows are read in a forward direction, starting at the current position.</span></span> <span data-ttu-id="4d5e3-130">Si  _IRowCount_ es negativo, **QueryRows** restablece el punto inicial moviendo hacia atrás el número de filas indicado.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-130">If  _IRowCount_ is negative, **QueryRows** resets the starting point by moving backward the indicated number of rows.</span></span> <span data-ttu-id="4d5e3-131">Después de restablecer el cursor, las filas se leen en orden de avance.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-131">After the cursor is reset, rows are read in forward order.</span></span> 
  
<span data-ttu-id="4d5e3-132">El **miembro cRows** de la estructura [SRowSet](srowset.md) a la que apunta el parámetro  _lppRows_ indica el número de filas devueltas.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-132">The **cRows** member in the [SRowSet](srowset.md) structure pointed to by the  _lppRows_ parameter indicates the number of rows returned.</span></span> <span data-ttu-id="4d5e3-133">Si se devuelven cero filas:</span><span class="sxs-lookup"><span data-stu-id="4d5e3-133">If zero rows are returned:</span></span> 
  
- <span data-ttu-id="4d5e3-134">El cursor ya estaba situado al principio de la tabla y el valor de  _IRowCount_ es negativo.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-134">The cursor was already positioned at the beginning of the table and the value of  _IRowCount_ is negative.</span></span> <span data-ttu-id="4d5e3-135">-Or-</span><span class="sxs-lookup"><span data-stu-id="4d5e3-135">-Or-</span></span> 
    
- <span data-ttu-id="4d5e3-136">El cursor ya estaba situado al final de la tabla y el valor de  _IRowCount_ es positivo.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-136">The cursor was already positioned at the end of the table and the value of  _IRowCount_ is positive.</span></span> 
    
<span data-ttu-id="4d5e3-137">El número de columnas y su orden es el mismo para cada fila.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-137">The number of columns and their ordering is the same for each row.</span></span> <span data-ttu-id="4d5e3-138">Si una propiedad no existe para una fila o hay un error al leer una propiedad, la estructura **SPropValue** de la propiedad de la fila contiene los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="4d5e3-138">If a property does not exist for a row or there is an error reading a property, the **SPropValue** structure for the property in the row contains the following values:</span></span> 
  
- <span data-ttu-id="4d5e3-139">PT_ERROR para el tipo de propiedad en el **miembro ulPropTag.**</span><span class="sxs-lookup"><span data-stu-id="4d5e3-139">PT_ERROR for the property type in the **ulPropTag** member.</span></span> 
    
- <span data-ttu-id="4d5e3-140">MAPI_E_NOT_FOUND para el **miembro Value.**</span><span class="sxs-lookup"><span data-stu-id="4d5e3-140">MAPI_E_NOT_FOUND for the **Value** member.</span></span> 
    
<span data-ttu-id="4d5e3-141">La memoria usada para las estructuras [SPropValue](spropvalue.md) del conjunto de filas señalado por el parámetro  _lppRows_ debe asignarse y liberarse por separado para cada fila.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-141">Memory used for the [SPropValue](spropvalue.md) structures in the row set pointed to by the  _lppRows_ parameter must be separately allocated and freed for each row.</span></span> <span data-ttu-id="4d5e3-142">Use [MAPIFreeBuffer para](mapifreebuffer.md) liberar las estructuras de valores de propiedad y liberar el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-142">Use [MAPIFreeBuffer](mapifreebuffer.md) to free the property value structures and to free the row set.</span></span> <span data-ttu-id="4d5e3-143">Sin embargo, cuando una llamada a **QueryRows** devuelve cero, lo que indica el principio o el final de la tabla, solo es necesario liberar la propia estructura **SRowSet.**</span><span class="sxs-lookup"><span data-stu-id="4d5e3-143">When a call to **QueryRows** returns zero, however, indicating the beginning or end of the table, only the **SRowSet** structure itself needs to be freed.</span></span> <span data-ttu-id="4d5e3-144">Para obtener más información acerca de cómo asignar y liberar memoria en una estructura **de SRowSet,** vea [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="4d5e3-144">For more information about how to allocate and free memory in an **SRowSet** structure, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
<span data-ttu-id="4d5e3-145">Las filas que se devuelven y el orden en que se devuelven dependen de si se han realizado o no llamadas correctas a [IMAPITable::Restrict](imapitable-restrict.md) e [IMAPITable::SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="4d5e3-145">The rows that are returned and the order in which they are returned depend on whether or not successful calls have been made to [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::SortTable](imapitable-sorttable.md).</span></span> <span data-ttu-id="4d5e3-146">**Restringir** filtra filas de la vista, lo que hace que **QueryRows** devuelva solo las filas que coinciden con los criterios especificados en la restricción.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-146">**Restrict** filters rows from the view, causing **QueryRows** to return only the rows that match the criteria specified in the restriction.</span></span> <span data-ttu-id="4d5e3-147">**SortTable** establece un criterio de ordenación estándar o categorizado, lo que afecta a la secuencia de filas devuelta por **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-147">**SortTable** establishes a standard or categorized sort order, affecting the sequence of rows returned by **QueryRows**.</span></span> <span data-ttu-id="4d5e3-148">Las filas devueltas están en el orden especificado en la estructura [SSortOrderSet](ssortorderset.md) pasada a **SortTable**.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-148">The returned rows are in the order specified in the [SSortOrderSet](ssortorderset.md) structure passed to **SortTable**.</span></span>
  
<span data-ttu-id="4d5e3-149">Las columnas devueltas para cada fila y el orden en que se devuelven dependen de si se ha realizado una llamada correcta a [IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="4d5e3-149">The columns returned for each row and the order in which they are returned depend on whether or not a successful call has been made to [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> <span data-ttu-id="4d5e3-150">**SetColumns** establece un conjunto de columnas, especificando las propiedades que se incluirán en las columnas de la tabla y el orden en que deben incluirse.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-150">**SetColumns** establishes a column set, specifying the properties to be included in columns in the table and the order in which they should be included.</span></span> <span data-ttu-id="4d5e3-151">Si se ha realizado una llamada **SetColumns,** las columnas concretas de cada fila y el orden de esas columnas coinciden con el conjunto de columnas especificado en la llamada.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-151">If a **SetColumns** call has been made, the particular columns in each row and the order of those columns match the column set specified in the call.</span></span> <span data-ttu-id="4d5e3-152">Si no se ha realizado ninguna llamada a **SetColumns,** la tabla devuelve su conjunto de columnas predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-152">If no **SetColumns** call has been made, the table returns its default column set.</span></span> 
  
<span data-ttu-id="4d5e3-153">Si no se ha realizado ninguna de estas llamadas, **QueryRows** devuelve todas las filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-153">If none of these calls has been made, **QueryRows** returns all of the rows in the table.</span></span> <span data-ttu-id="4d5e3-154">Cada fila contiene el conjunto de columnas predeterminado en orden predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-154">Each row contains the default column set in default order.</span></span> 
  
<span data-ttu-id="4d5e3-155">Cuando el conjunto de columnas establecido en una llamada a [IMAPITable::SetColumns](imapitable-setcolumns.md) incluye columnas establecidas en PR_NULL, la matriz [SPropValue](spropvalue.md) dentro del conjunto de filas devuelto en _lppRows contendrá ranuras vacías._</span><span class="sxs-lookup"><span data-stu-id="4d5e3-155">When the column set established in a call to [IMAPITable::SetColumns](imapitable-setcolumns.md) includes columns set to PR_NULL, the [SPropValue](spropvalue.md) array within the row set returned in  _lppRows_ will contain empty slots.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4d5e3-156">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="4d5e3-156">Notes to implementers</span></span>

<span data-ttu-id="4d5e3-157">Puede permitir que un autor de la llamada solicite que se incluya una columna no compatible en el conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-157">You can allow a caller to request an unsupported column to be included in the column set.</span></span> <span data-ttu-id="4d5e3-158">Cuando esto ocurre, PT_ERROR en la parte de tipo de propiedad de la etiqueta de propiedad y MAPI_E_NOT_FOUND en el valor de la propiedad de la columna no admitida.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-158">When this occurs, place PT_ERROR in the property type portion of the property tag and MAPI_E_NOT_FOUND in the property value for the unsupported column.</span></span> 
  
<span data-ttu-id="4d5e3-159">Trate el recuento de filas como una solicitud en lugar de un requisito.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-159">Treat the row count as a request rather than a requirement.</span></span> <span data-ttu-id="4d5e3-160">Puede devolver en cualquier lugar desde cero filas, si no hay filas en la dirección de la consulta, al número solicitado.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-160">You can return anywhere from zero rows, if there are no rows in the direction of the query, to the number requested.</span></span> 
  
<span data-ttu-id="4d5e3-161">Devuelve solo las filas que el usuario verá cuando se soliciten filas desde una vista de tabla categorizada, lo que permite al autor de la llamada hacer suposiciones válidas sobre el ámbito de los datos y evitar trabajos adicionales.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-161">Return only the rows that the user will see when rows are requested from a categorized table view, allowing the caller to make valid assumptions about the scope of the data and avoid extra work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4d5e3-162">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="4d5e3-162">Notes to callers</span></span>

<span data-ttu-id="4d5e3-163">Normalmente, terminará con tantas filas como haya especificado en el _parámetro lRowCount._</span><span class="sxs-lookup"><span data-stu-id="4d5e3-163">Usually you will end up with as many rows as you have specified in the  _lRowCount_ parameter.</span></span> <span data-ttu-id="4d5e3-164">Sin embargo, cuando los límites de memoria o implementación son un problema o cuando la operación llega al principio o al final de la tabla prematuramente, **QueryRows** devolverá menos filas de las solicitadas.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-164">However, when memory or implementation limits are an issue or when the operation reaches the beginning or end of the table prematurely, **QueryRows** will return less rows than requested.</span></span> 
  
<span data-ttu-id="4d5e3-165">Si **QueryRows** devuelve MAPI_E_BUSY, llame al método [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) y vuelva a intentar la llamada a **QueryRows** cuando se complete la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-165">If **QueryRows** returns MAPI_E_BUSY, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method and retry the call to **QueryRows** when the asynchronous operation is complete.</span></span> 
  
<span data-ttu-id="4d5e3-166">Al llamar **a QueryRows**, tenga en cuenta que el tiempo de las notificaciones asincrónicas puede provocar que el conjunto de filas que obtiene de **QueryRows** no represente con precisión los datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-166">When calling **QueryRows**, be aware that the timing of asynchronous notifications can potentially cause the row set that you get back from **QueryRows** not to accurately represent the underlying data.</span></span> <span data-ttu-id="4d5e3-167">Por ejemplo, una llamada a **QueryRows** a la tabla de contenido de una carpeta después de eliminar un mensaje, pero antes de recibir la notificación correspondiente hará que se devuelva la fila eliminada en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-167">For example, a call to **QueryRows** to a folder's contents table following the deletion of a message but prior to the receipt of the corresponding notification will cause the deleted row to be returned in the row set.</span></span> <span data-ttu-id="4d5e3-168">Espere siempre a que llegue una notificación antes de actualizar la vista del usuario de los datos.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-168">Always wait for a notification to arrive before updating the user's view of the data.</span></span> 
  
<span data-ttu-id="4d5e3-169">Para obtener más información acerca de cómo recuperar filas de tablas, vea [Recuperar datos de filas de tabla](retrieving-data-from-table-rows.md).</span><span class="sxs-lookup"><span data-stu-id="4d5e3-169">For more information about retrieving rows from tables, see [Retrieving Data from Table Rows](retrieving-data-from-table-rows.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4d5e3-170">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4d5e3-170">MFCMAPI reference</span></span>

<span data-ttu-id="4d5e3-171">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4d5e3-172">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="4d5e3-172">**File**</span></span>|<span data-ttu-id="4d5e3-173">**Función**</span><span class="sxs-lookup"><span data-stu-id="4d5e3-173">**Function**</span></span>|<span data-ttu-id="4d5e3-174">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="4d5e3-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4d5e3-175">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="4d5e3-175">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="4d5e3-176">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="4d5e3-176">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="4d5e3-177">MFCMAPI usa el **método IMAPITable::QueryRows** para recuperar filas de la tabla para cargar en la vista.</span><span class="sxs-lookup"><span data-stu-id="4d5e3-177">MFCMAPI uses the **IMAPITable::QueryRows** method to retrieve rows in the table to load into the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4d5e3-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d5e3-178">See also</span></span>



[<span data-ttu-id="4d5e3-179">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="4d5e3-179">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="4d5e3-180">FreeProws</span><span class="sxs-lookup"><span data-stu-id="4d5e3-180">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="4d5e3-181">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="4d5e3-181">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="4d5e3-182">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="4d5e3-182">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="4d5e3-183">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="4d5e3-183">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="4d5e3-184">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="4d5e3-184">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="4d5e3-185">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4d5e3-185">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4d5e3-186">SRow</span><span class="sxs-lookup"><span data-stu-id="4d5e3-186">SRow</span></span>](srow.md)
  
[<span data-ttu-id="4d5e3-187">SRowSet</span><span class="sxs-lookup"><span data-stu-id="4d5e3-187">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="4d5e3-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d5e3-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="4d5e3-189">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="4d5e3-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

