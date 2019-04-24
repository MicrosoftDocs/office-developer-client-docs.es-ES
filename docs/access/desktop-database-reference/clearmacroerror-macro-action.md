---
title: BorrarErrorDeMacro (acción de macro)
TOCTitle: ClearMacroError macro action
ms:assetid: 1091747e-e957-38c6-6454-5169f091323e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845338(v=office.15)
ms:contentKeyID: 48543296
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm109100
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f42386674ff76d550fb47a971860b4e1a5905236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296377"
---
# <a name="clearmacroerror-macro-action"></a><span data-ttu-id="822bd-102">BorrarErrorDeMacro (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="822bd-102">ClearMacroError macro action</span></span>


<span data-ttu-id="822bd-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="822bd-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="822bd-104">Puede usar la acción **BorrarErrorDeMacro** para borrar la información acerca de un error que está almacenado en el objeto **ErrorDeMacro**.</span><span class="sxs-lookup"><span data-stu-id="822bd-104">You can use the **ClearMacroError** action to clear information about an error that is stored in the **MacroError** object.</span></span>

## <a name="setting"></a><span data-ttu-id="822bd-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="822bd-105">Setting</span></span>

<span data-ttu-id="822bd-106">La acción **BorrarErrorDeMacro** no tiene argumentos.</span><span class="sxs-lookup"><span data-stu-id="822bd-106">The **ClearMacroError** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="822bd-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="822bd-107">Remarks</span></span>

- <span data-ttu-id="822bd-108">Cuando se produce un error en una macro, se almacena información sobre el error en el objeto **ErrorDeMacro**.</span><span class="sxs-lookup"><span data-stu-id="822bd-108">When an error occurs in a macro, information about the error is stored in the **MacroError** object.</span></span> <span data-ttu-id="822bd-109">Si no ha usado la acción **[AlOcurrirError](onerror-macro-action.md)** para suprimir los mensajes de error, la macro se detiene y la información de error se muestra en un mensaje de error estándar.</span><span class="sxs-lookup"><span data-stu-id="822bd-109">If you have not used the **[OnError](onerror-macro-action.md)** action to suppress error messages, the macro stops and the error information is displayed in a standard error message.</span></span> <span data-ttu-id="822bd-110">Sin embargo, si ha usado la acción **AlOcurrirError** para suprimir los mensajes de error, es posible que desee usar la información almacenada en el objeto **ErrorDeMacro** en una condición o en un mensaje de error personalizado.</span><span class="sxs-lookup"><span data-stu-id="822bd-110">However, if you have used the **OnError** action to suppress error messages, you might want to use the information stored in the **MacroError** object in a condition or in a custom error message.</span></span>
    
  <span data-ttu-id="822bd-p102">Una vez controlado un error, la información almacenada en el objeto **ErrorDeMacro** ya no está actualizada, por lo que se recomienda borrar el objeto mediante la acción **BorrarErrorDeMacro**. De este modo, se restablece en 0 el número de error almacenado en el objeto **ErrorDeMacro** y se borra cualquier otra información sobre el error que esté almacenada en el objeto, como la descripción del error, el nombre de la macro, el nombre de la acción, la condición y los argumentos. Esto permite volver a examinar más adelante el objeto **ErrorDeMacro** para comprobar si se ha producido otro error.</span><span class="sxs-lookup"><span data-stu-id="822bd-p102">After an error has been handled, the information in the **MacroError** object is out of date, so it is a good idea to clear the object by using the **ClearMacroError** action. Doing so resets the error number in the **MacroError** object to 0 and clears any other information about the error that is stored in the object, such as the error description, macro name, action name, condition, and arguments. This way, you can inspect the **MacroError** object again later to see if another error has occurred.</span></span>

- <span data-ttu-id="822bd-114">El objeto **ErrorDeMacro** se borra automáticamente cuando finaliza cualquier macro, de modo que no necesita utilizar la acción **BorrarErrorDeMacro** al finalizar una macro.</span><span class="sxs-lookup"><span data-stu-id="822bd-114">The **MacroError** object is automatically cleared when any macro ends, so you do not need to use the **ClearMacroError** action at the end of a macro.</span></span>

- <span data-ttu-id="822bd-p103">El objeto **ErrorDeMacro** contiene información referente a un solo error a la vez. Si se ha producido más de un error en una macro, el objeto **ErrorDeMacro** contiene solo la información sobre el último error.</span><span class="sxs-lookup"><span data-stu-id="822bd-p103">The **MacroError** object contains information about only one error at a time. If more than one error has occurred in a macro, the **MacroError** object contains information only about the last error.</span></span>

- <span data-ttu-id="822bd-117">Para ejecutar la acción **BorrarErrorDeMacro** en un módulo de VBA, utilice el método **BorrarErrorDeMacro** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="822bd-117">To run the **ClearMacroError** action in a VBA module, use the **ClearMacroError** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="822bd-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="822bd-118">Example</span></span>

