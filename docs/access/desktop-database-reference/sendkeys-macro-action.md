---
title: EnviarTeclas (acción de macro)
TOCTitle: SendKeys macro action
ms:assetid: 3b06fcfc-ea64-c780-b5fc-6fc72853f524
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192656(v=office.15)
ms:contentKeyID: 48544275
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm183441
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f8c45cdf0d9cf588f61d1b51b728a8a15f6d7e12
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722378"
---
# <a name="sendkeys-macro-action"></a><span data-ttu-id="75d90-102">EnviarTeclas (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="75d90-102">SendKeys macro action</span></span>

<span data-ttu-id="75d90-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="75d90-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Nota de seguridad" alt="Security note" /><span data-ttu-id="75d90-105">de seguridad\*\*</span><span class="sxs-lookup"><span data-stu-id="75d90-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="75d90-p101">
      No use la declaración <strong>SendKeys</strong> ni una macro AutoKeys con información sensible o confidencial porque un usuario malintencionado podría interceptar las pulsaciones de teclas y vulnerar la seguridad de su equipo y de sus datos.
</span><span class="sxs-lookup"><span data-stu-id="75d90-p101">Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75d90-108">Puede usar la acción **EnviarTeclas** para enviar pulsaciones de teclas directamente a Microsoft Access o a una aplicación activa basada en Windows.</span><span class="sxs-lookup"><span data-stu-id="75d90-108">You can use the **SendKeys** action to send keystrokes directly to Microsoft Access or to an active Windows-based application.</span></span>

> [!NOTE]
> <span data-ttu-id="75d90-109">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="75d90-109">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="75d90-110">Configuración</span><span class="sxs-lookup"><span data-stu-id="75d90-110">Setting</span></span>

<span data-ttu-id="75d90-111">La acción **EnviarTeclas** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="75d90-111">The **SendKeys** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75d90-112">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="75d90-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="75d90-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="75d90-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75d90-114"><strong>Pulsaciones de teclas</strong></span><span class="sxs-lookup"><span data-stu-id="75d90-114"><strong>Keystrokes</strong></span></span></p></td>
<td><p><span data-ttu-id="75d90-p102">Las pulsaciones de teclas que van a ser procesadas por Access o por la aplicación. Introduzca las pulsaciones de teclas en el cuadro <strong>Pulsaciones de teclas</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Puede escribir hasta 255 caracteres. Este argumento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="75d90-p102">The keystrokes you want Access or the application to process. Enter the keystrokes in the <strong>Keystrokes</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can type up to 255 characters. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75d90-119"><strong>Wait</strong></span><span class="sxs-lookup"><span data-stu-id="75d90-119"><strong>Wait</strong></span></span></p></td>
<td><p><span data-ttu-id="75d90-p103">Especifica si la macro debe hacer una pausa hasta que las pulsaciones se hayan procesado. Haga clic en <strong>Sí</strong> para hacer una pausa, o en <strong>No</strong> para no hacerla. La opción predeterminada es <strong>No</strong>.</span><span class="sxs-lookup"><span data-stu-id="75d90-p103">Specifies whether the macro should pause until the keystrokes have been processed. Click <strong>Yes</strong> (to pause) or <strong>No</strong> (to not pause). The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="75d90-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="75d90-123">Remarks</span></span>

<span data-ttu-id="75d90-124">Access procesa las pulsaciones que recibe a través de la acción **EnviarTeclas** exactamente como si se hubieran escrito directamente en una ventana de Access.</span><span class="sxs-lookup"><span data-stu-id="75d90-124">Access processes the keystrokes it receives through the **SendKeys** action exactly as if you had typed them directly in an Access window.</span></span>

<span data-ttu-id="75d90-125">Para especificar las pulsaciones, utilice la misma sintaxis que usaría para la instrucción **EnviarTeclas**.</span><span class="sxs-lookup"><span data-stu-id="75d90-125">To specify the keystrokes, use the same syntax as you would for the **SendKeys** statement.</span></span>

