---
title: Comandos, funciones y estados de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- states [excel 2007],commands [Excel 2007],worksheet functions [Excel 2007],macro-sheet functions [Excel 2007],Excel states
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: c941ba7445f1f0598bf044b5f177ad576df0137c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716239"
---
# <a name="excel-commands-functions-and-states"></a><span data-ttu-id="92f83-104">Estados, comandos y funciones de Excel</span><span class="sxs-lookup"><span data-stu-id="92f83-104">Excel Commands, Functions, and States</span></span>

 <span data-ttu-id="92f83-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="92f83-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="92f83-106">Microsoft Excel reconoce dos tipos muy diferentes de funciones agregadas: comandos y funciones.</span><span class="sxs-lookup"><span data-stu-id="92f83-106">Microsoft Excel recognizes two very different types of added functionality: commands and functions.</span></span>
  
## <a name="commands"></a><span data-ttu-id="92f83-107">Comandos</span><span class="sxs-lookup"><span data-stu-id="92f83-107">Commands</span></span>

<span data-ttu-id="92f83-108">En Excel, los comandos tienen las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="92f83-108">In Excel, commands have the following characteristics:</span></span>
  
- <span data-ttu-id="92f83-109">Realizan acciones del mismo modo que los usuarios.</span><span class="sxs-lookup"><span data-stu-id="92f83-109">They perform actions in the same way that users do.</span></span>
    
- <span data-ttu-id="92f83-110">Pueden hacer lo que haga un usuario (sujeto a los límites de la interfaz que se use), como modificar la configuración de Excel, abrir, cerrar y editar documentos, iniciar actualizaciones, etc.</span><span class="sxs-lookup"><span data-stu-id="92f83-110">They can do anything a user can do (subject to the limits of the interface used), such as altering Excel settings, opening, closing, and editing documents, initiating recalculations, and so on.</span></span>
    
- <span data-ttu-id="92f83-111">Se pueden configurar para que se los llamen cuando se producen determinadas capturas de eventos.</span><span class="sxs-lookup"><span data-stu-id="92f83-111">They can be set up to be called when certain trapped events occur.</span></span>
    
- <span data-ttu-id="92f83-112">Pueden mostrar cuadros de diálogo e interactuar con el usuario.</span><span class="sxs-lookup"><span data-stu-id="92f83-112">They can display dialog boxes and interact with the user.</span></span>
    
- <span data-ttu-id="92f83-113">Se pueden vincular para controlar los objetos de modo que se les llame al realizar alguna acción en ese objeto, como al hacer clic.</span><span class="sxs-lookup"><span data-stu-id="92f83-113">They can be linked to control objects so that they are called when some action is taken on that object, such as left-clicking.</span></span>
    
- <span data-ttu-id="92f83-114">Excel nunca los llamará durante una actualización.</span><span class="sxs-lookup"><span data-stu-id="92f83-114">They are never called by Excel during a recalculation.</span></span>
    
- <span data-ttu-id="92f83-115">Las funciones no pueden llamarlos durante una actualización.</span><span class="sxs-lookup"><span data-stu-id="92f83-115">They cannot be called by functions during a recalculation.</span></span>
    
## <a name="functions"></a><span data-ttu-id="92f83-116">Funciones</span><span class="sxs-lookup"><span data-stu-id="92f83-116">Functions</span></span>

<span data-ttu-id="92f83-117">Las funciones de Excel hacen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="92f83-117">Functions in Excel do the following:</span></span>
  
- <span data-ttu-id="92f83-118">Normalmente toman argumentos y siempre devuelven un resultado.</span><span class="sxs-lookup"><span data-stu-id="92f83-118">They usually take arguments and always return a result.</span></span>
    
- <span data-ttu-id="92f83-119">Se pueden introducir en una o varias celdas como parte de una fórmula de Excel.</span><span class="sxs-lookup"><span data-stu-id="92f83-119">They can be entered into one or more cells as part of an Excel formula.</span></span>
    
- <span data-ttu-id="92f83-120">Se pueden usar en las definiciones de nombre definido.</span><span class="sxs-lookup"><span data-stu-id="92f83-120">They can be used in defined name definitions.</span></span>
    
- <span data-ttu-id="92f83-121">Se pueden usar en expresiones de umbral y de límite de formato condicional.</span><span class="sxs-lookup"><span data-stu-id="92f83-121">They can be used in conditional formatting limit and threshold expressions.</span></span>
    
- <span data-ttu-id="92f83-122">Los comandos las pueden llamar.</span><span class="sxs-lookup"><span data-stu-id="92f83-122">They can be called by commands.</span></span>
    
- <span data-ttu-id="92f83-123">No pueden llamar a comandos.</span><span class="sxs-lookup"><span data-stu-id="92f83-123">They cannot call commands.</span></span>
    
