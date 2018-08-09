---
title: IMAPITableSetColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetColumns
api_type:
- COM
ms.assetid: 9a39cf8d-df0f-493c-b272-f15c65b3f15e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9eeab1e1186aeb5a9b458facd59bd4cc155e8014
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817601"
---
# <a name="imapitablesetcolumns"></a><span data-ttu-id="75541-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="75541-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="75541-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="75541-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="75541-105">Define las propiedades concretas y el orden de las propiedades que aparecen como columnas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="75541-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="75541-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="75541-106">Parameters</span></span>

 <span data-ttu-id="75541-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="75541-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="75541-108">[entrada] Puntero a una matriz de etiquetas de propiedad que identifica las propiedades que se incluirán como columnas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="75541-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="75541-109">La parte de tipo de propiedad de cada etiqueta se puede establecer en un tipo válido o en **PR_NULL** para reservar espacio para adiciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="75541-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="75541-110">El parámetro _lpPropTagArray_ no puede establecerse en NULL; cada tabla debe tener al menos una columna.</span><span class="sxs-lookup"><span data-stu-id="75541-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="75541-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="75541-111">_ulFlags_</span></span>
  
> <span data-ttu-id="75541-112">[entrada] Máscara de bits de indicadores que controla la devolución de una llamada asincrónica a **SetColumns**, por ejemplo, cuando se usa **SetColumns** en la notificación.</span><span class="sxs-lookup"><span data-stu-id="75541-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="75541-113">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="75541-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="75541-114">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="75541-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="75541-115">Las solicitudes que la operación de configuración de columna realizan asincrónicamente causando **SetColumns** devolver potencialmente antes de la operación ha finalizado completamente.</span><span class="sxs-lookup"><span data-stu-id="75541-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="75541-116">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="75541-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="75541-117">Permite a la tabla para posponer la operación de configuración de la columna hasta que los datos se necesita realmente.</span><span class="sxs-lookup"><span data-stu-id="75541-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="75541-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75541-118">Return value</span></span>

<span data-ttu-id="75541-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="75541-119">S_OK</span></span> 
  
> <span data-ttu-id="75541-120">La operación de configuración de columna fue correcta.</span><span class="sxs-lookup"><span data-stu-id="75541-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="75541-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="75541-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="75541-122">Otra operación está en curso que impide que la columna Configuración de la operación de inicio.</span><span class="sxs-lookup"><span data-stu-id="75541-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="75541-123">Debe ser permite la operación en curso para llevar a cabo o se debe detener.</span><span class="sxs-lookup"><span data-stu-id="75541-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="75541-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="75541-124">Remarks</span></span>

<span data-ttu-id="75541-125">El conjunto de columnas de una tabla es el grupo de propiedades que componen las columnas para las filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="75541-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="75541-126">No hay una columna predeterminado establecido para cada tipo de tabla.</span><span class="sxs-lookup"><span data-stu-id="75541-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="75541-127">El conjunto de columnas predeterminado se compone de las propiedades que el implementador de la tabla incluye automáticamente.</span><span class="sxs-lookup"><span data-stu-id="75541-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="75541-128">Los usuarios de la tabla pueden modificar este valor predeterminado que se establece mediante una llamada al método **IMAPITable::SetColumns** .</span><span class="sxs-lookup"><span data-stu-id="75541-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="75541-129">Puede solicitar que otras columnas se agregará al conjunto si el implementador de la tabla es compatible con ellos que pueden quitar columnas o que se puede cambiar el orden de columnas predeterminado.</span><span class="sxs-lookup"><span data-stu-id="75541-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="75541-130">**SetColumns** especifica las columnas que se devuelven con cada fila y el orden de estas columnas dentro de la fila.</span><span class="sxs-lookup"><span data-stu-id="75541-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="75541-131">El éxito de la operación **SetColumns** es evidente sólo después de que se ha realizado una llamada posterior para recuperar los datos de la tabla.</span><span class="sxs-lookup"><span data-stu-id="75541-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="75541-132">A continuación, es que los errores se notifican.</span><span class="sxs-lookup"><span data-stu-id="75541-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="75541-133">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="75541-133">Notes to implementers</span></span>

