---
title: Acción de macro eco (referencia de escritorio de la base de datos de Access)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 03eeab3884e093b7c22f8fd23d5471d1dc620bc8
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997458"
---
# <a name="echo-macro-action"></a><span data-ttu-id="a8db0-102">Eco (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="a8db0-102">Echo macro action</span></span>

<span data-ttu-id="a8db0-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8db0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a8db0-p101">Puede usar la acción **Eco** para especificar si se activa el eco. Por ejemplo, puede usar esta acción para ocultar o mostrar los resultados de una macro mientras se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="a8db0-p101">You can use the **Echo** action to specify whether echo is turned on. For example, you can use this action to hide or show the results of a macro while it runs.</span></span>

## <a name="setting"></a><span data-ttu-id="a8db0-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="a8db0-106">Setting</span></span>

> [!NOTE]
> <span data-ttu-id="a8db0-107">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="a8db0-107">This action will not be allowed if the database is not trusted.</span></span>

<span data-ttu-id="a8db0-108">La acción **Eco** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="a8db0-108">The **Echo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8db0-109">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="a8db0-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a8db0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8db0-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8db0-111"><strong>Eco activo</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-111"><strong>Echo On</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-p102">Haga clic en <strong>Sí</strong> (activar el eco) o <strong>No</strong> (desactivar el eco) en el cuadro <strong>Eco activo</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. El valor predeterminado es <strong>Sí</strong>.  </span><span class="sxs-lookup"><span data-stu-id="a8db0-p102">Click <strong>Yes</strong> (turn echo on) or <strong>No</strong> (turn echo off) in the <strong>Echo On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8db0-114"><strong>Texto de la barra de estado</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-114"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-115">El texto para mostrar en la barra de estado cuando el eco está desactivado.</span><span class="sxs-lookup"><span data-stu-id="a8db0-115">The text to display in the status bar when echo is turned off.</span></span> <span data-ttu-id="a8db0-116">Por ejemplo, cuando se desactiva el eco, puede mostrar la barra de estado &quot;se está ejecutando la macro.&quot;</span><span class="sxs-lookup"><span data-stu-id="a8db0-116">For example, when echo is turned off, the status bar can display &quot;The macro is running.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a8db0-117">Cuando se ejecuta una macro, actualización de la pantalla muestra a menudo información no esencial para el funcionamiento de la macro.</span><span class="sxs-lookup"><span data-stu-id="a8db0-117">When a macro runs, screen updating often shows information not essential to the functioning of the macro.</span></span> <span data-ttu-id="a8db0-118">Al configurar el argumento **Eco activo** en **No**, la macro se ejecuta sin actualizar la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a8db0-118">When you set the **Echo On** argument to **No**, the macro runs without updating the screen.</span></span> <span data-ttu-id="a8db0-119">Cuando la macro termina, Access activa automáticamente el eco y vuelve a dibujar la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a8db0-119">When the macro finishes, Access automatically turns echo back on and repaints the window.</span></span> <span data-ttu-id="a8db0-120">La configuración **No** para el argumento **Eco activo** no afecta a la funcionalidad de la macro o a sus resultados.</span><span class="sxs-lookup"><span data-stu-id="a8db0-120">The **No** setting for the **Echo On** argument doesn't affect the functionality of the macro or its results.</span></span>

<span data-ttu-id="a8db0-p105">La acción **Eco** no suprime la visualización de los cuadros de diálogo modales, como mensajes de error o formularios emergentes, como hojas de propiedades. Puede usar los cuadros de diálogo y los formularios emergentes para recopilar o mostrar información, incluso si el eco está desactivado. Para suprimir todos los cuadros de diálogo o de mensaje, excepto los cuadros de mensaje de error y los cuadros de diálogo que necesitan que el usuario introduzca información, use la acción **EstablecerAdvertencias**.</span><span class="sxs-lookup"><span data-stu-id="a8db0-p105">The **Echo** action doesn't suppress the display of modal dialog boxes, such as error messages, or pop-up forms, such as property sheets. You can use dialog boxes and pop-up forms to gather or display information, even if echo is turned off. To suppress all message or dialog boxes except error message boxes and dialog boxes that require the user to enter information, use the **SetWarnings** action.</span></span>

