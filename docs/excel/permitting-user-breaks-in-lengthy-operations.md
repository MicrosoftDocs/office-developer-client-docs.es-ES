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
# <a name="permitting-user-breaks-in-lengthy-operations"></a><span data-ttu-id="ac2cc-104">Permitir interrupciones de usuarios en operaciones largas</span><span class="sxs-lookup"><span data-stu-id="ac2cc-104">Permitting User Breaks in Lengthy Operations</span></span>

 <span data-ttu-id="ac2cc-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ac2cc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ac2cc-106">Aunque Windows utiliza multitarea preferente, donde sus funciones o comandos pueden tardar mucho tiempo en ejecutarse, es aconsejable producir algún tiempo en el sistema operativo ahora y otra vez para ayudarle a programar tareas simultáneas.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-106">Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks.</span></span> <span data-ttu-id="ac2cc-107">Uso de las llamadas nativas de Windows, puede hacerlo mediante el uso de la función de suspensión.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-107">Using native Windows calls, you can do this by using the sleep function.</span></span> <span data-ttu-id="ac2cc-108">Uso de la API de C, puede hacerlo mediante el uso de la [función xlAbort](xlabort.md), que no sólo proporciona el procesador para una instantánea, pero también comprueba si el usuario ha presionado la tecla Cancelar, **ESC**.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-108">Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.</span></span>
  
<span data-ttu-id="ac2cc-109">Por lo tanto, la función **xlAbort** permite su código para comprobar si el usuario desea finalizar el proceso, hacer la limpieza necesaria y, a continuación, devolver el control a Excel.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-109">The **xlAbort** function therefore enables your code to check whether the user wants to end the process, do the necessary cleanup, and then return control to Excel.</span></span> <span data-ttu-id="ac2cc-110">La función también permite borrar la condición de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-110">The function also enables you to clear the break condition.</span></span> <span data-ttu-id="ac2cc-111">Esto permite que los comandos mostrar un cuadro de diálogo para comprobar si el usuario desea finalizar el comando.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-111">This enables your commands to display a dialog box to verify whether the user wants to end the command.</span></span> <span data-ttu-id="ac2cc-112">Si no desea que el usuario finalizar el comando, llamar a la función **xlAbort** con el argumento *FALSE* borra el salto.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-112">If the user does not want to end the command, calling the **xlAbort** function with the argument  *FALSE*  clears the break.</span></span> <span data-ttu-id="ac2cc-113">(El argumento predeterminado es *TRUE* , que simplemente se comprueba la condición pero la desactive.)</span><span class="sxs-lookup"><span data-stu-id="ac2cc-113">(The default argument is  *TRUE*  , which simply checks the condition but does not clear it.)</span></span> 
  
<span data-ttu-id="ac2cc-114">Puede llamar a la función **xlAbort** desde una función definida por el usuario (UDF) o desde un comando XLL.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-114">You can call the **xlAbort** function from a user-defined function (UDF) or from an XLL command.</span></span> <span data-ttu-id="ac2cc-115">En un archivo UDF, cuando la función **xlAbort** devuelve **TRUE**, tener detecta un salto de usuario, haría normalmente Cortar corta el cálculo de la función y devolver algún valor para indicar que el cálculo no se ha completado, quizás un error o un valor cero.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-115">In a UDF, when the **xlAbort** function returns **TRUE**, having detected a user break, you would typically cut short the function calculation and return some value to indicate that the calculation was not completed, perhaps an error or zero.</span></span> <span data-ttu-id="ac2cc-116">No desactive la condición de interrupción para que otras instancias de funciones prolongadas que también comprobación esta condición también de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-116">You would not clear the break condition so that other instances of lengthy functions that also check this condition also break.</span></span> <span data-ttu-id="ac2cc-117">Excel borra implícitamente esta condición cuando finaliza la actualización.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-117">Excel implicitly clears this condition when a recalculation ends.</span></span>
  
<span data-ttu-id="ac2cc-118">Cuando se detecta una condición de interrupción en un comando, normalmente, desactive la condición mediante una llamada a la función **xlAbort** nuevo con el argumento **es FALSE**, aunque Excel borra implícitamente esta condición cuando finaliza un comando.</span><span class="sxs-lookup"><span data-stu-id="ac2cc-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ac2cc-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac2cc-119">See also</span></span>



[<span data-ttu-id="ac2cc-120">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="ac2cc-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="ac2cc-121">Actualización multiproceso en Excel</span><span class="sxs-lookup"><span data-stu-id="ac2cc-121">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="ac2cc-122">Desarrollo de XLL de Excel de 2013</span><span class="sxs-lookup"><span data-stu-id="ac2cc-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="ac2cc-123">Obtener acceso a la instancia de Excel y los controladores de la ventana principal</span><span class="sxs-lookup"><span data-stu-id="ac2cc-123">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)

