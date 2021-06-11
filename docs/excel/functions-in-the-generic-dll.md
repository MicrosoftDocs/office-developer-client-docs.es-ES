---
title: Funciones de la DLL genérica
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- dll genérica [excel 2007], functions,functions [Excel 2007], DLL genérica
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3064e1a09ad8850e121da678f3702a6236574599
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420601"
---
# <a name="functions-in-the-generic-dll"></a>Funciones de la DLL genérica

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
La carpeta contiene Microsoft Visual Studio archivos de proyecto y archivos de código fuente necesarios para `\EXAMPLES\GENERIC\` compilar el ejemplo DLL GENERIC.xll. Puede usar este proyecto como plantilla para escribir sus propios Microsoft Excel XLLs. El código fuente de este proyecto muestra muchas de las características de la API Excel C. 
  
Al cargar GENERIC.xll, se crea un nuevo **menú Genérico** con cuatro comandos: 
  
- **Cuadro** de diálogo: muestra Microsoft Excel cuadro de diálogo. 
    
- **Baile:** mueve la selección hasta que presiona la **tecla ESC.** 
    
- **Cuadro de diálogo** nativo: muestra Windows cuadro de diálogo. 
    
- **Exit:** descarga GENERIC.xll y quita el **menú Genérico.** 
    
GENERIC.xll también proporciona tres funciones de hoja de cálculo, Func1, FuncSum y FuncFib, que se pueden usar siempre que se cargue GENERIC.xll. GENERIC.xll se puede cargar con el Administrador de complementos o se carga si estaba activo al final normal de la última Excel sesión.
  
Este proyecto usa la biblioteca de marcos (FRMWRK32.lib).
  
## <a name="in-this-section"></a>En esta sección

[DIALOGMsgProc](dialogmsgproc.md)
  
[ExcelCursorProc](excelcursorproc.md)
  
[HookExcelWindow](hookexcelwindow.md)
  
[UnhookExcelWindow](unhookexcelwindow.md)
  
[fShowDialog](fshowdialog.md)
  
[fDance](fdance.md)
  
[fDialog/fDialog12](fdialog-fdialog12.md)
  
[fExit](fexit.md)
  
[Func1](func1.md)
  
[FuncSum](funcsum.md)
  
[FuncFib](funcfib.md)
  
## <a name="see-also"></a>Vea también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

