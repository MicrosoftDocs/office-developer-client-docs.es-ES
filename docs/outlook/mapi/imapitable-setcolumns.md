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
ms.openlocfilehash: 897330feb216dbc3ab143378977c77141cf488f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416352"
---
# <a name="imapitablesetcolumns"></a><span data-ttu-id="8f555-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="8f555-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="8f555-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f555-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f555-105">Define las propiedades y el orden de las propiedades específicas que aparecerán como columnas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="8f555-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8f555-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8f555-106">Parameters</span></span>

 <span data-ttu-id="8f555-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="8f555-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="8f555-108">a Puntero a una matriz de etiquetas de propiedad que identifican las propiedades que se van a incluir como columnas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="8f555-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="8f555-109">La parte de tipo de propiedad de cada etiqueta se puede establecer en un tipo válido o en **PR_NULL** para reservar espacio para adiciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8f555-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="8f555-110">El parámetro _lpPropTagArray_ no puede establecerse en null; todas las tablas deben tener al menos una columna.</span><span class="sxs-lookup"><span data-stu-id="8f555-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="8f555-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8f555-111">_ulFlags_</span></span>
  
> <span data-ttu-id="8f555-112">a Máscara de la máscara que controla la devolución de una llamada asincrónica a **SetColumns**, por ejemplo, cuando se usa **SetColumns** en la notificación.</span><span class="sxs-lookup"><span data-stu-id="8f555-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="8f555-113">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="8f555-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="8f555-114">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="8f555-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="8f555-115">Solicita que la operación de configuración de columna se realice de forma asincrónica, lo que provoca que **SetColumns** pueda devolver potencialmente antes de que la operación se haya completado completamente.</span><span class="sxs-lookup"><span data-stu-id="8f555-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="8f555-116">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="8f555-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="8f555-117">Permite a la tabla posponer la operación de configuración de columna hasta que se necesiten los datos en realidad.</span><span class="sxs-lookup"><span data-stu-id="8f555-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8f555-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f555-118">Return value</span></span>

<span data-ttu-id="8f555-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="8f555-119">S_OK</span></span> 
  
> <span data-ttu-id="8f555-120">La operación de configuración de columna se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8f555-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="8f555-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="8f555-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="8f555-122">Hay otra operación en curso que impide que se inicie la operación de configuración de columna.</span><span class="sxs-lookup"><span data-stu-id="8f555-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="8f555-123">Debe permitirse que la operación en curso se complete o que deba detenerse.</span><span class="sxs-lookup"><span data-stu-id="8f555-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8f555-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8f555-124">Remarks</span></span>

<span data-ttu-id="8f555-125">El conjunto de columnas de una tabla es el grupo de propiedades que componen las columnas de las filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="8f555-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="8f555-126">Hay un conjunto de columnas predeterminado para cada tipo de tabla.</span><span class="sxs-lookup"><span data-stu-id="8f555-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="8f555-127">El conjunto de columnas predeterminado se compone de las propiedades que incluye automáticamente el implementador de la tabla.</span><span class="sxs-lookup"><span data-stu-id="8f555-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="8f555-128">Tabla los usuarios pueden modificar este conjunto predeterminado llamando al método **IMAPITable:: SetColumns** .</span><span class="sxs-lookup"><span data-stu-id="8f555-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="8f555-129">Pueden solicitar que se agreguen otras columnas al conjunto predeterminado si el implementador de la tabla es compatible con las columnas que se van a quitar o el orden de las columnas que se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="8f555-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="8f555-130">**SetColumns** especifica las columnas que se devuelven con cada fila y el orden de estas columnas dentro de la fila.</span><span class="sxs-lookup"><span data-stu-id="8f555-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="8f555-131">El éxito de la operación de **SetColumns** sólo es aparente después de realizar una llamada posterior para recuperar los datos de la tabla.</span><span class="sxs-lookup"><span data-stu-id="8f555-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="8f555-132">Entonces, se informa de que se han producido errores.</span><span class="sxs-lookup"><span data-stu-id="8f555-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8f555-133">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="8f555-133">Notes to implementers</span></span>

