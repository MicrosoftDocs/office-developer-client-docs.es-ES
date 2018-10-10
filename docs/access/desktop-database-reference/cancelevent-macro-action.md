---
title: CancelarEvento (acción de macro)
TOCTitle: CancelEvent Macro Action
ms:assetid: d9d3ea99-c9fb-2524-c570-e3ee6d20af98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835110(v=office.15)
ms:contentKeyID: 48548066
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm78430
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 52822d45b30c631dcabe3c38b6722398e96f489f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485885"
---
# <a name="cancelevent-macro-action"></a><span data-ttu-id="403f9-102">CancelarEvento (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="403f9-102">CancelEvent Macro Action</span></span>


<span data-ttu-id="403f9-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="403f9-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="403f9-104">Puede usar la acción **CancelarEvento** para cancelar el evento que causó que Access ejecutar la macro que contiene esta acción.</span><span class="sxs-lookup"><span data-stu-id="403f9-104">You can use the **CancelEvent** action to cancel the event that caused Access to run the macro containing this action.</span></span> <span data-ttu-id="403f9-105">El nombre de la macro es el valor de una propiedad de evento como **BeforeUpdate**, **OnOpen**, **OnUnload** u **OnPrint**.</span><span class="sxs-lookup"><span data-stu-id="403f9-105">The macro name is the setting of an event property such as **BeforeUpdate**, **OnOpen**, **OnUnload**, or **OnPrint**.</span></span>

## <a name="setting"></a><span data-ttu-id="403f9-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="403f9-106">Setting</span></span>

<span data-ttu-id="403f9-107">La acción **CancelarEvento** no tiene argumentos.</span><span class="sxs-lookup"><span data-stu-id="403f9-107">The **CancelEvent** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="403f9-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="403f9-108">Remarks</span></span>

<span data-ttu-id="403f9-p102">En un formulario, suele utilizarse la acción **CancelarEvento** en una macro de validación con la propiedad de evento **BeforeUpdate**. Cuando un usuario escribe datos en un control o en un registro, Access ejecuta la macro antes de agregar los datos a la base de datos. Si los datos no pasan las condiciones de validación de la macro, la acción **CancelarEvento** cancela el proceso de actualización antes de que se inicie.</span><span class="sxs-lookup"><span data-stu-id="403f9-p102">In a form, you typically use the **CancelEvent** action in a validation macro with the **BeforeUpdate** event property. When a user enters data in a control or record, Access runs the macro before adding the data to the database. If the data fails the validation conditions in the macro, the **CancelEvent** action cancels the update process before it starts.</span></span>

<span data-ttu-id="403f9-112">A menudo, esta acción se usa con la acción **CuadroDeMensaje** para indicar que los datos no han pasado las condiciones de validación y para proporcionar información útil sobre la clase de datos que debe especificarse.</span><span class="sxs-lookup"><span data-stu-id="403f9-112">Often, you use this action with the **MessageBox** action to indicate that the data has failed the validation conditions and to provide helpful information about the kind of data that should be entered.</span></span>

