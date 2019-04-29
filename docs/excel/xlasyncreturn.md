---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 32d5075af34cda9753c5d082bd4ab00afab1ecff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414112"
---
# <a name="xlasyncreturn"></a><span data-ttu-id="5ddb6-103">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="5ddb6-103">xlAsyncReturn</span></span>

<span data-ttu-id="5ddb6-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5ddb6-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5ddb6-105">Se usa para devolver el resultado de una función asincrónica definida por el usuario (UDF).</span><span class="sxs-lookup"><span data-stu-id="5ddb6-105">Used to return the result of an asynchronous user-defined function (UDF).</span></span>
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a><span data-ttu-id="5ddb6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5ddb6-106">Parameters</span></span>

<span data-ttu-id="5ddb6-107">_pxAsyncHandle_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="5ddb6-107">_pxAsyncHandle_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="5ddb6-108">Identificador asincrónico de la FDU a la que se devuelve el resultado.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-108">The asynchronous handle of the UDF to which the result is returned.</span></span>
  
<span data-ttu-id="5ddb6-109">_pxFunctionResult_</span><span class="sxs-lookup"><span data-stu-id="5ddb6-109">_pxFunctionResult_</span></span>
  
<span data-ttu-id="5ddb6-110">El valor devuelto de UDF.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-110">The return value of the UDF.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="5ddb6-111">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ddb6-111">Property value/Return value</span></span>

<span data-ttu-id="5ddb6-112">Si se ejecuta correctamente, devuelve **true** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="5ddb6-112">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="5ddb6-113">Si no se realiza correctamente, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-113">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ddb6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5ddb6-114">Remarks</span></span>

<span data-ttu-id="5ddb6-115">**xlAsyncReturn** es la única devolución de llamada que Excel permite en los subprocesos que no son de cálculo durante la actualización.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-115">**xlAsyncReturn** is the only callback Excel allows on non-calculation threads during recalculation.</span></span> <span data-ttu-id="5ddb6-116">La parte asincrónica de una UDF asincrónica no debe realizar ninguna devolución de llamada que no sea **xlAsyncReturn**.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-116">The asynchronous portion of an asynchronous UDF must not perform any callbacks other than **xlAsyncReturn**.</span></span> <span data-ttu-id="5ddb6-117">El XLL debe liberar la memoria asignada para contener el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-117">The XLL must free memory allocated to hold the return value.</span></span>
  
<span data-ttu-id="5ddb6-118">Los parámetros _pxAsyncHandle_ y _pxFunctionResult_ también pueden ser de tipo **xltypeMulti** cuando se usan para devolver una matriz de identificadores y los valores correspondientes en una sola devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-118">The _pxAsyncHandle_ and  _pxFunctionResult_ parameters can also be of type **xltypeMulti** when used to return an array of handles and corresponding values in a single callback.</span></span> <span data-ttu-id="5ddb6-119">Al usar una sola devolución de llamada, pase un LPXLOPER12 que apunte a las estructuras XLOPER12 que contienen matrices unidimensionales que contienen los identificadores asincrónicos y los valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-119">When using a single callback, pass an LPXLOPER12 that points to XLOPER12 structures that contain one dimensional arrays that contain the asynchronous handles and return values.</span></span> <span data-ttu-id="5ddb6-120">Estas matrices deben estar en el mismo orden para que Excel coincida correctamente con un identificador asincrónico con su valor correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-120">These arrays must be in the same order for Excel to correctly match an asynchronous handle with its corresponding value.</span></span> 
  
<span data-ttu-id="5ddb6-121">En el ejemplo siguiente se muestra cómo realizar una llamada por lotes mediante **xlAsyncReturn**.</span><span class="sxs-lookup"><span data-stu-id="5ddb6-121">The following example shows how you can make a batch call using **xlAsyncReturn**.</span></span>
  
```cpp
int batchSize = 10;
    LPXLOPER12 pHandles = new XLOPER12[batchSize];
    LPXLOPER12 pValues = new XLOPER12[batchSize];
    /*Add code to fill in LPXLOPER12 arrays (pHandles and pValues)
    with the XOPER12 structures that contain the asynchronous handles
    and values, in respective order*/
    //Create an XLOPER12 of type xltypeMulti, and fill the Handle array
    XLOPER12 handleArray;
    handleArray.xltype = xltypeMulti;
    handleArray.val.array.rows = 1;
    handleArray.val.array.columns = (COL)batchSize;
    handleArray.val.array.lparray = pHandles;
    
    //Create an XLOPER12 if type xltypeMulti, and fill the Values array
    XLOPER12 valueArray;
    valueArray.xltype = xltypeMulti;
    valueArray.val.array.rows = 1;
    valueArray.val.array.columns = (COL)batchSize;
    valueArray.val.array.lparray = pValues;
    //Make the callback with the return value
    int ret = Excel12(xlAsyncReturn, 0, 2, &amp;handleArray, &amp;valueArray);
    //Add code to free the allocated memory here (pHandles, pValues, valueArray, handleArray)
    return ret;

```

## <a name="see-also"></a><span data-ttu-id="5ddb6-122">Ver también</span><span class="sxs-lookup"><span data-stu-id="5ddb6-122">See also</span></span>

- [<span data-ttu-id="5ddb6-123">Funciones asincrónicas definidas por el usuario</span><span class="sxs-lookup"><span data-stu-id="5ddb6-123">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

