---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- función xlcoerce [Excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d84839535d5eb913ca8a62d631238e3330683d0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424836"
---
# <a name="xlcoerce"></a>xlCoerce

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Convierte un tipo de **XLOPER**/ **XLOPER12** a otro o busca valores de celda en una hoja. 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a>Parameters

 _pxSource_
  
El **XLOPER XLOPER**/ de origen**XLOPER12** que debe convertirse. 
  
 _pxDestType_ (**xltypeInt**)
  
(Opcional). Una máscara de bits de los tipos resultantes que desea aceptar. Debe usar el operador bit **** a bit or (|) para especificar varios tipos posibles. Si se omite este argumento, las referencias a celdas individuales se convierten en uno de los tipos de valor **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (si la celda a la que se hace referencia está vacía) y las referencias a bloques de celdas se convierten en **xltypeMulti**. Esto hace que **xlCoerce** sea la forma más cómoda de buscar valores de celda. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Devuelve el valor convertido (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**o **xltypeMulti**).
  
## <a name="remarks"></a>Comentarios

 **xlCoerce** no se puede convertir a o desde **xltypeBigData** o **xltypeFlow**. Pasar un tipo **xltypeMissing** o **xltypeNil** como _pxDestType_ equivale a omitir el argumento. En algunos casos, se puede producir un error en la conversión. Por ejemplo, algunas cadenas no se pueden convertir en números, mientras que otras pueden. 
  
Si una matriz o una referencia de varias celdas se convierte en un tipo de valor único, el resultado es el valor de la celda superior izquierda o elemento de matriz.
  
## <a name="example"></a>Ejemplo

El siguiente código se puede encontrar en `\SAMPLES\EXAMPLE\EXAMPLE.C`. 
  
> [!NOTE]
> La función **xlcAlert** intenta convertir implícitamente su argumento en una cadena para que el paso de coerción que se muestra aquí se pudiera quitar de hecho, y **xInt** podría pasarse directamente a **xlcAlert**. Como **xlcAlert** es una macro de comando, este código sólo funciona correctamente cuando se llama desde una hoja de macros. 
  
```cs
short WINAPI xlCoerceExample(short iVal)
{
   XLOPER12 xStr, xInt, xDestType;
   xInt.xltype = xltypeInt;
   xInt.val.w = iVal;
   xDestType.xltype = xltypeInt;
   xDestType.val.w = xltypeStr;
   Excel12f(xlCoerce, &xStr, 2, (LPXLOPER12)&xInt, (LPXLOPER12)&xDestType);
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xStr);
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xStr);
   return 1;
}
```

## <a name="see-also"></a>Ver también



[xlSet](xlset.md)


[Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