<span data-ttu-id="8f555-134">Algunos proveedores permiten la llamada de **SetColumns** para ordenar sólo las columnas de la tabla que forman parte de las columnas disponibles para una vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="8f555-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="8f555-135">Otros proveedores permiten una llamada de **SetColumns** para ordenar todas las columnas de la tabla, incluidas las que contienen propiedades que no están en el conjunto de columnas original.</span><span class="sxs-lookup"><span data-stu-id="8f555-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="8f555-136">Cuando TBL_BATCH se establece para operaciones asincrónicas, los proveedores deben devolver un tipo de propiedad de PT_ERROR y un valor de propiedad NULL para las columnas que no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="8f555-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="8f555-137">No es necesario que responda a la marca TBL_ASYNC que solicita que la operación sea asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8f555-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="8f555-138">Si no admite la definición de conjunto de columnas asincrónica, realice la operación de forma sincrónica.</span><span class="sxs-lookup"><span data-stu-id="8f555-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="8f555-139">Si puede admitir la marca TBL_ASYNC y hay otra operación asincrónica todavía en curso, devuelva MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="8f555-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="8f555-140">De lo contrario, devuelva S_OK independientemente de si se admiten todas las propiedades incluidas en la matriz de etiquetas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="8f555-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="8f555-141">Los errores resultantes de propiedades no admitidas deben devolverse desde los métodos de **IMAPITable** que recuperan datos, como **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="8f555-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="8f555-142">No genere notificaciones para las filas de tabla que están ocultas para que las llamadas a **Restrict**se vean.</span><span class="sxs-lookup"><span data-stu-id="8f555-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="8f555-143">Al enviar notificaciones de tabla, el orden de las propiedades del miembro de **fila** de la estructura [TABLE_NOTIFICATION](table_notification.md) y el orden especificado por la llamada de **SetColumns** más reciente deben ser iguales a la hora de la solicitud de notificación. se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="8f555-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="8f555-144">Otra marca, TBL_BATCH, permite a los llamadores especificar que el implementador de la tabla puede aplazar la evaluación de los resultados de la operación hasta un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="8f555-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="8f555-145">Siempre que sea posible, los autores de la llamada deben establecer esta marca porque la operación por lotes mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8f555-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="8f555-146">A menudo es conveniente que los autores de las llamadas reserven algunas columnas del conjunto de filas recuperadas para los valores que se van a agregar más adelante.</span><span class="sxs-lookup"><span data-stu-id="8f555-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="8f555-147">Para ello, los autores de las llamadas colocan **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) en las posiciones deseadas en la matriz de etiquetas de propiedad pasada a **SetColumns**; a continuación, la tabla devolverá **PR_NULL** en las posiciones de todas las filas recuperadas con **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="8f555-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="8f555-148">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="8f555-148">Notes to callers</span></span>

