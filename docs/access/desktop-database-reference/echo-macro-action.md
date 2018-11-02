---
title: Acción de macro eco (referencia de escritorio de la base de datos de Access)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 947e3569d52558cc154ea751ecce204d02cbf7ec
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921547"
---
# <a name="echo-macro-action"></a><span data-ttu-id="8fd30-102">Eco (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="8fd30-102">Echo macro action</span></span>


<span data-ttu-id="8fd30-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8fd30-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8fd30-p101">Puede usar la acción **Eco** para especificar si se activa el eco. Por ejemplo, puede usar esta acción para ocultar o mostrar los resultados de una macro mientras se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="8fd30-p101">You can use the **Echo** action to specify whether echo is turned on. For example, you can use this action to hide or show the results of a macro while it runs.</span></span>

## <a name="setting"></a><span data-ttu-id="8fd30-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="8fd30-106">Setting</span></span>


> [!NOTE]
> <span data-ttu-id="8fd30-p102">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.</span><span class="sxs-lookup"><span data-stu-id="8fd30-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>



<span data-ttu-id="8fd30-109">La acción **Eco** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="8fd30-109">The **Echo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8fd30-110">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="8fd30-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8fd30-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fd30-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8fd30-112"><strong>Eco activo</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-112"><strong>Echo On</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-p103">Haga clic en <strong>Sí</strong> (activar el eco) o <strong>No</strong> (desactivar el eco) en el cuadro <strong>Eco activo</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. El valor predeterminado es <strong>Sí</strong>.  </span><span class="sxs-lookup"><span data-stu-id="8fd30-p103">Click <strong>Yes</strong> (turn echo on) or <strong>No</strong> (turn echo off) in the <strong>Echo On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fd30-115"><strong>Texto de la barra de estado</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-115"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-116">El texto para mostrar en la barra de estado cuando el eco está desactivado.</span><span class="sxs-lookup"><span data-stu-id="8fd30-116">The text to display in the status bar when echo is turned off.</span></span> <span data-ttu-id="8fd30-117">Por ejemplo, cuando se desactiva el eco, puede mostrar la barra de estado &quot;se está ejecutando la macro.&quot;</span><span class="sxs-lookup"><span data-stu-id="8fd30-117">For example, when echo is turned off, the status bar can display &quot;The macro is running.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8fd30-p105">Cuando ejecuta una macro, la actualización de la pantalla suele mostrar la información no esencial para el funcionamiento de la macro. Al configurar el argumento **Eco activo** en **No**, la macro se ejecuta sin actualizar la pantalla. Cuando la macro termina, Access activa automáticamente el eco y vuelve a dibujar la pantalla. La configuración **No** para el argumento **Eco activo** no afecta a la funcionalidad de la macro o a sus resultados.</span><span class="sxs-lookup"><span data-stu-id="8fd30-p105">When runs a macro, screen updating often shows information not essential to the functioning of the macro. When you set the **Echo On** argument to **No**, the macro runs without updating the screen. When the macro finishes, Access automatically turns echo back on and repaints the window. The **No** setting for the **Echo On** argument doesn't affect the functionality of the macro or its results.</span></span>

<span data-ttu-id="8fd30-p106">La acción **Eco** no suprime la visualización de los cuadros de diálogo modales, como mensajes de error o formularios emergentes, como hojas de propiedades. Puede usar los cuadros de diálogo y los formularios emergentes para recopilar o mostrar información, incluso si el eco está desactivado. Para suprimir todos los cuadros de diálogo o de mensaje, excepto los cuadros de mensaje de error y los cuadros de diálogo que necesitan que el usuario introduzca información, use la acción **EstablecerAdvertencias**.</span><span class="sxs-lookup"><span data-stu-id="8fd30-p106">The **Echo** action doesn't suppress the display of modal dialog boxes, such as error messages, or pop-up forms, such as property sheets. You can use dialog boxes and pop-up forms to gather or display information, even if echo is turned off. To suppress all message or dialog boxes except error message boxes and dialog boxes that require the user to enter information, use the **SetWarnings** action.</span></span>

