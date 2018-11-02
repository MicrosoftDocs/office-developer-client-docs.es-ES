---
title: EjecutarMacro (acción de macro)
TOCTitle: RunMacro macro action
ms:assetid: 25966f20-8160-0821-b88a-ed08b7786fdc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191868(v=office.15)
ms:contentKeyID: 48543787
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm43195
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7aace8618e9ca5cdd540c15d04869dbce8c3a891
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926118"
---
# <a name="runmacro-macro-action"></a><span data-ttu-id="bb84a-102">EjecutarMacro (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="bb84a-102">RunMacro macro action</span></span>


<span data-ttu-id="bb84a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bb84a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bb84a-p101">Puede usar la acción **EjecutarMacro** para ejecutar una macro. La macro puede estar dentro de un grupo de macros.</span><span class="sxs-lookup"><span data-stu-id="bb84a-p101">You can use the **RunMacro** action to run a macro. The macro can be in a macro group.</span></span>

<span data-ttu-id="bb84a-106">Podrá usar esta acción en los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="bb84a-106">You can use this action:</span></span>

  - <span data-ttu-id="bb84a-107">Ejecutar una macro desde dentro de otra macro.</span><span class="sxs-lookup"><span data-stu-id="bb84a-107">To run a macro from within another macro.</span></span>

  - <span data-ttu-id="bb84a-108">Ejecutar una macro según una condición determinada.</span><span class="sxs-lookup"><span data-stu-id="bb84a-108">To run a macro based on a certain condition.</span></span>

  - <span data-ttu-id="bb84a-109">Asociar una macro a un comando de menú personalizado.</span><span class="sxs-lookup"><span data-stu-id="bb84a-109">To attach a macro to a custom menu command.</span></span>

## <a name="setting"></a><span data-ttu-id="bb84a-110">Configuración</span><span class="sxs-lookup"><span data-stu-id="bb84a-110">Setting</span></span>

<span data-ttu-id="bb84a-111">La acción **EjecutarMacro** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="bb84a-111">The **RunMacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bb84a-112">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="bb84a-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="bb84a-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb84a-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb84a-114"><strong>Nombre de macro</strong></span><span class="sxs-lookup"><span data-stu-id="bb84a-114"><strong>Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="bb84a-115">Nombre de la macro que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="bb84a-115">The name of the macro to run.</span></span> <span data-ttu-id="bb84a-116">El cuadro <strong>Nombre de la Macro</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todas las macros (y grupos de macros) en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="bb84a-116">The <strong>Macro Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all macros (and macro groups) in the current database.</span></span> <span data-ttu-id="bb84a-117">Si la macro se encuentra en un grupo de macros, aparece bajo el nombre del grupo de macros en la lista formato <em>nombregrupomacros</em>. <em>macroname</em>.</span><span class="sxs-lookup"><span data-stu-id="bb84a-117">If the macro is in a macro group, it's listed under the macro group name in the list as <em>macrogroupname</em>.<em>macroname</em>.</span></span> <span data-ttu-id="bb84a-118">Este argumento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bb84a-118">This is a required argument.</span></span> <span data-ttu-id="bb84a-119">Si ejecuta una macro que contiene la acción <strong>EjecutarMacro</strong> en una base de datos de biblioteca, Microsoft Access busca la macro con este nombre en la base de datos de biblioteca y no en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="bb84a-119">If you run a macro containing the <strong>RunMacro</strong> action in a library database, Microsoft Access looks for the macro with this name in the library database and doesn't look for it in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb84a-120"><strong>Número de repeticiones</strong></span><span class="sxs-lookup"><span data-stu-id="bb84a-120"><strong>Repeat Count</strong></span></span></p></td>
<td><p><span data-ttu-id="bb84a-p103">Número máximo de veces que la macro se va a ejecutar. Si deja este argumento en blanco (y el argumento <strong>Expresión de repetición</strong> también está en blanco), la macro se ejecuta una sola vez.</span><span class="sxs-lookup"><span data-stu-id="bb84a-p103">The maximum number of times the macro will run. If you leave this argument blank (and the <strong>Repeat Expression</strong> argument is also blank), the macro runs once.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb84a-123"><strong>Expresión de repetición</strong></span><span class="sxs-lookup"><span data-stu-id="bb84a-123"><strong>Repeat Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="bb84a-p104">Una expresión que se evalúa como <strong>Verdadero</strong> (–1) o <strong>Falso</strong> (0). La macro detiene su ejecución si la expresión se evalúa como <strong>Falso</strong>. La expresión se evalúa cada vez que se ejecuta la macro.</span><span class="sxs-lookup"><span data-stu-id="bb84a-p104">An expression that evaluates to <strong>True</strong> (–1) or <strong>False</strong> (0). The macro stops running if the expression evaluates to <strong>False</strong>. The expression is evaluated each time the macro runs.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="bb84a-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb84a-127">Remarks</span></span>

