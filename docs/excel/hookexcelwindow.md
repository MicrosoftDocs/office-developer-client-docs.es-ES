---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- Función hookexcelwindow [excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4103bf3a95388d20efeb74fcd736aeb5520d0845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413510"
---
# <a name="hookexcelwindow"></a>HookExcelWindow

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Instala **ExcelCursorProc para** que se llame antes del **WndProc principal de** Microsoft Excel.
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parámetros

 _hWndExcel_ (**HANDLE**)
  
El controlador principal de Windows de Excel.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La función no devuelve un valor.
  
## <a name="remarks"></a>Comentarios

La función obtiene la dirección de **WndProc** de Excel mediante el uso de **GetWindowLong()**. Almacena este valor en una global que se puede usar para llamar al **WndProc** predeterminado y también para restaurarlo. Por último, reemplaza esta dirección por la dirección de **ExcelCursorProc** mediante **SetWindowLong()**.
  
### <a name="example"></a>Ejemplo

Vea  `\SAMPLES\GENERIC\GENERIC.C` el código fuente de esta función. 
  
## <a name="see-also"></a>Consulte también



[Funciones en la DLL genérica](functions-in-the-generic-dll.md)