<span data-ttu-id="822bd-119">En la siguiente macro se usa la acción **AlOcurrirError** con el argumento **Siguiente** para suprimir los mensajes de error y, a continuación, se usa la acción **AbrirFormulario** para abrir un formulario.</span><span class="sxs-lookup"><span data-stu-id="822bd-119">The following macro uses the **OnError** action with the **Next** argument to suppress error messages, and then uses the **OpenForm** action to open a form.</span></span> <span data-ttu-id="822bd-120">Para este ejemplo, se crea deliberadamente un error usando la acción **IrARegistro** para ir al registro anterior.</span><span class="sxs-lookup"><span data-stu-id="822bd-120">For this example, an error is deliberately created by using the **GoToRecord** action to go to the previous record.</span></span> <span data-ttu-id="822bd-121">La condición \*\* \[ErrorDeMacro\].\[ \>Número\]\<0\*\* prueba el objeto **ErrorDeMacro** .</span><span class="sxs-lookup"><span data-stu-id="822bd-121">The condition **\[MacroError\].\[Number\]\<\>0** tests the **MacroError** object.</span></span> <span data-ttu-id="822bd-122">Si se genera un error, su número no es cero y se ejecuta la acción **CuadroDeMensaje**.</span><span class="sxs-lookup"><span data-stu-id="822bd-122">If an error has occurred, the error number is non-zero, and the **MessageBox** action runs.</span></span> <span data-ttu-id="822bd-123">En el cuadro de mensaje aparece el nombre de la acción que causó el error (en este caso, la acción **IrARegistro** ) y se muestra el número de error.</span><span class="sxs-lookup"><span data-stu-id="822bd-123">The message box displays the name of the action that caused the error (in this case, the **GoToRecord** action), and the error number is displayed.</span></span> <span data-ttu-id="822bd-124">Por último, al ejecutarse la acción **BorrarErrorDeMacro** se borra el objeto **ErrorDeMacro**.</span><span class="sxs-lookup"><span data-stu-id="822bd-124">Finally, running the **ClearMacroError** action clears the **MacroError** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="822bd-125">Condición</span><span class="sxs-lookup"><span data-stu-id="822bd-125">Condition</span></span></p></th>
<th><p><span data-ttu-id="822bd-126">Acción</span><span class="sxs-lookup"><span data-stu-id="822bd-126">Action</span></span></p></th>
<th><p><span data-ttu-id="822bd-127">Argumentos</span><span class="sxs-lookup"><span data-stu-id="822bd-127">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="822bd-128"><strong>OnError</strong></span><span class="sxs-lookup"><span data-stu-id="822bd-128"><strong>OnError</strong></span></span></p></td>
<td><p><span data-ttu-id="822bd-129"><strong>Ir a</strong>: <strong>Siguiente</strong></span><span class="sxs-lookup"><span data-stu-id="822bd-129"><strong>Go to</strong>: <strong>Next</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="822bd-130"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="822bd-130"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="822bd-131"><strong>Nombre del formulario</strong>: CategoryForm<strong>View</strong>: <strong>FormWindow Mode</strong>: <strong>normal</strong></span><span class="sxs-lookup"><span data-stu-id="822bd-131"><strong>Form Name</strong>: CategoryForm<strong>View</strong>: <strong>FormWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="822bd-132"><strong>GoToRecord</strong></span><span class="sxs-lookup"><span data-stu-id="822bd-132"><strong>GoToRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="822bd-133"><strong>Tipo de objeto</strong>: <strong>formularionombre Name</strong>: CategoryForm<strong>Record</strong>: Previous</span><span class="sxs-lookup"><span data-stu-id="822bd-133"><strong>Object Type</strong>: <strong>FormObject Name</strong>: CategoryForm<strong>Record</strong>: Previous</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="822bd-134">[ErrorDeMacro]. Números &lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="822bd-134">[MacroError].[Number]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="822bd-135"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="822bd-135"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="822bd-136"><strong>Mensaje</strong>: =&quot;error # &quot; &amp; [ErrorDeMacro]. Números &amp; en &quot; [ &amp; ErrorDeMacro]. &quot; ActionName &amp; &quot; acción. &quot; <strong>Bip</strong>: <strong>SíTipo</strong>: información</span><span class="sxs-lookup"><span data-stu-id="822bd-136"><strong>Message</strong>: =&quot;Error # &quot; &amp; [MacroError].[Number] &amp; &quot; on &quot; &amp; [MacroError].[ActionName] &amp; &quot; action.&quot;<strong>Beep</strong>: <strong>YesType</strong>: Information</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="822bd-137"><strong>ClearMacroError</strong></span><span class="sxs-lookup"><span data-stu-id="822bd-137"><strong>ClearMacroError</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

