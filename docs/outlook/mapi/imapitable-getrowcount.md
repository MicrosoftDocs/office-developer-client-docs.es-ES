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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b13bf3bdd8392efc42ad189e48dffad8636f0708
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328892"
---
# <a name="imapitablegetrowcount"></a><span data-ttu-id="cfeba-103">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="cfeba-103">IMAPITable::GetRowCount</span></span>

  
  
<span data-ttu-id="cfeba-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cfeba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cfeba-105">Devuelve el número total de filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="cfeba-105">Returns the total number of rows in the table.</span></span> 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a><span data-ttu-id="cfeba-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="cfeba-106">Parameters</span></span>

 <span data-ttu-id="cfeba-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cfeba-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cfeba-108">Reserve debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cfeba-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="cfeba-109">_lpulCount_</span><span class="sxs-lookup"><span data-stu-id="cfeba-109">_lpulCount_</span></span>
  
> <span data-ttu-id="cfeba-110">contempla Puntero al número de filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="cfeba-110">[out] Pointer to the number of rows in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cfeba-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfeba-111">Return value</span></span>

<span data-ttu-id="cfeba-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="cfeba-112">S_OK</span></span> 
  
> <span data-ttu-id="cfeba-113">El recuento de filas se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="cfeba-113">The row count was successfully returned.</span></span>
    
<span data-ttu-id="cfeba-114">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="cfeba-114">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="cfeba-115">Hay otra operación en curso que impide que se inicie la operación de recuperación de recuento de filas.</span><span class="sxs-lookup"><span data-stu-id="cfeba-115">Another operation is in progress that prevents the row count retrieval operation from starting.</span></span> <span data-ttu-id="cfeba-116">Debe permitirse que la operación en curso se complete o que deba detenerse.</span><span class="sxs-lookup"><span data-stu-id="cfeba-116">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="cfeba-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="cfeba-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="cfeba-118">La tabla no puede calcular el número de filas.</span><span class="sxs-lookup"><span data-stu-id="cfeba-118">The table cannot calculate the number of rows.</span></span>
    
<span data-ttu-id="cfeba-119">MAPI_W_APPROX_COUNT</span><span class="sxs-lookup"><span data-stu-id="cfeba-119">MAPI_W_APPROX_COUNT</span></span> 
  
