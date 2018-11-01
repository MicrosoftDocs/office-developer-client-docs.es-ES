---
title: Acción de macro MessageBox
TOCTitle: MessageBox Macro Action
ms:assetid: 326a0e68-38fb-4f81-b319-5a70caa5aec4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192304(v=office.15)
ms:contentKeyID: 48544077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6654d2994b472ff2d495b60fffd5fcdbd6e58089
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885237"
---
# <a name="messagebox-macro-action"></a><span data-ttu-id="7adf9-102">Acción de macro MessageBox</span><span class="sxs-lookup"><span data-stu-id="7adf9-102">MessageBox Macro Action</span></span>


<span data-ttu-id="7adf9-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7adf9-103">**Applies to**: Access 2013, Office 2013</span></span>




<span data-ttu-id="7adf9-p101">Puede usar la acción **CuadroDeMensajes** para mostrar un cuadro de mensaje que contenga una advertencia o un mensaje informativo. Por ejemplo, puede usar la acción **CuadroDeMensajes** con macros de validación. Cuando un control o un registro produce un error en una condición de validación de la macro, un cuadro de mensaje puede mostrar un mensaje de error y proporcionar instrucciones sobre el tipo de datos que se debe introducir.</span><span class="sxs-lookup"><span data-stu-id="7adf9-p101">You can use the **MessageBox** action to display a message box containing a warning or an informational message. For example, you can use the **MessageBox** action with validation macros. When a control or record fails a validation condition in the macro, a message box can display an error message and provide instructions about the kind of data that should be entered.</span></span>

## <a name="setting"></a><span data-ttu-id="7adf9-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="7adf9-107">Setting</span></span>

<span data-ttu-id="7adf9-108">La acción **CuadroDeMensajes** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="7adf9-108">The **MessageBox** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7adf9-109">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="7adf9-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="7adf9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7adf9-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7adf9-111"><strong>Mensaje</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-111"><strong>Message</strong></span></span></p></td>
<td><p><span data-ttu-id="7adf9-p102">El texto del mensaje de texto. Introduzca el texto del mensaje en el cuadro <strong>Mensaje</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Puede escribir hasta 255 caracteres o introducir una expresión (precedida de un signo de igual).  </span><span class="sxs-lookup"><span data-stu-id="7adf9-p102">The text in the message box. Enter the message text in the <strong>Message</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can type up to 255 characters or enter an expression (preceded by an equal sign).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7adf9-115"><strong>Sonido</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-115"><strong>Beep</strong></span></span></p></td>
<td><p><span data-ttu-id="7adf9-p103">Especifica si el altavoz del equipo emite un sonido al mostrar el mensaje. Haga clic en <strong>Sí</strong> (emitir el sonido) o <strong>No</strong> (no emitir el sonido). El valor predeterminado es <strong>Sí</strong>.  </span><span class="sxs-lookup"><span data-stu-id="7adf9-p103">Specifies whether your computer's speaker sounds a beep tone when the message displays. Click <strong>Yes</strong> (sound the beep tone) or <strong>No</strong> (don't sound the beep tone). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7adf9-119"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-119"><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="7adf9-p104">El tipo de cuadro de mensaje. Cada tipo tiene un icono distinto. Haga clic en <strong>Ninguno</strong>, <strong>Crítico</strong>, <strong>¿Advertencia?</strong>, <strong>Advertencia</strong> o <strong>Información</strong>. El valor predeterminado es <strong>Ninguno</strong>.  </span><span class="sxs-lookup"><span data-stu-id="7adf9-p104">The type of message box. Each type has a different icon. Click <strong>None</strong>, <strong>Critical</strong>, <strong>Warning?</strong>, <strong>Warning!</strong>, or <strong>Information</strong>. The default is <strong>None</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7adf9-124"><strong>Título</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-124"><strong>Title</strong></span></span></p></td>
<td><p><span data-ttu-id="7adf9-125">El texto que se muestra en la barra de título del cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="7adf9-125">The text displayed in the message box title bar.</span></span> <span data-ttu-id="7adf9-126">Por ejemplo, puede tener la visualización de la barra de título &quot;validación del identificador de cliente&quot;.</span><span class="sxs-lookup"><span data-stu-id="7adf9-126">For example, you can have the title bar display &quot;Customer ID Validation&quot;.</span></span> <span data-ttu-id="7adf9-127">Si deja este argumento en blanco, &quot;Microsoft Access&quot; se muestra.</span><span class="sxs-lookup"><span data-stu-id="7adf9-127">If you leave this argument blank, &quot;Microsoft Access&quot; is displayed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7adf9-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7adf9-128">Remarks</span></span>

