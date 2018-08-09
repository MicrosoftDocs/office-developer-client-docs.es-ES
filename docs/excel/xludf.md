---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- función xlUDF [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8f45f800ca50d2a46792e7cf5e00ac25bd099e8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815754"
---
# <a name="xludf"></a>xlUDF

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llama a una función definida por el usuario (UDF). Esta función permite una DLL para llamar a Visual Basic para las funciones definidas por el usuario de aplicaciones (VBA), funciones de lenguaje de macros XLM y registradas funciones contenida en otros complementos.
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a>Parámetros

_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** o **xltypeNum**)
  
La referencia de la función que desea llamar. Esto puede ser una referencia de celda de hoja de macros, el nombre registrado de la función como una cadena o el identificador de registro de la función. Para agregar en funciones XLL registradas con **xlfRegister** o **REGISTRE** con el argumento _pxFunctionText_ proporcionado, el identificador puede obtenerse mediante el uso de **xlfEvaluate** para buscar el nombre. 
  
_pxArg1..._
  
Cero o más argumentos para la función definida por el usuario. Cuando se está llamando a esta función de versiones anteriores a Excel 2007, el número máximo de argumentos adicionales que se pueden pasar es 29, que es 30 incluidos _pxFnRef_. Iniciar en Excel 2007, este límite se ha elevado a 254, que es de 255 incluidos _pxFnRef_.
  
## <a name="return-value"></a>Valor devuelto

Devuelve todo lo que el valor de la función definida por el usuario devuelta.
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo se ejecuta **TestMacro** en hoja Macro1 en Libro1. XLS. Asegúrese de que la macro está en una hoja denominada Macro1. 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlUDFExample(void)
{       
   XLOPER12 xMacroName, xMacroRef, xRes;
   xMacroName.xltype = xltypeStr;
   xMacroName.val.str = L"\044[BOOK1.XLSX]Macro1!TestMacro";
   Excel12(xlfEvaluate, &xMacroRef, 1, (LPXLOPER12)&xMacroName);
   Excel12(xlUDF, &xRes, 1, (LPXLOPER12)&xMacroRef);
   return 1;
}
```

## <a name="see-also"></a>Vea también

- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

