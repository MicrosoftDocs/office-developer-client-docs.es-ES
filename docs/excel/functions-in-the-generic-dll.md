---
title: Funciones de la DLL genérica
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- DLL genérica [Excel 2007], funciones, funciones [Excel 2007], DLL genérica
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
  
La carpeta `\EXAMPLES\GENERIC\` contiene los archivos de proyecto de Microsoft Visual Studio y los archivos de código fuente necesarios para compilar la dll genérica de ejemplo. XLL. Puede usar este proyecto como una plantilla para escribir sus propios XLL de Microsoft Excel. El código fuente de este proyecto muestra muchas de las características de la API de C de Excel. 
  
Cuando se carga GENERIC. XLL, se crea un nuevo menú **genérico** con cuatro comandos: 
  
- **Dialog** -muestra un cuadro de diálogo de Microsoft Excel. 
    
- **Baile** : mueve la selección hasta que presione la tecla **ESC** . 
    
- Cuadro de diálogo **nativo** : muestra un cuadro de diálogo de Windows. 
    
- **Exit** -descarga Generic. XLL y quita el menú **genérico** . 
    
GENERIC. XLL también proporciona tres funciones de hoja de cálculo, Func1, FuncSum y FuncFib, que se pueden usar siempre que se cargue GENERIC. XLL. GENERIC. XLL se puede cargar mediante el administrador de complementos o se carga si estaba activo en el final normal de la última sesión de Excel.
  
Este proyecto usa la biblioteca de marcos (FRMWRK32. lib).
  
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
  
## <a name="see-also"></a>Ver también



[Funciones de la biblioteca de marcos](functions-in-the-framework-library.md)

