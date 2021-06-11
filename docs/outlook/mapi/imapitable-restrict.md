---
title: IMAPITableRestrict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Restrict
api_type:
- COM
ms.assetid: a5bfc190-b58f-44c3-893c-8727df14ee58
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6cca6bc12fa6f100885b7bf705d79fa24a2e2f91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414623"
---
# <a name="imapitablerestrict"></a><span data-ttu-id="2d593-103">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="2d593-103">IMAPITable::Restrict</span></span>

  
  
<span data-ttu-id="2d593-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d593-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d593-105">Aplica un filtro a una tabla, lo que reduce el conjunto de filas a solo aquellas filas que coincidan con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="2d593-105">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2d593-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="2d593-106">Parameters</span></span>

 <span data-ttu-id="2d593-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="2d593-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="2d593-108">[in] Puntero a una [estructura SRestriction](srestriction.md) que define las condiciones del filtro.</span><span class="sxs-lookup"><span data-stu-id="2d593-108">[in] Pointer to an [SRestriction](srestriction.md) structure defining the conditions of the filter.</span></span> <span data-ttu-id="2d593-109">Si se pasa NULL en el  _parámetro lpRestriction,_ se quita el filtro actual.</span><span class="sxs-lookup"><span data-stu-id="2d593-109">Passing NULL in the  _lpRestriction_ parameter removes the current filter.</span></span> 
    
 <span data-ttu-id="2d593-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2d593-110">_ulFlags_</span></span>
  
> <span data-ttu-id="2d593-111">[in] Máscara de bits de marcas que controla el tiempo de la operación de restricción.</span><span class="sxs-lookup"><span data-stu-id="2d593-111">[in] Bitmask of flags that controls the timing of the restriction operation.</span></span> <span data-ttu-id="2d593-112">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="2d593-112">The following flags can be set:</span></span>
    
<span data-ttu-id="2d593-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="2d593-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="2d593-114">Inicia la operación de forma asincrónica y devuelve antes de que finalice la operación.</span><span class="sxs-lookup"><span data-stu-id="2d593-114">Starts the operation asynchronously and returns before the operation completes.</span></span>
    
<span data-ttu-id="2d593-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="2d593-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="2d593-116">Aplaza la evaluación del filtro hasta que se requieran los datos de la tabla.</span><span class="sxs-lookup"><span data-stu-id="2d593-116">Defers evaluation of the filter until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2d593-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d593-117">Return value</span></span>

<span data-ttu-id="2d593-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="2d593-118">S_OK</span></span> 
  
> <span data-ttu-id="2d593-119">El filtro se aplicó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2d593-119">The filter was successfully applied.</span></span>
    
<span data-ttu-id="2d593-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="2d593-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="2d593-121">Hay otra operación en curso que impide que se inicie la operación de restricción.</span><span class="sxs-lookup"><span data-stu-id="2d593-121">Another operation is in progress that prevents the restriction operation from starting.</span></span> <span data-ttu-id="2d593-122">Debe permitirse completar la operación en curso o detenerse.</span><span class="sxs-lookup"><span data-stu-id="2d593-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="2d593-123">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="2d593-123">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="2d593-124">La tabla no puede realizar la operación porque el filtro determinado al que apunta el parámetro  _lpRestriction_ es demasiado complicado.</span><span class="sxs-lookup"><span data-stu-id="2d593-124">The table cannot perform the operation because the particular filter pointed to by the  _lpRestriction_ parameter is too complicated.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2d593-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2d593-125">Remarks</span></span>

<span data-ttu-id="2d593-126">El **método IMAPITable::Restrict** establece una restricción o filtro en una tabla.</span><span class="sxs-lookup"><span data-stu-id="2d593-126">The **IMAPITable::Restrict** method establishes a restriction, or filter, on a table.</span></span> <span data-ttu-id="2d593-127">Si hay una restricción anterior, se descarta y se aplica la nueva.</span><span class="sxs-lookup"><span data-stu-id="2d593-127">If there is a previous restriction, it is discarded and the new one applied.</span></span> <span data-ttu-id="2d593-128">Aplicar una restricción no afecta a los datos subyacentes de una tabla; simplemente modifica la vista limitando las filas que se pueden recuperar a filas que contienen datos que satisfacen la restricción.</span><span class="sxs-lookup"><span data-stu-id="2d593-128">Applying a restriction has no affect on the underlying data of a table; it simply alters the view by limiting the rows that can be retrieved to rows containing data that satisfy the restriction.</span></span> 
  
