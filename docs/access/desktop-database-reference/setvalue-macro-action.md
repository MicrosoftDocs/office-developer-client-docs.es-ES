---
title: EstablecerValor (acción de macro)
TOCTitle: SetValue macro action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 6b6f16c22e9265159c73279cfa1b2644adbc0277
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722693"
---
# <a name="setvalue-macro-action"></a><span data-ttu-id="49ef0-102">EstablecerValor (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="49ef0-102">SetValue macro action</span></span>

<span data-ttu-id="49ef0-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49ef0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49ef0-104">Puede usar la ación **SetValue** para configurar el valor de un campo, un control o una propiedad de Microsoft Access en un formulario, una hoja de datos del formulario o un informe.</span><span class="sxs-lookup"><span data-stu-id="49ef0-104">You can use the **SetValue** action to set the value of a Microsoft Access field, control, or property on a form, a form datasheet, or a report.</span></span>

> [!NOTE]
> - <span data-ttu-id="49ef0-105">[!NOTA] No puede usar la acción **SetValue** para configuar el valor de una propiedad de Access que devuelva un objeto.</span><span class="sxs-lookup"><span data-stu-id="49ef0-105">You cannot use the **SetValue** action to set the value of an Access property that returns an object.</span></span>
> - <span data-ttu-id="49ef0-106">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="49ef0-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="49ef0-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="49ef0-107">Setting</span></span>

<span data-ttu-id="49ef0-108">La acción **SetValue** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="49ef0-108">The **SetValue** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49ef0-109">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="49ef0-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="49ef0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="49ef0-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49ef0-111"><strong>Item</strong></span><span class="sxs-lookup"><span data-stu-id="49ef0-111"><strong>Item</strong></span></span></p></td>
<td><p><span data-ttu-id="49ef0-p101">El nombre del campo, el control o la propiedad cuyo valor quiere configurar. Escriba el nombre del campo, el control o la propiedad en el cuadro <strong>Elemento </strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Debe usar la sintaxis completa para hacer referencia a este elemento, como <em>controlname</em> (para un control en el formulario o el informe desde el que se llamó a la macro) o <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>. Se trata de un argumento obligatorio.</span><span class="sxs-lookup"><span data-stu-id="49ef0-p101">The name of the field, control, or property whose value you want to set. Enter the field, control, or property name in the <strong>Item</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You must use the full syntax to refer to this item, such as <em>controlname</em> (for a control on the form or report from which the macro was called) or <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49ef0-116"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="49ef0-116"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="49ef0-p102">La expresión que Access usa para configurar el valor de este elemento. Siempre debe usar la sintaxis completa para hacer referencia a los objetos de la expresión. Por ejemplo, para aumentar el valor de un control Salario de un formulario Empleados en un 10 por ciento, use Forms!Employees!Salary\*1.1. Se trata de un argumento obligatorio.</span><span class="sxs-lookup"><span data-stu-id="49ef0-p102">The expression Access uses to set the value for this item. You must always use the full syntax to refer to any objects in the expression. For example, to increase the value in a Salary control on an Employees form by 10 percent, use Forms!Employees!Salary\*1.1. This is a required argument.</span></span></p><p><span data-ttu-id="49ef0-121"><strong>Nota</strong>: no debe utilizar un signo de igual (=) antes de la expresión en este argumento.</span><span class="sxs-lookup"><span data-stu-id="49ef0-121"><strong>NOTE</strong>: You shouldn't use an equal sign (=) before the expression in this argument.</span></span> <span data-ttu-id="49ef0-122">Si lo hace, Access evalúa la expresión y, a continuación, utiliza este valor como la expresión en este argumento.</span><span class="sxs-lookup"><span data-stu-id="49ef0-122">If you do, Access evaluates the expression and then uses this value as the expression in this argument.</span></span> <span data-ttu-id="49ef0-123">Esto puede producir resultados inesperados si la expresión es una cadena.</span><span class="sxs-lookup"><span data-stu-id="49ef0-123">This can produce unexpected results if the expression is a string.</span></span></p>
<p><span data-ttu-id="49ef0-124">Por ejemplo, si escribe <strong> = &quot;cadena1&quot; </strong> para este argumento, Access evalúa primero la expresión como Cadena1.</span><span class="sxs-lookup"><span data-stu-id="49ef0-124">For example, if you type <strong>=&quot;String1&quot;</strong> for this argument, Access first evaluates the expression as String1.</span></span> <span data-ttu-id="49ef0-125">A continuación, utiliza Cadena1 como la expresión en este argumento, esperando encontrar un control o una propiedad denominados cadena1 en el formulario o informe que llamó a la macro.</span><span class="sxs-lookup"><span data-stu-id="49ef0-125">Then it uses String1 as the expression in this argument, expecting to find a control or property named String1 on the form or report that called the macro.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="49ef0-126">[!NOTA] En una base de datos de Access (.mdb o .accdb), haga clic en el botón **Crear** para usar el Generador de expresiones para crear una expresión para cualquiera de estos argumentos.</span><span class="sxs-lookup"><span data-stu-id="49ef0-126">In an Access database (.mdb or .accdb), click the **Build** button to use the Expression Builder to create an expression for either of these arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="49ef0-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="49ef0-127">Remarks</span></span>