<span data-ttu-id="403f9-113">La acción **CancelarEvento** puede cancelar los eventos siguientes.</span><span class="sxs-lookup"><span data-stu-id="403f9-113">The following events can be canceled by the **CancelEvent** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="403f9-114"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="403f9-114"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="403f9-115"><strong>Dirty</strong></span><span class="sxs-lookup"><span data-stu-id="403f9-115"><strong>Dirty</strong></span></span></p></td>
<td><p><span data-ttu-id="403f9-116"><strong>MouseDown</strong></span><span class="sxs-lookup"><span data-stu-id="403f9-116"><strong>MouseDown</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="403f9-117"><strong>BeforeDelConfirm</strong></span><span class="sxs-lookup"><span data-stu-id="403f9-117"><strong>BeforeDelConfirm</strong></span></span></p></td>
<td><p><span data-ttu-id="403f9-118"><strong>Salir</strong></span><span class="sxs-lookup"><span data-stu-id="403f9-118"><strong>Exit</strong></span></span></p></td>
<td><p><span data-ttu-id="403f9-119"><strong>NoData</strong></span><span class="sxs-lookup"><span data-stu-id="403f9-119"><strong>NoData</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="403f9-120"><strong>BeforeInsert</strong></span><span class="sxs-lookup"><span data-stu-id="403f9-120"><strong>BeforeInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="403f9-121"><strong>Filter</strong></span><span class="sxs-lookup"><span data-stu-id="403f9-121"><strong>Filter</strong></span></span></p></td>
<td><p><span data-ttu-id="403f9-122"><strong>Open</strong></span><span class="sxs-lookup"><span data-stu-id="403f9-122"><strong>Open</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="403f9-123"><strong>BeforeUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="403f9-123"><strong>BeforeUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="403f9-124"><strong>Formato</strong></span><span class="sxs-lookup"><span data-stu-id="403f9-124"><strong>Format</strong></span></span></p></td>
<td><p><span data-ttu-id="403f9-125"><strong>Print</strong></span><span class="sxs-lookup"><span data-stu-id="403f9-125"><strong>Print</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="403f9-126"><strong>DblClick</strong></span><span class="sxs-lookup"><span data-stu-id="403f9-126"><strong>DblClick</strong></span></span></p></td>
<td><p><span data-ttu-id="403f9-127"><strong>KeyPress</strong></span><span class="sxs-lookup"><span data-stu-id="403f9-127"><strong>KeyPress</strong></span></span></p></td>
<td><p><span data-ttu-id="403f9-128"><strong>Unload</strong></span><span class="sxs-lookup"><span data-stu-id="403f9-128"><strong>Unload</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="403f9-129"><strong>Delete</strong></span><span class="sxs-lookup"><span data-stu-id="403f9-129"><strong>Delete</strong></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="403f9-130">[!NOTA] Puede usar la acción <STRONG>CancelarEvento</STRONG> con el evento <STRONG>BajarMouse</STRONG> sólo para cancelar el evento que se produce al hacer clic con el botón secundario en un objeto.</span><span class="sxs-lookup"><span data-stu-id="403f9-130">You can use the <STRONG>CancelEvent</STRONG> action with the <STRONG>MouseDown</STRONG> event only to cancel the event that occurs when you right-click an object.</span></span></P>



<span data-ttu-id="403f9-131">Si la configuración de la propiedad de evento **AlHacerDobleClic** de un control especifica una macro que contiene la acción **CancelarEvento**, la acción cancela el evento **HacerDobleClic**.</span><span class="sxs-lookup"><span data-stu-id="403f9-131">If a control's **OnDblClick** event property setting specifies a macro containing the **CancelEvent** action, the action cancels the **DblClick** event.</span></span>

<span data-ttu-id="403f9-p103">Para los eventos que pueden cancelarse, el comportamiento predeterminado para el evento (es decir, lo que generalmente hace Access cuando ocurre un evento) se produce después de que se ejecuta la macro para el evento. Esto permite cancelar el comportamiento predeterminado. Por ejemplo, cuando hace doble clic en una palabra en la que está el punto de inserción en un cuadro de texto, Access en general selecciona la palabra. Puede cancelar este comportamiento predeterminado en una macro para el evento **HacerDobleClic** y realizar alguna otra acción, como abrir un formulario que contenga información acerca de los datos en el cuadro de texto. Para eventos que se pueden cancelar, el comportamiento predeterminado se produce antes de que se ejecuta la macro.</span><span class="sxs-lookup"><span data-stu-id="403f9-p103">For events that can be canceled, the default behavior for the event (that is, what Access typically does when the event occurs) occurs after the macro for the event runs. This enables you to cancel the default behavior. For example, when you double-click a word that the insertion point is on in a text box, Access normally selects the word. You can cancel this default behavior in the macro for the **DblClick** event and perform some other action, such as opening a form containing information about the data in the text box. For events that can't be canceled, the default behavior occurs before the macro runs.</span></span>