<span data-ttu-id="8fd30-p107">Puede ejecutar la acción **Eco** varias veces en una macro. Esto permite cambiar el texto de la barra de estado mientras se ejecuta la macro.</span><span class="sxs-lookup"><span data-stu-id="8fd30-p107">You can run the **Echo** action more than once in a macro. This allows you to change the status bar text while the macro runs.</span></span>

<span data-ttu-id="8fd30-127">Si desactiva el eco, puede usar la acción **MostrarCursorDeRelojDeArena** para cambiar el puntero del ratón por un icono de reloj de arena (o cualquier otro puntero del ratón que haya configurado en "Ocupado") para proporcionar una indicación visual de que la macro se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="8fd30-127">If you turn echo off, you can use the **DisplayHourglassPointer** action to change the mouse pointer into an hourglass icon (or whatever mouse pointer icon you've set for "Busy") to provide a visual indication that the macro is running.</span></span>

<span data-ttu-id="8fd30-128">Para ejecutar la acción **Eco** en un módulo Visual Basic para Aplicaciones (VBA), use el método **Eco** del objeto **DocMd**.</span><span class="sxs-lookup"><span data-stu-id="8fd30-128">To run the **Echo** action in a Visual Basic for Applications (VBA) module, use the **Echo** method of the **DoCmd** object.</span></span>

## <a name="examples"></a><span data-ttu-id="8fd30-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8fd30-129">Examples</span></span>

<span data-ttu-id="8fd30-130">**Configurar el valor de un control con una macro**</span><span class="sxs-lookup"><span data-stu-id="8fd30-130">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="8fd30-p108">La siguiente macro abre el formulario Agregar productos desde un botón del formulario Proveedores. Muestra el uso de las acciones **Eco**, **CerrarVentana**, **AbrirFormulario**, **ConfigurarValor** e **IrAControl**. La acción **ConfigurarValor** configura el control Id. de proveedor en el formulario Productos para el proveedor actual del formulario Proveedores. La acción **IrAControl** mueve el foco al campo Id. de categoría, donde puede empezar a introducir los datos para el nuevo producto. Esta macro se debe adjuntar al botón Agregar productos del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="8fd30-p108">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8fd30-136">Acción</span><span class="sxs-lookup"><span data-stu-id="8fd30-136">Action</span></span></p></th>
<th><p><span data-ttu-id="8fd30-137">Argumentos: Configuración</span><span class="sxs-lookup"><span data-stu-id="8fd30-137">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="8fd30-138">Comentario</span><span class="sxs-lookup"><span data-stu-id="8fd30-138">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8fd30-139"><strong>Eco</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-139"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-140"><strong>Eco activo</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-140"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-141">Detener la actualización de la pantalla mientras se ejecuta la macro.</span><span class="sxs-lookup"><span data-stu-id="8fd30-141">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fd30-142"><strong>CerrarVentana</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-142"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-143"><strong>Tipo de objeto</strong>: <strong>Nombre de FormObject</strong>: lista de producto <strong>Guardar</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-143"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-144">Cerrar el formulario Lista de productos</span><span class="sxs-lookup"><span data-stu-id="8fd30-144">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fd30-145"><strong>AbrirFormulario</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-145"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-146"><strong>Nombre del formulario</strong>: productos <strong>vista</strong>: <strong>Modo FormData</strong>: <strong>Modo AddWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-146"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-147">Abrir el formulario Productos.</span><span class="sxs-lookup"><span data-stu-id="8fd30-147">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fd30-148"><strong>ConfigurarValor</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-148"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-149"><strong>Elemento</strong>: [Forms]![Products]![SupplierID] <strong>Expresión</strong>: IdProveedor</span><span class="sxs-lookup"><span data-stu-id="8fd30-149"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="8fd30-150">Configurar el control Id. de proveedor para el proveedor actual del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="8fd30-150">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fd30-151"><strong>IrAControl</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-151"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-152"><strong>Nombre del control</strong>: IdCategoría</span><span class="sxs-lookup"><span data-stu-id="8fd30-152"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="8fd30-153">Ir al control Id. de categoría.</span><span class="sxs-lookup"><span data-stu-id="8fd30-153">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8fd30-154">**Sincronizar los formularios con una macro**</span><span class="sxs-lookup"><span data-stu-id="8fd30-154">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="8fd30-p109">La siguiente macro abre el formulario Lista de productos en la esquina inferior derecha del formulario Proveedores y muestra los productos del proveedor actual. Muestra el uso de las acciones **Eco**, **CuadroDeMensajes**, **IrAControl**, **DetenerMacro**, **AbrirFormulario** y **MoverYCambiarTamañoDeVentana**. También muestra el uso de una expresión condicional con las acciones **CuadroDeMensajes**, **IrAControl** y **DetenerMacro**. Esta macro se debe adjuntar al botón Revisar productos del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="8fd30-p109">The following macro opens the Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8fd30-159">Condición</span><span class="sxs-lookup"><span data-stu-id="8fd30-159">Condition</span></span></p></th>
<th><p><span data-ttu-id="8fd30-160">Acción</span><span class="sxs-lookup"><span data-stu-id="8fd30-160">Action</span></span></p></th>
<th><p><span data-ttu-id="8fd30-161">Argumentos: Configuración</span><span class="sxs-lookup"><span data-stu-id="8fd30-161">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="8fd30-162">Comentario</span><span class="sxs-lookup"><span data-stu-id="8fd30-162">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="8fd30-163"><strong>Eco</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-163"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-164"><strong>Eco activo</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-164"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-165">Detener la actualización de la pantalla mientras se ejecuta la macro.</span><span class="sxs-lookup"><span data-stu-id="8fd30-165">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fd30-166">IsNull([Id. de proveedor])</span><span class="sxs-lookup"><span data-stu-id="8fd30-166">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="8fd30-167"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-167"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-168"><strong>Mensaje</strong>: mover al registro del proveedor los productos que quiera ver, luego, haga clic de nuevo en el botón Revisar productos.</span><span class="sxs-lookup"><span data-stu-id="8fd30-168"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="8fd30-169"><strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: seleccionar un proveedor</span><span class="sxs-lookup"><span data-stu-id="8fd30-169"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="8fd30-170">Si no hay ningún proveedor actual en el formulario Proveedores, mostrar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8fd30-170">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fd30-171">...</span><span class="sxs-lookup"><span data-stu-id="8fd30-171"></span></span></p></td>
<td><p><span data-ttu-id="8fd30-172"><strong>IrAControl</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-172"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-173"><strong>Nombre del control</strong>: NombreDeEmpresa</span><span class="sxs-lookup"><span data-stu-id="8fd30-173"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="8fd30-174">Mover el foco al control NombreDeEmpresa.</span><span class="sxs-lookup"><span data-stu-id="8fd30-174">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fd30-175">...</span><span class="sxs-lookup"><span data-stu-id="8fd30-175"></span></span></p></td>
<td><p><span data-ttu-id="8fd30-176"><strong>DetenerMacro</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-176"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="8fd30-177">Detener la macro.</span><span class="sxs-lookup"><span data-stu-id="8fd30-177">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="8fd30-178"><strong>AbrirFormulario</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-178"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-179"><strong>Nombre del formulario</strong>: <strong>vista</strong>de lista de producto: <strong>Nombre de DatasheetFilter</strong>: <strong>condición Where</strong>: [ID de proveedor] = [formularios]! [Proveedores]! [SupplierID] <strong>Modo de datos</strong>: <strong>Modo de lectura OnlyWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-179"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-180">Abrir el formulario Lista de productos y mostrar los productos del proveedor actual.</span><span class="sxs-lookup"><span data-stu-id="8fd30-180">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="8fd30-181"><strong>MoverYCambiarTamañoDeVentana</strong></span><span class="sxs-lookup"><span data-stu-id="8fd30-181"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="8fd30-182"><strong>Derecha</strong>: 0.7799&quot; <strong>hacia abajo</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="8fd30-182"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="8fd30-183">Coloque el formulario Lista de productos en la esquina inferior derecha del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="8fd30-183">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

