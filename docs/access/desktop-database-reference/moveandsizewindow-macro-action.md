---
title: MoveAndSizeWindow Macro Action
TOCTitle: MoveAndSizeWindow Macro Action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d423668f5ef53abf4216fa8f976c674474a752ed
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485291"
---
# <a name="moveandsizewindow-macro-action"></a><span data-ttu-id="96047-102">MoveAndSizeWindow Macro Action</span><span class="sxs-lookup"><span data-stu-id="96047-102">MoveAndSizeWindow Macro Action</span></span>


<span data-ttu-id="96047-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="96047-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="96047-104">Si ha establecido el documento de opciones de la ventana para usar ventanas superpuestas en lugar de documentos con fichas, puede utilizar la acción **Moverycambiartamañodeventana** para mover o cambiar el tamaño de la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="96047-104">If you have set your document window options to use overlapping windows instead of tabbed documents, you can use the **MoveAndSizeWindow** action to move or resize the active window.</span></span> <span data-ttu-id="96047-105">Para obtener información acerca de cómo configurar las opciones de la ventana de documento, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="96047-105">For information on how to set document window options, see the Remarks section.</span></span>

## <a name="setting"></a><span data-ttu-id="96047-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="96047-106">Setting</span></span>

<span data-ttu-id="96047-107">La acción **Moverycambiartamañodeventana** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="96047-107">The **MoveAndSizeWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96047-108">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="96047-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="96047-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="96047-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96047-110"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="96047-110"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="96047-111">Nueva posición horizontal de la esquina superior izquierda de la ventana, medida desde el borde izquierdo de la ventana contenedora.</span><span class="sxs-lookup"><span data-stu-id="96047-111">The new horizontal position of the window's upper-left corner, measured from the left edge of its containing window.</span></span> <span data-ttu-id="96047-112">Especifique la posición en el cuadro de la <strong>derecha</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros.</span><span class="sxs-lookup"><span data-stu-id="96047-112">Enter the position in the <strong>Right</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96047-113"><strong>Down</strong></span><span class="sxs-lookup"><span data-stu-id="96047-113"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="96047-114">Nueva posición vertical de la esquina superior izquierda de la ventana, medida desde el borde superior de la ventana contenedora.</span><span class="sxs-lookup"><span data-stu-id="96047-114">The new vertical position of the window's upper-left corner, measured from the top edge of its containing window.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96047-115"><strong>Width</strong></span><span class="sxs-lookup"><span data-stu-id="96047-115"><strong>Width</strong></span></span></p></td>
<td><p><span data-ttu-id="96047-116">Nuevo ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="96047-116">The window's new width.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96047-117"><strong>Height</strong></span><span class="sxs-lookup"><span data-stu-id="96047-117"><strong>Height</strong></span></span></p></td>
<td><p><span data-ttu-id="96047-118">Nuevo alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="96047-118">The window's new height.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96047-119">Si deja un argumento en blanco, Microsoft Access utiliza la configuración actual de la ventana.</span><span class="sxs-lookup"><span data-stu-id="96047-119">If you leave an argument blank, Microsoft Access uses the window's current setting.</span></span>

<span data-ttu-id="96047-120">Debe escribir un valor para al menos un argumento.</span><span class="sxs-lookup"><span data-stu-id="96047-120">You must enter a value for at least one argument.</span></span>


> [!NOTE]
> <P><span data-ttu-id="96047-121">Cada medida es en pulgadas o centímetros, dependiendo de la configuración regional en el Panel de Control de Windows.</span><span class="sxs-lookup"><span data-stu-id="96047-121">Each measurement is in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="96047-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96047-122">Remarks</span></span>

<span data-ttu-id="96047-123">Para configurar una aplicación para utilizar ventanas superpuestas en lugar de documentos con fichas, utilice el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="96047-123">To set up an application to use overlapping windows instead of tabbed documents, use the following procedure:</span></span>

1.  <span data-ttu-id="96047-124">y, a continuación, haga clic en **Opciones**</span><span class="sxs-lookup"><span data-stu-id="96047-124">and then click **Options**</span></span>

2.  <span data-ttu-id="96047-125">Haga clic en **base de datos actual**.</span><span class="sxs-lookup"><span data-stu-id="96047-125">Click **Current Database**.</span></span>

3.  <span data-ttu-id="96047-126">En la sección **Opciones de aplicación**, bajo **Opciones de la ventana de documentos**, haga clic en **Ventanas superpuestas**.</span><span class="sxs-lookup"><span data-stu-id="96047-126">In the **Application Options** section, under **Document Window Options**, click **Overlapping Windows**.</span></span>

4.  <span data-ttu-id="96047-127">Haga clic en **Aceptar**y, a continuación, cierre y vuelva a abrir la base de datos.</span><span class="sxs-lookup"><span data-stu-id="96047-127">Click **OK**, and then close and reopen the database.</span></span>

<span data-ttu-id="96047-128">Esta acción es similar a hacer clic en **mover** o **tamaño** en el menú **Control** de la ventana.</span><span class="sxs-lookup"><span data-stu-id="96047-128">This action is similar to clicking **Move** or **Size** on the window's **Control** menu.</span></span> <span data-ttu-id="96047-129">Con los comandos de menú, se utilizan las teclas de desplazamiento para mover o cambiar el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="96047-129">With the menu commands, you use the keyboard's arrow keys to move or resize the window.</span></span> <span data-ttu-id="96047-130">Con la acción **Moverycambiartamañodeventana** , introduzca directamente las medidas de posición y tamaño.</span><span class="sxs-lookup"><span data-stu-id="96047-130">With the **MoveAndSizeWindow** action, you enter the position and size measurements directly.</span></span> <span data-ttu-id="96047-131">También puede usar el mouse para mover y cambiar el tamaño de windows.</span><span class="sxs-lookup"><span data-stu-id="96047-131">You can also use the mouse to move and size windows.</span></span>

