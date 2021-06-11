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
# <a name="imapitablesetcolumns"></a><span data-ttu-id="d4dab-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="d4dab-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="d4dab-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4dab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4dab-105">Define las propiedades concretas y el orden de las propiedades que se mostrarán como columnas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="d4dab-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d4dab-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d4dab-106">Parameters</span></span>

 <span data-ttu-id="d4dab-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="d4dab-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="d4dab-108">[in] Puntero a una matriz de etiquetas de propiedades que identifican las propiedades que se incluirán como columnas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="d4dab-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="d4dab-109">La parte del tipo de propiedad de cada etiqueta se puede establecer en un tipo válido o en **PR_NULL** para reservar espacio para las adiciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d4dab-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="d4dab-110">El  _parámetro lpPropTagArray_ no se puede establecer en NULL; cada tabla debe tener al menos una columna.</span><span class="sxs-lookup"><span data-stu-id="d4dab-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="d4dab-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d4dab-111">_ulFlags_</span></span>
  
> <span data-ttu-id="d4dab-112">[in] Máscara de bits de marcas que controla la devolución de una llamada asincrónica a **SetColumns**, por ejemplo, cuando se usa **SetColumns** en la notificación.</span><span class="sxs-lookup"><span data-stu-id="d4dab-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="d4dab-113">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="d4dab-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="d4dab-114">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="d4dab-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="d4dab-115">Solicita que la operación de configuración de columna se realice de forma asincrónica, lo que hace que **SetColumns** vuelva potencialmente antes de que la operación se haya completado por completo.</span><span class="sxs-lookup"><span data-stu-id="d4dab-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="d4dab-116">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="d4dab-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="d4dab-117">Permite a la tabla posponer la operación de configuración de columna hasta que los datos son realmente necesarios.</span><span class="sxs-lookup"><span data-stu-id="d4dab-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d4dab-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4dab-118">Return value</span></span>

<span data-ttu-id="d4dab-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d4dab-119">S_OK</span></span> 
  
> <span data-ttu-id="d4dab-120">La operación de configuración de columna se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d4dab-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="d4dab-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="d4dab-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="d4dab-122">Hay otra operación en curso que impide que se inicie la operación de configuración de columna.</span><span class="sxs-lookup"><span data-stu-id="d4dab-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="d4dab-123">Debe permitirse completar la operación en curso o detenerse.</span><span class="sxs-lookup"><span data-stu-id="d4dab-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d4dab-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d4dab-124">Remarks</span></span>

<span data-ttu-id="d4dab-125">El conjunto de columnas de una tabla es el grupo de propiedades que forma las columnas de las filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d4dab-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="d4dab-126">Hay un conjunto de columnas predeterminado para cada tipo de tabla.</span><span class="sxs-lookup"><span data-stu-id="d4dab-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="d4dab-127">El conjunto de columnas predeterminado está hecho de las propiedades que el implementador de tabla incluye automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d4dab-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="d4dab-128">Los usuarios de tabla pueden modificar este conjunto predeterminado llamando al **método IMAPITable::SetColumns.**</span><span class="sxs-lookup"><span data-stu-id="d4dab-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="d4dab-129">Pueden solicitar que se agregó otras columnas al conjunto predeterminado si el implementador de tablas las admite para que se quiten las columnas o que se cambie el orden de las columnas.</span><span class="sxs-lookup"><span data-stu-id="d4dab-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="d4dab-130">**SetColumns** especifica las columnas que se devuelven con cada fila y el orden de estas columnas dentro de la fila.</span><span class="sxs-lookup"><span data-stu-id="d4dab-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="d4dab-131">El éxito de la **operación SetColumns** solo se muestra después de realizar una llamada posterior para recuperar los datos de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d4dab-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="d4dab-132">A continuación, se notifican los errores.</span><span class="sxs-lookup"><span data-stu-id="d4dab-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d4dab-133">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="d4dab-133">Notes to implementers</span></span>

