---
title: AbrirFormulario (acción de macro)
TOCTitle: OpenForm macro action
ms:assetid: c519a9d7-99d4-4765-ad96-59c3fe1be9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823095(v=office.15)
ms:contentKeyID: 48547604
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf89b61a65c11f09d5a07e52caeee5ad416c118a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707629"
---
# <a name="openform-macro-action"></a><span data-ttu-id="0bd57-102">AbrirFormulario (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="0bd57-102">OpenForm macro action</span></span>

<span data-ttu-id="0bd57-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0bd57-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0bd57-p101">Puede usar la acción **AbrirFormulario** para abrir un formulario en la vista Formulario, Diseño, Vista preliminar u Hoja de datos. Puede seleccionar los modos de entrada de datos y ventana para el formulario y restringir los registros que se muestra en él.</span><span class="sxs-lookup"><span data-stu-id="0bd57-p101">You can use the **OpenForm** action to open a form in Form view, Design view, Print Preview, or Datasheet view. You can select data entry and window modes for the form and restrict the records that the form displays.</span></span>

## <a name="setting"></a><span data-ttu-id="0bd57-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="0bd57-106">Setting</span></span>

<span data-ttu-id="0bd57-107">La acción **AbrirFormulario** incluye estos argumentos.</span><span class="sxs-lookup"><span data-stu-id="0bd57-107">The **OpenForm** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0bd57-108">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="0bd57-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="0bd57-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0bd57-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bd57-110"><strong>Nombre de formulario</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-110"><strong>Form Name</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-p102">El nombre del formulario que se va a abrir. El cuadro <strong>Nombre de formulario</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todos los formularios en la base de datos actual. Este es un argumento obligatorio. Si ejecuta una macro que contiene la acción <strong>AbrirFormulario</strong> en una base de datos de biblioteca, Microsoft Access busca primero el formulario con este nombre en la base de datos de biblioteca y, luego, en la base de datos actual.  </span><span class="sxs-lookup"><span data-stu-id="0bd57-p102">The name of the form to open. The <strong>Form Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all forms in the current database. This is a required argument. If you run a macro containing the <strong>OpenForm</strong> action in a library database, Microsoft Access first looks for the form with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bd57-115"><strong>Vista</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-p103">Vista en la que se abrirá el formulario. Haga clic en <strong>Formulario</strong>, <strong>Diseño</strong>, <strong>Vista preliminar</strong>, <strong>Hoja de datos</strong>, <strong>Tabla dinámica</strong> o <strong>Gráfico dinámico</strong> en el cuadro <strong>Vista</strong>. El valor predeterminado es <strong>Formulario</strong>.  </span><span class="sxs-lookup"><span data-stu-id="0bd57-p103">The view in which the form will open. Click <strong>Form</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>Datasheet</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Form</strong>.</span></span></p><p><span data-ttu-id="0bd57-119"><strong>Nota</strong>: el valor del argumento <STRONG>vista</STRONG> reemplaza los valores de las propiedades del formulario <STRONG>DefaultView</STRONG> y <STRONG>ViewsAllowed</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="0bd57-119"><strong>NOTE</strong>: The <STRONG>View</STRONG> argument setting overrides the settings of the form's <STRONG>DefaultView</STRONG> and <STRONG>ViewsAllowed</STRONG> properties.</span></span> <span data-ttu-id="0bd57-120">Por ejemplo, si la propiedad <STRONG>ViewsAllowed</STRONG> de un formulario se establece en la <STRONG>hoja de datos</STRONG>, puede usar la acción <STRONG>AbrirFormulario</STRONG> para abrir el formulario en la vista formulario.</span><span class="sxs-lookup"><span data-stu-id="0bd57-120">For example, if a form's <STRONG>ViewsAllowed</STRONG> property is set to <STRONG>Datasheet</STRONG>, you can still use the <STRONG>OpenForm</STRONG> action to open the form in Form view.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bd57-121"><strong>Nombre de filtro</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-121"><strong>Filter Name</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-p105">Filtro que restringe u ordena los registros del formulario. Puede escribir el nombre de una consulta existente o un filtro que se haya guardado como consulta. Sin embargo, la consulta debe incluir todos los campos en el formulario que va a abrir o tener la propiedad <strong>OutputAllFields</strong> establecida en <strong>Sí</strong>.  </span><span class="sxs-lookup"><span data-stu-id="0bd57-p105">A filter that restricts or sorts the form's records. You can enter the name of either an existing query or a filter that was saved as a query. However, the query must include all the fields in the form you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bd57-125"><strong>Condición WHERE</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-125"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-126">Cláusula WHERE de SQL válida (sin la palabra WHERE) o expresión que Access usa para seleccionar registros de la consulta o tabla subyacente del formulario.</span><span class="sxs-lookup"><span data-stu-id="0bd57-126">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the form's underlying table or query.</span></span> <span data-ttu-id="0bd57-127">Si selecciona un filtro con el argumento <strong>Nombre de filtro</strong>, Access aplica esta cláusula WHERE a los resultados del filtro.</span><span class="sxs-lookup"><span data-stu-id="0bd57-127">If you select a filter with the <strong>Filter Name</strong> argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="0bd57-128">Para abrir un formulario y restringir sus registros a los especificados por el valor de un control de otro formulario, utilice la siguiente expresión: <strong>[</strong><em>fieldname</em><strong>] = Forms! [</strong> <em>FormName</em> <strong>]! [</strong><em>controlname en otro formulario</em><strong>]</strong> sustituya <em>fieldname</em> por el nombre de un campo en la tabla o consulta subyacente del formulario que desea abrir.</span><span class="sxs-lookup"><span data-stu-id="0bd57-128">To open a form and restrict its records to those specified by the value of a control on another form, use the following expression: <strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on other form</em><strong>]</strong> Replace <em>fieldname</em> with the name of a field in the underlying table or query of the form you want to open.</span></span> <span data-ttu-id="0bd57-129">Reemplace <em>nombreDeFormulario</em> y <em>nombrecontrol en otro formulario</em> con el nombre de otro formulario y el control del otro formulario que contiene el valor que desea en el primer formulario para que coincida con los registros.</span><span class="sxs-lookup"><span data-stu-id="0bd57-129">Replace <em>formname</em> and <em>controlname on other form</em> with the name of the other form and the control on the other form that contains the value you want records in the first form to match.</span></span></p><p><span data-ttu-id="0bd57-130"><strong>Nota</strong>: la longitud máxima del argumento <STRONG>Condición Where</STRONG> es de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0bd57-130"><strong>NOTE</strong>: The maximum length of the <STRONG>Where Condition</STRONG> argument is 255 characters.</span></span> <span data-ttu-id="0bd57-131">Si necesita escribir una cláusula WHERE de SQL más compleja y más larga, utilice el método <STRONG>OpenForm</STRONG> del objeto <STRONG>DoCmd</STRONG> en un de Visual Basic para aplicaciones (VBA) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="0bd57-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <STRONG>OpenForm</STRONG> method of the <STRONG>DoCmd</STRONG> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="0bd57-132">Puede especificar instrucciones de cláusula WHERE de SQL de hasta 32.768 caracteres en VBA.</span><span class="sxs-lookup"><span data-stu-id="0bd57-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bd57-133"><strong>Modo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-133"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-p108">Modo de entrada de datos para el formulario. Esto se aplica solo a los formularios abiertos en la vista Formulario o la vista Hoja de datos. Haga clic en <strong>Agregar</strong> (el usuario puede agregar nuevos registros, pero no puede editar registros existentes), <strong>Editar</strong> (el usuario puede editar registros existentes y agregar nuevos registros), o <strong>Solo lectura</strong> (el usuario solo puede ver registros). El valor predeterminado es <strong>Editar</strong>. <strong>Notas</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-p108">The data entry mode for the form. This applies only to forms opened in Form view or Datasheet view. Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>. <strong>Notes</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="0bd57-p109">La configuración del argumento <strong>Modo de datos</strong> invalida la configuración de las propiedades <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong> y <strong>DataEntry</strong> del formulario. Por ejemplo, si la propiedad <strong>AllowEdits</strong> de un formulario se establece en <strong>No</strong>, aún puede usar la acción <strong>AbrirFormulario</strong> para abrir el formulario en modo Edición.  </span><span class="sxs-lookup"><span data-stu-id="0bd57-p109">The <strong>Data Mode</strong> argument setting overrides the settings of the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties. For example, if a form's <strong>AllowEdits</strong> property is set to <strong>No</strong>, you can still use the <strong>OpenForm</strong> action to open the form in Edit mode.</span></span></p></li>
<li><p><span data-ttu-id="0bd57-141">Si deja este argumento en blanco, Access abre el formulario en el modo de entrada de datos establecido por las propiedades <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong> y <strong>DataEntry</strong>.</span><span class="sxs-lookup"><span data-stu-id="0bd57-141">If you leave this argument blank, Access opens the form in the data entry mode set by the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bd57-142"><strong>Modo de ventana</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-142"><strong>Window Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-p110">Modo de ventana en el que se abre el formulario. Haga clic en <strong>Normal</strong> (el formulario se abre en el modo establecido por sus propiedades), <strong>Oculto</strong> (el formulario se oculta), <strong>Icono</strong> (el formulario se abre minimizado como una pequeña barra de título en la parte inferior de la pantalla) o <strong>Diálogo</strong> (las propiedades <strong>Modal</strong> y <strong>Emergente</strong> del formulario se establecen en <strong>Sí</strong>). El valor predeterminado es <strong>Normal</strong>.  </span><span class="sxs-lookup"><span data-stu-id="0bd57-p110">The window mode in which the form opens. Click <strong>Normal</strong> (the form opens in the mode set by its properties), <strong>Hidden</strong> (the form is hidden), <strong>Icon</strong> (the form opens minimized as a small title bar at the bottom of the screen), or <strong>Dialog</strong> (the form's <strong>Modal</strong> and <strong>PopUp</strong> properties are set to <strong>Yes</strong>). The default is <strong>Normal</strong>.</span></span></p><p><span data-ttu-id="0bd57-146"><strong>Nota</strong>: algunos valores del argumento <STRONG>Modo de la ventana</STRONG> no se aplican al uso de documentos con fichas.</span><span class="sxs-lookup"><span data-stu-id="0bd57-146"><strong>NOTE</strong>: Some <STRONG>Window Mode</STRONG> argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="0bd57-147">Para cambiar a ventanas superpuestas:</span><span class="sxs-lookup"><span data-stu-id="0bd57-147">To switch to overlapping windows:</span></span></p>
<ol>
<li><p><span data-ttu-id="0bd57-148">Haga clic en la pestaña archivo y, a continuación, haga clic en <strong>Opciones</strong>.</span><span class="sxs-lookup"><span data-stu-id="0bd57-148">Click the File tab and then click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="0bd57-149">En el cuadro de diálogo <strong>Opciones de Access</strong>, haga clic en <strong>Base de datos actual</strong>.</span><span class="sxs-lookup"><span data-stu-id="0bd57-149">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="0bd57-150">En la sección <strong>Opciones de la aplicación</strong>, en <strong>Opciones de la ventana de documentos</strong>, haga clic en <strong>Ventanas superpuestas</strong>.</span><span class="sxs-lookup"><span data-stu-id="0bd57-150">In the <strong>Application Options</strong>section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="0bd57-151">Haga clic en <strong>Aceptar</strong> y, a continuación, cierre y vuelva a abrir la base de datos.</span><span class="sxs-lookup"><span data-stu-id="0bd57-151">Click <strong>OK</strong>, then close and reopen the database.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0bd57-152">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0bd57-152">Remarks</span></span>