<span data-ttu-id="bb84a-128">Si escribe un nombre de grupo de macros en el argumento **Nombre de macro**, Access ejecuta la primera macro del grupo de macros.</span><span class="sxs-lookup"><span data-stu-id="bb84a-128">If you enter a macro group name for the **Macro Name** argument, Access runs the first macro in the macro group.</span></span>

<span data-ttu-id="bb84a-p105">Esta acción es similar a hacer clic en **Ejecutar macro** en la ficha **Herramientas de base de datos**, seleccionar una macro y hacer clic en **Aceptar**. Sin embargo, el comando ejecuta la macro solo una vez, mientras que la acción **EjecutarMacro** puede ejecutar una macro tantas veces como se desee.</span><span class="sxs-lookup"><span data-stu-id="bb84a-p105">This action is similar to clicking **Run Macro** on the **Database Tools** tab, selecting a macro, and clicking **OK**. However, this command runs the macro only once, whereas the **RunMacro** action can run a macro as many times as you want.</span></span>


> [!TIP]
> <P><span data-ttu-id="bb84a-131">[!SUGERENCIA] Puede usar los argumentos <STRONG>Número de repeticiones</STRONG> y <STRONG>Expresión de repetición</STRONG> para determinar cuántas veces se ejecuta la macro:</span><span class="sxs-lookup"><span data-stu-id="bb84a-131">You can use the <STRONG>Repeat Count</STRONG> and <STRONG>Repeat Expression</STRONG> arguments to determine how many times the macro runs:</span></span></P>



  - <span data-ttu-id="bb84a-132">Si deja ambos argumentos en blanco, la macro se ejecuta una vez.</span><span class="sxs-lookup"><span data-stu-id="bb84a-132">If you leave both arguments blank, the macro runs once.</span></span>

  - <span data-ttu-id="bb84a-133">Si especifica un número en **Número de repeticiones**, pero deja la **Expresión de repetición** en blanco, la macro se ejecuta el número de veces especificado.</span><span class="sxs-lookup"><span data-stu-id="bb84a-133">If you enter a number for **Repeat Count** but leave **Repeat Expression** blank, the macro runs the specified number of times.</span></span>

  - <span data-ttu-id="bb84a-134">Si deja el argumento **Número de repeticiones** en blanco, pero especifica una expresión en **Expresión de repetición**, la macro se ejecuta hasta que la expresión se evalúe como **Falso**.</span><span class="sxs-lookup"><span data-stu-id="bb84a-134">If you leave **Repeat Count** blank but enter an expression for **Repeat Expression**, the macro runs until the expression evaluates to **False**.</span></span>

  - <span data-ttu-id="bb84a-135">Si especifica valores en ambos argumentos, la macro se ejecuta el número de veces que especifica el argumento **Número de repeticiones** o hasta que la **Expresión de repetición** se evalúe como **Falso** (el primer caso de los dos que se produzca).</span><span class="sxs-lookup"><span data-stu-id="bb84a-135">If you enter values for both arguments, the macro runs the number of times specified in **Repeat Count** or until **Repeat Expression** evaluates to **False**, whichever occurs first.</span></span>

<span data-ttu-id="bb84a-p106">Cuando se ejecuta una macro que contiene la acción **EjecutarMacro** y se llega a la acción **EjecutarMacro**, Access ejecuta la macro a la que se ha llamado. Cuando esta macro termina, Access vuelve a la macro original y ejecuta la acción siguiente.</span><span class="sxs-lookup"><span data-stu-id="bb84a-p106">When you run a macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called macro. When the called macro has finished, Access returns to the original macro and runs the next action.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="bb84a-138">Puede llamar a una macro del mismo grupo de macros o de otro grupo de macros.</span><span class="sxs-lookup"><span data-stu-id="bb84a-138">You can call a macro in the same macro group or in another macro group.</span></span></P>
> <LI>
> <P><span data-ttu-id="bb84a-p107">Puede anidar macros. Es decir, puede ejecutar la macro A, que a su vez llama a la macro B, y así sucesivamente. En cada caso, cuando termina la macro a la que se ha llamado, Access regresa a la macro que efectuó la llamada y ejecuta la siguiente acción de esa macro.</span><span class="sxs-lookup"><span data-stu-id="bb84a-p107">You can nest macros. That is, you can run macro A, which in turn calls macro B, and so on. In each case, when the called macro has finished, Access returns to the macro that called it and runs the next action in that macro.</span></span></P></LI></UL>



<span data-ttu-id="bb84a-142">Para ejecutar la acción **EjecutarMacro** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **RunMacro** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="bb84a-142">To run the **RunMacro** action in a Visual Basic for Applications (VBA) module, use the **RunMacro** method of the **DoCmd** object.</span></span>