<span data-ttu-id="7adf9-p106">Puede usar la acción **CuadroDeMensajes** para crear un mensaje de error con formato parecido a los mensajes de error integrados que muestra Microsoft Access. La acción **CuadroDeMensajes** permite proporcionar un mensaje en tres secciones para el argumento Mensaje. Las secciones se separan mediante el carácter "@".</span><span class="sxs-lookup"><span data-stu-id="7adf9-p106">You can use the **MessageBox** action to create a formatted error message similar to built-in error messages displayed by Microsoft Access. The **MessageBox** action permits you to supply a message in three sections for the Message argument. You separate the sections with the "@" character.</span></span>

<span data-ttu-id="7adf9-p107">En el siguiente ejemplo se muestra un cuadro de mensaje con formato con un mensaje con secciones. La primera sección del texto del mensaje se muestra como encabezado en negrita. La segunda sección se muestra como texto normal bajo el encabezado. La tercera sección se muestra como texto normal bajo la segunda sección, con una línea en blanco entre ellas.</span><span class="sxs-lookup"><span data-stu-id="7adf9-p107">The following example displays a formatted message box with a sectioned message. The first section of text in the message is displayed as a bold heading. The second section is displayed as plain text beneath that heading. The third section is displayed as plain text beneath the second section, with a blank line between them.</span></span>

<span data-ttu-id="7adf9-136">Escriba la siguiente cadena en el argumento **Mensaje**:</span><span class="sxs-lookup"><span data-stu-id="7adf9-136">Type the following string in the **Message** argument:</span></span>

<span data-ttu-id="7adf9-137">**Botón incorrecto\!@This botón no Work.@Try otra.**</span><span class="sxs-lookup"><span data-stu-id="7adf9-137">**Wrong button\!@This button doesn't work.@Try another.**</span></span>

<span data-ttu-id="7adf9-p108">No puede ejecutar la acción **CuadroDeMensajes** en un módulo Visual Basic para aplicaciones (VBA). En su lugar, use la función **CuadroMsj**.</span><span class="sxs-lookup"><span data-stu-id="7adf9-p108">You can't run the **MessageBox** action in a Visual Basic for Applications (VBA) module. Use the **MsgBox** function instead.</span></span>

## <a name="examples"></a><span data-ttu-id="7adf9-140">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7adf9-140">Examples</span></span>