<span data-ttu-id="0bd57-153">Esta acción es similar a la de hacer doble clic en un formulario en el panel de navegación o la de hacer clic con el botón derecho en el formulario del panel de navegación y después seleccionar una vista.</span><span class="sxs-lookup"><span data-stu-id="0bd57-153">This action is similar to double-clicking a form in the Navigation Pane, or right-clicking the form in the Navigation Pane and then selecting a view.</span></span>

<span data-ttu-id="0bd57-p112">Un formulario puede ser modal (se debe cerrar u ocultar para que el usuario pueda realizar cualquier otra acción) o sin modo (el usuario se puede mover a otra ventana mientras se abre el formulario). También puede ser un formulario emergente (un formulario utilizado para recopilar o mostrar información que permanece en la parte superior de todas las demás ventanas de Access). Establezca las propiedades **Modal** y **PopUp** cuando diseñe el formulario. Si usa **Normal** para el argumento **Modo de ventana**, el formulario se abre en el modo especificado por esta configuración de propiedad. Si usa **Diálogo** para el argumento **Modo de ventana**, ambas propiedades se establecen en **Sí**. Un formulario abierto como oculto o como icono se devuelve al modo especificado por su propiedad cuando se muestra o se restaura.</span><span class="sxs-lookup"><span data-stu-id="0bd57-p112">A form can be modal (it must be closed or hidden before the user can perform any other action) or modeless (the user can move to other windows while the form is open). It can also be a pop-up form (a form used to collect or display information that remains on top of all other Access windows). You set the **Modal** and **PopUp** properties when you design the form. If you use **Normal** for the **Window Mode** argument, the form opens in the mode specified by these property settings. If you use **Dialog** for the **Window Mode** argument, these properties are both set to **Yes**. A form opened as hidden or as an icon returns to the mode specified by its property settings when you show or restore it.</span></span>