<span data-ttu-id="75541-134">Algunos proveedores permiten una llamada **SetColumns** ordenar sólo columnas de la tabla que forman parte de las columnas disponibles para una vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="75541-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="75541-135">Otros proveedores de permiten una llamada **SetColumns** ordenar todas las columnas de tabla, incluidas aquellas que contienen propiedades no en el conjunto de columna original.</span><span class="sxs-lookup"><span data-stu-id="75541-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="75541-136">Cuando se establece TBL_BATCH para operaciones asincrónicas, proveedores deben devolver un tipo de propiedad de PT_ERROR y un valor de la propiedad null para las columnas que no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="75541-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="75541-137">No es necesario responder a la solicitud de marca TBL_ASYNC que la operación de ser asincrónica.</span><span class="sxs-lookup"><span data-stu-id="75541-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="75541-138">Si no admite la definición del conjunto de columna asincrónica, realizar la operación de forma sincrónica.</span><span class="sxs-lookup"><span data-stu-id="75541-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="75541-139">Si puede admitir la marca TBL_ASYNC y otro asincrónica operación todavía está en progreso, MAPI_E_BUSY devuelto.</span><span class="sxs-lookup"><span data-stu-id="75541-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="75541-140">De lo contrario, devuelve S_OK, independientemente de si o no admiten todas las propiedades que se incluyen en la matriz de la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="75541-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="75541-141">Desde métodos **IMAPITable** que recuperar datos, como **QueryRows**se deben devolver errores resultante de propiedades no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="75541-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="75541-142">No generan notificaciones para las filas de tabla que están ocultos de la vista mediante llamadas a **restringir**.</span><span class="sxs-lookup"><span data-stu-id="75541-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="75541-143">Al enviar las notificaciones de tabla, el orden de las propiedades en el miembro de **fila** de la estructura [TABLE_NOTIFICATION](table_notification.md) y el orden especificado por la llamada más reciente de **SetColumns** debe ser el mismo a partir de la hora en que la notificación de solicitud se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="75541-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="75541-144">Otro indicador, TBL_BATCH, permite que los autores de llamadas especificar que el implementador de tabla puede aplazar la evaluación de los resultados de la operación hasta más adelante.</span><span class="sxs-lookup"><span data-stu-id="75541-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="75541-145">Siempre que sea posible, los autores de llamadas deben establecer esta marca debido a que la operación por lotes mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="75541-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="75541-146">A menudo es conveniente para los autores de llamadas reservar algunas columnas en el conjunto de filas devueltas para los valores que se agregarán más adelante.</span><span class="sxs-lookup"><span data-stu-id="75541-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="75541-147">Los autores de llamadas hacer esto mediante la colocación de **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) en la posición que desee en la matriz de etiqueta de propiedad que se pasan a **SetColumns**; en la tabla será, a continuación, pase a la copia **PR_NULL** en las posiciones de todas las filas recuperadas con **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="75541-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="75541-148">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="75541-148">Notes to callers</span></span>

