---
title: DetenerMacro (acción de macro)
TOCTitle: StopMacro macro action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe319e0f7a811d3bcd3b2fc18c4a3d951187fbe8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704437"
---
# <a name="stopmacro-macro-action"></a><span data-ttu-id="85eb4-102">DetenerMacro (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="85eb4-102">StopMacro macro action</span></span>

<span data-ttu-id="85eb4-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85eb4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85eb4-104">Puede utilizar la acción **DetenerMacro** para detener la macro que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="85eb4-104">You can use the **StopMacro** action to stop the currently running macro.</span></span>

## <a name="setting"></a><span data-ttu-id="85eb4-105">Setting</span><span class="sxs-lookup"><span data-stu-id="85eb4-105">Setting</span></span>

<span data-ttu-id="85eb4-106">La acción **DetenerMacro** no tiene ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="85eb4-106">The **StopMacro** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="85eb4-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85eb4-107">Remarks</span></span>

<span data-ttu-id="85eb4-108">Esta acción se suele utilizar cuando una condición haga necesario detener la macro.</span><span class="sxs-lookup"><span data-stu-id="85eb4-108">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="85eb4-109">Puede usar una expresión condicional en la fila de acción de la macro que contiene esta acción.</span><span class="sxs-lookup"><span data-stu-id="85eb4-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="85eb4-110">Cuando la expresión se evalúa como **True** (-1), Microsoft Access detiene la macro.</span><span class="sxs-lookup"><span data-stu-id="85eb4-110">When the expression evaluates to **True** (–1), Microsoft Access stops the macro.</span></span>

<span data-ttu-id="85eb4-111">Por ejemplo, podría crear una macro que se abre un formulario que muestra los totales de pedidos diarios para la fecha especificada en un cuadro de diálogo personalizado.</span><span class="sxs-lookup"><span data-stu-id="85eb4-111">For example, you might create a macro that opens a form showing the daily order totals for the date entered in a custom dialog box.</span></span> <span data-ttu-id="85eb4-112">Podría utilizar una expresión condicional para asegurarse de que el control de **Fecha de pedido** en el cuadro de diálogo contiene una fecha válida.</span><span class="sxs-lookup"><span data-stu-id="85eb4-112">You could use a conditional expression to be sure that the **Order Date** control on the dialog box contains a valid date.</span></span> <span data-ttu-id="85eb4-113">Si no es así, la acción de **cuadro de mensaje** puede mostrar un mensaje de error y la acción **DetenerMacro** puede detener la macro.</span><span class="sxs-lookup"><span data-stu-id="85eb4-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the macro.</span></span>

<span data-ttu-id="85eb4-114">Si la macro ha utilizado las acciones **eco** o **EstablecerAdvertencias** para desactivar el eco o la presentación de mensajes del sistema, la acción **DetenerMacro volverá** a activarlos automáticamente.</span><span class="sxs-lookup"><span data-stu-id="85eb4-114">If the macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopMacro** action automatically turns them back on.</span></span>

<span data-ttu-id="85eb4-115">Esta acción no está disponible en un módulo de Visual Basic para Aplicaciones (VBA).</span><span class="sxs-lookup"><span data-stu-id="85eb4-115">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

## <a name="example"></a><span data-ttu-id="85eb4-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="85eb4-116">Example</span></span>

<span data-ttu-id="85eb4-117">En la siguiente macro se muestra el uso de la acción **AlOcurrirError**.</span><span class="sxs-lookup"><span data-stu-id="85eb4-117">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="85eb4-118">En este ejemplo, la acción **AlOcurrirError** especifica que Access ejecute una macro de tratamiento de errores personalizada denominada ErrorHandler cuando se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="85eb4-118">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="85eb4-119">Cuando se produce un error, se llama la submacro CatchErrors.</span><span class="sxs-lookup"><span data-stu-id="85eb4-119">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="85eb4-120">Si el número de error es 2102, se muestra un mensaje específico y se detiene la ejecución de la macro.</span><span class="sxs-lookup"><span data-stu-id="85eb4-120">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="85eb4-121">De lo contrario, se muestra un mensaje que describe el error y se detiene la macro para que pueda realizar la resolución de problemas adicional.</span><span class="sxs-lookup"><span data-stu-id="85eb4-121">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="85eb4-122">Esta macro mostrará un cuadro de mensaje referente al objeto **ErrorDeMacro** para mostrar información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="85eb4-122">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="85eb4-123">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="85eb4-123">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    /* MACRO: mcrThrowErrors                                  */
    /* PURPOSE: Error handling using macros in Access 2010    */
    
    OnError
        Go to Macro Name
        Macro Name CatchErrors
    
    OpenForm 
        Form Name frmSamples
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    MessageBox 
        Message This message appears after the OpenForm action
        Beep Yes
        Type None
        Title
    
    
    /* SUBMACRO: CatchErrors                                   */
    
    SubMacro: CatchErrors
        If [MacroError].[Number]=2101 Then
            MessageBox
                Message Cannot find the specified form!
                Beep Yes
                Type Critical
                Title
            StopMacro
    
        Else
            MessageBox
                Message =[MacroErro].[Description]
                Beep Yes
                Type None
                Title Unhandled Error
    
            SingleStep
        End If
    
    End SubMacro
```