<span data-ttu-id="96047-132">Puede usar esta acción en cualquier ventana, en cualquier vista.</span><span class="sxs-lookup"><span data-stu-id="96047-132">You can use this action on any window, in any view.</span></span>

<span data-ttu-id="96047-133">**Sugerencias**</span><span class="sxs-lookup"><span data-stu-id="96047-133">**Tips**</span></span>

  - <span data-ttu-id="96047-134">Para mover una ventana sin cambiar su tamaño, especifique valores para la **derecha** y **abajo** argumentos pero deja en blanco los argumentos **ancho** y **alto** .</span><span class="sxs-lookup"><span data-stu-id="96047-134">To move a window without resizing it, enter values for the **Right** and **Down** arguments but leave the **Width** and **Height** arguments blank.</span></span>

  - <span data-ttu-id="96047-135">Para cambiar el tamaño de una ventana sin moverla, especifique valores para los argumentos de **alto** y **ancho** pero deja en blanco los argumentos **derecha** y **abajo** .</span><span class="sxs-lookup"><span data-stu-id="96047-135">To resize a window without moving it, enter values for the **Width** and **Height** arguments but leave the **Right** and **Down** arguments blank.</span></span>

<span data-ttu-id="96047-136">Para ejecutar la acción **Moverycambiartamañodeventana** en un módulo Visual Basic para aplicaciones (VBA), use el método **MoveSize** del objeto **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="96047-136">To run the **MoveAndSizeWindow** action in a Visual Basic for Applications (VBA) module, use the **MoveSize** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="96047-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="96047-137">Example</span></span>

<span data-ttu-id="96047-138">**Sincronizar formularios con una macro**</span><span class="sxs-lookup"><span data-stu-id="96047-138">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="96047-p104">La siguiente macro abre Lista de productos en la esquina inferior derecha del formulario Proveedores y muestra los productos del proveedor actual. Muestra el uso de las acciones **Eco**, **CuadroDeMensajes**, **IrAControl**, **DetenerMacro**, **AbrirFormulario** y **MoverYCambiarTamañoDeVentana**. También muestra el uso de una expresión condicional con las acciones **CuadroDeMensajes**, **IrAControl** y **DetenerMacro**. Esta macro se debe adjuntar al botón Revisar productos del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="96047-p104">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96047-143">Condición</span><span class="sxs-lookup"><span data-stu-id="96047-143">Condition</span></span></p></th>
<th><p><span data-ttu-id="96047-144">Acción</span><span class="sxs-lookup"><span data-stu-id="96047-144">Action</span></span></p></th>
<th><p><span data-ttu-id="96047-145">Argumentos: Configuración</span><span class="sxs-lookup"><span data-stu-id="96047-145">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="96047-146">Comentario</span><span class="sxs-lookup"><span data-stu-id="96047-146">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="96047-147"><strong>Eco</strong></span><span class="sxs-lookup"><span data-stu-id="96047-147"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="96047-148"><strong>Eco activo</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="96047-148"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="96047-149">Detener la actualización de la pantalla mientras se ejecuta la macro.</span><span class="sxs-lookup"><span data-stu-id="96047-149">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96047-150">IsNull([Id. de proveedor])</span><span class="sxs-lookup"><span data-stu-id="96047-150">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="96047-151"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="96047-151"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="96047-152"><strong>Mensaje</strong>: mover al registro del proveedor los productos que quiera ver, luego, haga clic de nuevo en el botón Revisar productos.</span><span class="sxs-lookup"><span data-stu-id="96047-152"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="96047-153"><strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: seleccionar un proveedor</span><span class="sxs-lookup"><span data-stu-id="96047-153"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="96047-154">Si no hay ningún proveedor actual en el formulario Proveedores, mostrar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="96047-154">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="96047-155"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="96047-155"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="96047-156"><strong>Nombre del control</strong>: NombreDeEmpresa</span><span class="sxs-lookup"><span data-stu-id="96047-156"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="96047-157">Mover el foco al control NombreDeEmpresa.</span><span class="sxs-lookup"><span data-stu-id="96047-157">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96047-158">...</span><span class="sxs-lookup"><span data-stu-id="96047-158"></span></span></p></td>
<td><p><span data-ttu-id="96047-159"><strong>DetenerMacro</strong></span><span class="sxs-lookup"><span data-stu-id="96047-159"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="96047-160">Detener la macro.</span><span class="sxs-lookup"><span data-stu-id="96047-160">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="96047-161"><strong>AbrirFormulario</strong></span><span class="sxs-lookup"><span data-stu-id="96047-161"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="96047-162"><strong>Nombre del formulario</strong>: <strong>vista</strong>de lista de producto: <strong>Nombre de DatasheetFilter</strong>: <strong>condición Where</strong>: [ID de proveedor] = [formularios]! [Proveedores]! [SupplierID] <strong>Modo de datos</strong>: <strong>Modo de lectura OnlyWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="96047-162"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="96047-163">Abrir el formulario Lista de productos y mostrar los productos del proveedor actual.</span><span class="sxs-lookup"><span data-stu-id="96047-163">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="96047-164"><strong>MoverYCambiarTamañoDeVentana</strong></span><span class="sxs-lookup"><span data-stu-id="96047-164"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="96047-165"><strong>Derecha</strong>: 0.7799&quot; <strong>hacia abajo</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="96047-165"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="96047-166">Coloque el formulario Lista de productos en la esquina inferior derecha del formulario Proveedores.</span><span class="sxs-lookup"><span data-stu-id="96047-166">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

