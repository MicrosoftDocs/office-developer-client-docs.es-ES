---
title: Funciones en el archivo DLL genérica
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- dll genérico [excel 2007], funciones, funciones [Excel 2007], DLL genérica
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e78f276e58ca1c98786e28ed5167762cf0bfdf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815652"
---
# <a name="functions-in-the-generic-dll"></a>Funciones en el archivo DLL genérica

 **Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
La carpeta `\EXAMPLES\GENERIC\` contiene los archivos de proyecto de Microsoft Visual Studio y archivos de código fuente que se necesitan para compilar el ejemplo GENERIC.xll del archivo DLL. Puede usar este proyecto como una plantilla para escribir su propia XLL de Microsoft Excel. El código de origen de este proyecto muestra muchas de las características de la API de C de Excel. 
  
Cuando se carga GENERIC.xll, crea un nuevo menú **genérico** con cuatro comandos: 
  
- **Cuadro de diálogo** - muestra un cuadro de diálogo de Microsoft Excel. 
    
- **Baile** - mueve la selección alrededor de hasta que se presione la tecla **ESC** . 
    
- **Cuadro de diálogo nativo** - muestra un cuadro de diálogo de Windows. 
    
- **Exit** - GENERIC.xll de descarga y se quita el menú **genérica** . 
    
GENERIC.xll también proporciona tres funciones de hoja de cálculo, Func1, FuncSum y FuncFib, que se puede utilizar siempre que se carga GENERIC.xll. GENERIC.xll se pueden cargar con el Administrador de complementos, o se carga si estaba activo al final de la última sesión de Excel normal.
  
Este proyecto usa la biblioteca de framework (FRMWRK32.lib).
  
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



[Funciones de la biblioteca de Framework](functions-in-the-framework-library.md)