> [!NOTE]
> <span data-ttu-id="75d90-126">[!NOTA] Puede ocurrir un error si el argumento **Pulsaciones de teclas** contiene una sintaxis incorrecta, texto mal escrito u otros valores que no sean apropiados para la ventana a la que se envían las pulsaciones.</span><span class="sxs-lookup"><span data-stu-id="75d90-126">An error can occur if the **Keystrokes** argument contains incorrect syntax, misspelled text, or other values that aren't appropriate for the window the keystrokes are sent to.</span></span>

<span data-ttu-id="75d90-p104">Puede usar esta acción para insertar información en un cuadro de diálogo, particularmente si no desea interrumpir la macro para responder de forma manual al cuadro de diálogo. Algunas acciones de Access, como **Imprimir** o **BuscarRegistro**, seleccionan de forma automática las opciones de determinados cuadros de diálogo de uso frecuente. Puede usar la acción **EnviarTeclas** para seleccionar las opciones de los cuadros de diálogo que se usan menos frecuentemente.</span><span class="sxs-lookup"><span data-stu-id="75d90-p104">You can use this action to enter information in a dialog box, particularly if you don't want to interrupt the macro to respond manually to the dialog box. Some Access actions, such as **PrintOut** and **FindRecord**, automatically select the options in certain frequently used dialog boxes. You can use the **SendKeys** action to select the options in less commonly used dialog boxes.</span></span>

> [!NOTE]
> - <span data-ttu-id="75d90-130">Dado que el cuadro de diálogo suspende la macro, se deberá colocar la acción **EnviarTeclas** antes de la acción que abre el cuadro de diálogo, y establecer el argumento **Esperar** en **No**.</span><span class="sxs-lookup"><span data-stu-id="75d90-130">Because the dialog box suspends the macro, you must put the **SendKeys** action before the action that causes the dialog box to open and set the **Wait** argument to **No**.</span></span>
> - <span data-ttu-id="75d90-p105">El momento en que las pulsaciones de teclas llegan a Access o a otra aplicación puede no ser el adecuado. Por ello, se recomienda que, si existe otro método (como la acción **BuscarRegistro** ) disponible para realizar la tarea deseada, se utilice en vez de usar la acción **EnviarTeclas** para rellenar las opciones de cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="75d90-p105">The timing of the keystrokes reaching Access or another application can be tricky. As a result, it's recommended that if there's some other method (such as the **FindRecord** action) you can use to achieve a desired task, use that method rather than using the **SendKeys** action to fill in the options in a dialog box.</span></span>

<span data-ttu-id="75d90-133">Si desea enviar más de 255 caracteres a Access o a cualquier otra aplicación basada en Windows, puede utilizar varias acciones **EnviarTeclas** seguidas en una macro.</span><span class="sxs-lookup"><span data-stu-id="75d90-133">If you want to send more than 255 characters to Access or another Windows-based application, you can use several **SendKeys** actions in succession in a macro.</span></span>

<span data-ttu-id="75d90-p106">El uso de la acción **EnviarTeclas** para enviar pulsaciones de teclado desencadena los correspondientes eventos **KeyDown**, **KeyUp** y **KeyPress**. El envío de pulsaciones de teclas no ANSI (como una tecla de función) no desencadena el evento **KeyPress**.</span><span class="sxs-lookup"><span data-stu-id="75d90-p106">Using the **SendKeys** action to send keystrokes triggers the appropriate **KeyDown**, **KeyUp**, and **KeyPress** events. Sending non-ANSI keystrokes (such as a function key) doesn't trigger the **KeyPress** event.</span></span>

<span data-ttu-id="75d90-p107">Esta acción no está disponible en un módulo de Visual Basic para Aplicaciones (VBA). En su lugar, utilice la instrucción **EnviarTeclas**.</span><span class="sxs-lookup"><span data-stu-id="75d90-p107">This action isn't available from a Visual Basic for Applications (VBA) module. Use the **SendKeys** statement instead.</span></span>