<span data-ttu-id="49ef0-p105">Puede usar esta acción para configurar un valor para un campo o un control de un formulario, una hoja de datos de formulario o un informe. También puede configurar el valor de casi todas las propiedades de los controles, formularios e informes de cualquier vista. Para averiguar si una propiedad determinada se puede configurar con una macro y en qué vistas se puede configurar, consulte el tema Ayuda para la propiedad en el Editor de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="49ef0-p105">You can use this action to set a value for a field or control on a form, a form datasheet, or a report. You can also set the value for almost all control, form, and report properties in any view. To find out whether a particular property can be set by using a macro and which views it can be set in, see the Help topic for that property in the Visual Basic Editor.</span></span>

<span data-ttu-id="49ef0-131">También puede configurar el valor de un campo en la tabla subyacente de un formulario, incluso si el formulario no contiene un control enlazado al campo.</span><span class="sxs-lookup"><span data-stu-id="49ef0-131">You can also set the value for a field in a form's underlying table even if the form doesn't contain a control bound to the field.</span></span> <span data-ttu-id="49ef0-132">Use la sintaxis **Forms**\!*formname*\!*fieldname* en el cuadro **elemento** para establecer el valor de ese campo.</span><span class="sxs-lookup"><span data-stu-id="49ef0-132">Use the syntax **Forms**\!*formname*\!*fieldname* in the **Item** box to set the value for such a field.</span></span> <span data-ttu-id="49ef0-133">También puede consultar a un campo de tabla subyacente de un informe mediante el uso de la sintaxis de **informes de**\!*reportname*\!*fieldname*, pero debe haber un control del informe enlazado a este campo o el campo debe hacer referencia a un control calculado en el informe.</span><span class="sxs-lookup"><span data-stu-id="49ef0-133">You can also refer to a field in a report's underlying table by using the syntax **Reports**\!*reportname*\!*fieldname*, but there must be a control on the report bound to this field, or the field must be referred to in a calculated control on the report.</span></span>

<span data-ttu-id="49ef0-p107">Si configura el valor de un control en un formulario, la acción **SetValue** no desencadena las reglas de validación de nivel de formulario del control, pero desencadena las reglas de validación de nivel de tabla del campo subyacente si el control es un control enlazado. La acción **SetValue** también desencadena la actualización, pero puede que no se produzca de forma inmediata. Para desencadenar la actualización inmediatamente y forzar la finalización de la actualización, use la acción **RepaintObject**. El valor que se configura en un control con la acción **SetValue** tampoco se ve afectada por una máscara de entrada configurada en la propiedad **InputMask** del control o del campo subyacente.</span><span class="sxs-lookup"><span data-stu-id="49ef0-p107">If you set the value of a control on a form, the **SetValue** action doesn't trigger the control's form-level validation rules, but it does trigger the underlying field's table-level validation rules if the control is a bound control. The **SetValue** action also triggers recalculation, but the recalculation may not happen immediately. To trigger immediate repainting and force the recalculation to completion, use the **RepaintObject** action. The value you set in a control by using the **SetValue** action is also not affected by an input mask set in the control's or underlying field's **InputMask** property.</span></span>

