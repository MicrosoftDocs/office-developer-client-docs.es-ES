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
ms.openlocfilehash: 179d76b56c1ba9b40768c691d0b1555377f7adb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595051"
---
# <a name="imapitablequeryrows"></a><span data-ttu-id="c8fa1-103">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="c8fa1-103">IMAPITable::QueryRows</span></span>

  
  
<span data-ttu-id="c8fa1-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8fa1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8fa1-105">Devuelve una o varias filas de una tabla, que comienza en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-105">Returns one or more rows from a table, beginning at the current cursor position.</span></span>
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a><span data-ttu-id="c8fa1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8fa1-106">Parameters</span></span>

 <span data-ttu-id="c8fa1-107">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="c8fa1-107">_lRowCount_</span></span>
  
> <span data-ttu-id="c8fa1-108">[entrada] Número máximo de filas que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-108">[in] Maximum number of rows to be returned.</span></span>
    
 <span data-ttu-id="c8fa1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c8fa1-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c8fa1-110">[entrada] Máscara de bits de indicadores que controlan cómo se devuelven filas.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-110">[in] Bitmask of flags that control how rows are returned.</span></span> <span data-ttu-id="c8fa1-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="c8fa1-111">The following flag can be set:</span></span>
    
<span data-ttu-id="c8fa1-112">TBL_NOADVANCE</span><span class="sxs-lookup"><span data-stu-id="c8fa1-112">TBL_NOADVANCE</span></span> 
  
> <span data-ttu-id="c8fa1-113">Impide que el cursor avance como consecuencia de la recuperación de filas.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-113">Prevents the cursor from advancing as a result of the row retrieval.</span></span> <span data-ttu-id="c8fa1-114">Si se establece la marca TBL_NOADVANCE, devuelven los puntos de cursor a la primera fila.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-114">If the TBL_NOADVANCE flag is set, the cursor points to the first row returned.</span></span> <span data-ttu-id="c8fa1-115">Si no está establecido el indicador TBL_NOADVANCE, el cursor señala a la fila que sigue a la última fila devuelta.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-115">If the TBL_NOADVANCE flag is not set, the cursor points to the row following the last row returned.</span></span>
    
 <span data-ttu-id="c8fa1-116">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="c8fa1-116">_lppRows_</span></span>
  
> <span data-ttu-id="c8fa1-117">[out] Puntero a un puntero a una estructura [SRowSet](srowset.md) que contiene las filas de tabla.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-117">[out] Pointer to a pointer to an [SRowSet](srowset.md) structure holding the table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c8fa1-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8fa1-118">Return value</span></span>

<span data-ttu-id="c8fa1-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="c8fa1-119">S_OK</span></span> 
  
> <span data-ttu-id="c8fa1-120">Las filas correctamente se han devuelto.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-120">The rows were successfully returned.</span></span>
    
<span data-ttu-id="c8fa1-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="c8fa1-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="c8fa1-122">Otra operación está en curso que impide que la operación de recuperación de la fila de inicio.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-122">Another operation is in progress that prevents the row retrieval operation from starting.</span></span> <span data-ttu-id="c8fa1-123">Debe ser permite la operación en curso para llevar a cabo o se debe detener.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="c8fa1-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c8fa1-124">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="c8fa1-125">El parámetro _IRowCount_ se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-125">The  _IRowCount_ parameter is set to zero.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c8fa1-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8fa1-126">Remarks</span></span>

<span data-ttu-id="c8fa1-127">El método **IMAPITable:: QueryRows** Obtiene una o varias filas de datos de una tabla.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-127">The **IMAPITable::QueryRows** method gets one or more rows of data from a table.</span></span> <span data-ttu-id="c8fa1-128">El valor del parámetro _IRowCount_ influye en el punto de partida para la recuperación.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-128">The value of the  _IRowCount_ parameter affects the starting point for the retrieval.</span></span> <span data-ttu-id="c8fa1-129">Si _IRowCount_ es positivo, se leen las filas hacia delante, comenzando en la posición actual.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-129">If  _IRowCount_ is positive, rows are read in a forward direction, starting at the current position.</span></span> <span data-ttu-id="c8fa1-130">Si _IRowCount_ es negativo, **QueryRows** restablece el punto de partida moviendo hacia atrás el número de filas indicado.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-130">If  _IRowCount_ is negative, **QueryRows** resets the starting point by moving backward the indicated number of rows.</span></span> <span data-ttu-id="c8fa1-131">Después de restablece el cursor, se leen las filas en orden hacia delante.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-131">After the cursor is reset, rows are read in forward order.</span></span> 
  
