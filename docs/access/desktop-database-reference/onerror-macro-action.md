---
title: AlOcurrirError (acción de macro)
TOCTitle: OnError Macro Action
ms:assetid: 5c6073c4-2c0f-0ed2-83b0-477636e2d81c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194562(v=office.15)
ms:contentKeyID: 48545088
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62274
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b27ffa119d37cd7ddf80292acd9a1e1e131b0359
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484805"
---
# <a name="onerror-macro-action"></a><span data-ttu-id="53dbb-102">AlOcurrirError (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="53dbb-102">OnError Macro Action</span></span>

<span data-ttu-id="53dbb-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="53dbb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="53dbb-104">Puede usar la acción **AlOcurrirError** para especificar lo que va a ocurrir cuando se produce un error en una macro.</span><span class="sxs-lookup"><span data-stu-id="53dbb-104">You can use the **OnError** action to specify what should happen when an error occurs in a macro.</span></span>

## <a name="setting"></a><span data-ttu-id="53dbb-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="53dbb-105">Setting</span></span>

<span data-ttu-id="53dbb-106">La acción **AlOcurrirError** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="53dbb-106">The **OnError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53dbb-107">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="53dbb-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="53dbb-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="53dbb-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53dbb-109">Ir a</span><span class="sxs-lookup"><span data-stu-id="53dbb-109">Go to</span></span></p></td>
<td><p><span data-ttu-id="53dbb-p101">Permite especificar el comportamiento general que debe producirse cuando se detecta un error. Haga clic en la flecha desplegable y, a continuación, haga clic en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="53dbb-p101">Specify the general behavior that should occur when an error is encountered. Click the drop-down arrow and then click one of the following settings:</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53dbb-112">Configuración</span><span class="sxs-lookup"><span data-stu-id="53dbb-112">Setting</span></span></p></th>
<th><p><span data-ttu-id="53dbb-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="53dbb-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53dbb-114"><strong>Siguiente</strong></span><span class="sxs-lookup"><span data-stu-id="53dbb-114"><strong>Next</strong></span></span></p></td>
<td><p><span data-ttu-id="53dbb-p102">Microsoft Office Access 2007 registra los detalles del error en el objeto <strong>ErrorDeMacro</strong> pero no detiene la macro. La macro continúa con la siguiente acción.</span><span class="sxs-lookup"><span data-stu-id="53dbb-p102">Microsoft Office Access 2007 records the details of the error in the <strong>MacroError</strong> object but does not stop the macro. The macro continues with the next action.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53dbb-117"><strong>Nombre de macro</strong></span><span class="sxs-lookup"><span data-stu-id="53dbb-117"><strong>Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="53dbb-118">Access detiene la macro actual y ejecuta la macro especificada en el argumento <strong>Nombre de macro</strong>.</span><span class="sxs-lookup"><span data-stu-id="53dbb-118">Access stops the current macro and runs the macro that is named in the <strong>Macro Name</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53dbb-119"><strong>Fail</strong></span><span class="sxs-lookup"><span data-stu-id="53dbb-119"><strong>Fail</strong></span></span></p></td>
<td><p><span data-ttu-id="53dbb-120">Access detiene la macro actual y muestra un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="53dbb-120">Access stops the current macro and displays an error message.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53dbb-121">Nombre de macro</span><span class="sxs-lookup"><span data-stu-id="53dbb-121">Macro Name</span></span></p></td>
<td><p><span data-ttu-id="53dbb-122">Si el argumento Ir a está establecido en nombre de Macro, escriba el nombre de la macro que se usará para el tratamiento de errores.</span><span class="sxs-lookup"><span data-stu-id="53dbb-122">If the Go to argument is set to Macro Name, type the name of the macro to be used for error handling.</span></span> <span data-ttu-id="53dbb-123">El nombre que escriba debe coincidir con un nombre en la columna <strong>Nombre de Macro</strong> de la macro actual; no se puede escribir el nombre de un objeto de macro diferente.</span><span class="sxs-lookup"><span data-stu-id="53dbb-123">The name you type must match a name in the <strong>Macro Name</strong> column of the current macro; you can't enter the name of a different macro object.</span></span> <span data-ttu-id="53dbb-124">En el ejemplo siguiente, la macro <strong>ErrorHandler</strong> se encuentra en el mismo objeto de macro que la acción <strong>AlOcurrirError</strong> .</span><span class="sxs-lookup"><span data-stu-id="53dbb-124">In the example below, the <strong>ErrorHandler</strong> macro is contained in the same macro object as the <strong>OnError</strong> action.</span></span> <span data-ttu-id="53dbb-125">Este argumento debe mantenerse en blanco si el argumento Ir a está establecido en <strong>siguiente</strong> o <strong>producirá un error</strong>.</span><span class="sxs-lookup"><span data-stu-id="53dbb-125">This argument must be left blank if the Go to argument is set to <strong>Next</strong> or <strong>Fail</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="53dbb-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53dbb-126">Remarks</span></span>

- <span data-ttu-id="53dbb-p104">La acción **AlOcurrirError** suele situarse al comienzo de una macro, si bien se puede colocar también más adelante. Las reglas establecidas por la acción se harán efectivas cuando se ejecute la acción.</span><span class="sxs-lookup"><span data-stu-id="53dbb-p104">The **OnError** action is usually placed at the beginning of a macro, but you can also place the action later in the macro. The rules established by the action will take effect whenever the action is run.</span></span>

- <span data-ttu-id="53dbb-p105">Si se establece el argumento Ir a en **Error**, Access se comporta de la misma manera que se comportaría si no hubiera ninguna acción **AlOcurrirError** en la macro. Es decir, si se detecta un error, Access detiene la macro y muestra un mensaje de error estándar. El valor **Error** se usa principalmente para desactivar el tratamiento de errores establecido anteriormente en una macro.</span><span class="sxs-lookup"><span data-stu-id="53dbb-p105">If you set the Go to argument to **Fail**, Access behaves the same way it would if there were no **OnError** action in the macro. That is, if an error is encountered, Access stops the macro and displays a standard error message. The main use for the **Fail** setting is to turn off any error handling that you established earlier in a macro.</span></span>

## <a name="example"></a><span data-ttu-id="53dbb-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53dbb-132">Example</span></span>

<span data-ttu-id="53dbb-133">En la siguiente macro se muestra el uso de la acción **AlOcurrirError**.</span><span class="sxs-lookup"><span data-stu-id="53dbb-133">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="53dbb-134">En este ejemplo, la acción **AlOcurrirError** especifica que Access ejecute una macro de tratamiento de errores personalizada denominada ErrorHandler cuando se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="53dbb-134">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="53dbb-135">Cuando se produce un error, se llama la submacro CatchErrors.</span><span class="sxs-lookup"><span data-stu-id="53dbb-135">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="53dbb-136">Si el número de error es 2102, se muestra un mensaje específico y se detiene la ejecución de la macro.</span><span class="sxs-lookup"><span data-stu-id="53dbb-136">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="53dbb-137">De lo contrario, se muestra un mensaje que describe el error y se detiene la macro para que pueda realizar la resolución de problemas adicional.</span><span class="sxs-lookup"><span data-stu-id="53dbb-137">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="53dbb-138">Esta macro mostrará un cuadro de mensaje referente al objeto **ErrorDeMacro** para mostrar información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="53dbb-138">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="53dbb-139">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="53dbb-139">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
