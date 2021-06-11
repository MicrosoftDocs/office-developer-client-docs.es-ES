---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- función excelcursorproc [excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d3cc41487f0cae31e110249fe148f5370319a39a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432495"
---
# <a name="excelcursorproc"></a>ExcelCursorProc

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Cuando se muestra un cuadro de diálogo modal sobre la Microsoft Excel, el cursor es un cursor ocupado sobre la Excel ventana. Este **WndProc** captura WM_SETCURSOR tipo Windows mensajes y cambia el cursor de nuevo a una flecha normal. 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Parameters

 _hWndDlg_ (**HWND**)
  
Contiene el identificador de Windows HWND del cuadro de diálogo.
  
 _message_ (**UINT**)
  
Mensaje al que responder.
  
 _wParam_ (**WPARAM**)
  
 _lParam_ (**LPARAM**)
  
Argumentos pasados por Windows.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

LRESULT: 0 si se controló el mensaje, de lo contrario, el resultado devuelto por **WndProc predeterminado**.
  
### <a name="example"></a>Ejemplo

Vea  `\SAMPLES\GENERIC\GENERIC.C` el código fuente de esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones en la DLL genérica](functions-in-the-generic-dll.md)

