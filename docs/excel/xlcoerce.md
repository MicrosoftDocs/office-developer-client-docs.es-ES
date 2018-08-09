---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- función xlCoerce [excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e0474b81a6d24663fe85303efc8fe2fd62cfdd82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815730"
---
# <a name="xlcoerce"></a>xlCoerce

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Convierte un tipo de **XLOPER**/ **XLOPER12** a otro, o tiene el mismo aspecto los valores de celda en una hoja. 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a>Parámetros

 _pxSource_
  
El origen de **XLOPER**/ **XLOPER12** que necesita que se va a convertir. 
  
 _pxDestType_ (**xltypeInt**)
  
(Opcional). Una máscara de bits de los tipos resultantes están dispuestos a Aceptar. Debe usar el operador **OR** bit a bit (|) para especificar varios tipos posibles. Si se omite este argumento, las referencias a celdas individuales se convierten en uno de los tipos de valor **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (si la celda a que se refiere a está vacía) y las referencias a los bloques de las celdas se convierten en **xltypeMulti**. Esto hace que **xlCoerce** la forma más conveniente para buscar valores de celda. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Devuelve el valor convertido (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**o **xltypeMulti**).
  
## <a name="remarks"></a>Comentarios

 no se puede convertir **xlCoerce** a o desde **xltypeBigData** o **xltypeFlow**. Pasar un tipo de **xltypeMissing** o **xltypeNil** como _pxDestType_ es equivalente a si se omite el argumento. Puede producirse un error de conversión en algunos casos. Por ejemplo, algunas cadenas no se puede convertir a números, mientras que otros usuarios puedan. 
  
Si una matriz o una referencia de celda múltiples se convierte en un tipo de valor único, el resultado es el valor de la superior izquierdo celda o elemento de matriz.
  
## <a name="example"></a>Ejemplo

El siguiente código puede encontrarse en `\SAMPLES\EXAMPLE\EXAMPLE.C`. 
  
> [!NOTE]
> La función **xlcAlert** implícitamente intenta convertir su argumento en una cadena de modo que en realidad se pudo quitar el paso de conversión que se muestra aquí y **xInt** se podía pasar directamente a **xlcAlert**. Como **xlcAlert** es una macro de comando, este código sólo funciona correctamente cuando se llame desde una hoja de macros. 
  
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

## <a name="see-also"></a>Vea también



[xlSet](xlset.md)


[Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

