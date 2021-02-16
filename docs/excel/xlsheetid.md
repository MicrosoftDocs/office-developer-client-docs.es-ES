---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- función xlsheetid [excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a2ca1bb478c5c985ad7032e30ed0cfe3aef31406
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428434"
---
# <a name="xlsheetid"></a>xlSheetId

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Busca el identificador de hoja de una hoja con nombre para crear referencias externas.
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a>Parámetros

_pxSheetName_ (**xltypeStr**)
  
(Opcional). Nombre del libro y la hoja que desea averiguar. Si se omite, la **función xlSheetId** devuelve el identificador de hoja de la hoja activa (frontal). 
  
## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de hoja  _en pxRes- \> val.mref.idSheet_. 
  
> [!NOTE]
> El puntero de matriz  _pxRes- \> val.mref.lpmref_ se establece en NULL después de esta llamada para que no sea necesario llamar **a xlFree** para liberar la memoria que contiene normalmente este tipo, aunque es completamente seguro hacerlo. 
  
## <a name="remarks"></a>Comentarios

El libro que contiene la hoja especificada debe estar abierto para usar esta función. No hay ninguna forma de construir una referencia a un libro sin abrir desde una DLL. Para obtener más información acerca del **uso de xlSheetId** para crear referencias, vea Administración de memoria en [Excel](memory-management-in-excel.md) para obtener ejemplos de **construcción xltypeRef.** 
  
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

