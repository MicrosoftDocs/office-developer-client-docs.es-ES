---
title: Permitir interrupciones de usuario en operaciones largas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- función xlabort [excel 2007],tareas simultáneas [Excel 2007],saltos de usuario [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 650af14e4e97ebd2642a4442a87965f313d3b556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414693"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a>Permitir interrupciones de usuario en operaciones largas

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Aunque Windows usa la multitarea preventiva, donde las funciones o comandos pueden tardar mucho tiempo en ejecutarse, es una buena práctica ceder un poco de tiempo al sistema operativo de vez en cuando para ayudarle a programar tareas simultáneas. Si usa llamadas Windows nativas, puede hacerlo mediante la función de suspensión. Con la API de C, puede hacerlo mediante la función [xlAbort](xlabort.md), que no solo produce el procesador durante un instante, sino que también comprueba si el usuario ha presionado la tecla de cancelación, **ESC**.
  
Por lo tanto, la función **xlAbort** permite al código comprobar si el usuario desea finalizar el proceso, realizar la limpieza necesaria y, a continuación, devolver el control a Excel. La función también permite borrar la condición de interrupción. Esto permite que los comandos muestren un cuadro de diálogo para comprobar si el usuario desea finalizar el comando. Si el usuario no desea finalizar el comando, al llamar a la función **xlAbort** con el argumento  *FALSE*  se borra el salto. (El argumento predeterminado es  *TRUE*  , que simplemente comprueba la condición, pero no la borra). 
  
Puede llamar a la **función xlAbort** desde una función definida por el usuario (UDF) o desde un comando XLL. En una UDF, cuando la función **xlAbort** devuelve **TRUE**, después de detectar un salto de usuario, normalmente se corta el cálculo de función y se devuelve algún valor para indicar que el cálculo no se completó, quizás un error o cero. No se borraría la condición de interrupción para que otras instancias de funciones largas que también comprueban esta condición también se rompan. Excel borra implícitamente esta condición cuando finaliza una actualización.
  
Al detectar una condición de interrupción en un comando, normalmente se borra la condición llamando de nuevo a la función **xlAbort** con el argumento **FALSE**, aunque Excel borra implícitamente esta condición cuando finaliza un comando.
  
## <a name="see-also"></a>Vea también



[Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Actualización multiproceso en Excel](multithreaded-recalculation-in-excel.md)
  
[Desarrollar archivos XLL de Excel](developing-excel-xlls.md)
  
[Obtener acceso a la instancia de Excel y los controladores de la ventana principal](how-to-access-excel-instance-and-main-window-handles.md)

