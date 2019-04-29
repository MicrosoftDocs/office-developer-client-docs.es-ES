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
# <a name="xlasyncreturn"></a>xlAsyncReturn

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se usa para devolver el resultado de una función asincrónica definida por el usuario (UDF).
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a>Parameters

_pxAsyncHandle_ (**xltypeBigData**)
  
Identificador asincrónico de la FDU a la que se devuelve el resultado.
  
_pxFunctionResult_
  
El valor devuelto de UDF.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Si se ejecuta correctamente, devuelve **true** (**xltypeBool**). Si no se realiza correctamente, devuelve **false**.
  
## <a name="remarks"></a>Comentarios

**xlAsyncReturn** es la única devolución de llamada que Excel permite en los subprocesos que no son de cálculo durante la actualización. La parte asincrónica de una UDF asincrónica no debe realizar ninguna devolución de llamada que no sea **xlAsyncReturn**. El XLL debe liberar la memoria asignada para contener el valor devuelto.
  
Los parámetros _pxAsyncHandle_ y _pxFunctionResult_ también pueden ser de tipo **xltypeMulti** cuando se usan para devolver una matriz de identificadores y los valores correspondientes en una sola devolución de llamada. Al usar una sola devolución de llamada, pase un LPXLOPER12 que apunte a las estructuras XLOPER12 que contienen matrices unidimensionales que contienen los identificadores asincrónicos y los valores devueltos. Estas matrices deben estar en el mismo orden para que Excel coincida correctamente con un identificador asincrónico con su valor correspondiente. 
  
En el ejemplo siguiente se muestra cómo realizar una llamada por lotes mediante **xlAsyncReturn**.
  
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

## <a name="see-also"></a>Ver también

- [Funciones asincrónicas definidas por el usuario](asynchronous-user-defined-functions.md)

