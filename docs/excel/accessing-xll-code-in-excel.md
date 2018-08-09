---
title: Acceso al código XLL en Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- acceso al código xll [excel 2007], XLL [Excel 2007], obtener acceso a código, comandos [Excel 2007], registro, funciones [Excel 2007], registro, llamar a los XLL de Excel, registrar comandos [Excel 2007], registrar funciones [Excel 2007]
localization_priority: Normal
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1523f9e8213cb955f1bfd995c42f921b001299fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815522"
---
# <a name="accessing-xll-code-in-excel"></a><span data-ttu-id="7e701-104">Acceso al código XLL en Excel</span><span class="sxs-lookup"><span data-stu-id="7e701-104">Accessing XLL code in Excel</span></span>

<span data-ttu-id="7e701-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7e701-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7e701-106">Para ser accesibles en Microsoft Excel, las funciones y los comandos que contiene un XLL:</span><span class="sxs-lookup"><span data-stu-id="7e701-106">To be accessible in Microsoft Excel, the functions and commands that an XLL contains:</span></span>
  
- <span data-ttu-id="7e701-107">Debe ser exportada por el XLL.</span><span class="sxs-lookup"><span data-stu-id="7e701-107">Must be exported by the XLL.</span></span>
    
- <span data-ttu-id="7e701-108">Debe estar registrada con Excel.</span><span class="sxs-lookup"><span data-stu-id="7e701-108">Must be registered with Excel.</span></span>
    
## <a name="registering-functions-and-commands-with-excel"></a><span data-ttu-id="7e701-109">Registrar las funciones y comandos con Excel</span><span class="sxs-lookup"><span data-stu-id="7e701-109">Registering functions and commands with Excel</span></span>

<span data-ttu-id="7e701-110">Registro indica a Excel lo siguiente acerca de un punto de entrada del archivo DLL:</span><span class="sxs-lookup"><span data-stu-id="7e701-110">Registration tells Excel the following about a DLL entry point:</span></span>
  
- <span data-ttu-id="7e701-111">Si está oculto o, si una función, si está visible en el Asistente para la función.</span><span class="sxs-lookup"><span data-stu-id="7e701-111">Whether it is hidden or, if a function, whether it is visible in the Function Wizard.</span></span>
    
- <span data-ttu-id="7e701-112">Si es que se puede llamar solo desde una hoja de macros XLM, o también desde una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="7e701-112">Whether it is callable only from an XLM macro sheet, or also from a worksheet.</span></span>
    
- <span data-ttu-id="7e701-113">Si un comando, si es una función de hoja de cálculo o una función equivalente de hoja de macro.</span><span class="sxs-lookup"><span data-stu-id="7e701-113">If a command, whether it is a worksheet function or a macro sheet equivalent function.</span></span>
    
- <span data-ttu-id="7e701-114">¿Cuál es su nombre de exportación DLL o XLL y qué nombre que desea que utilice Excel.</span><span class="sxs-lookup"><span data-stu-id="7e701-114">What its XLL/DLL export name is, and what name you want Excel to use.</span></span>
    
- <span data-ttu-id="7e701-115">Si se trata de una función:</span><span class="sxs-lookup"><span data-stu-id="7e701-115">If it is a function:</span></span>
    
  - <span data-ttu-id="7e701-116">¿Qué datos tipos devuelve y toma como argumentos.</span><span class="sxs-lookup"><span data-stu-id="7e701-116">What data types it returns and takes as arguments.</span></span>
    
  - <span data-ttu-id="7e701-117">Si devuelve su resultado mediante la modificación de un argumento en su lugar.</span><span class="sxs-lookup"><span data-stu-id="7e701-117">Whether it returns its result by modifying an argument in place.</span></span>
    
  - <span data-ttu-id="7e701-118">Si es volátil.</span><span class="sxs-lookup"><span data-stu-id="7e701-118">Whether it is volatile.</span></span>
    
  - <span data-ttu-id="7e701-119">Si es seguro para subprocesos (comenzando admitidos en Excel 2007).</span><span class="sxs-lookup"><span data-stu-id="7e701-119">Whether it is thread safe (supported starting in Excel 2007).</span></span>
    
  - <span data-ttu-id="7e701-120">¿Qué editor de Autocompletar y el Asistente para la función pegar texto deben mostrar para ayudar con la función de llamada.</span><span class="sxs-lookup"><span data-stu-id="7e701-120">What text the Paste Function Wizard and AutoComplete editor should display to help with calling the function.</span></span>
    
  - <span data-ttu-id="7e701-121">Qué función categoría debe aparecer en.</span><span class="sxs-lookup"><span data-stu-id="7e701-121">Which function category it should be listed under.</span></span>
    