<span data-ttu-id="7adf9-141">**Sincronizar formularios con una macro**</span><span class="sxs-lookup"><span data-stu-id="7adf9-141">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="7adf9-p109">La siguiente macro abre Lista de productos en la esquina inferior derecha del formulario Proveedores y muestra los productos del proveedor actual. Muestra el uso de las acciones **Eco**, **CuadroDeMensajes**, **IrAControl**, **DetenerMacro**, **AbrirFormulario** y **MoverYCambiarTamañoDeVentana**. También muestra el uso de una expresión condicional con las acciones **CuadroDeMensajes**, **IrAControl** y **DetenerMacro**. Esta macro se debe adjuntar al botón Revisar productos del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="7adf9-p109">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7adf9-146">Condición</span><span class="sxs-lookup"><span data-stu-id="7adf9-146">Condition</span></span></p></th>
<th><p><span data-ttu-id="7adf9-147">Acción</span><span class="sxs-lookup"><span data-stu-id="7adf9-147">Action</span></span></p></th>
<th><p><span data-ttu-id="7adf9-148">Argumentos: Configuración</span><span class="sxs-lookup"><span data-stu-id="7adf9-148">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="7adf9-149">Comentario</span><span class="sxs-lookup"><span data-stu-id="7adf9-149">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="7adf9-150"><strong>Eco</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-150"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="7adf9-151"><strong>Eco activo</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-151"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="7adf9-152">Detener la actualización de la pantalla mientras se ejecuta la macro.</span><span class="sxs-lookup"><span data-stu-id="7adf9-152">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7adf9-153">IsNull([IdProveedor])</span><span class="sxs-lookup"><span data-stu-id="7adf9-153">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="7adf9-154"><strong>CuadroDeMensajes</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-154"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="7adf9-155"><strong>Mensaje</strong>: mover al registro del proveedor los productos que quiera ver, luego, haga clic de nuevo en el botón Revisar productos.</span><span class="sxs-lookup"><span data-stu-id="7adf9-155"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="7adf9-156"><strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: seleccionar un proveedor</span><span class="sxs-lookup"><span data-stu-id="7adf9-156"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="7adf9-157">Si no hay ningún proveedor actual en el formulario Proveedores, mostrar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="7adf9-157">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7adf9-158">...</span><span class="sxs-lookup"><span data-stu-id="7adf9-158"></span></span></p></td>
<td><p><span data-ttu-id="7adf9-159"><strong>IrAControl</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-159"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="7adf9-160"><strong>Nombre del control</strong>: NombreDeEmpresa</span><span class="sxs-lookup"><span data-stu-id="7adf9-160"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="7adf9-161">Mover el foco al control NombreDeEmpresa.</span><span class="sxs-lookup"><span data-stu-id="7adf9-161">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7adf9-162">...</span><span class="sxs-lookup"><span data-stu-id="7adf9-162"></span></span></p></td>
<td><p><span data-ttu-id="7adf9-163"><strong>DetenerMacro</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7adf9-164">Detener la macro.</span><span class="sxs-lookup"><span data-stu-id="7adf9-164">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="7adf9-165"><strong>AbrirFormulario</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-165"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="7adf9-166"><strong>Nombre del formulario</strong>: <strong>vista</strong>de lista de producto: <strong>Nombre DatasheetFilter</strong>: <strong>condición Where</strong>: [Id] = [formularios]! [Proveedores]! [SupplierID] <strong>Modo de datos</strong>: <strong>Modo de lectura OnlyWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-166"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="7adf9-167">Abrir el formulario Lista de productos y mostrar los productos del proveedor actual.</span><span class="sxs-lookup"><span data-stu-id="7adf9-167">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="7adf9-168"><strong>MoverYCambiarTamañoDeVentana</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-168"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="7adf9-169"><strong>Derecha</strong>: 0.7799&quot; <strong>hacia abajo</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="7adf9-169"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="7adf9-170">Coloque el formulario Lista de productos en la esquina inferior derecha del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="7adf9-170">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7adf9-171">**Validar los datos con una macro**</span><span class="sxs-lookup"><span data-stu-id="7adf9-171">**Validate data by using a macro**</span></span>

