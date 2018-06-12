---
title: IMAPITableGetRowCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetRowCount
api_type:
- COM
ms.assetid: 44a12c92-7462-4acf-9520-5d4c2d7f1d47
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: a591a49c1cb0ec936d09d59b4632d15e4842dd2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817599"
---
# <a name="imapitablegetrowcount"></a><span data-ttu-id="18c0a-103">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="18c0a-103">IMAPITable::GetRowCount</span></span>

  
  
<span data-ttu-id="18c0a-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="18c0a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="18c0a-105">Devuelve el número total de filas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="18c0a-105">Returns the total number of rows in the table.</span></span> 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a><span data-ttu-id="18c0a-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="18c0a-106">Parameters</span></span>

 <span data-ttu-id="18c0a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="18c0a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="18c0a-108">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="18c0a-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="18c0a-109">_lpulCount_</span><span class="sxs-lookup"><span data-stu-id="18c0a-109">_lpulCount_</span></span>
  
> <span data-ttu-id="18c0a-110">[out] Puntero al número de filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="18c0a-110">[out] Pointer to the number of rows in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="18c0a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18c0a-111">Return value</span></span>

<span data-ttu-id="18c0a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="18c0a-112">S_OK</span></span> 
  
> <span data-ttu-id="18c0a-113">El recuento de filas se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="18c0a-113">The row count was successfully returned.</span></span>
    
<span data-ttu-id="18c0a-114">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="18c0a-114">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="18c0a-115">Otra operación está en curso que impide que la operación de recuperación del recuento de fila de inicio.</span><span class="sxs-lookup"><span data-stu-id="18c0a-115">Another operation is in progress that prevents the row count retrieval operation from starting.</span></span> <span data-ttu-id="18c0a-116">Debe ser permite la operación en curso para llevar a cabo o se debe detener.</span><span class="sxs-lookup"><span data-stu-id="18c0a-116">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="18c0a-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="18c0a-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="18c0a-118">La tabla no puede calcular el número de filas.</span><span class="sxs-lookup"><span data-stu-id="18c0a-118">The table cannot calculate the number of rows.</span></span>
    
<span data-ttu-id="18c0a-119">MAPI_W_APPROX_COUNT</span><span class="sxs-lookup"><span data-stu-id="18c0a-119">MAPI_W_APPROX_COUNT</span></span> 
  
