---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e7ba37629ff2198339394448410ffd16477d4766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815717"
---
# <a name="xlasyncreturn"></a><span data-ttu-id="8784f-103">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="8784f-103">xlAsyncReturn</span></span>

<span data-ttu-id="8784f-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8784f-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8784f-105">Se usa para devolver el resultado de una función asincrónica definidas por el usuario (UDF).</span><span class="sxs-lookup"><span data-stu-id="8784f-105">Used to return the result of an asynchronous user-defined function (UDF).</span></span>
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a><span data-ttu-id="8784f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8784f-106">Parameters</span></span>

<span data-ttu-id="8784f-107">_pxAsyncHandle_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="8784f-107">_pxAsyncHandle_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="8784f-108">El controlador asincrónico del archivo UDF a la que se devuelve el resultado.</span><span class="sxs-lookup"><span data-stu-id="8784f-108">The asynchronous handle of the UDF to which the result is returned.</span></span>
  
<span data-ttu-id="8784f-109">_pxFunctionResult_</span><span class="sxs-lookup"><span data-stu-id="8784f-109">_pxFunctionResult_</span></span>
  
<span data-ttu-id="8784f-110">El valor devuelto de la UDF.</span><span class="sxs-lookup"><span data-stu-id="8784f-110">The return value of the UDF.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="8784f-111">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8784f-111">Property value/Return value</span></span>

<span data-ttu-id="8784f-112">Si se realiza correctamente, devuelve **TRUE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="8784f-112">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="8784f-113">Si no lo consigue, devuelve **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="8784f-113">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8784f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8784f-114">Remarks</span></span>

<span data-ttu-id="8784f-115">**xlAsyncReturn** es la devolución de llamada sólo permite que Excel en subprocesos de cálculo que no sean durante la actualización.</span><span class="sxs-lookup"><span data-stu-id="8784f-115">**xlAsyncReturn** is the only callback Excel allows on non-calculation threads during recalculation.</span></span> <span data-ttu-id="8784f-116">La parte asincrónica de una UDF asincrónica no debe llevar a cabo cualquier devoluciones de llamada que no sea **xlAsyncReturn**.</span><span class="sxs-lookup"><span data-stu-id="8784f-116">The asynchronous portion of an asynchronous UDF must not perform any callbacks other than **xlAsyncReturn**.</span></span> <span data-ttu-id="8784f-117">El XLL debe liberar memoria asignada para contener el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="8784f-117">The XLL must free memory allocated to hold the return value.</span></span>
  
<span data-ttu-id="8784f-118">Los parámetros _pxAsyncHandle_ y _pxFunctionResult_ también pueden ser de tipo **xltypeMulti** cuando se usa para devolver una matriz de identificadores y los valores correspondientes en una devolución de llamada único.</span><span class="sxs-lookup"><span data-stu-id="8784f-118">The _pxAsyncHandle_ and  _pxFunctionResult_ parameters can also be of type **xltypeMulti** when used to return an array of handles and corresponding values in a single callback.</span></span> <span data-ttu-id="8784f-119">Cuando se utiliza una devolución de llamada única, pase una LPXLOPER12 que apunta al XLOPER12 estructuras que contienen uno dimensionales matrices que contienen los controladores asincrónicos y valores devuelven.</span><span class="sxs-lookup"><span data-stu-id="8784f-119">When using a single callback, pass an LPXLOPER12 that points to XLOPER12 structures that contain one dimensional arrays that contain the asynchronous handles and return values.</span></span> <span data-ttu-id="8784f-120">Estas matrices deben estar en el mismo orden para Excel para que coincidan correctamente con un controlador asincrónico con su valor correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8784f-120">These arrays must be in the same order for Excel to correctly match an asynchronous handle with its corresponding value.</span></span> 
  
<span data-ttu-id="8784f-121">En el ejemplo siguiente se muestra cómo puede hacer que un lote de llamar con **xlAsyncReturn**.</span><span class="sxs-lookup"><span data-stu-id="8784f-121">The following example shows how you can make a batch call using **xlAsyncReturn**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="8784f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="8784f-122">See also</span></span>

- [<span data-ttu-id="8784f-123">Funciones asincrónicas definidas por el usuario</span><span class="sxs-lookup"><span data-stu-id="8784f-123">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