<span data-ttu-id="c8fa1-132">El miembro **cRows** en la estructura de [SRowSet](srowset.md) indicada por el parámetro _lppRows_ indica el número de filas devueltas.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-132">The **cRows** member in the [SRowSet](srowset.md) structure pointed to by the  _lppRows_ parameter indicates the number of rows returned.</span></span> <span data-ttu-id="c8fa1-133">Si se devuelven cero filas:</span><span class="sxs-lookup"><span data-stu-id="c8fa1-133">If zero rows are returned:</span></span> 
  
- <span data-ttu-id="c8fa1-134">Ya se ha colocado el cursor al principio de la tabla y el valor de _IRowCount_ es negativo.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-134">The cursor was already positioned at the beginning of the table and the value of  _IRowCount_ is negative.</span></span> <span data-ttu-id="c8fa1-135">- O -</span><span class="sxs-lookup"><span data-stu-id="c8fa1-135">-Or-</span></span> 
    
- <span data-ttu-id="c8fa1-136">Ya se ha colocado el cursor al final de la tabla y el valor de _IRowCount_ es positivo.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-136">The cursor was already positioned at the end of the table and the value of  _IRowCount_ is positive.</span></span> 
    
<span data-ttu-id="c8fa1-137">El número de columnas y su ordenación es el mismo para cada fila.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-137">The number of columns and their ordering is the same for each row.</span></span> <span data-ttu-id="c8fa1-138">Si no existe una propiedad de una fila o hay un error al leer una propiedad, la estructura de **SPropValue** para la propiedad en la fila contiene los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="c8fa1-138">If a property does not exist for a row or there is an error reading a property, the **SPropValue** structure for the property in the row contains the following values:</span></span> 
  
- <span data-ttu-id="c8fa1-139">PT_ERROR para el tipo de propiedad en el miembro **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="c8fa1-139">PT_ERROR for the property type in the **ulPropTag** member.</span></span> 
    
- <span data-ttu-id="c8fa1-140">MAPI_E_NOT_FOUND para el miembro de **valor** .</span><span class="sxs-lookup"><span data-stu-id="c8fa1-140">MAPI_E_NOT_FOUND for the **Value** member.</span></span> 
    
<span data-ttu-id="c8fa1-141">Memoria usada para las estructuras [SPropValue](spropvalue.md) en el conjunto de filas que apunta el parámetro _lppRows_ debe ser asignado y liberan para cada fila por separado.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-141">Memory used for the [SPropValue](spropvalue.md) structures in the row set pointed to by the  _lppRows_ parameter must be separately allocated and freed for each row.</span></span> <span data-ttu-id="c8fa1-142">Utilice [MAPIFreeBuffer](mapifreebuffer.md) para liberar las estructuras de valor de propiedad y para liberar la fila establezca.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-142">Use [MAPIFreeBuffer](mapifreebuffer.md) to free the property value structures and to free the row set.</span></span> <span data-ttu-id="c8fa1-143">Cuando una llamada a **QueryRows** devuelve cero, sin embargo, que indica al principio o al final de la tabla, la estructura de **SRowSet** propio debe liberarse.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-143">When a call to **QueryRows** returns zero, however, indicating the beginning or end of the table, only the **SRowSet** structure itself needs to be freed.</span></span> <span data-ttu-id="c8fa1-144">Para obtener más información acerca de cómo asignar y liberar memoria en una estructura **SRowSet** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="c8fa1-144">For more information about how to allocate and free memory in an **SRowSet** structure, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
<span data-ttu-id="c8fa1-145">Las filas que se devuelven y el orden en el que se devuelven dependen de si [IMAPITable:: Restrict](imapitable-restrict.md) y [SortTable](imapitable-sorttable.md)se han realizado llamadas correctas.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-145">The rows that are returned and the order in which they are returned depend on whether or not successful calls have been made to [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::SortTable](imapitable-sorttable.md).</span></span> <span data-ttu-id="c8fa1-146">**Restrict** filtra las filas de la vista, lo que provoca que **QueryRows** devolver sólo las filas que coinciden con los criterios especificados en la restricción.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-146">**Restrict** filters rows from the view, causing **QueryRows** to return only the rows that match the criteria specified in the restriction.</span></span> <span data-ttu-id="c8fa1-147">**SortTable** establece un estándar o clasificar el criterio de ordenación, que afectan a la secuencia de filas devueltas por **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-147">**SortTable** establishes a standard or categorized sort order, affecting the sequence of rows returned by **QueryRows**.</span></span> <span data-ttu-id="c8fa1-148">Las filas devueltas se encuentran en el orden especificado en la estructura de [SSortOrderSet](ssortorderset.md) que se pasan a **SortTable**.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-148">The returned rows are in the order specified in the [SSortOrderSet](ssortorderset.md) structure passed to **SortTable**.</span></span>
  
