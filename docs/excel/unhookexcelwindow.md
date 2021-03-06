---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- función unhookexcelwindow
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: aef2734aeb4d9cf5df33e3d012cef309e8a1eb6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409450"
---
# <a name="unhookexcelwindow"></a>UnhookExcelWindow

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Quita el **ExcelCursorProc** instalado anteriormente por **HookExcelWindow**. Esto se habría hecho para que se llamara **a ExcelCursorProc** antes de Microsoft Excel **WndProc principal**.
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parameters

 _hWndExcel_ (**HANDLE**)
  
El Excel controlador Windows principal.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La función no devuelve un valor.
  
## <a name="remarks"></a>Comentarios

Esta función restaura el Excel **WndProc** predeterminado mediante **SetWindowLong()** para restaurar la dirección guardada por **HookExcelWindow()**.
  
### <a name="example"></a>Ejemplo

Vea  `\SAMPLES\GENERIC\GENERIC.C` el código fuente de esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones en la DLL genérica](functions-in-the-generic-dll.md)