<span data-ttu-id="7e701-122">Todo esto se logra mediante la API C función [xlfRegister](xlfregister-form-1.md), equivalente a la función XLM **registrar**.</span><span class="sxs-lookup"><span data-stu-id="7e701-122">This is all achieved using the C API function [xlfRegister](xlfregister-form-1.md), equivalent to the XLM function **REGISTER**.</span></span>
  
## <a name="calling-xll-functions-directly-from-excel"></a><span data-ttu-id="7e701-123">Llamar a funciones XLL directamente desde Excel</span><span class="sxs-lookup"><span data-stu-id="7e701-123">Calling XLL functions directly from Excel</span></span>

<span data-ttu-id="7e701-124">Una vez registrados, funciones de hoja de hoja de cálculo y de macros XLL pueden llamarse desde cualquier lugar que una función integrada se puede llamar desde:</span><span class="sxs-lookup"><span data-stu-id="7e701-124">Once they are registered, XLL worksheet and macro sheet functions can be called from anywhere a built-in function can be called from:</span></span>
  
- <span data-ttu-id="7e701-125">Una sola celda o matriz fórmula en una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="7e701-125">A single-cell or array formula on a worksheet.</span></span>
    
- <span data-ttu-id="7e701-126">Una sola celda o matriz fórmula en una hoja de macros.</span><span class="sxs-lookup"><span data-stu-id="7e701-126">A single-cell or array formula on a macro sheet.</span></span>
    
- <span data-ttu-id="7e701-127">La definición de un nombre definido.</span><span class="sxs-lookup"><span data-stu-id="7e701-127">The definition of a defined name.</span></span>
    
- <span data-ttu-id="7e701-128">La condición y el límite de campos en un cuadro de diálogo Formato condicional.</span><span class="sxs-lookup"><span data-stu-id="7e701-128">The condition and limit fields in a conditional format dialog box.</span></span>
    
