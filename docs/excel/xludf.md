---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- función xludf [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 569334847c7612b86f6ddc967f159e2ef425cbbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430647"
---
# <a name="xludf"></a>xlUDF

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llama a una función definida por el usuario (UDF). Esta función permite que un DLL llame a funciones definidas por el usuario de Visual Basic para Aplicaciones (VBA), funciones de lenguaje de macros XLM y funciones registradas contenidas en otros complementos.
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a>Parameters

_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** o **xltypeNum**)
  
Referencia de la función a la que desea llamar. Puede ser una referencia de celda de hoja de macros, el nombre registrado de la función como una cadena o el identificador de registro de la función. Para las funciones de complemento XLL registradas mediante **xlfRegister** o **REGISTER** con el argumento  _pxFunctionText_ proporcionado, el identificador se puede obtener mediante **xlfEvaluate** para buscar el nombre. 
  
_pxArg1, ..._
  
Cero o más argumentos para la función definida por el usuario. Cuando se llama a esta función en versiones anteriores a Excel 2007, el número máximo de argumentos adicionales que se pueden pasar es 29, que es 30, incluido _pxFnRef_. A partir Excel 2007, este límite se eleva a 254, que es 255, incluido _pxFnRef_.
  
## <a name="return-value"></a>Valor devuelto

Devuelve el valor que devuelva la función definida por el usuario.
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo se **ejecuta TestMacro** en la hoja Macro1 en BOOK1.XLS. Asegúrese de que la macro se encuentra en una hoja denominada Macro1. 
  
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

