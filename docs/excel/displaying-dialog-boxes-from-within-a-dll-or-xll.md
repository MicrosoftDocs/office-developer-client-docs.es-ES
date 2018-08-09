---
title: Mostrar cuadros de diálogo de un DLL o XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLL [excel 2007], mostrar cuadros de diálogo de cuadros de diálogo [Excel 2007], mostrar desde una DLL o XLL, archivos DLL [Excel 2007], mostrar cuadros de diálogo de
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: afb21125bc54a2607a997c7b2f7c73ef2f528f28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815536"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>Mostrar cuadros de diálogo de un DLL o XLL

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Para mostrar un cuadro de diálogo de Win32, por ejemplo, mediante la función de Windows SDK **DialogBox**, primero debe obtener la instancia completa de 32 bits y los identificadores de ventana principal de Excel. Para obtener más información, vea [acceso instancia de Excel y los identificadores de ventana principal](how-to-access-excel-instance-and-main-window-handles.md). 
  
Suponiendo que el proyecto contiene el recurso de cuadro de diálogo, debe seguir varios pasos para establecer la rutina de tratamiento de mensajes en los el cuadro de diálogo mostrado recientemente y para restaurar el mensaje Excel rutina de control cuando se cierra el cuadro de diálogo. El comando de ejemplo [fShowDialog](fshowdialog.md) en el proyecto genérico, se muestra el uso de las funciones de Windows para hacer esto correctamente. 
  
También puede mostrar cuadros de diálogo mediante la API de C sin tener que usar funciones del SDK de Windows. Sin embargo, las capacidades de cuadro de diálogo de la API de C son muy limitadas en comparación con los de Windows, Visual Basic para aplicaciones (VBA) o Microsoft Foundation Classes (MFC). (Por ejemplo, cuadros de diálogo de la API de C son siempre modales).
  
## <a name="see-also"></a>Vea también



[Crear XLL](creating-xlls.md)
  
[Desarrollar DLL](developing-dlls.md)
  
[Obtener acceso a la instancia de Excel y los controladores de la ventana principal](how-to-access-excel-instance-and-main-window-handles.md)
  
[Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