<span data-ttu-id="2d593-129">Hay varios tipos diferentes de restricciones, cada una descrita con una estructura diferente.</span><span class="sxs-lookup"><span data-stu-id="2d593-129">There are several different types of restrictions, each described with a different structure.</span></span> <span data-ttu-id="2d593-130">La [estructura SRestriction](srestriction.md) contiene dos miembros: un valor que indica el tipo de restricción y la estructura específica aplicable a ese tipo.</span><span class="sxs-lookup"><span data-stu-id="2d593-130">The [SRestriction](srestriction.md) structure contains two members: a value that indicates the type of restriction and the specific structure applicable for that type.</span></span> 
  
<span data-ttu-id="2d593-131">Las notificaciones de las filas de tabla ocultas de la vista por llamadas a **Restrict** nunca se generan.</span><span class="sxs-lookup"><span data-stu-id="2d593-131">Notifications for table rows that are hidden from view by calls to **Restrict** are never generated.</span></span> 
  
<span data-ttu-id="2d593-132">Una restricción de propiedad en una propiedad multivalor funciona como una restricción en una propiedad de un solo valor.</span><span class="sxs-lookup"><span data-stu-id="2d593-132">A property restriction on a multivalued property works like a restriction on a single-valued property.</span></span> <span data-ttu-id="2d593-133">Una propiedad multivalor que se va a usar en una restricción de propiedad debe tener el MVI_FLAG de marca.</span><span class="sxs-lookup"><span data-stu-id="2d593-133">A multivalued property to be used in a property restriction must have the MVI_FLAG flag set.</span></span> <span data-ttu-id="2d593-134">Si no tiene esta marca establecida, se trata como una tupla totalmente ordenada.</span><span class="sxs-lookup"><span data-stu-id="2d593-134">If it doesn't have this flag set, it is treated as a totally ordered tuple.</span></span> <span data-ttu-id="2d593-135">Una comparación de dos columnas multivalor compara los elementos de columna en orden, informando de la relación de las columnas en la primera desigualdad.</span><span class="sxs-lookup"><span data-stu-id="2d593-135">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality.</span></span> <span data-ttu-id="2d593-136">La igualdad solo se devuelve si las columnas comparadas contienen los mismos valores en el mismo orden.</span><span class="sxs-lookup"><span data-stu-id="2d593-136">Equality is returned only if the columns compared contain the same values in the same order.</span></span> <span data-ttu-id="2d593-137">Si una columna tiene menos valores que la otra, la relación notificada es la de un valor nulo con el otro valor.</span><span class="sxs-lookup"><span data-stu-id="2d593-137">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
<span data-ttu-id="2d593-138">Para obtener más información acerca de las restricciones, vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="2d593-138">For more information about restrictions, see [About Restrictions](about-restrictions.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="2d593-139">Si crea consultas dinámicas para buscar datos en el servidor, use el método **FindRow** en lugar de usar el método **Restrict** y el **método QueryRows** juntos.</span><span class="sxs-lookup"><span data-stu-id="2d593-139">If you create dynamic queries to search for data on the server, use the **FindRow** method instead of using the **Restrict** method and the **QueryRows** method together.</span></span> <span data-ttu-id="2d593-140">El **método Restrict** crea una vista en caché que se usa para evaluar todos los mensajes agregados o modificados en la carpeta base.</span><span class="sxs-lookup"><span data-stu-id="2d593-140">The **Restrict** method creates a cached view that is used to evaluate all messages added to or modified in the base folder.</span></span> <span data-ttu-id="2d593-141">Si una aplicación cliente usa el **método Restrict** para cada consulta dinámica, se creará una vista en caché para cada consulta.</span><span class="sxs-lookup"><span data-stu-id="2d593-141">If a client application uses the **Restrict** method for each dynamic query, a cached view will be created for each query.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2d593-142">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="2d593-142">Notes to callers</span></span>

<span data-ttu-id="2d593-143">Para descartar la restricción actual sin crear una nueva, pase NULL en  _lpRestriction_.</span><span class="sxs-lookup"><span data-stu-id="2d593-143">To discard the current restriction without creating a new one, pass NULL in  _lpRestriction_.</span></span>
  
<span data-ttu-id="2d593-144">Si hay otra llamada de tabla asincrónica en curso, lo que hace que **Restrict** devuelva MAPI_E_BUSY, puede llamar a [IMAPITable::Abort](imapitable-abort.md) para detener la llamada.</span><span class="sxs-lookup"><span data-stu-id="2d593-144">If another asynchronous table call is in progress, causing **Restrict** to return MAPI_E_BUSY, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the call.</span></span> 
  
 <span data-ttu-id="2d593-145">**Restrict** funciona de forma sincrónica a menos que establezca una de las marcas.</span><span class="sxs-lookup"><span data-stu-id="2d593-145">**Restrict** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="2d593-146">Si establece la marca TBL_BATCH, **Restrict** pospone la evaluación de la restricción a menos que solicite los datos.</span><span class="sxs-lookup"><span data-stu-id="2d593-146">If you set the TBL_BATCH flag, **Restrict** postpones the evaluation of the restriction unless you request the data.</span></span> <span data-ttu-id="2d593-147">Si se TBL_ASYNC marca, **Restrict** funciona de forma asincrónica, lo que podría devolverse antes de finalizar la operación.</span><span class="sxs-lookup"><span data-stu-id="2d593-147">If the TBL_ASYNC flag is set, **Restrict** operates asynchronously, potentially returning before the completion of the operation.</span></span>
  
<span data-ttu-id="2d593-148">Todos los marcadores de una tabla se descartan cuando se realiza una llamada a **Restrict** y BOOKMARK_CURRENT, la posición actual del cursor, se establece en el principio de la tabla.</span><span class="sxs-lookup"><span data-stu-id="2d593-148">All bookmarks for a table are discarded when a call to **Restrict** is made, and BOOKMARK_CURRENT, the current cursor position, is set to the beginning of the table.</span></span> 
  
<span data-ttu-id="2d593-149">Si intenta imponer una restricción de propiedad a una propiedad que no está en el conjunto de columnas de la tabla, los resultados no están definidos.</span><span class="sxs-lookup"><span data-stu-id="2d593-149">If you attempt to impose a property restriction on a property that is not in the table's column set, the results are undefined.</span></span> <span data-ttu-id="2d593-150">Siempre que no esté seguro de si se admite una propiedad en una tabla, combine la restricción de propiedad con una restricción existente.</span><span class="sxs-lookup"><span data-stu-id="2d593-150">Whenever you are unsure as to whether a property is supported in a table, combine the property restriction with an exists restriction.</span></span> <span data-ttu-id="2d593-151">La restricción existe comprueba la existencia de la propiedad antes de intentar imponer la restricción de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2d593-151">The exists restriction checks for the existence of the property before attempting to impose the property restriction.</span></span> 
  
<span data-ttu-id="2d593-152">No espere recibir una notificación de tabla en una fila que se haya filtrado de una tabla debido a una restricción.</span><span class="sxs-lookup"><span data-stu-id="2d593-152">Do not expect to receive a table notification on a row that has been filtered from a table due to a restriction.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2d593-153">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2d593-153">MFCMAPI reference</span></span>

<span data-ttu-id="2d593-154">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2d593-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2d593-155">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="2d593-155">**File**</span></span>|<span data-ttu-id="2d593-156">**Función**</span><span class="sxs-lookup"><span data-stu-id="2d593-156">**Function**</span></span>|<span data-ttu-id="2d593-157">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="2d593-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2d593-158">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="2d593-158">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="2d593-159">CContentsTableListCtrl::ApplyRestriction</span><span class="sxs-lookup"><span data-stu-id="2d593-159">CContentsTableListCtrl::ApplyRestriction</span></span>  <br/> |<span data-ttu-id="2d593-160">MFCMAPI usa el **método IMAPITable::Restrict** para establecer una restricción en una tabla.</span><span class="sxs-lookup"><span data-stu-id="2d593-160">MFCMAPI uses the **IMAPITable::Restrict** method to set a restriction on a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d593-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d593-161">See also</span></span>



[<span data-ttu-id="2d593-162">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="2d593-162">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="2d593-163">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="2d593-163">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="2d593-164">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="2d593-164">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="2d593-165">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="2d593-165">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="2d593-166">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="2d593-166">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="2d593-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d593-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="2d593-168">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="2d593-168">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

