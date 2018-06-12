---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- xlsheetid (función) [excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e4e184d4e456ffe26292fe31b1b41463834216f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815743"
---
# <a name="xlsheetid"></a>xlSheetId

**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Busca el identificador de hoja de una hoja con nombre con el fin de construir las referencias externas.
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a>Sintaxis

_pxSheetName_ (**xltypeStr**)
  
(Opcional). El nombre de la libreta de direcciones y la hoja que desea averiguar sobre. Si se omite, la función **xlSheetId** devuelve el identificador de hoja de la hoja activa (frontal). 
  
## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de hoja en _pxRes -\>val.mref.idSheet_. 
  
> [!NOTE]
> El _pxRes -\>val.mref.lpmref_ puntero de matriz se establece en NULL después de esta llamada para que no es necesario llamar a **xlFree** para liberar la memoria que normalmente contiene este tipo, aunque es completamente seguro hacerlo. 
  
## <a name="remarks"></a>Notas

El libro que contiene la hoja especificada debe estar abierto para poder utilizar esta función. No hay ninguna forma para construir una referencia a un libro sin abrir desde un archivo DLL. Para obtener más información acerca del uso de **xlSheetId** para construir referencias, vea [Administración de memoria en Excel](memory-management-in-excel.md) para obtener ejemplos de construcción de **xltypeRef** . 
  
## <a name="example"></a>Ejemplo

 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetIdExample(void)
{       
   XLOPER12 xSheetName, xRes;
   xSheetName.xltype = xltypeStr;
   xSheetName.val.str = L"\022[BOOK1.XLSX]Sheet1";
   Excel12(xlSheetId, &xRes, 1, (LPXLOPER12)&xSheetName);
   Excel12f(xlcAlert, 0, 1, TempNum12(xRes.val.mref.idSheet));
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Vea también

- [xlSheetNm](xlsheetnm.md)
- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

