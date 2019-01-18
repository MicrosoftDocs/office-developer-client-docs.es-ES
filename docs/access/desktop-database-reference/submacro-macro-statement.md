---
title: Submacro (instrucción de macro)
TOCTitle: Submacro macro statement
ms:assetid: fb580c19-52cd-c0bd-9117-4fa721eead6b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837173(v=office.15)
ms:contentKeyID: 48548867
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: caabfb0f4e90134c10d5ab728f19e1fd2a4437dd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716197"
---
# <a name="submacro-macro-statement"></a><span data-ttu-id="48a0d-102">Submacro (instrucción de macro)</span><span class="sxs-lookup"><span data-stu-id="48a0d-102">Submacro macro statement</span></span>

<span data-ttu-id="48a0d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="48a0d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="48a0d-104">La instrucción **Submacro** define una macro independiente en la ventana del Diseñador de macros.</span><span class="sxs-lookup"><span data-stu-id="48a0d-104">The **Submacro** statement defines a separate macro in the Macro Designer window.</span></span>

## <a name="setting"></a><span data-ttu-id="48a0d-105">Valores</span><span class="sxs-lookup"><span data-stu-id="48a0d-105">Setting</span></span>

<span data-ttu-id="48a0d-106">La acción **Submacro** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="48a0d-106">The **Submacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48a0d-107">Argumento</span><span class="sxs-lookup"><span data-stu-id="48a0d-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="48a0d-108">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="48a0d-108">Required</span></span></p></th>
<th><p><span data-ttu-id="48a0d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="48a0d-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48a0d-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="48a0d-110">Name</span></span></p></td>
<td><p><span data-ttu-id="48a0d-111">Sí</span><span class="sxs-lookup"><span data-stu-id="48a0d-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="48a0d-112">Una cadena que aparece como el nombre de la macro.</span><span class="sxs-lookup"><span data-stu-id="48a0d-112">A string that appears as the name of the macro.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="48a0d-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="48a0d-113">Example</span></span>

<span data-ttu-id="48a0d-114">En la siguiente macro se muestra el uso de la acción **AlOcurrirError**.</span><span class="sxs-lookup"><span data-stu-id="48a0d-114">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="48a0d-115">En este ejemplo, la acción **AlOcurrirError** especifica que Access ejecute una macro de tratamiento de errores personalizada denominada ErrorHandler cuando se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="48a0d-115">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="48a0d-116">Cuando se produce un error, se llama la submacro CatchErrors.</span><span class="sxs-lookup"><span data-stu-id="48a0d-116">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="48a0d-117">Si el número de error es 2102, se muestra un mensaje específico y se detiene la ejecución de la macro.</span><span class="sxs-lookup"><span data-stu-id="48a0d-117">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="48a0d-118">De lo contrario, se muestra un mensaje que describe el error y se detiene la macro para que pueda realizar la resolución de problemas adicional.</span><span class="sxs-lookup"><span data-stu-id="48a0d-118">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="48a0d-119">Esta macro mostrará un cuadro de mensaje referente al objeto **ErrorDeMacro** para mostrar información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="48a0d-119">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="48a0d-120">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="48a0d-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
