---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- función xlsheetnm [Excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5d62be7ebef71547de3a903db4c1a030984b8640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303874"
---
# <a name="xlsheetnm"></a>xlSheetNm

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve el nombre de una hoja de cálculo o de una hoja de macros de su identificador de hoja interno incluido en una referencia externa, o el nombre de la hoja actual si se pasa una referencia interna.
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a>Parameters

_pxExtref_ (**xltypeRef** o **xltypeSRef**)
  
Una referencia a la hoja cuyo nombre desea.
  
Si va a pasar una referencia externa (**xltypeRef**), solo debe contener el identificador de la hoja. Las estructuras de datos que describen las celdas de la hoja de cálculo se omiten y no es necesario proporcionarlas. Si el identificador se establece en cero, **xlSheetNm** devuelve el nombre de la hoja actual. 
  
Si va a pasar una referencia interna (**xltypeSef**), **xlSheetNm** devuelve el nombre de la hoja actual. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Devuelve el nombre de la hoja (**xltypeStr**) en el formulario `[Book1]Sheet1`.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra el nombre de la hoja desde la que se llamó a la función. La función sólo funciona correctamente si se llama desde una hoja de macros mientras se ejecuta una macro de comando XLM. Esto se debe a que llama a **xlcAlert**, que solo pueden hacer los comandos y debe llamarse desde una hoja en lugar de un cuadro de diálogo, un menú o una barra de comandos para que **xlfCaller** devuelva una referencia. 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetNmExample(void)
{
   XLOPER12 xRes, xSheetName;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlSheetNm, &xSheetName, 1, (LPXLOPER12)&xRes);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xSheetName);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xSheetName);
   return 1;
}
```

## <a name="see-also"></a>Vea también

- [xlSheetId](xlsheetid.md)
- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

