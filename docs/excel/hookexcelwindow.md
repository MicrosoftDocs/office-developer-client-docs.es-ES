---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- hookexcelwindow (función) [excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8965cc6b1e3d24001c42744f2ee7d447aa4c79b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815645"
---
# <a name="hookexcelwindow"></a>HookExcelWindow

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Instala **ExcelCursorProc** para que se le llama antes de la principal de Microsoft Excel **WndProc**.
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parámetros

 _hWndExcel_ (**Controlar**)
  
El identificador de Windows principal de Excel.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La función no devuelve un valor.
  
## <a name="remarks"></a>Comentarios

La función obtiene la dirección de Excel **WndProc** mediante el uso de **GetWindowLong()**. Este valor almacena en global que se puede usar el valor predeterminado **WndProc** de llamadas y restaurarlo. Por último, esta dirección reemplaza con la dirección de **ExcelCursorProc** con **SetWindowLong()**.
  
### <a name="example"></a>Ejemplo

Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones de la DLL genérica](functions-in-the-generic-dll.md)

