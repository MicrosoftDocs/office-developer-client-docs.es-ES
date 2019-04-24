---
title: EjecutarCódigo (acción de macro)
TOCTitle: RunCode macro action
ms:assetid: cb0625be-4b5d-4927-9b0e-59a6e411b5bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834373(v=office.15)
ms:contentKeyID: 48547706
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98700
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 646c1393cc798c1f827e6ceaebf46bfe7c87bcbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306835"
---
# <a name="runcode-macro-action"></a><span data-ttu-id="dccaf-102">EjecutarCódigo (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="dccaf-102">RunCode macro action</span></span>

<span data-ttu-id="dccaf-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dccaf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dccaf-104">Puede usar la acción **EjecutarCódigo** para llamar a un procedimiento Function de Visual Basic para Aplicaciones (VBA).</span><span class="sxs-lookup"><span data-stu-id="dccaf-104">You can use the **RunCode** action to call a Visual Basic for Applications (VBA) Function procedure.</span></span>

## <a name="setting"></a><span data-ttu-id="dccaf-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="dccaf-105">Setting</span></span>

<span data-ttu-id="dccaf-106">La acción **EjecutarCódigo** utiliza el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="dccaf-106">The **RunCode** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dccaf-107">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="dccaf-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="dccaf-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="dccaf-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dccaf-109"><strong>Nombre de función</strong></span><span class="sxs-lookup"><span data-stu-id="dccaf-109"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="dccaf-p101">Nombre del procedimiento Function de VBA que va a ejecutarse. Encierre entre paréntesis los argumentos de la función. Especifique el nombre de la función en el cuadro <strong>Nombre de función</strong> situado en la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Este argumento es obligatorio.  </span><span class="sxs-lookup"><span data-stu-id="dccaf-p101">The name of the VBA Function procedure to call. Enclose any function arguments in parentheses. Enter the function name in the <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p><p><span data-ttu-id="dccaf-114"><strong>Nota</strong>: en una base de datos de Access (. mdb o. accdb), haga clic en el botón <strong>generar</strong> para usar el generador de expresiones para seleccionar una función para este argumento.</span><span class="sxs-lookup"><span data-stu-id="dccaf-114"><strong>NOTE</strong>: In an Access database (.mdb or .accdb), click the <strong>Build</strong> button to use the Expression Builder to select a function for this argument.</span></span> <span data-ttu-id="dccaf-115">Haga clic en la función deseada de la lista del Generador de expresiones.</span><span class="sxs-lookup"><span data-stu-id="dccaf-115">Click the desired function in the list in the Expression Builder.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dccaf-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dccaf-116">Remarks</span></span>

<span data-ttu-id="dccaf-117">Los procedimientos de función definidos por usuario se almacenan en módulos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dccaf-117">The user-defined Function procedures are stored in Microsoft Access modules.</span></span>

<span data-ttu-id="dccaf-118">Debe incluir paréntesis, incluso si el procedimiento de función no tiene ningún argumento, como en el siguiente ejemplo:</span><span class="sxs-lookup"><span data-stu-id="dccaf-118">You must include parentheses, even if the Function procedure doesn't have any arguments, as in the following example:</span></span>

`TestFunction()`

<span data-ttu-id="dccaf-119">A diferencia de los nombres de funciones definidas por el usuario que se usan para la configuración de propiedades de eventos, el nombre de la función en**=** el argumento nombre de **función** no empieza con un signo igual ().</span><span class="sxs-lookup"><span data-stu-id="dccaf-119">Unlike user-defined function names used for event property settings, the function name in the **Function Name** argument doesn't begin with an equal sign (**=**).</span></span>

<span data-ttu-id="dccaf-120">Access no utiliza el valor devuelto por la función.</span><span class="sxs-lookup"><span data-stu-id="dccaf-120">Access ignores the return value of the function.</span></span>

> [!NOTE]
> <span data-ttu-id="dccaf-121">No podrá llamar a un procedimiento Function desde una macro si el nombre de la función coincide con el del módulo.</span><span class="sxs-lookup"><span data-stu-id="dccaf-121">You can't call a Function procedure from a macro if the function name is the same as the module name.</span></span>

> [!TIP]
> <span data-ttu-id="dccaf-p103">[!SUGERENCIA] Para ejecutar un procedimiento Sub o un procedimiento de evento escrito en Visual Basic, cree un procedimiento de función que llama al procedimiento Sub o al procedimiento de evento. A continuación, utilice la acción **EjecutarCódigo** para ejecutar el procedimiento de función.</span><span class="sxs-lookup"><span data-stu-id="dccaf-p103">To run a Sub procedure or event procedure written in Visual Basic, create a Function procedure that calls the Sub procedure or event procedure. Then use the **RunCode** action to run the Function procedure.</span></span>

<span data-ttu-id="dccaf-p104">Si utiliza la acción **EjecutarCódigo** para llamar a una función, Access busca la función especificada por el argumento **Nombre de función** en los módulos estándar de la base de datos. Sin embargo, cuando esta acción se ejecuta como respuesta a la elección de un comando de menú de un formulario o informe, o como respuesta a un evento de un formulario o informe, Access busca primero la función en el módulo de clases del formulario o informe y, después, en los módulos estándar. Access no busca la función especificada por el argumento **Nombre de función** en los módulos de clases que aparecen en el área **Módulos** del panel de navegación.</span><span class="sxs-lookup"><span data-stu-id="dccaf-p104">If you use the **RunCode** action to call a function, Access looks for the function with the name specified by the **Function Name** argument in the standard modules for the database. However, when this action runs in response to clicking a menu command on a form or report or in response to an event on a form or report, Access first looks for the function in the form's or report's class module and then in the standard modules. Access doesn't search the class modules that appear in the **Modules** area of the Navigation Pane for the function specified by the **Function Name** argument.</span></span>

<span data-ttu-id="dccaf-p105">Esta acción no está disponible para módulos de VBA. En su lugar, ejecute el procedimiento de función que desee directamente en VBA.</span><span class="sxs-lookup"><span data-stu-id="dccaf-p105">This action isn't available in a VBA module. Instead, run the desired Function procedure directly in VBA.</span></span>

