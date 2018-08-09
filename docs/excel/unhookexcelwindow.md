---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- unhookexcelwindow (función)
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7b70bf4ed0ff45921df407605baa692c7621bca4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815713"
---
# <a name="unhookexcelwindow"></a>UnhookExcelWindow

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Quita el **ExcelCursorProc** que se había instalado por **HookExcelWindow**. Esto habría se ha realizado el modo en que se llamó a **ExcelCursorProc** antes de la principal de Microsoft Excel **WndProc**.
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parámetros

 _hWndExcel_ (**Controlar**)
  
El identificador de Windows principal de Excel.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La función no devuelve un valor.
  
## <a name="remarks"></a>Comentarios

Esta función restaura el valor predeterminado de Excel **WndProc** con **SetWindowLong()** para restaurar la dirección que se guardó por **HookExcelWindow()**.
  
### <a name="example"></a>Ejemplo

Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones de la DLL genérica](functions-in-the-generic-dll.md)

