---
title: MoverYCambiarTamañoDeVentana (acción de macro)
TOCTitle: MoveAndSizeWindow macro action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1b127995a2f9a0af7da80e9df862259b570870e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288809"
---
# <a name="moveandsizewindow-macro-action"></a><span data-ttu-id="1be0d-102">MoverYCambiarTamañoDeVentana (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="1be0d-102">MoveAndSizeWindow macro action</span></span>

<span data-ttu-id="1be0d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1be0d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1be0d-104">Si ha establecido las opciones de la ventana de documento para que usen ventanas superpuestas en lugar de documentos con fichas, puede usar la acción **MoveAndSizeWindow** para mover o cambiar el tamaño de la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="1be0d-104">If you have set your document window options to use overlapping windows instead of tabbed documents, you can use the **MoveAndSizeWindow** action to move or resize the active window.</span></span> <span data-ttu-id="1be0d-105">Para obtener información sobre cómo establecer las opciones de la ventana del documento, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="1be0d-105">For information on how to set document window options, see the Remarks section.</span></span>

## <a name="setting"></a><span data-ttu-id="1be0d-106">Setting</span><span class="sxs-lookup"><span data-stu-id="1be0d-106">Setting</span></span>

<span data-ttu-id="1be0d-107">La **acción MoveAndSizeWindow** tiene los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="1be0d-107">The **MoveAndSizeWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1be0d-108">Argumento de acción</span><span class="sxs-lookup"><span data-stu-id="1be0d-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="1be0d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1be0d-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1be0d-110"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="1be0d-110"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="1be0d-111">Nueva posición horizontal de la esquina superior izquierda de la ventana, medida desde el borde izquierdo de la ventana contenedora.</span><span class="sxs-lookup"><span data-stu-id="1be0d-111">The new horizontal position of the window's upper-left corner, measured from the left edge of its containing window.</span></span> <span data-ttu-id="1be0d-112">Escriba la posición en <strong>el</strong> cuadro Derecho en la sección <strong>Argumentos de acción</strong> del panel Generador de macros.</span><span class="sxs-lookup"><span data-stu-id="1be0d-112">Enter the position in the <strong>Right</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be0d-113"><strong>Down</strong></span><span class="sxs-lookup"><span data-stu-id="1be0d-113"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="1be0d-114">Nueva posición vertical de la esquina superior izquierda de la ventana, medida desde el borde superior de la ventana contenedora.</span><span class="sxs-lookup"><span data-stu-id="1be0d-114">The new vertical position of the window's upper-left corner, measured from the top edge of its containing window.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be0d-115"><strong>Width</strong></span><span class="sxs-lookup"><span data-stu-id="1be0d-115"><strong>Width</strong></span></span></p></td>
<td><p><span data-ttu-id="1be0d-116">Nuevo ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1be0d-116">The window's new width.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be0d-117"><strong>Height</strong></span><span class="sxs-lookup"><span data-stu-id="1be0d-117"><strong>Height</strong></span></span></p></td>
<td><p><span data-ttu-id="1be0d-118">Nuevo alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1be0d-118">The window's new height.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1be0d-119">Si deja un argumento en blanco, Microsoft Access usa la configuración actual de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1be0d-119">If you leave an argument blank, Microsoft Access uses the window's current setting.</span></span>

<span data-ttu-id="1be0d-120">Debe escribir un valor para al menos un argumento.</span><span class="sxs-lookup"><span data-stu-id="1be0d-120">You must enter a value for at least one argument.</span></span>

> [!NOTE]
> <span data-ttu-id="1be0d-121">Cada medida se encuentra en pulgadas o centímetros, según la configuración regional del Panel de control de Windows.</span><span class="sxs-lookup"><span data-stu-id="1be0d-121">Each measurement is in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span>

## <a name="remarks"></a><span data-ttu-id="1be0d-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1be0d-122">Remarks</span></span>

<span data-ttu-id="1be0d-123">Para configurar una aplicación para que use ventanas superpuestas en lugar de documentos con fichas, use el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="1be0d-123">To set up an application to use overlapping windows instead of tabbed documents, use the following procedure:</span></span>

1.  <span data-ttu-id="1be0d-124">Opciones de **clic**</span><span class="sxs-lookup"><span data-stu-id="1be0d-124">Click **Options**</span></span>

2.  <span data-ttu-id="1be0d-125">Haga clic **en Base de datos actual.**</span><span class="sxs-lookup"><span data-stu-id="1be0d-125">Click **Current Database**.</span></span>

3.  <span data-ttu-id="1be0d-126">En la sección **Opciones de aplicación**, bajo **Opciones de la ventana de documentos**, haga clic en **Ventanas superpuestas**.</span><span class="sxs-lookup"><span data-stu-id="1be0d-126">In the **Application Options** section, under **Document Window Options**, click **Overlapping Windows**.</span></span>

4.  <span data-ttu-id="1be0d-127">Haga **clic en Aceptar** y, a continuación, cierre y vuelva a abrir la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1be0d-127">Click **OK**, and then close and reopen the database.</span></span>

<span data-ttu-id="1be0d-128">Esta acción es similar a hacer clic **en Mover** o **Cambiar** tamaño en el menú **Control de** la ventana.</span><span class="sxs-lookup"><span data-stu-id="1be0d-128">This action is similar to clicking **Move** or **Size** on the window's **Control** menu.</span></span> <span data-ttu-id="1be0d-129">Con los comandos de menú, se usan las teclas de dirección del teclado para mover o cambiar el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1be0d-129">With the menu commands, you use the keyboard's arrow keys to move or resize the window.</span></span> <span data-ttu-id="1be0d-130">Con la **acción MoveAndSizeWindow,** se escriben las medidas de posición y tamaño directamente.</span><span class="sxs-lookup"><span data-stu-id="1be0d-130">With the **MoveAndSizeWindow** action, you enter the position and size measurements directly.</span></span> <span data-ttu-id="1be0d-131">También puedes usar el mouse para mover y cambiar el tamaño de las ventanas.</span><span class="sxs-lookup"><span data-stu-id="1be0d-131">You can also use the mouse to move and size windows.</span></span>

