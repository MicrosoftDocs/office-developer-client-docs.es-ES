---
title: Obtener acceso a código XLL en Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- obtener acceso al código xll [excel 2007], XLL [Excel 2007], obtener acceso a código, comandos [Excel 2007], registro, funciones [Excel 2007], registro llamadas a XLL desde Excel, registrar comandos [Excel 2007], registrar funciones [Excel 2007]
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d1332b0dffc052404c75c4ec51d94879457c3da0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705284"
---
# <a name="accessing-xll-code-in-excel"></a><span data-ttu-id="1f99e-104">Obtener acceso a código XLL en Excel</span><span class="sxs-lookup"><span data-stu-id="1f99e-104">Accessing XLL code in Excel</span></span>

<span data-ttu-id="1f99e-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1f99e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1f99e-106">Para que sean accesibles en Microsoft Excel, las funciones y los comandos que contiene un XLL:</span><span class="sxs-lookup"><span data-stu-id="1f99e-106">To be accessible in Microsoft Excel, the functions and commands that an XLL contains:</span></span>
  
- <span data-ttu-id="1f99e-107">Las debe exportar el XLL.</span><span class="sxs-lookup"><span data-stu-id="1f99e-107">Must be exported by the XLL.</span></span>
    
- <span data-ttu-id="1f99e-108">Deben estar registradas con Excel.</span><span class="sxs-lookup"><span data-stu-id="1f99e-108">Must be registered with Excel.</span></span>
    
## <a name="registering-functions-and-commands-with-excel"></a><span data-ttu-id="1f99e-109">Registrar las funciones y comandos con Excel</span><span class="sxs-lookup"><span data-stu-id="1f99e-109">Registering functions and commands with Excel</span></span>

<span data-ttu-id="1f99e-110">El registro indica a Excel lo siguiente sobre un punto de entrada de la DLL:</span><span class="sxs-lookup"><span data-stu-id="1f99e-110">Registration tells Excel the following about a DLL entry point:</span></span>
  
- <span data-ttu-id="1f99e-111">Si está oculto o, si es una función, si está visible en el Asistente para funciones.</span><span class="sxs-lookup"><span data-stu-id="1f99e-111">Whether it is hidden or, if a function, whether it is visible in the Function Wizard.</span></span>
    
- <span data-ttu-id="1f99e-112">Si se puede llamar solo desde una hoja de macros XLM o también desde una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="1f99e-112">Whether it is callable only from an XLM macro sheet, or also from a worksheet.</span></span>
    
- <span data-ttu-id="1f99e-113">Si es un comando, si es una función de hoja de cálculo o una función equivalente de hoja de macros.</span><span class="sxs-lookup"><span data-stu-id="1f99e-113">If a command, whether it is a worksheet function or a macro sheet equivalent function.</span></span>
    
- <span data-ttu-id="1f99e-114">Cuál es el nombre de la exportación DLL o XLL y qué nombre desea que use Excel.</span><span class="sxs-lookup"><span data-stu-id="1f99e-114">What its XLL/DLL export name is, and what name you want Excel to use.</span></span>
    
- <span data-ttu-id="1f99e-115">Si es una función:</span><span class="sxs-lookup"><span data-stu-id="1f99e-115">If it is a function:</span></span>
    
  - <span data-ttu-id="1f99e-116">Qué tipos de datos devuelve y toma como argumentos.</span><span class="sxs-lookup"><span data-stu-id="1f99e-116">What data types it returns and takes as arguments.</span></span>
    
  - <span data-ttu-id="1f99e-117">Si devuelve el resultado modificando un argumento en su lugar.</span><span class="sxs-lookup"><span data-stu-id="1f99e-117">Whether it returns its result by modifying an argument in place.</span></span>
    
  - <span data-ttu-id="1f99e-118">Si es volátil.</span><span class="sxs-lookup"><span data-stu-id="1f99e-118">Whether it is volatile.</span></span>
    
  - <span data-ttu-id="1f99e-119">Si es seguro para subprocesos (compatible a partir de Excel 2007).</span><span class="sxs-lookup"><span data-stu-id="1f99e-119">Whether it is thread safe (supported starting in Excel 2007).</span></span>
    
  - <span data-ttu-id="1f99e-120">Qué texto deben mostrar el Asistente para funciones de pegado y el editor de Autocompletar para ayudar con la función de llamadas.</span><span class="sxs-lookup"><span data-stu-id="1f99e-120">What text the Paste Function Wizard and AutoComplete editor should display to help with calling the function.</span></span>
    
  - <span data-ttu-id="1f99e-121">La categoría de la función en la que se debe enumerar.</span><span class="sxs-lookup"><span data-stu-id="1f99e-121">Which function category it should be listed under.</span></span>
    