- <span data-ttu-id="7e701-129">Desde otro complemento a través de la API de C funcionar [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="7e701-129">From another add-in via the C API function [xlUDF](xludf.md).</span></span>
    
- <span data-ttu-id="7e701-130">Desde Visual Basic para aplicaciones (VBA) a través del método **Application.Run** .</span><span class="sxs-lookup"><span data-stu-id="7e701-130">From Visual Basic for Applications (VBA) via the **Application.Run** method.</span></span> 
    
<span data-ttu-id="7e701-131">Puede obtener una referencia a la celda o rango de celdas que llama dentro de la función mediante la función de API C **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="7e701-131">You can obtain a reference to the calling cell or range of cells within your function using the C API function **xlfCaller**.</span></span> <span data-ttu-id="7e701-132">Si se llama a la función de la expresión de formato condicional de la celda, todavía se devuelve una referencia a la celda asociada o celdas, por lo que no se puede suponer que la fórmula de la celda contiene la función XLL.</span><span class="sxs-lookup"><span data-stu-id="7e701-132">If the function was called from the cell's conditional format expression, you are still returned a reference to the associated cell or cells, so you cannot assume that the cell's formula contains the XLL function.</span></span> <span data-ttu-id="7e701-133">Si la función se ha llamado desde una función VBA definida por el usuario (UDF), **xlfCaller** vuelve a ser la dirección de las celdas que llamó a la función VBA.</span><span class="sxs-lookup"><span data-stu-id="7e701-133">If your function was called from a VBA user-defined function (UDF), **xlfCaller** again returns the address of the cells that called the VBA function.</span></span> <span data-ttu-id="7e701-134">Para obtener más información, vea [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="7e701-134">For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="7e701-135">Excel también llama a código de función XLL desde los cuadros de diálogo **Asistente para la función Pegar** y **Reemplazar** .</span><span class="sxs-lookup"><span data-stu-id="7e701-135">Excel also calls XLL function code from the **Paste Function Wizard** and **Replace** dialog boxes.</span></span> <span data-ttu-id="7e701-136">Es posible que necesite restringir el código ejecuta normal en el caso del cuadro de diálogo **Argumentos de la función Pegar** , especialmente donde la función puede tardar mucho tiempo en ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="7e701-136">You might need to restrict your code's normal running in the case of the **Paste Function Arguments** dialog box, especially where your function can take a long time to execute.</span></span> <span data-ttu-id="7e701-137">Para detectar si desde cualquiera de estos cuadros de diálogo se llama a la función, debe implementar un fragmento de código en el proyecto que recorre en iteración todas las ventanas abiertas para determinar si la ventana en primer plano es uno de estos cuadros de diálogo y, si es así, cuál.</span><span class="sxs-lookup"><span data-stu-id="7e701-137">To detect if your function is being called from either of these dialog boxes, you must implement some code in your project that iterates through all the open windows to determine if the front window is one of these dialog boxes, and, if so, which one.</span></span> 
  
## <a name="calling-xll-commands-directly-from-excel"></a><span data-ttu-id="7e701-138">Llamar a los comandos XLL directamente desde Excel</span><span class="sxs-lookup"><span data-stu-id="7e701-138">Calling XLL commands directly from Excel</span></span>

<span data-ttu-id="7e701-139">Una vez registrados, pueden llamar a los comandos XLL en todas las formas en que se pueden llamar a otras macros definidas por el usuario:</span><span class="sxs-lookup"><span data-stu-id="7e701-139">Once they are registered, XLL commands can be called in all the ways that other user-defined macros can be called:</span></span>
  
- <span data-ttu-id="7e701-140">Por la que está asociada a un objeto de control incrustado en una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="7e701-140">By being associated with a control object embedded on a worksheet.</span></span>
    
- <span data-ttu-id="7e701-141">Desde el cuadro de diálogo Ejecutar Macro.</span><span class="sxs-lookup"><span data-stu-id="7e701-141">From the Run Macro dialog box.</span></span>
    
- <span data-ttu-id="7e701-142">Desde una macro VBA definida por el usuario mediante el método **Application.Run** .</span><span class="sxs-lookup"><span data-stu-id="7e701-142">From a VBA user-defined macro using the **Application.Run** method.</span></span> 
    
- <span data-ttu-id="7e701-143">Desde un elemento de menú personalizado o barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="7e701-143">From a customized menu item or toolbar.</span></span>
    
- <span data-ttu-id="7e701-144">Mediante una pulsación de tecla de método abreviado configurar cuando se registra el comando.</span><span class="sxs-lookup"><span data-stu-id="7e701-144">Using a shortcut keystroke set up when registering the command.</span></span>
    
- <span data-ttu-id="7e701-145">Como el comando se ejecute cuando se captura un evento especificado.</span><span class="sxs-lookup"><span data-stu-id="7e701-145">As the command to be run when a specified event is trapped.</span></span>
    
> [!NOTE]
> <span data-ttu-id="7e701-146">Comandos XLL están ocultos en que no aparecen en la lista de macros disponibles en los cuadros de diálogo de Excel.</span><span class="sxs-lookup"><span data-stu-id="7e701-146">XLL commands are hidden in that they do not appear on the list of available macros in Excel dialog boxes.</span></span> <span data-ttu-id="7e701-147">Pero se pueden especificar manualmente en el campo de nombre de macro.</span><span class="sxs-lookup"><span data-stu-id="7e701-147">But they can be entered manually into the macro name field.</span></span> <span data-ttu-id="7e701-148">Excel espera que el nombre registrado como en estos cuadros de diálogo, no el nombre de la exportación del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="7e701-148">Excel expects the registered-as name in these dialog boxes, not the DLL export name.</span></span> 
  
<span data-ttu-id="7e701-149">Se supone que todos los comandos XLL registrados con Excel por Excel para tener el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="7e701-149">All XLL commands registered with Excel are assumed by Excel to be of the following form:</span></span>
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

<span data-ttu-id="7e701-p104">Excel omite el valor devuelto a menos que se le llame desde una hoja de macros XLM, en cuyo caso el valor devuelto se convierte a **TRUE** o **FALSE**. Por lo tanto, debe devolver 1 si el comando se ejecuta correctamente y 0 si tiene errores o el usuario lo cancela.</span><span class="sxs-lookup"><span data-stu-id="7e701-p104">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span>
  
<span data-ttu-id="7e701-152">Puede obtener información acerca de cómo se ha invocado el comando se usa la API C función **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="7e701-152">You can obtain information about how your command was invoked using the C API function **xlfCaller**.</span></span> <span data-ttu-id="7e701-153">Para obtener más información, vea [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="7e701-153">For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
<span data-ttu-id="7e701-154">Iniciar en la interfaz de usuario de Excel 2007 es muy diferente de las versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="7e701-154">Starting in Excel 2007 user interface is very different from earlier versions.</span></span> <span data-ttu-id="7e701-155">Las funciones de la API de C que permiten la adición y eliminación de barras de menús personalizadas, los menús, submenús, elementos de menú, barras de herramientas personalizadas y los botones de la barra de herramientas que aún se admiten en la mayoría de los casos.</span><span class="sxs-lookup"><span data-stu-id="7e701-155">The C API functions that permit the addition and deletion of custom menu bars, menus, submenus, menu items, custom toolbars and toolbar buttons are still supported in most cases.</span></span> <span data-ttu-id="7e701-156">Sin embargo, es posible que no siempre que el elemento se ha agregado un ofrecen de modo que los usuarios están familiarizados con.</span><span class="sxs-lookup"><span data-stu-id="7e701-156">However, they may not always make the added item available in a way that your users are familiar with.</span></span> <span data-ttu-id="7e701-157">Es recomendable comprobar minuciosamente que aún es accesible a cualquier funcionalidad se ha agregado o implementar una personalización específicas de la versión.</span><span class="sxs-lookup"><span data-stu-id="7e701-157">You should carefully check that any added functionality is still accessible, or implement a version-specific customization.</span></span> <span data-ttu-id="7e701-158">Inicio de la interfaz de usuario en Excel 2007 mejor personalizado mediante el uso de un módulo de código administrado que, a continuación, estar estrechamente acoplado a los comandos XLL.</span><span class="sxs-lookup"><span data-stu-id="7e701-158">Starting in Excel 2007 the user interface is best customized by using a managed code module that can then be tightly coupled to your XLL commands.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7e701-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e701-159">See also</span></span>

- [<span data-ttu-id="7e701-160">Crear XLL</span><span class="sxs-lookup"><span data-stu-id="7e701-160">Creating XLLs</span></span>](creating-xlls.md)
- [<span data-ttu-id="7e701-161">Llamar a funciones XLL desde el Asistente para funciones o los cuadros de diálogo Reemplazar</span><span class="sxs-lookup"><span data-stu-id="7e701-161">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [<span data-ttu-id="7e701-162">Administrador de complementos y funciones de la interfaz de XLL</span><span class="sxs-lookup"><span data-stu-id="7e701-162">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
- [<span data-ttu-id="7e701-163">Desarrollo de XLL de Excel de 2013</span><span class="sxs-lookup"><span data-stu-id="7e701-163">Developing Excel XLLs</span></span>](developing-excel-xlls.md)



