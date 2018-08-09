---
title: Permitir interrupciones de usuarios en operaciones largas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- función xlAbort [excel 2007], [Excel 2007], de tareas simultáneas saltos de usuario [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: b13f9b9a8c0e5621b25df13537632bdbe5dfc29e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815689"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a>Permitir interrupciones de usuarios en operaciones largas

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Aunque Windows utiliza multitarea preferente, donde sus funciones o comandos pueden tardar mucho tiempo en ejecutarse, es aconsejable producir algún tiempo en el sistema operativo ahora y otra vez para ayudarle a programar tareas simultáneas. Uso de las llamadas nativas de Windows, puede hacerlo mediante el uso de la función de suspensión. Uso de la API de C, puede hacerlo mediante el uso de la [función xlAbort](xlabort.md), que no sólo proporciona el procesador para una instantánea, pero también comprueba si el usuario ha presionado la tecla Cancelar, **ESC**.
  
Por lo tanto, la función **xlAbort** permite su código para comprobar si el usuario desea finalizar el proceso, hacer la limpieza necesaria y, a continuación, devolver el control a Excel. La función también permite borrar la condición de interrupción. Esto permite que los comandos mostrar un cuadro de diálogo para comprobar si el usuario desea finalizar el comando. Si no desea que el usuario finalizar el comando, llamar a la función **xlAbort** con el argumento *FALSE* borra el salto. (El argumento predeterminado es *TRUE* , que simplemente se comprueba la condición pero la desactive.) 
  
Puede llamar a la función **xlAbort** desde una función definida por el usuario (UDF) o desde un comando XLL. En un archivo UDF, cuando la función **xlAbort** devuelve **TRUE**, tener detecta un salto de usuario, haría normalmente Cortar corta el cálculo de la función y devolver algún valor para indicar que el cálculo no se ha completado, quizás un error o un valor cero. No desactive la condición de interrupción para que otras instancias de funciones prolongadas que también comprobación esta condición también de interrupción. Excel borra implícitamente esta condición cuando finaliza la actualización.
  
Cuando se detecta una condición de interrupción en un comando, normalmente, desactive la condición mediante una llamada a la función **xlAbort** nuevo con el argumento **es FALSE**, aunque Excel borra implícitamente esta condición cuando finaliza un comando.
  
## <a name="see-also"></a>Vea también



[Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Actualización multiproceso en Excel](multithreaded-recalculation-in-excel.md)
  
[Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)
  
[Obtener acceso a la instancia de Excel y los controladores de la ventana principal](how-to-access-excel-instance-and-main-window-handles.md)