<span data-ttu-id="1f99e-122">Todo ello se consigue con la función de la API de C [xlfRegister](xlfregister-form-1.md), equivalente a la función XLM **REGISTER**.</span><span class="sxs-lookup"><span data-stu-id="1f99e-122">This is all achieved using the C API function [xlfRegister](xlfregister-form-1.md), equivalent to the XLM function **REGISTER**.</span></span>
  
## <a name="calling-xll-functions-directly-from-excel"></a><span data-ttu-id="1f99e-123">Llamadas a funciones XLL directamente desde Excel</span><span class="sxs-lookup"><span data-stu-id="1f99e-123">Calling XLL functions directly from Excel</span></span>

<span data-ttu-id="1f99e-124">Una vez que se han registrado, se puede llamar a las funciones de hoja de macros y la hoja de cálculo XLL desde cualquier lugar donde se pueda llamar a una función integrada:</span><span class="sxs-lookup"><span data-stu-id="1f99e-124">Once they are registered, XLL worksheet and macro sheet functions can be called from anywhere a built-in function can be called from:</span></span>
  
- <span data-ttu-id="1f99e-125">Una fórmula de matriz o de celda en una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="1f99e-125">A single-cell or array formula on a worksheet.</span></span>
    
- <span data-ttu-id="1f99e-126">Una fórmula de matriz o de celda en una hoja de macros.</span><span class="sxs-lookup"><span data-stu-id="1f99e-126">A single-cell or array formula on a macro sheet.</span></span>
    
- <span data-ttu-id="1f99e-127">La definición de un nombre definido.</span><span class="sxs-lookup"><span data-stu-id="1f99e-127">The definition of a defined name.</span></span>
    
- <span data-ttu-id="1f99e-128">Los campos de condición y de límite de un cuadro de diálogo con formato condicional.</span><span class="sxs-lookup"><span data-stu-id="1f99e-128">The condition and limit fields in a conditional format dialog box.</span></span>
    