<span data-ttu-id="0bd57-p113">Al abrir un formulario con el argumento **Modo de ventana** establecido en **Diálogo**, Access suspende la macro hasta que el formulario se cierra u oculta. Puede ocultar un formulario estableciendo su propiedad **Visible** en **No** mediante la acción **ConfigurarValor**.</span><span class="sxs-lookup"><span data-stu-id="0bd57-p113">When you open a form with the **Window Mode** argument set to **Dialog**, Access suspends the macro until the form is closed or hidden. You can hide a form by setting its **Visible** property to **No** by using the **SetValue** action.</span></span>

> [!TIP]
> <span data-ttu-id="0bd57-p114">[!SUGERENCIA] Puede seleccionar un formulario en el panel de navegación y arrastrarlo a una fila de acción de macro. Esto crea automáticamente una acción **AbrirFormulario** que abre el formulario en vista Formulario.</span><span class="sxs-lookup"><span data-stu-id="0bd57-p114">You can select a form in the Navigation Pane and drag it to a macro action row. This automatically creates an **OpenForm** action that opens the form in Form view.</span></span>

<span data-ttu-id="0bd57-164">El filtro y la condición WHERE que se aplican se convierten en los valores de la propiedad **Filter** del formulario.</span><span class="sxs-lookup"><span data-stu-id="0bd57-164">The filter and WHERE condition you apply become the setting of the form's **Filter** property.</span></span>