<span data-ttu-id="92f83-p101">Excel hace una distinción más entre funciones de hoja de cálculo definidas por el usuario y funciones definidas por el usuario que son diseñadas para trabajar en hojas de macros. Excel no limita las funciones de hoja de macros definidas por el usuario que solo se van a usar en hojas de macros: estas funciones se pueden usar en cualquier lugar en el que se pueda usar una función de hoja de cálculo normal.</span><span class="sxs-lookup"><span data-stu-id="92f83-p101">Excel makes a further distinction between user-defined worksheet functions and user-defined functions that are designed to work on macro sheets. Excel does not limit user-defined macro sheet functions only to being used on macro sheets: these functions can be used anywhere a normal worksheet function can be used.</span></span>
  
### <a name="worksheet-functions"></a><span data-ttu-id="92f83-126">Funciones de hoja de cálculo</span><span class="sxs-lookup"><span data-stu-id="92f83-126">Worksheet Functions</span></span>

<span data-ttu-id="92f83-127">Lo siguiente es verdadero de funciones de hoja de cálculo de Excel:</span><span class="sxs-lookup"><span data-stu-id="92f83-127">The following is true of Excel worksheet functions:</span></span>
  
- <span data-ttu-id="92f83-128">No pueden acceder a las funciones de información de hojas de macros.</span><span class="sxs-lookup"><span data-stu-id="92f83-128">They cannot access macro sheet information functions.</span></span>
    
- <span data-ttu-id="92f83-129">No pueden obtiener los valores de las celdas no actualizadas.</span><span class="sxs-lookup"><span data-stu-id="92f83-129">They cannot obtain the values of uncalculated cells.</span></span>
    
- <span data-ttu-id="92f83-130">Se pueden escribir y registrar como seguros para subprocesos a partir de Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="92f83-130">They can be written and registered as thread-safe starting in Excel 2007.</span></span>
    
### <a name="macro-sheet-functions"></a><span data-ttu-id="92f83-131">Funciones de hoja de macros</span><span class="sxs-lookup"><span data-stu-id="92f83-131">Macro-Sheet Functions</span></span>

<span data-ttu-id="92f83-132">Lo siguiente es verdadero de funciones de hoja de macros de Excel:</span><span class="sxs-lookup"><span data-stu-id="92f83-132">The following is true of Excel macro-sheet functions:</span></span>
  
- <span data-ttu-id="92f83-133">Pueden acceder a las funciones de información de hojas de macros.</span><span class="sxs-lookup"><span data-stu-id="92f83-133">They can access macro sheet information functions.</span></span>
    
- <span data-ttu-id="92f83-134">Pueden obtener los valores de las celdas no actualizadas, incluidos los valores de las celdas de llamada.</span><span class="sxs-lookup"><span data-stu-id="92f83-134">They can obtain the values of uncalculated cells including the values of the calling cells.</span></span>
    
- <span data-ttu-id="92f83-135">No se consideran inicios seguros para subprocesos en Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="92f83-135">They are not considered thread safe starting in Excel 2007.</span></span>
    
<span data-ttu-id="92f83-p102">Cómo trata Excel a una función definida por el usuario (UDF), qué permite que haga la función y cómo actualiza la función se determina al registrar la función. Si una función está registrada como una función de hoja de cálculo e intenta hacer algo que solo puede hacer una función de hoja de macros, la operación dará un error. A partir de Excel 2007, si una función de hoja de cálculo registrada como segura para subprocesos intenta llamar a una función de hoja de macros, la operación dará un error.</span><span class="sxs-lookup"><span data-stu-id="92f83-p102">How Excel treats a user-defined function (UDF), what it permits the function to do, and how it recalculates the function are all determined when you register the function. If a function is registered as a worksheet function but tries to do something that only a macro-sheet function can do, the operation fails. Starting in Excel 2007, if a worksheet function registered as thread safe tries to call a macro sheet function, again, the operation fails.</span></span>
  
<span data-ttu-id="92f83-139">Excel trata los UDF de Microsoft Visual Basic para aplicaciones (VBA) como funciones equivalentes de hoja de macros, en las que pueden acceder a la información del área de trabajo y al valor de las celdas no actualizadas, y no se consideran como seguros para subprocesos a partir de Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="92f83-139">Excel treats Microsoft Visual Basic for Applications (VBA) UDFs as macro sheet-equivalent functions, in that they can access workspace information and the value of uncalculated cells, and they are not considered as thread safe starting in Excel 2007.</span></span>
  
## <a name="excel-states"></a><span data-ttu-id="92f83-140">Estados de Excel</span><span class="sxs-lookup"><span data-stu-id="92f83-140">Excel States</span></span>

