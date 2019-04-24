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
# <a name="permitting-user-breaks-in-lengthy-operations"></a><span data-ttu-id="40dd9-104">Permitir los saltos de usuario en operaciones largas</span><span class="sxs-lookup"><span data-stu-id="40dd9-104">Permitting User Breaks in Lengthy Operations</span></span>

 <span data-ttu-id="40dd9-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="40dd9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="40dd9-106">Aunque Windows usa la multitarea preferente, donde las funciones o los comandos pueden tardar mucho tiempo en ejecutarse, se recomienda dar tiempo al sistema operativo ahora y de nuevo para ayudar a programar las tareas simultáneas.</span><span class="sxs-lookup"><span data-stu-id="40dd9-106">Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks.</span></span> <span data-ttu-id="40dd9-107">Mediante el uso de llamadas nativas de Windows, puede hacerlo con la función SLEEP.</span><span class="sxs-lookup"><span data-stu-id="40dd9-107">Using native Windows calls, you can do this by using the sleep function.</span></span> <span data-ttu-id="40dd9-108">Con la API de C, puede hacerlo con la [función xlAbort](xlabort.md), que no solo proporciona el procesador de forma instantánea, sino que también comprueba si el usuario ha presionado la tecla cancelar, **ESC**.</span><span class="sxs-lookup"><span data-stu-id="40dd9-108">Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.</span></span>
  
<span data-ttu-id="40dd9-109">Por lo tanto, la función **xlAbort** permite al código comprobar si el usuario desea finalizar el proceso, realizar la limpieza necesaria y, a continuación, devolver el control a Excel.</span><span class="sxs-lookup"><span data-stu-id="40dd9-109">The **xlAbort** function therefore enables your code to check whether the user wants to end the process, do the necessary cleanup, and then return control to Excel.</span></span> <span data-ttu-id="40dd9-110">La función también permite borrar la condición de interrupción.</span><span class="sxs-lookup"><span data-stu-id="40dd9-110">The function also enables you to clear the break condition.</span></span> <span data-ttu-id="40dd9-111">Esto permite que los comandos muestren un cuadro de diálogo para comprobar si el usuario desea finalizar el comando.</span><span class="sxs-lookup"><span data-stu-id="40dd9-111">This enables your commands to display a dialog box to verify whether the user wants to end the command.</span></span> <span data-ttu-id="40dd9-112">Si el usuario no desea finalizar el comando, al llamar a la función **xlAbort** con el argumento *false* , se borra el salto.</span><span class="sxs-lookup"><span data-stu-id="40dd9-112">If the user does not want to end the command, calling the **xlAbort** function with the argument  *FALSE*  clears the break.</span></span> <span data-ttu-id="40dd9-113">(El argumento predeterminado es *true* , que simplemente comprueba la condición pero no la borra).</span><span class="sxs-lookup"><span data-stu-id="40dd9-113">(The default argument is  *TRUE*  , which simply checks the condition but does not clear it.)</span></span> 
  
<span data-ttu-id="40dd9-114">Puede llamar a la función **xlAbort** desde una función definida por el usuario (UDF) o desde un comando XLL.</span><span class="sxs-lookup"><span data-stu-id="40dd9-114">You can call the **xlAbort** function from a user-defined function (UDF) or from an XLL command.</span></span> <span data-ttu-id="40dd9-115">En un archivo UDF, cuando la función **xlAbort** devuelve **true**, detectando un salto de usuario, normalmente se corta el cálculo de la función y devuelve algún valor para indicar que no se completó el cálculo, por ejemplo, un error o cero.</span><span class="sxs-lookup"><span data-stu-id="40dd9-115">In a UDF, when the **xlAbort** function returns **TRUE**, having detected a user break, you would typically cut short the function calculation and return some value to indicate that the calculation was not completed, perhaps an error or zero.</span></span> <span data-ttu-id="40dd9-116">No se borrará la condición de interrupción, por lo que también se interrumpirán otras instancias de funciones largas que también comprueban esta condición.</span><span class="sxs-lookup"><span data-stu-id="40dd9-116">You would not clear the break condition so that other instances of lengthy functions that also check this condition also break.</span></span> <span data-ttu-id="40dd9-117">Excel borra implícitamente esta condición cuando finaliza un nuevo cálculo.</span><span class="sxs-lookup"><span data-stu-id="40dd9-117">Excel implicitly clears this condition when a recalculation ends.</span></span>
  
<span data-ttu-id="40dd9-118">Cuando se detecta una condición de salto en un comando, normalmente se borra la condición al llamar de nuevo a la función **xlAbort** con el argumento **false**, si bien Excel implícitamente borra esta condición cuando finaliza un comando.</span><span class="sxs-lookup"><span data-stu-id="40dd9-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="40dd9-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="40dd9-119">See also</span></span>



[<span data-ttu-id="40dd9-120">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="40dd9-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="40dd9-121">Actualización multiproceso en Excel</span><span class="sxs-lookup"><span data-stu-id="40dd9-121">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="40dd9-122">Desarrollo de XLL de Excel de 2013</span><span class="sxs-lookup"><span data-stu-id="40dd9-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="40dd9-123">Obtener acceso a la instancia de Excel y los controladores de la ventana principal</span><span class="sxs-lookup"><span data-stu-id="40dd9-123">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)

