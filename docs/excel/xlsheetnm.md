---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- xlsheetnm (función) [excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 815565d886b1aea203f6b3b9774325d6b534abd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815753"
---
# <a name="xlsheetnm"></a>xlSheetNm

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve el nombre de una hoja de cálculo u hoja de macro de su identificador de hoja interna dentro de una referencia externa, o el nombre de la hoja actual si se pasa una referencia interna.
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a>Parámetros

_pxExtref_ (**xltypeRef** o **xltypeSRef**)
  
Una referencia a la hoja cuyo nombre desea.
  
Si se pasa una referencia externa (**xltypeRef**) necesario que sólo contenga el identificador de la hoja. Las estructuras de datos que describen las celdas en la hoja de cálculo se omiten y no es necesario que se debe proporcionar. Si el identificador se establece en cero, **xlSheetNm** devuelve el nombre de la hoja actual. 
  
Si se pasa una referencia interna (**xltypeSef**), **xlSheetNm** devuelve el nombre de la hoja actual. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Devuelve el nombre de la hoja (**xltypeStr**) en el formulario `[Book1]Sheet1`.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra el nombre de la hoja desde que se llamó a la función. La función funciona correctamente sólo si se llama a partir de una hoja de macros mientras se ejecuta una macro de comando XLM. Esto es debido a que se llama **xlcAlert**, que pueden hacer sólo comandos, y debe llamarse desde una hoja en lugar de un cuadro de diálogo, menú o la barra de comandos en orden para **xlfCaller** devolver una referencia. 
  
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