<span data-ttu-id="92f83-141">Excel puede estar en uno de varios estados en un momento dado, dependiendo de las acciones del usuario, un proceso externo, un evento capturado que ejecuta una macro o un evento de mantenimiento programado de Excel, como **Autosave**.</span><span class="sxs-lookup"><span data-stu-id="92f83-141">Excel can be in one of a number of states at any given time depending on the actions of the user, an external process, a trapped event running a macro, or a timed Excel housekeeping event such as **Autosave**.</span></span>
  
<span data-ttu-id="92f83-142">Los estados que experimentan los usuarios son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="92f83-142">The states that the user experiences are as follows:</span></span>
  
- <span data-ttu-id="92f83-p103">**Estado Listo:** no se ejecutan comandos o macros. No se muestran cuadros de diálogo. No se editan celdas y el usuario no está en medio de una operación de cortar, y copiar y pegar. Ningún objeto insertado tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="92f83-p103">**Ready state:** No commands or macros are being run. No dialog boxes are being displayed. No cells are being edited and the user is not in the middle of a cut/copy and paste operation. No embedded object has focus.</span></span> 
    
- <span data-ttu-id="92f83-147">**Modo Editar:** el usuario empieza a escribir los caracteres de entrada válidos en una celda desbloqueada o desprotegida, o presiona **F2** en una o varias celdas desbloqueadas o desprotegidas.</span><span class="sxs-lookup"><span data-stu-id="92f83-147">**Edit mode:** The user has started to type valid input characters into an unlocked or unprotected cell, or has pressed **F2** on one or more unlocked or unprotected cells.</span></span> 
    
- <span data-ttu-id="92f83-148">**Modo Cortar/Copiar y pegar:** el usuario corta o copia una celda o un rango de celdas y aún no las ha pegado, o las ha pegado con el cuadro de diálogo de pegado especial que permite varias operaciones de pegado.</span><span class="sxs-lookup"><span data-stu-id="92f83-148">**Cut/copy and paste mode:** The user has cut or copied a cell or range of cells and has not yet pasted them, or has pasted them using the paste-special dialog box, which enables multiple paste operations.</span></span> 
    
- <span data-ttu-id="92f83-149">**Modo Señalar:** el usuario edita una fórmula y selecciona celdas cuyas direcciones se agregan a la fórmula que se edita.</span><span class="sxs-lookup"><span data-stu-id="92f83-149">**Point mode:** The user is editing a formula and is selecting cells whose addresses are added to the formula being edited.</span></span> 
    
<span data-ttu-id="92f83-p104">El usuario puede borrar los modos de Editar, Señalar y Cortar/Copiar presionando la tecla **ESC**, que devuelve a Excel a su estado listo. Otros eventos pueden borrar estos estados, como los siguientes:</span><span class="sxs-lookup"><span data-stu-id="92f83-p104">The user can clear the edit, point, and cut/copy modes by pressing the **ESC** key, which returns Excel to its ready state. Other events can clear these states, such as the following:</span></span> 
  
- <span data-ttu-id="92f83-152">El usuario abre un cuadro de diálogo integrado.</span><span class="sxs-lookup"><span data-stu-id="92f83-152">The user opens a built-in dialog box.</span></span>
    
- <span data-ttu-id="92f83-153">El usuario inicia una actualización.</span><span class="sxs-lookup"><span data-stu-id="92f83-153">The user initiates a recalculation.</span></span>
    
- <span data-ttu-id="92f83-154">El usuario ejecuta un comando.</span><span class="sxs-lookup"><span data-stu-id="92f83-154">The user runs a command.</span></span>
    
- <span data-ttu-id="92f83-155">Excel realiza una operación **Autosave**.</span><span class="sxs-lookup"><span data-stu-id="92f83-155">Excel performs an **Autosave** operation.</span></span> 
    
- <span data-ttu-id="92f83-156">Se captura un evento de temporizador.</span><span class="sxs-lookup"><span data-stu-id="92f83-156">A timer event is trapped.</span></span>
    
<span data-ttu-id="92f83-p105">El último ejemplo es importante para los desarrolladores de complementos. Debe tener en cuenta el impacto de la facilidad de uso normal de Excel, donde se configuran y ejecutan capturas de eventos de temporizador. Cuando se trata de una parte importante de funcionalidad del complemento, debe proporcionar a los usuarios un modo sencillo para suspenderlo, para que puedan cortar/copiar y pegar normalmente cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="92f83-p105">The last example is of importance to add-in developers. You should consider the impact of the normal usability of Excel where frequent timer event traps are being set and executed. When this is an important part of your add-in's functionality, you should provide users with an easily accessible way of suspending it, so that they can cut/copy and paste normally when they need to.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="92f83-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="92f83-160">See also</span></span>



[<span data-ttu-id="92f83-161">Conceptos de programación de Excel</span><span class="sxs-lookup"><span data-stu-id="92f83-161">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
[<span data-ttu-id="92f83-162">Permitir interrupciones de usuarios en operaciones largas</span><span class="sxs-lookup"><span data-stu-id="92f83-162">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)

