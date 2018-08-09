---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- excelcursorproc (función) [excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 07be8da4a07b988d5e848048a088859b58ea3a14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815626"
---
# <a name="excelcursorproc"></a>ExcelCursorProc

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Cuando se muestra un cuadro de diálogo modal a través de la ventana de Microsoft Excel, el cursor es un cursor no disponible a través de la ventana de Excel. Este capturas **WndProc** WM_SETCURSOR escriba mensajes de Windows y los cambios que se copia el cursor a una flecha normal. 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Parámetros

 _hWndDlg_ (**HWND**)
  
Contiene el identificador de Windows de HWND del cuadro de diálogo.
  
 _mensaje_ (**UINT**)
  
El mensaje para responder a.
  
 _wParam_ (**WPARAM**)
  
 _lParam_ (**LPARAM**)
  
Argumentos que se pasan por parte de Windows.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

LRESULT: 0 si se ha controlado el mensaje, en caso contrario, el resultado devuelto por el valor predeterminado **WndProc**.
  
### <a name="example"></a>Ejemplo

Vea `\SAMPLES\GENERIC\GENERIC.C` para el código de origen para esta función. 
  
## <a name="see-also"></a>Vea también



[Funciones de la DLL genérica](functions-in-the-generic-dll.md)