> [!NOTE]
> <P><span data-ttu-id="403f9-p104">[!NOTA] Si la propiedad de evento <STRONG>AlDescargar</STRONG> de un formulario especifica una macro que lleva a cabo la acción <STRONG>CancelarEvento</STRONG>, no podrá cerrar el formulario. Debe corregir la condición que generó la acción <STRONG>CancelarEvento</STRONG> o abrir la macro y eliminar la acción <STRONG>CancelarEvento</STRONG>. Si el formulario es modal, no podrá abrir la macro.</span><span class="sxs-lookup"><span data-stu-id="403f9-p104">If a form's <STRONG>OnUnload</STRONG> event property specifies a macro that carries out a <STRONG>CancelEvent</STRONG> action, you won't be able to close the form. You must either correct the condition that caused the <STRONG>CancelEvent</STRONG> action to be carried out or open the macro and delete the <STRONG>CancelEvent</STRONG> action. If the form is a modal form, you won't be able to open the macro.</span></span></P>



<span data-ttu-id="403f9-140">Para llevar a cabo la acción **CancelarEvento** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **CancelEvent** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="403f9-140">To carry out the **CancelEvent** action in a Visual Basic for Applications (VBA) module, use the **CancelEvent** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="403f9-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="403f9-141">Example</span></span>

<span data-ttu-id="403f9-142"> Validar datos con una macro</span><span class="sxs-lookup"><span data-stu-id="403f9-142">Validate data by using a macro</span></span>