<span data-ttu-id="a8db0-p106">Puede ejecutar la acción **Eco** varias veces en una macro. Esto permite cambiar el texto de la barra de estado mientras se ejecuta la macro.</span><span class="sxs-lookup"><span data-stu-id="a8db0-p106">You can run the **Echo** action more than once in a macro. This allows you to change the status bar text while the macro runs.</span></span>

<span data-ttu-id="a8db0-126">Si desactiva el eco, puede usar la acción **MostrarCursorDeRelojDeArena** para cambiar el puntero del ratón por un icono de reloj de arena (o cualquier otro puntero del ratón que haya configurado en "Ocupado") para proporcionar una indicación visual de que la macro se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="a8db0-126">If you turn echo off, you can use the **DisplayHourglassPointer** action to change the mouse pointer into an hourglass icon (or whatever mouse pointer icon you've set for "Busy") to provide a visual indication that the macro is running.</span></span>

<span data-ttu-id="a8db0-127">Para ejecutar la acción **Eco** en un módulo Visual Basic para Aplicaciones (VBA), use el método **Eco** del objeto **DocMd**.</span><span class="sxs-lookup"><span data-stu-id="a8db0-127">To run the **Echo** action in a Visual Basic for Applications (VBA) module, use the **Echo** method of the **DoCmd** object.</span></span>

## <a name="examples"></a><span data-ttu-id="a8db0-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a8db0-128">Examples</span></span>

### <a name="set-the-value-of-a-control-by-using-a-macro"></a><span data-ttu-id="a8db0-129">Configurar el valor de un control con una macro</span><span class="sxs-lookup"><span data-stu-id="a8db0-129">Set the value of a control by using a macro</span></span>

<span data-ttu-id="a8db0-p107">La siguiente macro abre el formulario Agregar productos desde un botón del formulario Proveedores. Muestra el uso de las acciones **Eco**, **CerrarVentana**, **AbrirFormulario**, **ConfigurarValor** e **IrAControl**. La acción **ConfigurarValor** configura el control Id. de proveedor en el formulario Productos para el proveedor actual del formulario Proveedores. La acción **IrAControl** mueve el foco al campo Id. de categoría, donde puede empezar a introducir los datos para el nuevo producto. Esta macro se debe adjuntar al botón Agregar productos del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="a8db0-p107">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8db0-135">Acción</span><span class="sxs-lookup"><span data-stu-id="a8db0-135">Action</span></span></p></th>
<th><p><span data-ttu-id="a8db0-136">Argumentos: Configuración</span><span class="sxs-lookup"><span data-stu-id="a8db0-136">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="a8db0-137">Comentario</span><span class="sxs-lookup"><span data-stu-id="a8db0-137">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8db0-138"><strong>Eco</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-138"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-139"><strong>Eco activo</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-139"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-140">Detener la actualización de la pantalla mientras se ejecuta la macro.</span><span class="sxs-lookup"><span data-stu-id="a8db0-140">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8db0-141"><strong>CerrarVentana</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-141"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-142"><strong>Tipo de objeto</strong>: <strong>Nombre de FormObject</strong>: lista de producto <strong>Guardar</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-142"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-143">Cerrar el formulario Lista de productos</span><span class="sxs-lookup"><span data-stu-id="a8db0-143">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8db0-144"><strong>AbrirFormulario</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-144"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-145"><strong>Nombre del formulario</strong>: productos <strong>vista</strong>: <strong>Modo FormData</strong>: <strong>Modo AddWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-145"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-146">Abrir el formulario Productos.</span><span class="sxs-lookup"><span data-stu-id="a8db0-146">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8db0-147"><strong>ConfigurarValor</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-147"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-148"><strong>Elemento</strong>: [Forms]![Products]![SupplierID] <strong>Expresión</strong>: IdProveedor</span><span class="sxs-lookup"><span data-stu-id="a8db0-148"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="a8db0-149">Configurar el control Id. de proveedor para el proveedor actual del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="a8db0-149">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8db0-150"><strong>IrAControl</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-150"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-151"><strong>Nombre del control</strong>: IdCategoría</span><span class="sxs-lookup"><span data-stu-id="a8db0-151"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="a8db0-152">Ir al control Id. de categoría.</span><span class="sxs-lookup"><span data-stu-id="a8db0-152">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a><span data-ttu-id="a8db0-153">Sincronizar los formularios con una macro</span><span class="sxs-lookup"><span data-stu-id="a8db0-153">Synchronize forms by using a macro</span></span>

<span data-ttu-id="a8db0-p108">La siguiente macro abre el formulario Lista de productos en la esquina inferior derecha del formulario Proveedores y muestra los productos del proveedor actual. Muestra el uso de las acciones **Eco**, **CuadroDeMensajes**, **IrAControl**, **DetenerMacro**, **AbrirFormulario** y **MoverYCambiarTamañoDeVentana**. También muestra el uso de una expresión condicional con las acciones **CuadroDeMensajes**, **IrAControl** y **DetenerMacro**. Esta macro se debe adjuntar al botón Revisar productos del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="a8db0-p108">The following macro opens the Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8db0-158">Condición</span><span class="sxs-lookup"><span data-stu-id="a8db0-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="a8db0-159">Acción</span><span class="sxs-lookup"><span data-stu-id="a8db0-159">Action</span></span></p></th>
<th><p><span data-ttu-id="a8db0-160">Argumentos: Configuración</span><span class="sxs-lookup"><span data-stu-id="a8db0-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="a8db0-161">Comentario</span><span class="sxs-lookup"><span data-stu-id="a8db0-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="a8db0-162"><strong>Eco</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-163"><strong>Eco activo</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-164">Detener la actualización de la pantalla mientras se ejecuta la macro.</span><span class="sxs-lookup"><span data-stu-id="a8db0-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8db0-165">IsNull([Id. de proveedor])</span><span class="sxs-lookup"><span data-stu-id="a8db0-165">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="a8db0-166"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-167"><strong>Mensaje</strong>: mover al registro del proveedor los productos que quiera ver, luego, haga clic de nuevo en el botón Revisar productos.</span><span class="sxs-lookup"><span data-stu-id="a8db0-167"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="a8db0-168"><strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: seleccionar un proveedor</span><span class="sxs-lookup"><span data-stu-id="a8db0-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="a8db0-169">Si no hay ningún proveedor actual en el formulario Proveedores, mostrar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="a8db0-169">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8db0-170">...</span><span class="sxs-lookup"><span data-stu-id="a8db0-170"></span></span></p></td>
<td><p><span data-ttu-id="a8db0-171"><strong>IrAControl</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-171"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-172"><strong>Nombre del control</strong>: NombreDeEmpresa</span><span class="sxs-lookup"><span data-stu-id="a8db0-172"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="a8db0-173">Mover el foco al control NombreDeEmpresa.</span><span class="sxs-lookup"><span data-stu-id="a8db0-173">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8db0-174">...</span><span class="sxs-lookup"><span data-stu-id="a8db0-174"></span></span></p></td>
<td><p><span data-ttu-id="a8db0-175"><strong>DetenerMacro</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-175"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a8db0-176">Detener la macro.</span><span class="sxs-lookup"><span data-stu-id="a8db0-176">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="a8db0-177"><strong>AbrirFormulario</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-177"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-178"><strong>Nombre del formulario</strong>: <strong>vista</strong>de lista de producto: <strong>Nombre de DatasheetFilter</strong>: <strong>condición Where</strong>: [ID de proveedor] = [formularios]! [Proveedores]! [SupplierID] <strong>Modo de datos</strong>: <strong>Modo de lectura OnlyWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-178"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-179">Abrir el formulario Lista de productos y mostrar los productos del proveedor actual.</span><span class="sxs-lookup"><span data-stu-id="a8db0-179">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="a8db0-180"><strong>MoverYCambiarTamañoDeVentana</strong></span><span class="sxs-lookup"><span data-stu-id="a8db0-180"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="a8db0-181"><strong>Derecha</strong>: 0.7799&quot; <strong>hacia abajo</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="a8db0-181"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="a8db0-182">Coloque el formulario Lista de productos en la esquina inferior derecha del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="a8db0-182">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