<span data-ttu-id="8f555-149">Al crear la matriz de etiquetas de propiedad para el parámetro _lpPropTagArray_ , ordene las etiquetas en el orden en que desea que aparezcan las columnas en la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="8f555-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="8f555-150">Puede especificar propiedades multivalor para incluirlas en el conjunto de columnas aplicando la marca de instancia multivalor o constante MVI_FLAG a la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8f555-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="8f555-151">Establezca esta marca pasando la etiqueta de propiedad para la versión de un solo valor de la propiedad como un parámetro a la macro MVI_PROP de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8f555-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="8f555-152">La macro MVI_PROP definirá MVI_FLAG para la propiedad, convirtiendo la etiqueta en una etiqueta con varios valores.</span><span class="sxs-lookup"><span data-stu-id="8f555-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="8f555-153">Si intenta llamar erróneamente a MVI_PROP en una propiedad de un solo valor, MAPI omitirá la llamada y dejará sin cambios la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8f555-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="8f555-154">Puede incluir etiquetas de propiedad establecidas en **PR_NULL** en la matriz de etiquetas de propiedad para reservar espacio en el conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="8f555-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="8f555-155">El espacio de reserva le permite agregar a un conjunto de columnas sin tener que asignar una nueva matriz de etiquetas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="8f555-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="8f555-156">Cuando la llamada a **SetColumns** provoca un cambio en el orden de las columnas de una tabla y una o más de estas columnas representa una propiedad multivalor, es posible que aumente el número de filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="8f555-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="8f555-157">Si esto ocurre, se descartan todos los marcadores de la tabla.</span><span class="sxs-lookup"><span data-stu-id="8f555-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="8f555-158">Para obtener más información acerca de cómo las columnas multivalor afectan a las tablas, vea [Working with](working-with-multivalued-columns.md)multiValued Columns.</span><span class="sxs-lookup"><span data-stu-id="8f555-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="8f555-159">Establecer columnas es una operación sincrónica de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8f555-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="8f555-160">Sin embargo, puede permitir que la tabla posponga la operación hasta el momento en que se necesiten los datos mediante la configuración de la marca TBL_BATCH.</span><span class="sxs-lookup"><span data-stu-id="8f555-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="8f555-161">La configuración de esta marca puede mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8f555-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="8f555-162">Otra marca, TBL_ASYNC, hace que la operación sea asincrónica, lo que permite que **SetColumns** vuelva antes de que se complete la operación.</span><span class="sxs-lookup"><span data-stu-id="8f555-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="8f555-163">Para determinar cuándo se produce la finalización, llame al [IMAPITable:: getStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="8f555-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="8f555-164">Si una llamada a **SetColumns** devuelve MAPI_E_BUSY, que indica que otra operación impide que se inicie la operación, puede llamar al método [IMAPITable:: ABORT](imapitable-abort.md) para detener la operación en curso.</span><span class="sxs-lookup"><span data-stu-id="8f555-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="8f555-165">También puede llamar a [HrAddColumnsEx](hraddcolumnsex.md) para cambiar un conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="8f555-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="8f555-166">La diferencia entre **HrAddColumnsEx** y **IMAPITable:: SetColumns** es que **HrAddColumnsEx** es menos flexible; solo puede Agregar columnas.</span><span class="sxs-lookup"><span data-stu-id="8f555-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="8f555-167">Las columnas adicionales se colocan al principio del conjunto de columnas; todas las columnas existentes aparecen a continuación de estas columnas.</span><span class="sxs-lookup"><span data-stu-id="8f555-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8f555-168">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8f555-168">MFCMAPI reference</span></span>

<span data-ttu-id="8f555-169">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="8f555-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8f555-170">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="8f555-170">**File**</span></span>|<span data-ttu-id="8f555-171">**Función**</span><span class="sxs-lookup"><span data-stu-id="8f555-171">**Function**</span></span>|<span data-ttu-id="8f555-172">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="8f555-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8f555-173">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="8f555-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="8f555-174">CContentsTableListCtrl::D oSetColumns</span><span class="sxs-lookup"><span data-stu-id="8f555-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="8f555-175">MFCMAPI usa el método **IMAPITable:: SetColumns** para establecer las columnas deseadas para la tabla.</span><span class="sxs-lookup"><span data-stu-id="8f555-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8f555-176">Ver también</span><span class="sxs-lookup"><span data-stu-id="8f555-176">See also</span></span>



[<span data-ttu-id="8f555-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="8f555-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="8f555-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="8f555-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="8f555-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="8f555-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="8f555-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="8f555-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="8f555-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="8f555-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="8f555-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="8f555-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="8f555-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="8f555-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="8f555-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="8f555-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="8f555-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8f555-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="8f555-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="8f555-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="8f555-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8f555-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="8f555-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8f555-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="8f555-189">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="8f555-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