<span data-ttu-id="75541-149">Al crear la matriz de la etiqueta de propiedad para el parámetro _lpPropTagArray_ , orden de las etiquetas en el orden que desea que las columnas que aparecen en la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="75541-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="75541-150">Puede especificar propiedades multivalor que se deben incluir en la columna establecer aplicando el indicador de instancia multivalor o constante MVI_FLAG, en la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="75541-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="75541-151">Establezca esta marca pasando la etiqueta de propiedad para la versión de un solo valor de la propiedad como un parámetro a la macro MVI_PROP como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="75541-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="75541-152">La macro MVI_PROP establecerá MVI_FLAG para la propiedad, convirtiendo la etiqueta en una etiqueta multivalor.</span><span class="sxs-lookup"><span data-stu-id="75541-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="75541-153">Si intenta llamar a MVI_PROP en una propiedad de un solo valor erróneamente, MAPI omitir la llamada y deje la etiqueta de propiedad sin cambios.</span><span class="sxs-lookup"><span data-stu-id="75541-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="75541-154">Puede incluir etiquetas de propiedad se establece en **PR_NULL** en la matriz de la etiqueta de propiedad para reservar espacio en el conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="75541-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="75541-155">Reservar espacio permite agregar a una columna establecer sin tener que volver a asignar una matriz de etiqueta de propiedad nuevo.</span><span class="sxs-lookup"><span data-stu-id="75541-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="75541-156">Cuando la llamada a **SetColumns** hace que un cambio al orden de las columnas de una tabla y una o varias de estas columnas representan una propiedad multivalor, es posible que el número de filas de la tabla para aumentar.</span><span class="sxs-lookup"><span data-stu-id="75541-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="75541-157">Si esto ocurre, se descartan todos los marcadores de la tabla.</span><span class="sxs-lookup"><span data-stu-id="75541-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="75541-158">Para obtener más información acerca de cómo columnas con varios valores afectan a las tablas, vea [trabajar con columnas con varios valores](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="75541-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="75541-159">Configuración de columnas predeterminada es una operación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="75541-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="75541-160">Sin embargo, puede permitir que la tabla que se va a posponer la operación hasta que se necesitan los datos mediante la configuración de la marca TBL_BATCH.</span><span class="sxs-lookup"><span data-stu-id="75541-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="75541-161">Al establecer este indicador puede mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="75541-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="75541-162">Otro indicador, TBL_ASYNC, hace que la operación asincrónica, lo que permite **SetColumns** devolver antes de completar la operación.</span><span class="sxs-lookup"><span data-stu-id="75541-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="75541-163">Para determinar cuándo se produce la finalización, llame a [IMAPITable::GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="75541-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="75541-164">Si una llamada a **SetColumns** devuelve MAPI_E_BUSY, que indica que otra operación impide que la operación de inicio, se puede llamar a [IMAPITable::Abort](imapitable-abort.md) para detener la operación en curso.</span><span class="sxs-lookup"><span data-stu-id="75541-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="75541-165">También puede llamar a [HrAddColumnsEx](hraddcolumnsex.md) para cambiar un conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="75541-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="75541-166">La diferencia entre **HrAddColumnsEx** y **IMAPITable::SetColumns** es que **HrAddColumnsEx** es menos flexible; sólo puede agregar columnas.</span><span class="sxs-lookup"><span data-stu-id="75541-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="75541-167">Las columnas adicionales se colocan al principio del conjunto de columna; todas las columnas existentes aparecen a continuación de estas columnas.</span><span class="sxs-lookup"><span data-stu-id="75541-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="75541-168">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="75541-168">MFCMAPI reference</span></span>

<span data-ttu-id="75541-169">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="75541-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="75541-170">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="75541-170">**File**</span></span>|<span data-ttu-id="75541-171">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="75541-171">**Function**</span></span>|<span data-ttu-id="75541-172">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="75541-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="75541-173">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="75541-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="75541-174">CContentsTableListCtrl::DoSetColumns</span><span class="sxs-lookup"><span data-stu-id="75541-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="75541-175">MFCMAPI usa el método **IMAPITable::SetColumns** para establecer las columnas de la tabla que desee.</span><span class="sxs-lookup"><span data-stu-id="75541-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="75541-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="75541-176">See also</span></span>



[<span data-ttu-id="75541-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="75541-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="75541-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="75541-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="75541-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="75541-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="75541-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="75541-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="75541-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="75541-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="75541-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="75541-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="75541-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="75541-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="75541-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="75541-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="75541-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="75541-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="75541-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="75541-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="75541-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="75541-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="75541-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="75541-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="75541-189">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="75541-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

