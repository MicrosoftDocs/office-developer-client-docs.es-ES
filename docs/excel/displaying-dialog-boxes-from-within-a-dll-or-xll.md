---
title: Mostrar cuadros de diálogo desde una DLL o XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLL [Excel 2007], Mostrar cuadros de diálogo de, cuadros de diálogo [Excel 2007], mostrar desde una DLL o XLL, dll [Excel 2007], Mostrar cuadros de diálogo de
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7b00430b047fe792afef701d210ccde06dd16216
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417871"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>Mostrar cuadros de diálogo desde una DLL o XLL

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Para mostrar un cuadro de diálogo Win32 mediante, por ejemplo, la función **DialogBox**de Windows SDK, primero debe obtener la instancia completa de 32 bits y los identificadores de la ventana principal de Excel. Para obtener más información, consulte identificadores de [instancia de Excel y ventana principal](how-to-access-excel-instance-and-main-window-handles.md). 
  
SuPoniendo que el proyecto contiene el recurso de cuadro de diálogo, debe realizar varios pasos para establecer la rutina de tratamiento de mensajes en el cuadro de diálogo que se acaba de mostrar y restaurar la rutina de tratamiento de mensajes de Excel cuando se cierra el cuadro de diálogo. El comando de ejemplo [fShowDialog](fshowdialog.md) en el proyecto genérico demuestra el uso de las funciones de Windows para hacer esto correctamente. 
  
También puede mostrar cuadros de diálogo mediante la API de C sin tener que usar funciones de Windows SDK. Sin embargo, las funciones de cuadro de diálogo de la API de C son muy limitadas en comparación con las de Windows, Visual Basic para aplicaciones (VBA) o Microsoft Foundation Classes (MFC). (Por ejemplo, los cuadros de diálogo de la API de C siempre son modales).
  
## <a name="see-also"></a>Vea también



[Crear XLL](creating-xlls.md)
  
[Desarrollar DLL](developing-dlls.md)
  
[Obtener acceso a la instancia de Excel y los controladores de la ventana principal](how-to-access-excel-instance-and-main-window-handles.md)
  
[Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