<span data-ttu-id="49ef0-p108">Para cambiar el valor de un control, puede usar la acción **SetValue** en una macro especificada por la propiedad de evento **AfterUpdate** del control. Sin embargo, no puede usar la acción **SetValue** en una macro especificada por una propiedad de evento **BeforeUpdate** del control para cambiar el valor del control (aunque puede usar la acción **SetValue** para cambiar el valor de otros controles). También puede usar la acción **SetValue** en una macro especificada por la propiedad **BeforeUpdate** o **AfterUpdate** de un formulario para cambiar el valor de los controles del registro actual.</span><span class="sxs-lookup"><span data-stu-id="49ef0-p108">To change the value of a control, you can use the **SetValue** action in a macro specified by the control's **AfterUpdate** event property. However, you can't use the **SetValue** action in a macro specified by a control's **BeforeUpdate** event property to change the value of the control (although you can use the **SetValue** action to change the value of other controls). You can also use the **SetValue** action in a macro specified by the **BeforeUpdate** or **AfterUpdate** property of a form to change the value of any controls in the current record.</span></span>

> [!NOTE]
> <span data-ttu-id="49ef0-141">No puede usar la acción **SetValue** para configurar el valor de los siguientes controles:</span><span class="sxs-lookup"><span data-stu-id="49ef0-141">You can't use the **SetValue** action to set the value of the following controls:</span></span>
> - <span data-ttu-id="49ef0-142">Controles enlazados y calculados en informes.</span><span class="sxs-lookup"><span data-stu-id="49ef0-142">Bound controls and calculated controls on reports.</span></span>
> - <span data-ttu-id="49ef0-143">Controles calculados en formularios.</span><span class="sxs-lookup"><span data-stu-id="49ef0-143">Calculated controls on forms.</span></span>

> [!TIP]
> <span data-ttu-id="49ef0-144">[!SUGERENCIA] Puede usar la acción **SetValue** para ocultar o mostrar un formulario en la vista Formulario.</span><span class="sxs-lookup"><span data-stu-id="49ef0-144">You can use the **SetValue** action to hide or show a form in Form view.</span></span> <span data-ttu-id="49ef0-145">¡Escriba **formularios**! formname \*\*\*\*. Visible\*\* en el cuadro **elemento** y **No** o **Sí** en el cuadro **expresión** .</span><span class="sxs-lookup"><span data-stu-id="49ef0-145">Enter **Forms**!*formname\*\*\*.Visible*\* in the **Item** box, and **No** or **Yes** in the **Expression** box.</span></span> <span data-ttu-id="49ef0-146">Configurar una propiedad **Visible** de un formulario modal en **No** oculta el formulario y lo convierte en no modal.</span><span class="sxs-lookup"><span data-stu-id="49ef0-146">Setting a modal form's **Visible** property to **No** hides the form and makes it modeless.</span></span> <span data-ttu-id="49ef0-147">Configurar la propiedad en **Sí** muestra el formulario y lo convierte en modal de nuevo.</span><span class="sxs-lookup"><span data-stu-id="49ef0-147">Setting the property to **Yes** displays the form and makes it modal again.</span></span>

