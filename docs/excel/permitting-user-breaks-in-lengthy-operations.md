---
title: Permitir los saltos de usuario en operaciones largas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- función xlAbort [Excel 2007], tareas simultáneas [Excel 2007], saltos de usuario [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 650af14e4e97ebd2642a4442a87965f313d3b556
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310384"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a>Permitir los saltos de usuario en operaciones largas

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Aunque Windows usa la multitarea preferente, donde las funciones o los comandos pueden tardar mucho tiempo en ejecutarse, se recomienda dar tiempo al sistema operativo ahora y de nuevo para ayudar a programar las tareas simultáneas. Mediante el uso de llamadas nativas de Windows, puede hacerlo con la función SLEEP. Con la API de C, puede hacerlo con la [función xlAbort](xlabort.md), que no solo proporciona el procesador de forma instantánea, sino que también comprueba si el usuario ha presionado la tecla cancelar, **ESC**.
  
Por lo tanto, la función **xlAbort** permite al código comprobar si el usuario desea finalizar el proceso, realizar la limpieza necesaria y, a continuación, devolver el control a Excel. La función también permite borrar la condición de interrupción. Esto permite que los comandos muestren un cuadro de diálogo para comprobar si el usuario desea finalizar el comando. Si el usuario no desea finalizar el comando, al llamar a la función **xlAbort** con el argumento *false* , se borra el salto. (El argumento predeterminado es *true* , que simplemente comprueba la condición pero no la borra). 
  
Puede llamar a la función **xlAbort** desde una función definida por el usuario (UDF) o desde un comando XLL. En un archivo UDF, cuando la función **xlAbort** devuelve **true**, detectando un salto de usuario, normalmente se corta el cálculo de la función y devuelve algún valor para indicar que no se completó el cálculo, por ejemplo, un error o cero. No se borrará la condición de interrupción, por lo que también se interrumpirán otras instancias de funciones largas que también comprueban esta condición. Excel borra implícitamente esta condición cuando finaliza un nuevo cálculo.
  
Cuando se detecta una condición de salto en un comando, normalmente se borra la condición al llamar de nuevo a la función **xlAbort** con el argumento **false**, si bien Excel implícitamente borra esta condición cuando finaliza un comando.
  
## <a name="see-also"></a>Vea también



[Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Actualización multiproceso en Excel](multithreaded-recalculation-in-excel.md)
  
[Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)
  
[Obtener acceso a la instancia de Excel y los controladores de la ventana principal](how-to-access-excel-instance-and-main-window-handles.md)