> <span data-ttu-id="cfeba-120">La llamada se realizó correctamente, pero se devolvió un recuento de filas aproximado porque no se pudo determinar el recuento de filas exacto, posiblemente debido a restricciones de memoria.</span><span class="sxs-lookup"><span data-stu-id="cfeba-120">The call succeeded, but an approximate row count was returned because the exact row count could not be determined possibly due to memory constraints.</span></span> <span data-ttu-id="cfeba-121">Para probar esta advertencia, use la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="cfeba-121">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="cfeba-122">Consulte [uso de macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="cfeba-122">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cfeba-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cfeba-123">Remarks</span></span>

<span data-ttu-id="cfeba-124">El método **IMAPITable:: GetRowCount** recupera el número total de filas de una tabla.</span><span class="sxs-lookup"><span data-stu-id="cfeba-124">The **IMAPITable::GetRowCount** method retrieves the total number of rows in a table.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="cfeba-125">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="cfeba-125">Notes to implementers</span></span>

<span data-ttu-id="cfeba-126">Si no puede determinar el número exacto de filas de la tabla, devuelva MAPI_W_APPROX_COUNT y un recuento de filas aproximado en el contenido del parámetro _lpulCount_ .</span><span class="sxs-lookup"><span data-stu-id="cfeba-126">If you cannot determine the table's exact row count, return MAPI_W_APPROX_COUNT and an approximate row count in the contents of the  _lpulCount_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cfeba-127">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="cfeba-127">Notes to callers</span></span>

<span data-ttu-id="cfeba-128">Use **GetRowCount** para averiguar el número de filas que contiene una tabla antes de realizar una llamada al método [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="cfeba-128">Use **GetRowCount** to find out how many rows a table holds before making a call to the [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the data.</span></span> <span data-ttu-id="cfeba-129">Si hay menos de veinte filas en la tabla, es seguro llamar a **QueryPosition** para recuperar toda la tabla.</span><span class="sxs-lookup"><span data-stu-id="cfeba-129">If there are less than twenty rows in the table, it is safe to call **QueryPosition** to retrieve the whole table.</span></span> <span data-ttu-id="cfeba-130">Si hay más de veinte filas en la tabla, considere la posibilidad de realizar varias llamadas a **QueryPosition** y limitar el número de filas recuperadas en cada llamada.</span><span class="sxs-lookup"><span data-stu-id="cfeba-130">If there are more than twenty rows in the table, consider making multiple calls to **QueryPosition** and limit the number of rows retrieved in each call.</span></span> 
  
<span data-ttu-id="cfeba-131">Algunas tablas no admiten **GetRowCount** y devuelven MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="cfeba-131">Some tables do not support **GetRowCount** and return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="cfeba-132">Si no se admite **GetRowCount** , una alternativa podría ser llamar al [IMAPITable:: QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="cfeba-132">If **GetRowCount** is not supported, an alternative might be to call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="cfeba-133">Con los resultados de **QueryPosition**, puede determinar la relación entre la fila actual y la última fila.</span><span class="sxs-lookup"><span data-stu-id="cfeba-133">With the results from **QueryPosition**, you can determine the relationship between the current row and last row.</span></span> 
  
<span data-ttu-id="cfeba-134">Cuando **GetRowCount** devuelve MAPI_E_BUSY porque temporalmente no puede recuperar un recuento de filas, llame al método [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md) .</span><span class="sxs-lookup"><span data-stu-id="cfeba-134">When **GetRowCount** returns MAPI_E_BUSY because it is temporarily unable to retrieve a row count, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method.</span></span> <span data-ttu-id="cfeba-135">Cuando **WaitForCompletion** devuelva, vuelva a intentar la llamada a **GetRowCount**.</span><span class="sxs-lookup"><span data-stu-id="cfeba-135">When **WaitForCompletion** returns, retry the call to **GetRowCount**.</span></span> <span data-ttu-id="cfeba-136">Otra forma de detectar si una operación asincrónica está en curso es llamar al método [IMAPITable:: getStatus](imapitable-getstatus.md) y comprobar el contenido del parámetro _lpulTableState_ .</span><span class="sxs-lookup"><span data-stu-id="cfeba-136">Another way to detect whether an asynchronous operation is in progress is to call the [IMAPITable::GetStatus](imapitable-getstatus.md) method and check the contents of the  _lpulTableState_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cfeba-137">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cfeba-137">MFCMAPI reference</span></span>

<span data-ttu-id="cfeba-138">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="cfeba-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cfeba-139">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="cfeba-139">**File**</span></span>|<span data-ttu-id="cfeba-140">**Función**</span><span class="sxs-lookup"><span data-stu-id="cfeba-140">**Function**</span></span>|<span data-ttu-id="cfeba-141">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="cfeba-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cfeba-142">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="cfeba-142">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="cfeba-143">CopyFolderContents</span><span class="sxs-lookup"><span data-stu-id="cfeba-143">CopyFolderContents</span></span>  <br/> |<span data-ttu-id="cfeba-144">MFCMAPI usa el método **IMAPITable:: GetRowCount** para determinar cuántas filas hay en la tabla de origen, por lo que se puede asignar memoria para realizar la copia.</span><span class="sxs-lookup"><span data-stu-id="cfeba-144">MFCMAPI uses the **IMAPITable::GetRowCount** method to determine how many rows are in the source table so memory can be allocated to perform the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cfeba-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfeba-145">See also</span></span>



[<span data-ttu-id="cfeba-146">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="cfeba-146">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="cfeba-147">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="cfeba-147">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md)
  
[<span data-ttu-id="cfeba-148">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="cfeba-148">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="cfeba-149">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="cfeba-149">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="cfeba-150">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cfeba-150">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="cfeba-151">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="cfeba-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