<span data-ttu-id="49ef0-p110">Cambiar el valor de o agregar nuevos datos a un control mediante la acción **SetValue** en una macro no desencadena eventos como **BeforeUpdate**, **BeforeInsert** o **Change** que ocurren al cambiar o introducir datos en estos controles en la interfaz de usuario. Estos eventos tampoco ocurren si configura el valor del control con un módulo de Visual Basic para aplicaciones (VBA).</span><span class="sxs-lookup"><span data-stu-id="49ef0-p110">Changing the value of or adding new data in a control by using the **SetValue** action in a macro doesn't trigger events such as **BeforeUpdate**, **BeforeInsert**, or **Change** that occur when you change or enter data in these controls in the user interface. These events also don't occur if you set the value of the control by using a Visual Basic for Applications (VBA) module.</span></span>

<span data-ttu-id="49ef0-p111">Esta acción no está disponible en un módulo de VBA. Configure el valor directamente en VBA.</span><span class="sxs-lookup"><span data-stu-id="49ef0-p111">This action isn't available in a VBA module. Set the value directly in VBA.</span></span>

## <a name="example"></a><span data-ttu-id="49ef0-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="49ef0-152">Example</span></span>

<span data-ttu-id="49ef0-153">**Configurar el valor de un control con una macro**</span><span class="sxs-lookup"><span data-stu-id="49ef0-153">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="49ef0-p112">La siguiente macro abre el formulario Agregar productos desde un botón del formulario Proveedores. Muestra el uso de las acciones **Eco**, **CerrarVentana**, **AbrirFormulario**, **ConfigurarValor** e **IrAControl**. La acción **SetValue** configura el control Id. de proveedor en el formulario Productos para el proveedor actual del formulario Proveedores. La acción **IrAControl** mueve el foco al campo Id. de categoría, donde puede empezar a introducir los datos para el nuevo producto. Esta macro se debe adjuntar al botón Agregar productos del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="49ef0-p112">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the SupplierID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the CategoryID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49ef0-159">Acción</span><span class="sxs-lookup"><span data-stu-id="49ef0-159">Action</span></span></p></th>
<th><p><span data-ttu-id="49ef0-160">Argumentos: Configuración</span><span class="sxs-lookup"><span data-stu-id="49ef0-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="49ef0-161">Comentario</span><span class="sxs-lookup"><span data-stu-id="49ef0-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49ef0-162"><strong>Eco</strong></span><span class="sxs-lookup"><span data-stu-id="49ef0-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="49ef0-163"><strong>Eco activo</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="49ef0-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="49ef0-164">Detener la actualización de la pantalla mientras se ejecuta la macro.</span><span class="sxs-lookup"><span data-stu-id="49ef0-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49ef0-165"><strong>CerrarVentana</strong></span><span class="sxs-lookup"><span data-stu-id="49ef0-165"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="49ef0-166"><strong>Tipo de objeto</strong>: <strong>Nombre de FormObject</strong>: lista de producto <strong>Guardar</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="49ef0-166"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="49ef0-167">Cerrar el formulario Lista de productos</span><span class="sxs-lookup"><span data-stu-id="49ef0-167">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49ef0-168"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="49ef0-168"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="49ef0-169"><strong>Nombre del formulario</strong>: productos <strong>vista</strong>: <strong>Modo FormData</strong>: <strong>Modo AddWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="49ef0-169"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="49ef0-170">Abrir el formulario Productos.</span><span class="sxs-lookup"><span data-stu-id="49ef0-170">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49ef0-171"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="49ef0-171"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="49ef0-172"><strong>Elemento</strong>: [Forms]![Products]![SupplierID] <strong>Expresión</strong>: IdProveedor</span><span class="sxs-lookup"><span data-stu-id="49ef0-172"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="49ef0-173">Configurar el control IdProveedor el proveedor actual del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="49ef0-173">Set the SupplierID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49ef0-174"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="49ef0-174"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="49ef0-175"><strong>Nombre del control</strong>: IdCategoría</span><span class="sxs-lookup"><span data-stu-id="49ef0-175"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="49ef0-176">Ir al control Id.</span><span class="sxs-lookup"><span data-stu-id="49ef0-176">Go to the CategoryID control.</span></span></p></td>
</tr>
</tbody>
</table>

