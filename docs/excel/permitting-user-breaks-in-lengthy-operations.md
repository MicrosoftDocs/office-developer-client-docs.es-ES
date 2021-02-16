---
title: Permitir interrupciones de usuario en operaciones largas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Función xlabort [excel 2007],tareas simultáneas [Excel 2007],saltos de usuario [Excel 2007]
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
# <a name="permitting-user-breaks-in-lengthy-operations"></a><span data-ttu-id="8eca9-104">Permitir interrupciones de usuario en operaciones largas</span><span class="sxs-lookup"><span data-stu-id="8eca9-104">Permitting User Breaks in Lengthy Operations</span></span>

 <span data-ttu-id="8eca9-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8eca9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8eca9-106">Aunque Windows usa multitareas preferentes, donde las funciones o comandos pueden tardar mucho tiempo en ejecutarse, es una buena práctica producir un poco de tiempo en el sistema operativo de vez en cuando para ayudarle a programar tareas simultáneas.</span><span class="sxs-lookup"><span data-stu-id="8eca9-106">Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks.</span></span> <span data-ttu-id="8eca9-107">Con las llamadas nativas de Windows, puedes hacerlo mediante la función de suspensión.</span><span class="sxs-lookup"><span data-stu-id="8eca9-107">Using native Windows calls, you can do this by using the sleep function.</span></span> <span data-ttu-id="8eca9-108">Con la API de C, puede hacerlo mediante la función [xlAbort](xlabort.md), que no solo produce el procesador durante un instante, sino que también comprueba si el usuario ha presionado la tecla de cancelación, **ESC**.</span><span class="sxs-lookup"><span data-stu-id="8eca9-108">Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.</span></span>
  
<span data-ttu-id="8eca9-109">Por lo tanto, la función **xlAbort** permite al código comprobar si el usuario desea finalizar el proceso, realizar la limpieza necesaria y, a continuación, devolver el control a Excel.</span><span class="sxs-lookup"><span data-stu-id="8eca9-109">The **xlAbort** function therefore enables your code to check whether the user wants to end the process, do the necessary cleanup, and then return control to Excel.</span></span> <span data-ttu-id="8eca9-110">La función también permite borrar la condición de interrupción.</span><span class="sxs-lookup"><span data-stu-id="8eca9-110">The function also enables you to clear the break condition.</span></span> <span data-ttu-id="8eca9-111">Esto permite que los comandos muestren un cuadro de diálogo para comprobar si el usuario desea finalizar el comando.</span><span class="sxs-lookup"><span data-stu-id="8eca9-111">This enables your commands to display a dialog box to verify whether the user wants to end the command.</span></span> <span data-ttu-id="8eca9-112">Si el usuario no desea finalizar el comando, al llamar a la función **xlAbort** con el argumento  *FALSE*  se borra el salto.</span><span class="sxs-lookup"><span data-stu-id="8eca9-112">If the user does not want to end the command, calling the **xlAbort** function with the argument  *FALSE*  clears the break.</span></span> <span data-ttu-id="8eca9-113">(El argumento predeterminado es  *TRUE*  , que simplemente comprueba la condición pero no la borra).</span><span class="sxs-lookup"><span data-stu-id="8eca9-113">(The default argument is  *TRUE*  , which simply checks the condition but does not clear it.)</span></span> 
  
<span data-ttu-id="8eca9-114">Puede llamar a la **función xlAbort** desde una función definida por el usuario (UDF) o desde un comando XLL.</span><span class="sxs-lookup"><span data-stu-id="8eca9-114">You can call the **xlAbort** function from a user-defined function (UDF) or from an XLL command.</span></span> <span data-ttu-id="8eca9-115">En una UDF, cuando la función **xlAbort** devuelve **TRUE**, después de haber detectado un salto de usuario, normalmente cortaría el cálculo de la función y devolvería algún valor para indicar que el cálculo no se completó, quizás un error o cero.</span><span class="sxs-lookup"><span data-stu-id="8eca9-115">In a UDF, when the **xlAbort** function returns **TRUE**, having detected a user break, you would typically cut short the function calculation and return some value to indicate that the calculation was not completed, perhaps an error or zero.</span></span> <span data-ttu-id="8eca9-116">No borraría la condición de interrupción para que otras instancias de funciones largas que también comprueben esta condición también se rompan.</span><span class="sxs-lookup"><span data-stu-id="8eca9-116">You would not clear the break condition so that other instances of lengthy functions that also check this condition also break.</span></span> <span data-ttu-id="8eca9-117">Excel borra implícitamente esta condición cuando finaliza una actualización.</span><span class="sxs-lookup"><span data-stu-id="8eca9-117">Excel implicitly clears this condition when a recalculation ends.</span></span>
  
<span data-ttu-id="8eca9-118">Cuando se detecta una condición de interrupción en un comando, normalmente se borra la condición llamando de nuevo a la función **xlAbort** con el argumento **FALSE**, aunque Excel borra implícitamente esta condición cuando finaliza un comando.</span><span class="sxs-lookup"><span data-stu-id="8eca9-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8eca9-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8eca9-119">See also</span></span>



[<span data-ttu-id="8eca9-120">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="8eca9-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="8eca9-121">Actualización multiproceso en Excel</span><span class="sxs-lookup"><span data-stu-id="8eca9-121">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="8eca9-122">Desarrollar archivos XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="8eca9-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="8eca9-123">Obtener acceso a la instancia de Excel y los controladores de la ventana principal</span><span class="sxs-lookup"><span data-stu-id="8eca9-123">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)