<span data-ttu-id="7adf9-p111">La siguiente macro de validación comprueba los códigos postales introducidos en el formulario Proveedores. Muestra el uso de las acciones **DetenerMacro**, **CuadroDeMensajes**, **CancelarEvento** e **IrAControl**. Una expresión condicional comprueba el país o región, y el código postal introducidos en un registro del formulario. Si el código postal no tiene el formato correcto para el país o región, la macro muestra un cuadro de mensaje y cancela el guardado del registro. Luego, devuelve el control CódigoPostal, donde puede corregir el error. Esta macro se debe adjuntar a la propiedad **BeforeUpdate** del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="7adf9-p111">The following validation macro checks the postal codes entered in a Suppliers form. It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions. A conditional expression checks the country/region and postal code entered in a record on the form. If the postal code isn't in the right format for the country/region, the macro displays a message box and cancels saving the record. It then returns you to the PostalCode control, where you can correct the error. This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7adf9-178">Condición</span><span class="sxs-lookup"><span data-stu-id="7adf9-178">Condition</span></span></p></th>
<th><p><span data-ttu-id="7adf9-179">Acción</span><span class="sxs-lookup"><span data-stu-id="7adf9-179">Action</span></span></p></th>
<th><p><span data-ttu-id="7adf9-180">Argumentos: Configuración</span><span class="sxs-lookup"><span data-stu-id="7adf9-180">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="7adf9-181">Comentario</span><span class="sxs-lookup"><span data-stu-id="7adf9-181">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7adf9-182">IsNull([PaísRegión])</span><span class="sxs-lookup"><span data-stu-id="7adf9-182">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="7adf9-183"><strong>DetenerMacro</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-183"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7adf9-184">Si PaísRegión es <strong>Null</strong>, el código postal no se podrá validar.</span><span class="sxs-lookup"><span data-stu-id="7adf9-184">If CountryRegion is <strong>Null</strong>, the postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7adf9-185">[PaísRegión] En (&quot;Francia&quot;,&quot;Italia&quot;,&quot;España&quot;) y Len([PostalCode]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="7adf9-185">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([PostalCode]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="7adf9-186"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="7adf9-187"><strong>Mensaje</strong>: el código postal debe ser de 5 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7adf9-187"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="7adf9-188"><strong>Bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Error de código Postal</span><span class="sxs-lookup"><span data-stu-id="7adf9-188"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="7adf9-189">Si el código postal no tiene 5 caracteres, mostrar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="7adf9-189">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7adf9-190">...</span><span class="sxs-lookup"><span data-stu-id="7adf9-190"></span></span></p></td>
<td><p><span data-ttu-id="7adf9-191"><strong>CancelarEvento</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-191"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7adf9-192">Cancelar el evento.</span><span class="sxs-lookup"><span data-stu-id="7adf9-192">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="7adf9-193"><strong>IrAControl</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-193"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="7adf9-194"><strong>Nombre del control</strong>: CódigoPostal</span><span class="sxs-lookup"><span data-stu-id="7adf9-194"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7adf9-195">[PaísRegión] En (&quot;Australia&quot;,&quot;Singapur&quot;) y Len([PostalCode]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="7adf9-195">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([PostalCode]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="7adf9-196"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-196"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="7adf9-197"><strong>Mensaje</strong>: el código postal debe ser de 4 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7adf9-197"><strong>Message</strong>: The postal code must be 4 characters.</span></span> <span data-ttu-id="7adf9-198"><strong>Bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Error de código Postal</span><span class="sxs-lookup"><span data-stu-id="7adf9-198"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="7adf9-199">Si el código postal no tiene 4 caracteres, mostrar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="7adf9-199">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7adf9-200">...</span><span class="sxs-lookup"><span data-stu-id="7adf9-200"></span></span></p></td>
<td><p><span data-ttu-id="7adf9-201"><strong>CancelarEvento</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-201"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7adf9-202">Cancelar el evento.</span><span class="sxs-lookup"><span data-stu-id="7adf9-202">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="7adf9-203"><strong>IrAControl</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-203"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="7adf9-204"><strong>Nombre del control</strong>: CódigoPostal</span><span class="sxs-lookup"><span data-stu-id="7adf9-204"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7adf9-205">([PaísRegión] = &quot;Canadá&quot;) Y ([CódigoPostal] no le gusta&quot;[A-z] [0-9] [A-z] [0-9] [A-z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="7adf9-205">([CountryRegion] = &quot;Canada&quot;) And ([PostalCode] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="7adf9-206"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-206"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="7adf9-207"><strong>Mensaje</strong>: El código postal no es válido.</span><span class="sxs-lookup"><span data-stu-id="7adf9-207"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="7adf9-208">Ejemplo de código de Canadá: H1J 1C3 <strong>Bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Error de código Postal</span><span class="sxs-lookup"><span data-stu-id="7adf9-208">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="7adf9-p115">Si el código postal no es correcto para Canadá, mostrar un mensaje. (Ejemplo de código canadiense: H1J 1C3)</span><span class="sxs-lookup"><span data-stu-id="7adf9-p115">If the postal code isn't correct for Canada, display a message. (Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7adf9-211">...</span><span class="sxs-lookup"><span data-stu-id="7adf9-211"></span></span></p></td>
<td><p><span data-ttu-id="7adf9-212"><strong>CancelarEvento</strong></span><span class="sxs-lookup"><span data-stu-id="7adf9-212"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7adf9-213">Cancelar el evento.</span><span class="sxs-lookup"><span data-stu-id="7adf9-213">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

