---
title: Mostrar cuadros de diálogo desde dentro de una DLL o XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlls [excel 2007], mostrar cuadros de diálogo de,cuadros de diálogo [Excel 2007], mostrar desde un DLL o XLL,DLL [Excel 2007], mostrar cuadros de diálogo de
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
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>Mostrar cuadros de diálogo desde dentro de una DLL o XLL

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Para mostrar un cuadro de diálogo de Win32 con, por ejemplo, la función **dialogBox** del SDK de Windows , primero debe obtener la instancia completa de 32 bits y los controladores de ventana principal para Excel. Para obtener más información, vea [Access Excel Instance y Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md). 
  
Suponiendo que el proyecto contiene el recurso de cuadro de diálogo, debe realizar varios pasos para establecer la rutina de control de mensajes en la del cuadro de diálogo recién mostrado y para restaurar la rutina de control de mensajes de Excel cuando se cierre el cuadro de diálogo. El comando [de ejemplo fShowDialog](fshowdialog.md) en el proyecto genérico muestra el uso de las funciones Windows para hacerlo correctamente. 
  
También puede mostrar cuadros de diálogo con la API de C sin tener que usar Windows SDK. Sin embargo, las capacidades de cuadro de diálogo de la API de C son muy limitadas en comparación con las de Windows, Visual Basic para Aplicaciones (VBA) o las clases de Microsoft Foundation (MFC). (Por ejemplo, los cuadros de diálogo de la API de C siempre son modales).
  
## <a name="see-also"></a>Vea también



[Crear XLL](creating-xlls.md)
  
[Desarrollar DLL](developing-dlls.md)
  
[Obtener acceso a la instancia de Excel y los controladores de la ventana principal](how-to-access-excel-instance-and-main-window-handles.md)
  
[Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