> <span data-ttu-id="18c0a-120">La llamada se ha realizado correctamente, pero se devolvió un recuento de filas aproximado debido a que el número exacto de filas no se puede determinar, posiblemente, debido a las restricciones de memoria.</span><span class="sxs-lookup"><span data-stu-id="18c0a-120">The call succeeded, but an approximate row count was returned because the exact row count could not be determined possibly due to memory constraints.</span></span> <span data-ttu-id="18c0a-121">Para probar esta advertencia, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="18c0a-121">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="18c0a-122">Vea [uso de Macros para el tratamiento de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="18c0a-122">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18c0a-123">Notas</span><span class="sxs-lookup"><span data-stu-id="18c0a-123">Remarks</span></span>

<span data-ttu-id="18c0a-124">El método **IMAPITable::GetRowCount** recupera el número total de filas en una tabla.</span><span class="sxs-lookup"><span data-stu-id="18c0a-124">The **IMAPITable::GetRowCount** method retrieves the total number of rows in a table.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="18c0a-125">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="18c0a-125">Notes to implementers</span></span>

<span data-ttu-id="18c0a-126">Si no puede determinar el número de fila exacto de la tabla, MAPI_W_APPROX_COUNT devuelto y una fila aproximada contar en el contenido del parámetro _lpulCount_ .</span><span class="sxs-lookup"><span data-stu-id="18c0a-126">If you cannot determine the table's exact row count, return MAPI_W_APPROX_COUNT and an approximate row count in the contents of the  _lpulCount_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="18c0a-127">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="18c0a-127">Notes to callers</span></span>

<span data-ttu-id="18c0a-128">Uso **GetRowCount** para averiguar el número de filas de una tabla contiene antes de realizar una llamada al método [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="18c0a-128">Use **GetRowCount** to find out how many rows a table holds before making a call to the [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the data.</span></span> <span data-ttu-id="18c0a-129">Si hay menos de veinte filas en la tabla, es seguro llamar **QueryPosition** para recuperar toda la tabla.</span><span class="sxs-lookup"><span data-stu-id="18c0a-129">If there are less than twenty rows in the table, it is safe to call **QueryPosition** to retrieve the whole table.</span></span> <span data-ttu-id="18c0a-130">Si hay más de veinte filas de la tabla, considere la posibilidad de realizar varias llamadas a **QueryPosition** y limitar el número de filas recuperadas en cada llamada.</span><span class="sxs-lookup"><span data-stu-id="18c0a-130">If there are more than twenty rows in the table, consider making multiple calls to **QueryPosition** and limit the number of rows retrieved in each call.</span></span> 
  
<span data-ttu-id="18c0a-131">Algunas tablas no admiten **GetRowCount** y devolver MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="18c0a-131">Some tables do not support **GetRowCount** and return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="18c0a-132">Si no se admite **GetRowCount** , es posible una alternativa llamar a [IMAPITable::QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="18c0a-132">If **GetRowCount** is not supported, an alternative might be to call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="18c0a-133">Con los resultados de **QueryPosition**, puede determinar la relación entre la fila actual y la última fila.</span><span class="sxs-lookup"><span data-stu-id="18c0a-133">With the results from **QueryPosition**, you can determine the relationship between the current row and last row.</span></span> 
  
<span data-ttu-id="18c0a-134">Cuando **GetRowCount** devuelve MAPI_E_BUSY porque está temporalmente no se puede recuperar un recuento de filas, llame al método [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) .</span><span class="sxs-lookup"><span data-stu-id="18c0a-134">When **GetRowCount** returns MAPI_E_BUSY because it is temporarily unable to retrieve a row count, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method.</span></span> <span data-ttu-id="18c0a-135">Cuando se devuelve **WaitForCompletion** , vuelva a intentar la llamada a **GetRowCount**.</span><span class="sxs-lookup"><span data-stu-id="18c0a-135">When **WaitForCompletion** returns, retry the call to **GetRowCount**.</span></span> <span data-ttu-id="18c0a-136">Llame al método [IMAPITable::GetStatus](imapitable-getstatus.md) y compruebe el contenido del parámetro _lpulTableState_ es otra forma de detectar si una operación asincrónica está en curso.</span><span class="sxs-lookup"><span data-stu-id="18c0a-136">Another way to detect whether an asynchronous operation is in progress is to call the [IMAPITable::GetStatus](imapitable-getstatus.md) method and check the contents of the  _lpulTableState_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="18c0a-137">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="18c0a-137">MFCMAPI reference</span></span>

<span data-ttu-id="18c0a-138">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="18c0a-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="18c0a-139">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="18c0a-139">**File**</span></span>|<span data-ttu-id="18c0a-140">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="18c0a-140">**Function**</span></span>|<span data-ttu-id="18c0a-141">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="18c0a-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="18c0a-142">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="18c0a-142">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="18c0a-143">CopyFolderContents</span><span class="sxs-lookup"><span data-stu-id="18c0a-143">CopyFolderContents</span></span>  <br/> |<span data-ttu-id="18c0a-144">MFCMAPI usa el método **IMAPITable::GetRowCount** para determinar cuántas filas se encuentran en la tabla de origen por lo que se puede asignar memoria para realizar la copia.</span><span class="sxs-lookup"><span data-stu-id="18c0a-144">MFCMAPI uses the **IMAPITable::GetRowCount** method to determine how many rows are in the source table so memory can be allocated to perform the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18c0a-145">Ver también</span><span class="sxs-lookup"><span data-stu-id="18c0a-145">See also</span></span>



[<span data-ttu-id="18c0a-146">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="18c0a-146">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="18c0a-147">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="18c0a-147">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md)
  
[<span data-ttu-id="18c0a-148">IMAPITable:: QueryRows</span><span class="sxs-lookup"><span data-stu-id="18c0a-148">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="18c0a-149">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="18c0a-149">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="18c0a-150">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="18c0a-150">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="18c0a-151">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="18c0a-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

