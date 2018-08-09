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
ms.openlocfilehash: 3ab069728f872d82246e8925c5ad35c07f41f02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817609"
---
# <a name="imapitablerestrict"></a><span data-ttu-id="c62ec-103">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="c62ec-103">IMAPITable::Restrict</span></span>

  
  
<span data-ttu-id="c62ec-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c62ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c62ec-105">Se aplica un filtro a una tabla, reducción de la fila que se establece en sólo las filas que coincidan con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="c62ec-105">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c62ec-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c62ec-106">Parameters</span></span>

 <span data-ttu-id="c62ec-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="c62ec-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="c62ec-108">[entrada] Puntero a una estructura de [SRestriction](srestriction.md) definición de las condiciones del filtro.</span><span class="sxs-lookup"><span data-stu-id="c62ec-108">[in] Pointer to an [SRestriction](srestriction.md) structure defining the conditions of the filter.</span></span> <span data-ttu-id="c62ec-109">Pasar NULL en el parámetro _lpRestriction_ , quita el filtro actual.</span><span class="sxs-lookup"><span data-stu-id="c62ec-109">Passing NULL in the  _lpRestriction_ parameter removes the current filter.</span></span> 
    
 <span data-ttu-id="c62ec-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c62ec-110">_ulFlags_</span></span>
  
> <span data-ttu-id="c62ec-111">[entrada] Máscara de bits de indicadores que controla la sincronización de la operación de restricción.</span><span class="sxs-lookup"><span data-stu-id="c62ec-111">[in] Bitmask of flags that controls the timing of the restriction operation.</span></span> <span data-ttu-id="c62ec-112">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="c62ec-112">The following flags can be set:</span></span>
    
<span data-ttu-id="c62ec-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="c62ec-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="c62ec-114">Inicia la operación de forma asincrónica y devuelve antes de que finalice la operación.</span><span class="sxs-lookup"><span data-stu-id="c62ec-114">Starts the operation asynchronously and returns before the operation completes.</span></span>
    
<span data-ttu-id="c62ec-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="c62ec-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="c62ec-116">Difiere la evaluación del filtro hasta que los datos de la tabla están necesarios.</span><span class="sxs-lookup"><span data-stu-id="c62ec-116">Defers evaluation of the filter until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c62ec-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c62ec-117">Return value</span></span>

<span data-ttu-id="c62ec-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c62ec-118">S_OK</span></span> 
  
> <span data-ttu-id="c62ec-119">El filtro se ha aplicado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c62ec-119">The filter was successfully applied.</span></span>
    
<span data-ttu-id="c62ec-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="c62ec-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="c62ec-121">Otra operación está en curso que impide que la operación de restricción de inicio.</span><span class="sxs-lookup"><span data-stu-id="c62ec-121">Another operation is in progress that prevents the restriction operation from starting.</span></span> <span data-ttu-id="c62ec-122">Debe ser permite la operación en curso para llevar a cabo o se debe detener.</span><span class="sxs-lookup"><span data-stu-id="c62ec-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="c62ec-123">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="c62ec-123">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="c62ec-124">La tabla no puede realizar la operación porque el filtro determinado indicado por el parámetro _lpRestriction_ es demasiado complicado.</span><span class="sxs-lookup"><span data-stu-id="c62ec-124">The table cannot perform the operation because the particular filter pointed to by the  _lpRestriction_ parameter is too complicated.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c62ec-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c62ec-125">Remarks</span></span>

<span data-ttu-id="c62ec-126">El método **IMAPITable:: Restrict** establece una restricción, o un filtro, en una tabla.</span><span class="sxs-lookup"><span data-stu-id="c62ec-126">The **IMAPITable::Restrict** method establishes a restriction, or filter, on a table.</span></span> <span data-ttu-id="c62ec-127">Si hay una restricción anterior, se descarta y aplica uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="c62ec-127">If there is a previous restriction, it is discarded and the new one applied.</span></span> <span data-ttu-id="c62ec-128">Aplicar una restricción no tiene ningún efecto en los datos subyacentes de una tabla; simplemente se modifica la vista al limitar las filas que se pueden recuperar a las filas que contienen datos que cumplen la restricción.</span><span class="sxs-lookup"><span data-stu-id="c62ec-128">Applying a restriction has no affect on the underlying data of a table; it simply alters the view by limiting the rows that can be retrieved to rows containing data that satisfy the restriction.</span></span> 
  