## <a name="examples"></a><span data-ttu-id="0bd57-165">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0bd57-165">Examples</span></span>

<span data-ttu-id="0bd57-166">**Configurar el valor de un control con una macro**</span><span class="sxs-lookup"><span data-stu-id="0bd57-166">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="0bd57-p115">La siguiente macro abre el formulario Agregar productos desde un botón del formulario Proveedores. Muestra el uso de las acciones **Eco**, **CerrarVentana**, **AbrirFormulario**, **ConfigurarValor** e **IrAControl**. La acción **ConfigurarValor** configura el control Id. de proveedor en el formulario Productos para el proveedor actual del formulario Proveedores. La acción **IrAControl** mueve el foco al campo Id. de categoría, donde puede empezar a introducir los datos para el nuevo producto. Esta macro se debe adjuntar al botón Agregar productos del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="0bd57-p115">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0bd57-172">Acción</span><span class="sxs-lookup"><span data-stu-id="0bd57-172">Action</span></span></p></th>
<th><p><span data-ttu-id="0bd57-173">Argumentos: Configuración</span><span class="sxs-lookup"><span data-stu-id="0bd57-173">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="0bd57-174">Comentario</span><span class="sxs-lookup"><span data-stu-id="0bd57-174">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bd57-175"><strong>Eco</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-175"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-176"><strong>Eco activo</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-176"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-177">Detener la actualización de la pantalla mientras se ejecuta la macro.</span><span class="sxs-lookup"><span data-stu-id="0bd57-177">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bd57-178"><strong>CerrarVentana</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-178"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-179"><strong>Tipo de objeto</strong>: <strong>Nombre de FormObject</strong>: lista de producto <strong>Guardar</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-179"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-180">Cerrar el formulario Lista de productos</span><span class="sxs-lookup"><span data-stu-id="0bd57-180">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bd57-181"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-181"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-182"><strong>Nombre del formulario</strong>: productos <strong>vista</strong>: <strong>Modo FormData</strong>: <strong>Modo AddWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-182"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-183">Abrir el formulario Productos.</span><span class="sxs-lookup"><span data-stu-id="0bd57-183">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bd57-184"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-184"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-185"><strong>Elemento</strong>: [Forms]![Products]![SupplierID] <strong>Expresión</strong>: IdProveedor</span><span class="sxs-lookup"><span data-stu-id="0bd57-185"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="0bd57-186">Configurar el control Id. de proveedor para el proveedor actual del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="0bd57-186">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bd57-187"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-187"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-188"><strong>Nombre del control</strong>: IdCategoría</span><span class="sxs-lookup"><span data-stu-id="0bd57-188"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="0bd57-189">Ir al control Id. de categoría.</span><span class="sxs-lookup"><span data-stu-id="0bd57-189">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0bd57-p116">La siguiente macro abre la lista de productos en la esquina inferior derecha del formulario Proveedores y muestra los productos del proveedor actual. Muestra el uso de las acciones **Eco**, **CuadroDeMensajes**, **IrAControl**, **DetenerMacro**, **AbrirFormulario** y **MoverYCambiarTamañoDeVentana**. También muestra el uso de una expresión condicional con las acciones **CuadroDeMensajes**, **IrAControl** y **DetenerMacro**. Esta macro se debe adjuntar al botón Revisar productos del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="0bd57-p116">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<span data-ttu-id="0bd57-194">**Sincronizar los formularios con una macro**</span><span class="sxs-lookup"><span data-stu-id="0bd57-194">**Synchronize forms by using a macro**</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0bd57-195">Condición</span><span class="sxs-lookup"><span data-stu-id="0bd57-195">Condition</span></span></p></th>
<th><p><span data-ttu-id="0bd57-196">Acción</span><span class="sxs-lookup"><span data-stu-id="0bd57-196">Action</span></span></p></th>
<th><p><span data-ttu-id="0bd57-197">Argumentos: Configuración</span><span class="sxs-lookup"><span data-stu-id="0bd57-197">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="0bd57-198">Comentario</span><span class="sxs-lookup"><span data-stu-id="0bd57-198">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="0bd57-199"><strong>Eco</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-199"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-200"><strong>Eco activo</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-200"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-201">Detener la actualización de la pantalla mientras se ejecuta la macro.</span><span class="sxs-lookup"><span data-stu-id="0bd57-201">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bd57-202">IsNull([IdProveedor])</span><span class="sxs-lookup"><span data-stu-id="0bd57-202">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="0bd57-203"><strong>CuadroDeMensajes</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-203"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-204"><strong>Mensaje</strong>: mover al registro del proveedor los productos que quiera ver, luego, haga clic de nuevo en el botón Revisar productos.</span><span class="sxs-lookup"><span data-stu-id="0bd57-204"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="0bd57-205"><strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: seleccionar un proveedor</span><span class="sxs-lookup"><span data-stu-id="0bd57-205"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="0bd57-206">Si no hay ningún proveedor actual en el formulario Proveedores, mostrar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="0bd57-206">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bd57-207">...</span><span class="sxs-lookup"><span data-stu-id="0bd57-207"></span></span></p></td>
<td><p><span data-ttu-id="0bd57-208"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-208"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-209"><strong>Nombre del control</strong>: NombreDeEmpresa</span><span class="sxs-lookup"><span data-stu-id="0bd57-209"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="0bd57-210">Mover el foco al control NombreDeEmpresa.</span><span class="sxs-lookup"><span data-stu-id="0bd57-210">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bd57-211">...</span><span class="sxs-lookup"><span data-stu-id="0bd57-211"></span></span></p></td>
<td><p><span data-ttu-id="0bd57-212"><strong>DetenerMacro</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-212"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0bd57-213">Detener la macro.</span><span class="sxs-lookup"><span data-stu-id="0bd57-213">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="0bd57-214"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-214"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-215"><strong>Nombre del formulario</strong>: <strong>vista</strong>de lista de producto: <strong>Nombre DatasheetFilter</strong>: <strong>condición Where</strong>: [Id] = [formularios]! [Proveedores]! [SupplierID] <strong>Modo de datos</strong>: <strong>Modo de lectura OnlyWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-215"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-216">Abrir el formulario Lista de productos y mostrar los productos del proveedor actual.</span><span class="sxs-lookup"><span data-stu-id="0bd57-216">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="0bd57-217"><strong>MoverYCambiarTamañoDeVentana</strong></span><span class="sxs-lookup"><span data-stu-id="0bd57-217"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="0bd57-218"><strong>Derecha</strong>: 0.7799&quot; <strong>hacia abajo</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="0bd57-218"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="0bd57-219">Coloque el formulario Lista de productos en la esquina inferior derecha del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="0bd57-219">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