<span data-ttu-id="d4dab-134">Algunos proveedores permiten que una **llamada SetColumns** ordene solo las columnas de tabla que forman parte de las columnas disponibles para una vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="d4dab-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="d4dab-135">Otros proveedores permiten que una **llamada SetColumns** ordene todas las columnas de tabla, incluidas aquellas que contienen propiedades que no están en el conjunto de columnas original.</span><span class="sxs-lookup"><span data-stu-id="d4dab-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="d4dab-136">Cuando TBL_BATCH para operaciones asincrónicas, los proveedores deben devolver un tipo de propiedad de PT_ERROR y un valor de propiedad de NULL para las columnas que no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="d4dab-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="d4dab-137">No es necesario responder a la marca TBL_ASYNC que solicita que la operación sea asincrónica.</span><span class="sxs-lookup"><span data-stu-id="d4dab-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="d4dab-138">Si no admite la definición de conjunto de columnas asincrónica, realice la operación sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="d4dab-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="d4dab-139">Si puede admitir la marca TBL_ASYNC y otra operación asincrónica todavía está en curso, devuelva MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="d4dab-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="d4dab-140">De lo contrario, S_OK independientemente de si admite o no todas las propiedades incluidas en la matriz de etiquetas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d4dab-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="d4dab-141">Los errores resultantes de propiedades no admitidas deben devolverse de métodos **IMAPITable** que recuperan datos, como **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="d4dab-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="d4dab-142">No genere notificaciones para las filas de tabla que están ocultas de la vista mediante llamadas a **Restrict**.</span><span class="sxs-lookup"><span data-stu-id="d4dab-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="d4dab-143">Al enviar notificaciones de tabla, el  orden de las propiedades en el miembro de fila de la estructura [TABLE_NOTIFICATION](table_notification.md) y el orden especificado por la llamada **SetColumns** más reciente debe ser el mismo que en el momento en que se envió la solicitud de notificación.</span><span class="sxs-lookup"><span data-stu-id="d4dab-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="d4dab-144">Otra marca, TBL_BATCH, permite a los autores de llamadas especificar que el implementador de tabla puede aplazar la evaluación de los resultados de la operación hasta una hora posterior.</span><span class="sxs-lookup"><span data-stu-id="d4dab-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="d4dab-145">Siempre que sea posible, los autores de llamadas deben establecer esta marca porque la operación por lotes mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d4dab-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="d4dab-146">A menudo es conveniente que los autores de llamadas reserven algunas columnas del conjunto de filas recuperado para que los valores se puedan agregar más adelante.</span><span class="sxs-lookup"><span data-stu-id="d4dab-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="d4dab-147">Los autores de llamadas hacen esto **colocando PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) en las posiciones deseadas en la matriz de etiquetas de propiedad pasada a **SetColumns**; a continuación, la tabla pasará **PR_NULL** en esas posiciones en todas las filas recuperadas con **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="d4dab-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="d4dab-148">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d4dab-148">Notes to callers</span></span>