<span data-ttu-id="403f9-p105">La siguiente macro de validación comprueba los códigos postales especificados en un formulario Proveedores. Muestra el uso de las acciones **DetenerMacro**, **CuadroDeMensaje**, **CancelarEvento** y **IrAControl**. Una expresión condicional comprueba el país o la región y el código postal especificados en un registro del formulario. Si el código postal no tiene el formato correcto para el país o la región, la macro muestra un cuadro de mensaje y cancela el proceso de guardar el registro. Después, lleva al usuario hasta el control CódigoPostal, donde puede corregir el error. Esta macro debe asociarse a la propiedad **AntesDeActualizar** del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="403f9-p105">The following validation macro checks the postal codes entered in a Suppliers form. It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions. A conditional expression checks the country/region and postal code entered in a record on the form. If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record. It then returns you to the Postal Code control, where you can correct the error. This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="403f9-149">Condición</span><span class="sxs-lookup"><span data-stu-id="403f9-149">Condition</span></span></p></th>
<th><p><span data-ttu-id="403f9-150">Acción</span><span class="sxs-lookup"><span data-stu-id="403f9-150">Action</span></span></p></th>
<th><p><span data-ttu-id="403f9-151">Argumentos: Configuración</span><span class="sxs-lookup"><span data-stu-id="403f9-151">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="403f9-152">Comentario</span><span class="sxs-lookup"><span data-stu-id="403f9-152">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="403f9-153">IsNull([PaísRegión])</span><span class="sxs-lookup"><span data-stu-id="403f9-153">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="403f9-154">StopMacro</span><span class="sxs-lookup"><span data-stu-id="403f9-154">StopMacro</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="403f9-155">Si PaísRegión es <strong>Nulo</strong>, no se podrá validar el código postal.</span><span class="sxs-lookup"><span data-stu-id="403f9-155">If CountryRegion is <strong>Null</strong>, postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="403f9-156">[PaísRegión] En (&quot;Francia&quot;,&quot;Italia&quot;,&quot;España&quot;) y longitud ([CódigoPostal]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="403f9-156">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="403f9-157">MessageBox</span><span class="sxs-lookup"><span data-stu-id="403f9-157">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="403f9-158">Mensaje: el código postal debe tener 5 caracteres. 

</span><span class="sxs-lookup"><span data-stu-id="403f9-158">Message: The postal code must be 5 characters.</span></span> <span data-ttu-id="403f9-159">Bip: <strong>Sí</strong> tipo: <strong>información</strong> título: Error de código Postal</span><span class="sxs-lookup"><span data-stu-id="403f9-159">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="403f9-160">Si el código postal no tiene 5 caracteres, mostrar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="403f9-160">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="403f9-161">...</span><span class="sxs-lookup"><span data-stu-id="403f9-161"></span></span></p></td>
<td><p><span data-ttu-id="403f9-162">CancelarEvento</span><span class="sxs-lookup"><span data-stu-id="403f9-162">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="403f9-163">Cancelar el evento.</span><span class="sxs-lookup"><span data-stu-id="403f9-163">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="403f9-164">GoToControl</span><span class="sxs-lookup"><span data-stu-id="403f9-164">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="403f9-165">Nombre del control: CódigoPostal</span><span class="sxs-lookup"><span data-stu-id="403f9-165">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="403f9-166">[PaísRegión] En (&quot;Australia&quot;,&quot;Singapur&quot;) y longitud ([CódigoPostal]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="403f9-166">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="403f9-167">MessageBox</span><span class="sxs-lookup"><span data-stu-id="403f9-167">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="403f9-168">Mensaje: el código postal debe tener 4 caracteres. 

</span><span class="sxs-lookup"><span data-stu-id="403f9-168">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="403f9-169">Bip: <strong>Sí</strong> tipo: <strong>información</strong> título: Error de código Postal</span><span class="sxs-lookup"><span data-stu-id="403f9-169">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="403f9-170">Si el código postal no tiene 4 caracteres, mostrar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="403f9-170">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="403f9-171">...</span><span class="sxs-lookup"><span data-stu-id="403f9-171"></span></span></p></td>
<td><p><span data-ttu-id="403f9-172">CancelarEvento</span><span class="sxs-lookup"><span data-stu-id="403f9-172">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="403f9-173">Cancelar el evento.</span><span class="sxs-lookup"><span data-stu-id="403f9-173">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="403f9-174">GoToControl</span><span class="sxs-lookup"><span data-stu-id="403f9-174">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="403f9-175">Nombre del control: CódigoPostal</span><span class="sxs-lookup"><span data-stu-id="403f9-175">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="403f9-176">([PaísRegión] = &quot;Canadá&quot;) Y ([CódigoPostal] no le gusta&quot;[A-z] [0-9] [A-z] [0-9] [A-z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="403f9-176">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="403f9-177">MessageBox</span><span class="sxs-lookup"><span data-stu-id="403f9-177">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="403f9-178">Mensaje: El código postal no es válido.</span><span class="sxs-lookup"><span data-stu-id="403f9-178">Message: The postal code is not valid.</span></span> <span data-ttu-id="403f9-179">Ejemplo de código de Canadá: H1J 1C3 Bip: <strong>Sí</strong> tipo: <strong>información</strong> título: Error de código Postal</span><span class="sxs-lookup"><span data-stu-id="403f9-179">Example of Canadian code: H1J 1C3 Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="403f9-p109">Si el código postal no es correcto para Canadá, mostrar un mensaje. (Ejemplo de código canadiense: H1J 1C3)</span><span class="sxs-lookup"><span data-stu-id="403f9-p109">If the postal code isn't correct for Canada, display a message. (Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="403f9-182">...</span><span class="sxs-lookup"><span data-stu-id="403f9-182"></span></span></p></td>
<td><p><span data-ttu-id="403f9-183">CancelarEvento</span><span class="sxs-lookup"><span data-stu-id="403f9-183">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="403f9-184">Cancelar el evento.</span><span class="sxs-lookup"><span data-stu-id="403f9-184">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