<span data-ttu-id="c62ec-129">Hay varios tipos diferentes de las restricciones, cada uno de ellos se describe con una estructura diferente.</span><span class="sxs-lookup"><span data-stu-id="c62ec-129">There are several different types of restrictions, each described with a different structure.</span></span> <span data-ttu-id="c62ec-130">La estructura de [SRestriction](srestriction.md) contiene dos miembros: un valor que indica el tipo de restricción y la estructura específica aplicable para ese tipo.</span><span class="sxs-lookup"><span data-stu-id="c62ec-130">The [SRestriction](srestriction.md) structure contains two members: a value that indicates the type of restriction and the specific structure applicable for that type.</span></span> 
  
<span data-ttu-id="c62ec-131">Las notificaciones para las filas de tabla que están ocultos de la vista mediante llamadas a **Restrict** nunca se generan.</span><span class="sxs-lookup"><span data-stu-id="c62ec-131">Notifications for table rows that are hidden from view by calls to **Restrict** are never generated.</span></span> 
  
<span data-ttu-id="c62ec-132">Una restricción de propiedad en una propiedad multivalor funciona como una restricción en una propiedad de un solo valor.</span><span class="sxs-lookup"><span data-stu-id="c62ec-132">A property restriction on a multivalued property works like a restriction on a single-valued property.</span></span> <span data-ttu-id="c62ec-133">Una propiedad multivalor para usarse en una restricción de propiedad debe tener la marca MVI_FLAG establecida.</span><span class="sxs-lookup"><span data-stu-id="c62ec-133">A multivalued property to be used in a property restriction must have the MVI_FLAG flag set.</span></span> <span data-ttu-id="c62ec-134">Si no tiene este indicador establecido, se trata como una tupla totalmente ordenada.</span><span class="sxs-lookup"><span data-stu-id="c62ec-134">If it doesn't have this flag set, it is treated as a totally ordered tuple.</span></span> <span data-ttu-id="c62ec-135">Una comparación de dos columnas con varios valores compara los elementos de columna en orden, la relación de las columnas en la primera desigualdad de informes.</span><span class="sxs-lookup"><span data-stu-id="c62ec-135">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality.</span></span> <span data-ttu-id="c62ec-136">Igualdad se devuelve sólo si las columnas que se comparan contienen los mismos valores en el mismo orden.</span><span class="sxs-lookup"><span data-stu-id="c62ec-136">Equality is returned only if the columns compared contain the same values in the same order.</span></span> <span data-ttu-id="c62ec-137">Si una columna tiene menos valores que el otro, la relación conocida es un valor nulo en el otro valor.</span><span class="sxs-lookup"><span data-stu-id="c62ec-137">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
<span data-ttu-id="c62ec-138">Para obtener más información acerca de las restricciones, vea [Restricciones de sobre](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="c62ec-138">For more information about restrictions, see [About Restrictions](about-restrictions.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="c62ec-139">Si crea consultas dinámicas para buscar datos en el servidor, use el método **FindRow** en lugar de usar el método **Restrict** y el método **QueryRows** juntos.</span><span class="sxs-lookup"><span data-stu-id="c62ec-139">If you create dynamic queries to search for data on the server, use the **FindRow** method instead of using the **Restrict** method and the **QueryRows** method together.</span></span> <span data-ttu-id="c62ec-140">El método **Restrict** crea una vista en caché que se usa para evaluar todos los mensajes, agregar o modificar en la carpeta base.</span><span class="sxs-lookup"><span data-stu-id="c62ec-140">The **Restrict** method creates a cached view that is used to evaluate all messages added to or modified in the base folder.</span></span> <span data-ttu-id="c62ec-141">Si una aplicación cliente usa el método **Restrict** para cada consulta dinámica, se creará una vista en caché para cada consulta.</span><span class="sxs-lookup"><span data-stu-id="c62ec-141">If a client application uses the **Restrict** method for each dynamic query, a cached view will be created for each query.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c62ec-142">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="c62ec-142">Notes to callers</span></span>

<span data-ttu-id="c62ec-143">Para descartar la restricción actual sin crear una nueva, pase NULL en _lpRestriction_.</span><span class="sxs-lookup"><span data-stu-id="c62ec-143">To discard the current restriction without creating a new one, pass NULL in  _lpRestriction_.</span></span>
  
<span data-ttu-id="c62ec-144">Si hay otra llamada tabla asincrónica en curso, lo que provoca que **Restrict** devolver MAPI_E_BUSY, puede llamar a [IMAPITable::Abort](imapitable-abort.md) para detener la llamada.</span><span class="sxs-lookup"><span data-stu-id="c62ec-144">If another asynchronous table call is in progress, causing **Restrict** to return MAPI_E_BUSY, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the call.</span></span> 
  
 <span data-ttu-id="c62ec-145">**Restrict** funciona de forma sincrónica a menos que establezca uno de los indicadores.</span><span class="sxs-lookup"><span data-stu-id="c62ec-145">**Restrict** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="c62ec-146">Si se establece la marca TBL_BATCH, **Restrict** pospone la evaluación de la restricción a menos que solicitar los datos.</span><span class="sxs-lookup"><span data-stu-id="c62ec-146">If you set the TBL_BATCH flag, **Restrict** postpones the evaluation of the restriction unless you request the data.</span></span> <span data-ttu-id="c62ec-147">Si se establece la marca TBL_ASYNC, **Restrict**funciona de forma asincrónica, potencialmente devolver antes de la finalización de la operación.</span><span class="sxs-lookup"><span data-stu-id="c62ec-147">If the TBL_ASYNC flag is set, **Restrict**operates asynchronously, potentially returning before the completion of the operation.</span></span>
  
<span data-ttu-id="c62ec-148">Cuando se realiza una llamada a **Restrict** y BOOKMARK_CURRENT, la posición actual del cursor, se establece en el principio de la tabla, se descartan todos los marcadores de una tabla.</span><span class="sxs-lookup"><span data-stu-id="c62ec-148">All bookmarks for a table are discarded when a call to **Restrict** is made, and BOOKMARK_CURRENT, the current cursor position, is set to the beginning of the table.</span></span> 
  
<span data-ttu-id="c62ec-149">Si se intenta imponer una restricción de propiedad en una propiedad que no está en el conjunto de columnas de la tabla, los resultados son no definidos.</span><span class="sxs-lookup"><span data-stu-id="c62ec-149">If you attempt to impose a property restriction on a property that is not in the table's column set, the results are undefined.</span></span> <span data-ttu-id="c62ec-150">Siempre que no está seguro de si se admite una propiedad en una tabla, combinar la restricción de propiedad con una restricción de existe.</span><span class="sxs-lookup"><span data-stu-id="c62ec-150">Whenever you are unsure as to whether a property is supported in a table, combine the property restriction with an exists restriction.</span></span> <span data-ttu-id="c62ec-151">El existe restricción comprueba la existencia de la propiedad antes de intentar imponer la restricción de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c62ec-151">The exists restriction checks for the existence of the property before attempting to impose the property restriction.</span></span> 
  
<span data-ttu-id="c62ec-152">No se debe esperar recibir una notificación de tabla en una fila que se ha filtrado de una tabla debido a una restricción.</span><span class="sxs-lookup"><span data-stu-id="c62ec-152">Do not expect to receive a table notification on a row that has been filtered from a table due to a restriction.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c62ec-153">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c62ec-153">MFCMAPI reference</span></span>

<span data-ttu-id="c62ec-154">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="c62ec-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c62ec-155">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="c62ec-155">**File**</span></span>|<span data-ttu-id="c62ec-156">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="c62ec-156">**Function**</span></span>|<span data-ttu-id="c62ec-157">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="c62ec-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c62ec-158">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="c62ec-158">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="c62ec-159">CContentsTableListCtrl::ApplyRestriction</span><span class="sxs-lookup"><span data-stu-id="c62ec-159">CContentsTableListCtrl::ApplyRestriction</span></span>  <br/> |<span data-ttu-id="c62ec-160">MFCMAPI usa el método **IMAPITable:: Restrict** para establecer una restricción en una tabla.</span><span class="sxs-lookup"><span data-stu-id="c62ec-160">MFCMAPI uses the **IMAPITable::Restrict** method to set a restriction on a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c62ec-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="c62ec-161">See also</span></span>



[<span data-ttu-id="c62ec-162">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="c62ec-162">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="c62ec-163">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="c62ec-163">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="c62ec-164">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="c62ec-164">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="c62ec-165">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="c62ec-165">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="c62ec-166">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="c62ec-166">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="c62ec-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c62ec-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="c62ec-168">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="c62ec-168">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