<span data-ttu-id="d4dab-149">Al crear la matriz de etiquetas de propiedad para el parámetro  _lpPropTagArray,_ ordene las etiquetas en el orden en que desea que las columnas aparezcan en la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="d4dab-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="d4dab-150">Puede especificar propiedades multivalor que se incluirán en el conjunto de columnas aplicando la marca de instancia multivalor o MVI_FLAG constante, a la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4dab-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="d4dab-151">Establezca esta marca pasando la etiqueta de propiedad de la versión de un solo valor de la propiedad como parámetro a la macro MVI_PROP siguiente:</span><span class="sxs-lookup"><span data-stu-id="d4dab-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="d4dab-152">La macro MVI_PROP establecerá MVI_FLAG para la propiedad, convirtiendo la etiqueta en una etiqueta multivalor.</span><span class="sxs-lookup"><span data-stu-id="d4dab-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="d4dab-153">Si intenta llamar erróneamente a MVI_PROP en una propiedad de un solo valor, MAPI omitirá la llamada y dejará la etiqueta de propiedad sin cambios.</span><span class="sxs-lookup"><span data-stu-id="d4dab-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="d4dab-154">Puede incluir etiquetas de propiedad **establecidas en PR_NULL** en la matriz de etiquetas de propiedad para reservar espacio en el conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="d4dab-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="d4dab-155">Reservar espacio permite agregar a un conjunto de columnas sin tener que asignar una nueva matriz de etiquetas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d4dab-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="d4dab-156">Cuando la llamada a **SetColumns** provoca un cambio en el orden de las columnas de una tabla y una o más de estas columnas representan una propiedad multivalor, es posible que aumente el número de filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d4dab-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="d4dab-157">Si esto ocurre, se descartan todos los marcadores de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d4dab-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="d4dab-158">Para obtener más información sobre cómo afectan las columnas multivalor a las tablas, vea [Working with Multivalued Columns](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="d4dab-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="d4dab-159">Establecer columnas es de forma predeterminada una operación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="d4dab-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="d4dab-160">Sin embargo, puede permitir que la tabla posponga la operación hasta que los datos se necesiten estableciendo la marca TBL_BATCH datos.</span><span class="sxs-lookup"><span data-stu-id="d4dab-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="d4dab-161">Establecer esta marca puede mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d4dab-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="d4dab-162">Otra marca, TBL_ASYNC, hace que la operación sea asincrónica, lo que permite que **SetColumns** vuelva antes de que se complete la operación.</span><span class="sxs-lookup"><span data-stu-id="d4dab-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="d4dab-163">Para determinar cuándo se produce la finalización, llame [a IMAPITable::GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="d4dab-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="d4dab-164">Si una llamada a **SetColumns** devuelve MAPI_E_BUSY, lo que indica que otra operación impide que se inicie la operación, puede llamar a [IMAPITable::Abort](imapitable-abort.md) para detener la operación en curso.</span><span class="sxs-lookup"><span data-stu-id="d4dab-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="d4dab-165">También puede llamar a [HrAddColumnsEx para](hraddcolumnsex.md) cambiar un conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="d4dab-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="d4dab-166">La diferencia entre **HrAddColumnsEx** e **IMAPITable::SetColumns** es que **HrAddColumnsEx** es menos flexible; solo puede agregar columnas.</span><span class="sxs-lookup"><span data-stu-id="d4dab-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="d4dab-167">Las columnas adicionales se colocan al principio del conjunto de columnas; todas las columnas existentes aparecen después de estas columnas.</span><span class="sxs-lookup"><span data-stu-id="d4dab-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d4dab-168">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d4dab-168">MFCMAPI reference</span></span>

<span data-ttu-id="d4dab-169">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d4dab-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d4dab-170">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="d4dab-170">**File**</span></span>|<span data-ttu-id="d4dab-171">**Función**</span><span class="sxs-lookup"><span data-stu-id="d4dab-171">**Function**</span></span>|<span data-ttu-id="d4dab-172">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="d4dab-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d4dab-173">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="d4dab-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="d4dab-174">CContentsTableListCtrl::D oSetColumns</span><span class="sxs-lookup"><span data-stu-id="d4dab-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="d4dab-175">MFCMAPI usa el **método IMAPITable::SetColumns** para establecer las columnas deseadas para la tabla.</span><span class="sxs-lookup"><span data-stu-id="d4dab-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4dab-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4dab-176">See also</span></span>



[<span data-ttu-id="d4dab-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="d4dab-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="d4dab-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="d4dab-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="d4dab-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="d4dab-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="d4dab-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="d4dab-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="d4dab-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="d4dab-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="d4dab-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="d4dab-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="d4dab-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="d4dab-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="d4dab-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="d4dab-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="d4dab-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d4dab-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="d4dab-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="d4dab-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="d4dab-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d4dab-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="d4dab-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d4dab-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="d4dab-189">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="d4dab-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