<span data-ttu-id="c8fa1-149">Devuelven las columnas de cada fila y el orden en el que se devuelven dependen de si se realizó una llamada correcta a [IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="c8fa1-149">The columns returned for each row and the order in which they are returned depend on whether or not a successful call has been made to [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> <span data-ttu-id="c8fa1-150">**SetColumns** establece un conjunto de columnas, la especificación de las propiedades que se deben incluir en las columnas de la tabla y el orden en el que se deben incluir.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-150">**SetColumns** establishes a column set, specifying the properties to be included in columns in the table and the order in which they should be included.</span></span> <span data-ttu-id="c8fa1-151">Si se ha realizado una llamada **SetColumns** , las columnas determinadas en cada fila y el orden de las columnas coinciden con el conjunto especificado en la llamada de columnas.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-151">If a **SetColumns** call has been made, the particular columns in each row and the order of those columns match the column set specified in the call.</span></span> <span data-ttu-id="c8fa1-152">Si se ha realizado ninguna llamada **SetColumns** , en la tabla devuelve su conjunto de columnas predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-152">If no **SetColumns** call has been made, the table returns its default column set.</span></span> 
  
<span data-ttu-id="c8fa1-153">Si se ha realizado ninguna de estas llamadas, **QueryRows** devuelve todas las filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-153">If none of these calls has been made, **QueryRows** returns all of the rows in the table.</span></span> <span data-ttu-id="c8fa1-154">Cada fila contiene la columna predeterminada está establecida en el orden predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-154">Each row contains the default column set in default order.</span></span> 
  
<span data-ttu-id="c8fa1-155">Cuando el conjunto de columnas establecido en una llamada a [IMAPITable::SetColumns](imapitable-setcolumns.md) incluye columnas establecida en PR_NULL, la matriz [SPropValue](spropvalue.md) dentro del conjunto de filas devuelto en _lppRows_ contendrá ranuras vacías.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-155">When the column set established in a call to [IMAPITable::SetColumns](imapitable-setcolumns.md) includes columns set to PR_NULL, the [SPropValue](spropvalue.md) array within the row set returned in  _lppRows_ will contain empty slots.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c8fa1-156">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="c8fa1-156">Notes to implementers</span></span>

<span data-ttu-id="c8fa1-157">Puede permitir que un autor de la llamada solicitar una columna no compatible que se deben incluir en el conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-157">You can allow a caller to request an unsupported column to be included in the column set.</span></span> <span data-ttu-id="c8fa1-158">Cuando esto ocurre, coloque PT_ERROR en la parte de tipo de propiedad de la etiqueta de propiedad y MAPI_E_NOT_FOUND en el valor de la propiedad para la columna no compatible.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-158">When this occurs, place PT_ERROR in the property type portion of the property tag and MAPI_E_NOT_FOUND in the property value for the unsupported column.</span></span> 
  
<span data-ttu-id="c8fa1-159">Trata el recuento de filas como una solicitud en lugar de un requisito.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-159">Treat the row count as a request rather than a requirement.</span></span> <span data-ttu-id="c8fa1-160">Puede devolver en cualquier lugar desde cero filas, si no hay ninguna fila en la dirección de la consulta, en el número solicitado.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-160">You can return anywhere from zero rows, if there are no rows in the direction of the query, to the number requested.</span></span> 
  
<span data-ttu-id="c8fa1-161">Devolver sólo las filas que se muestra al usuario cuando se solicitan las filas de una vista de tabla con categorías, lo que permite el autor de la llamada hacer válidos suposiciones sobre el alcance de los datos y para evitar trabajo adicional.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-161">Return only the rows that the user will see when rows are requested from a categorized table view, allowing the caller to make valid assumptions about the scope of the data and avoid extra work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c8fa1-162">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="c8fa1-162">Notes to callers</span></span>

<span data-ttu-id="c8fa1-163">Normalmente, terminará con un número de filas según lo especificado en el parámetro _lRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="c8fa1-163">Usually you will end up with as many rows as you have specified in the  _lRowCount_ parameter.</span></span> <span data-ttu-id="c8fa1-164">Sin embargo, cuando los límites de memoria o implementación son un problema o cuando la operación llega al principio o al final de la tabla de forma prematura, **QueryRows** devolverá menos filas que las solicitadas.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-164">However, when memory or implementation limits are an issue or when the operation reaches the beginning or end of the table prematurely, **QueryRows** will return less rows than requested.</span></span> 
  
<span data-ttu-id="c8fa1-165">Si **QueryRows** devuelve MAPI_E_BUSY, llame al método [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) y vuelva a intentar la llamada a **QueryRows** una vez finalizada la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-165">If **QueryRows** returns MAPI_E_BUSY, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method and retry the call to **QueryRows** when the asynchronous operation is complete.</span></span> 
  
<span data-ttu-id="c8fa1-166">Cuando se llama a **QueryRows**, tenga en cuenta que la sincronización de notificaciones asincrónicas puede causar el conjunto de filas que obtener back de **QueryRows** no para representar con precisión los datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-166">When calling **QueryRows**, be aware that the timing of asynchronous notifications can potentially cause the row set that you get back from **QueryRows** not to accurately represent the underlying data.</span></span> <span data-ttu-id="c8fa1-167">Por ejemplo, se establece una llamada a **QueryRows** a siguiente de tabla de contenido de una carpeta de la eliminación de un mensaje, pero antes de la recepción de la notificación correspondiente hará que la fila eliminada que se devuelve en la fila.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-167">For example, a call to **QueryRows** to a folder's contents table following the deletion of a message but prior to the receipt of the corresponding notification will cause the deleted row to be returned in the row set.</span></span> <span data-ttu-id="c8fa1-168">Espere siempre una notificación llegar antes de actualizar la vista del usuario de los datos.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-168">Always wait for a notification to arrive before updating the user's view of the data.</span></span> 
  
<span data-ttu-id="c8fa1-169">Para obtener más información acerca de cómo recuperar filas de tablas, vea [Recuperación de datos de las filas de tabla](retrieving-data-from-table-rows.md).</span><span class="sxs-lookup"><span data-stu-id="c8fa1-169">For more information about retrieving rows from tables, see [Retrieving Data from Table Rows](retrieving-data-from-table-rows.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c8fa1-170">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c8fa1-170">MFCMAPI reference</span></span>

<span data-ttu-id="c8fa1-171">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c8fa1-172">**File**</span><span class="sxs-lookup"><span data-stu-id="c8fa1-172">**File**</span></span>|<span data-ttu-id="c8fa1-173">**Función**</span><span class="sxs-lookup"><span data-stu-id="c8fa1-173">**Function**</span></span>|<span data-ttu-id="c8fa1-174">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="c8fa1-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c8fa1-175">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="c8fa1-175">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="c8fa1-176">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="c8fa1-176">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="c8fa1-177">MFCMAPI usa el método **IMAPITable:: QueryRows** para recuperar las filas de la tabla que se va a cargar en la vista.</span><span class="sxs-lookup"><span data-stu-id="c8fa1-177">MFCMAPI uses the **IMAPITable::QueryRows** method to retrieve rows in the table to load into the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8fa1-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8fa1-178">See also</span></span>



[<span data-ttu-id="c8fa1-179">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="c8fa1-179">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="c8fa1-180">FreeProws</span><span class="sxs-lookup"><span data-stu-id="c8fa1-180">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="c8fa1-181">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="c8fa1-181">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="c8fa1-182">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="c8fa1-182">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="c8fa1-183">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="c8fa1-183">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="c8fa1-184">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="c8fa1-184">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="c8fa1-185">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c8fa1-185">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c8fa1-186">SRow</span><span class="sxs-lookup"><span data-stu-id="c8fa1-186">SRow</span></span>](srow.md)
  
[<span data-ttu-id="c8fa1-187">SRowSet</span><span class="sxs-lookup"><span data-stu-id="c8fa1-187">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="c8fa1-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c8fa1-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="c8fa1-189">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="c8fa1-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