<span data-ttu-id="1be0d-132">Puede usar esta acción en cualquier ventana, en cualquier vista.</span><span class="sxs-lookup"><span data-stu-id="1be0d-132">You can use this action on any window, in any view.</span></span>

> [!TIP]
> - <span data-ttu-id="1be0d-133">Para mover una ventana sin cambiar el tamaño, escriba valores para los argumentos **Right** y **Down,** pero deje en blanco los argumentos **Width** y **Height.**</span><span class="sxs-lookup"><span data-stu-id="1be0d-133">To move a window without resizing it, enter values for the **Right** and **Down** arguments but leave the **Width** and **Height** arguments blank.</span></span>
> - <span data-ttu-id="1be0d-134">Para cambiar el tamaño de una ventana sin moverla, escriba valores para los argumentos **Width** y **Height,** pero deje en blanco los argumentos **Right** y **Down.**</span><span class="sxs-lookup"><span data-stu-id="1be0d-134">To resize a window without moving it, enter values for the **Width** and **Height** arguments but leave the **Right** and **Down** arguments blank.</span></span>

<span data-ttu-id="1be0d-135">Para ejecutar la **acción MoveAndSizeWindow** en un módulo Visual Basic para Aplicaciones (VBA), utilice el método **MoveSize** del **objeto DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="1be0d-135">To run the **MoveAndSizeWindow** action in a Visual Basic for Applications (VBA) module, use the **MoveSize** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="1be0d-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1be0d-136">Example</span></span>

<span data-ttu-id="1be0d-137">**Sincronizar formularios con una macro**</span><span class="sxs-lookup"><span data-stu-id="1be0d-137">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="1be0d-p104">La siguiente macro abre Lista de productos en la esquina inferior derecha del formulario Proveedores y muestra los productos del proveedor actual. Muestra el uso de las acciones **Eco**, **CuadroDeMensajes**, **IrAControl**, **DetenerMacro**, **AbrirFormulario** y **MoverYCambiarTamañoDeVentana**. También muestra el uso de una expresión condicional con las acciones **CuadroDeMensajes**, **IrAControl** y **DetenerMacro**. Esta macro se debe adjuntar al botón Revisar productos del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="1be0d-p104">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1be0d-142">Condition</span><span class="sxs-lookup"><span data-stu-id="1be0d-142">Condition</span></span></p></th>
<th><p><span data-ttu-id="1be0d-143">Acción</span><span class="sxs-lookup"><span data-stu-id="1be0d-143">Action</span></span></p></th>
<th><p><span data-ttu-id="1be0d-144">Argumentos: Configuración</span><span class="sxs-lookup"><span data-stu-id="1be0d-144">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="1be0d-145">Comentario</span><span class="sxs-lookup"><span data-stu-id="1be0d-145">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="1be0d-146"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="1be0d-146"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="1be0d-147"><strong>Eco activo</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="1be0d-147"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="1be0d-148">Detener la actualización de la pantalla mientras se ejecuta la macro.</span><span class="sxs-lookup"><span data-stu-id="1be0d-148">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be0d-149">IsNull([Id. de proveedor])</span><span class="sxs-lookup"><span data-stu-id="1be0d-149">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="1be0d-150"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="1be0d-150"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="1be0d-151"><strong>Mensaje</strong>: Mueva al registro de proveedores los productos que quiera ver y haga clic en el botón Revisar productos de nuevo.</span><span class="sxs-lookup"><span data-stu-id="1be0d-151"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="1be0d-152"><strong>Sonido</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Seleccionar un proveedor</span><span class="sxs-lookup"><span data-stu-id="1be0d-152"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="1be0d-153">Si no hay ningún proveedor actual en el formulario Proveedores, mostrar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="1be0d-153">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="1be0d-154"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="1be0d-154"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="1be0d-155"><strong>Nombre del control</strong>: NombreDeEmpresa</span><span class="sxs-lookup"><span data-stu-id="1be0d-155"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="1be0d-156">Mover el foco al control NombreDeEmpresa.</span><span class="sxs-lookup"><span data-stu-id="1be0d-156">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be0d-157">...</span><span class="sxs-lookup"><span data-stu-id="1be0d-157">...</span></span></p></td>
<td><p><span data-ttu-id="1be0d-158"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="1be0d-158"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="1be0d-159">Detener la macro.</span><span class="sxs-lookup"><span data-stu-id="1be0d-159">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="1be0d-160"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="1be0d-160"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="1be0d-161"><strong>Nombre del formulario</strong>: Vista de lista <strong>de productos</strong>: Nombre del filtro <strong>de hoja</strong>de datos : <strong>Condición</strong>Where : [Id. de proveedor] = [Formularios]! [Proveedores]! [SupplierID] <strong>Modo de datos</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="1be0d-161"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="1be0d-162">Abrir el formulario Lista de productos y mostrar los productos del proveedor actual.</span><span class="sxs-lookup"><span data-stu-id="1be0d-162">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="1be0d-163"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="1be0d-163"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="1be0d-164"><strong>Derecha</strong>: 0,7799 &quot; <strong>Abajo</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="1be0d-164"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="1be0d-165">Coloque el formulario Lista de productos en la esquina inferior derecha del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="1be0d-165">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