- <span data-ttu-id="1f99e-129">Desde otro complemento a través de la función de la API de C [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="1f99e-129">From another add-in via the C API function [xlUDF](xludf.md).</span></span>
    
- <span data-ttu-id="1f99e-130">Desde Visual Basic para aplicaciones (VBA) a través del método **Application.Run**.</span><span class="sxs-lookup"><span data-stu-id="1f99e-130">From Visual Basic for Applications (VBA) via the **Application.Run** method.</span></span> 
    
<span data-ttu-id="1f99e-131">Puede obtener una referencia a la celda o rango de celdas de llamada dentro de su función con la función de la API de C **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="1f99e-131">You can obtain a reference to the calling cell or range of cells within your function using the C API function **xlfCaller**.</span></span> <span data-ttu-id="1f99e-132">Si se llama a la función desde la expresión de formato condicional de la celda, se sigue devolviendo una referencia a la celda o celdas asociadas, por lo que no puede suponer que la fórmula contiene la función XLL.</span><span class="sxs-lookup"><span data-stu-id="1f99e-132">If the function was called from the cell's conditional format expression, you are still returned a reference to the associated cell or cells, so you cannot assume that the cell's formula contains the XLL function.</span></span> <span data-ttu-id="1f99e-133">Si la función se invoca desde una función VBA definida por el usuario (UDF), **xlfCaller** devuelve de nuevo a la dirección de las celdas que llamaron a la función VBA.</span><span class="sxs-lookup"><span data-stu-id="1f99e-133">If your function was called from a VBA user-defined function (UDF), **xlfCaller** again returns the address of the cells that called the VBA function.</span></span> <span data-ttu-id="1f99e-134">Para obtener más información, vea [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="1f99e-134">For more information, see [DataValidationPrompt](xlfcaller.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="1f99e-135">Excel también llama al código de la función XLL de la **Asistente para funciones de pegado** y los cuadros de diálogo **Reemplazar**.</span><span class="sxs-lookup"><span data-stu-id="1f99e-135">Excel also calls XLL function code from the **Paste Function Wizard** and **Replace** dialog boxes.</span></span> <span data-ttu-id="1f99e-136">Es posible que deba restringir la ejecución habitual del código en el caso del cuadro de diálogo **Argumentos para funciones de pegado** especialmente cuando la función puede tardar mucho tiempo en ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="1f99e-136">You might need to restrict your code's normal running in the case of the **Paste Function Arguments** dialog box, especially where your function can take a long time to execute.</span></span> <span data-ttu-id="1f99e-137">Para detectar si se llama a la función desde uno de estos cuadros de diálogo, deberá implementar en su proyecto código que recorra todas las ventanas abiertas para determinar si la ventana frontal es uno de estos cuadros de diálogo y, si es así, cuál.</span><span class="sxs-lookup"><span data-stu-id="1f99e-137">To detect if your function is being called from either of these dialog boxes, you must implement some code in your project that iterates through all the open windows to determine if the front window is one of these dialog boxes, and, if so, which one.</span></span> 
  
## <a name="calling-xll-commands-directly-from-excel"></a><span data-ttu-id="1f99e-138">Llamar a los comandos XLL directamente desde Excel</span><span class="sxs-lookup"><span data-stu-id="1f99e-138">Calling DLL commands directly from Excel</span></span>

<span data-ttu-id="1f99e-139">Una vez que se han registrado, se puede llamar a los comandos XLL de las mismas formas que se puede llamar a otras macros definidas por el usuario:</span><span class="sxs-lookup"><span data-stu-id="1f99e-139">Once they are registered, XLL commands can be called in all the ways that other user-defined macros can be called:</span></span>
  
- <span data-ttu-id="1f99e-140">Si se asocia a un objeto de control incrustado en una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="1f99e-140">By being associated with a control object embedded on a worksheet.</span></span>
    
- <span data-ttu-id="1f99e-141">Desde el cuadro de diálogo Ejecutar macro.</span><span class="sxs-lookup"><span data-stu-id="1f99e-141">From the Run Macro dialog box.</span></span>
    
- <span data-ttu-id="1f99e-142">Desde una macro VBA definida por el usuario con el método **Application.Run**.</span><span class="sxs-lookup"><span data-stu-id="1f99e-142">From a VBA user-defined macro using the **Application.Run** method.</span></span> 
    
- <span data-ttu-id="1f99e-143">Desde un elemento de menú o barra de herramientas personalizados.</span><span class="sxs-lookup"><span data-stu-id="1f99e-143">From a customized menu item or toolbar.</span></span>
    
- <span data-ttu-id="1f99e-144">Con una pulsación de tecla de método abreviado configurada cuando se registra el comando.</span><span class="sxs-lookup"><span data-stu-id="1f99e-144">Using a shortcut keystroke set up when registering the command.</span></span>
    
- <span data-ttu-id="1f99e-145">Como el comando que se ejecuta cuando se captura un evento específico.</span><span class="sxs-lookup"><span data-stu-id="1f99e-145">As the command to be run when a specified event is trapped.</span></span>
    
> [!NOTE]
> <span data-ttu-id="1f99e-146">Los comandos XLL están ocultos, pues no aparecen en la lista de macros disponibles en los cuadros de diálogo de Excel.</span><span class="sxs-lookup"><span data-stu-id="1f99e-146">XLL commands are hidden in that they do not appear on the list of available macros in Excel dialog boxes.</span></span> <span data-ttu-id="1f99e-147">Pero se pueden especificar manualmente en el campo de nombre de la macro.</span><span class="sxs-lookup"><span data-stu-id="1f99e-147">But they can be entered manually into the macro name field.</span></span> <span data-ttu-id="1f99e-148">Excel espera el nombre "registrado como" en estos cuadros de diálogo, no el nombre de la exportación DLL.</span><span class="sxs-lookup"><span data-stu-id="1f99e-148">Excel expects the registered-as name in these dialog boxes, not the DLL export name.</span></span> 
  
<span data-ttu-id="1f99e-149">Excel asume que todos los comandos XLL registrados con Excel tienen el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="1f99e-149">All XLL commands that are registered with Excel are assumed by Excel to be of the following form.</span></span>
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

<span data-ttu-id="1f99e-p104">Excel omite el valor devuelto a menos que se le llame desde una hoja de macros XLM, en cuyo caso el valor devuelto se convierte a **TRUE** o **FALSE**. Por lo tanto, debe devolver 1 si el comando se ejecuta correctamente y 0 si tiene errores o el usuario lo cancela.</span><span class="sxs-lookup"><span data-stu-id="1f99e-p104">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span>
  
<span data-ttu-id="1f99e-152">Puede obtener información sobre cómo se invocó el comando utilizando la función de la API de C **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="1f99e-152">You can obtain information about how your command was invoked using the C API function **xlfCaller**.</span></span> <span data-ttu-id="1f99e-153">Para obtener más información, vea [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="1f99e-153">For more information, see [DataValidationPrompt](xlfcaller.md).</span></span>
  
<span data-ttu-id="1f99e-154">A partir de Excel 2007, la interfaz de usuario es muy diferente a la de las versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="1f99e-154">Starting in Excel 2007 user interface is very different from earlier versions.</span></span> <span data-ttu-id="1f99e-155">Las funciones de la API de C que permiten la adición y eliminación de barras de menús, menús, submenús, elementos de menú, barras de herramientas personalizadas y botones de la barra de herramientas aún son compatibles en la mayoría de los casos.</span><span class="sxs-lookup"><span data-stu-id="1f99e-155">The C API functions that permit the addition and deletion of custom menu bars, menus, submenus, menu items, custom toolbars and toolbar buttons are still supported in most cases.</span></span> <span data-ttu-id="1f99e-156">No obstante, puede que no siempre hagan el elemento agregado disponible de un modo que resulte familiar a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="1f99e-156">However, they may not always make the added item available in a way that your users are familiar with.</span></span> <span data-ttu-id="1f99e-157">Compruebe con cuidado que las funciones agregadas sigan siendo accesibles o implemente una personalización específica de la versión.</span><span class="sxs-lookup"><span data-stu-id="1f99e-157">You should carefully check that any added functionality is still accessible, or implement a version-specific customization.</span></span> <span data-ttu-id="1f99e-158">Empezando en Excel 2007, la interfaz de usuario se personaliza mejor a través de un módulo de código administrado que puede trabajar estrechamente con los comandos XLL.</span><span class="sxs-lookup"><span data-stu-id="1f99e-158">Starting in Excel 2007 the user interface is best customized by using a managed code module that can then be tightly coupled to your XLL commands.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1f99e-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f99e-159">See also</span></span>

- [<span data-ttu-id="1f99e-160">Crear XLL</span><span class="sxs-lookup"><span data-stu-id="1f99e-160">Creating XLLs</span></span>](creating-xlls.md)
- [<span data-ttu-id="1f99e-161">Llamar a funciones XLL desde el Asistente para funciones o los cuadros de diálogo Reemplazar</span><span class="sxs-lookup"><span data-stu-id="1f99e-161">Call XLL functions from the Function Wizard or Replace dialog boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [<span data-ttu-id="1f99e-162">Administrador de complementos y funciones de la interfaz de XLL</span><span class="sxs-lookup"><span data-stu-id="1f99e-162">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
- [<span data-ttu-id="1f99e-163">Desarrollo de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="1f99e-163">Developing Excel XLLs</span></span>](developing-excel-xlls.md)



