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
# <a name="xlasyncreturn"></a>xlAsyncReturn

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se usa para devolver el resultado de una función asincrónica definidas por el usuario (UDF).
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a>Parámetros

_pxAsyncHandle_ (**xltypeBigData**)
  
El controlador asincrónico del archivo UDF a la que se devuelve el resultado.
  
_pxFunctionResult_
  
El valor devuelto de la UDF.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Si se realiza correctamente, devuelve **TRUE** (**xltypeBool**). Si no lo consigue, devuelve **FALSE**.
  
## <a name="remarks"></a>Comentarios

**xlAsyncReturn** es la devolución de llamada sólo permite que Excel en subprocesos de cálculo que no sean durante la actualización. La parte asincrónica de una UDF asincrónica no debe llevar a cabo cualquier devoluciones de llamada que no sea **xlAsyncReturn**. El XLL debe liberar memoria asignada para contener el valor devuelto.
  
Los parámetros _pxAsyncHandle_ y _pxFunctionResult_ también pueden ser de tipo **xltypeMulti** cuando se usa para devolver una matriz de identificadores y los valores correspondientes en una devolución de llamada único. Cuando se utiliza una devolución de llamada única, pase una LPXLOPER12 que apunta al XLOPER12 estructuras que contienen uno dimensionales matrices que contienen los controladores asincrónicos y valores devuelven. Estas matrices deben estar en el mismo orden para Excel para que coincidan correctamente con un controlador asincrónico con su valor correspondiente. 
  
En el ejemplo siguiente se muestra cómo puede hacer que un lote de llamar con **xlAsyncReturn**.
  
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

## <a name="see-also"></a>Vea también

- [Funciones asincrónicas definidas por el usuario](asynchronous-user-defined-functions.md)

