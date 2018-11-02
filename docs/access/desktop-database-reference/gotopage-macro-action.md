---
title: IrAPágina (acción de macro)
TOCTitle: GoToPage macro action
ms:assetid: 611aadff-83b7-e74d-4093-93fb5ce6e3ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194858(v=office.15)
ms:contentKeyID: 48545199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm129285
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dd38a7f4973195fdd758934ceec787d623c3353c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923269"
---
# <a name="gotopage-macro-action"></a><span data-ttu-id="33cca-102">IrAPágina (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="33cca-102">GoToPage macro action</span></span>


<span data-ttu-id="33cca-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="33cca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="33cca-p101">Puede usar la acción **IrAPágina** para mover el enfoque del formulario activo al primer control de una página especificada. Puede usar esta acción si ha creado un formulario con saltos de página que contenga grupos de información relacionada. Por ejemplo, podría tener un formulario Empleados con información personal en una página, información de la oficina en otra e información de las ventas en una tercera. Puede usar la acción **IrAPágina** para moverse a la página deseada. También puede presentar varias páginas de información en un único formulario mediante controles de pestaña.</span><span class="sxs-lookup"><span data-stu-id="33cca-p101">You can use the **GoToPage** action to move the focus in the active form to the first control on a specified page. You can use this action if you have created a form with page breaks that contains groups of related information. For example, you might have an Employees form with personal information on one page, office information on another page, and sales information on a third page. You can use the **GoToPage** action to move to the desired page. You can also present multiple pages of information on a single form by using tab controls.</span></span>

## <a name="setting"></a><span data-ttu-id="33cca-109">Configuración</span><span class="sxs-lookup"><span data-stu-id="33cca-109">Setting</span></span>

<span data-ttu-id="33cca-110">La acción **IrAPágina** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="33cca-110">The **GoToPage** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="33cca-111">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="33cca-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="33cca-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="33cca-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33cca-113"><strong>Número de página</strong></span><span class="sxs-lookup"><span data-stu-id="33cca-113"><strong>Page Number</strong></span></span></p></td>
<td><p><span data-ttu-id="33cca-p102">Número de la página a la que se desea trasladar el enfoque. Especifique el número de página en el cuadro <strong>Número de página</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Si deja este argumento en blanco, el enfoque permanece en la página activa. Puede usar los argumentos <strong>Derecho</strong> y <strong>Abajo</strong> para mostrar la parte de la página que desea ver.</span><span class="sxs-lookup"><span data-stu-id="33cca-p102">The number of the page to which you want to move the focus. Enter the page number in the <strong>Page Number</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. If you leave this argument blank, the focus stays on the current page. You can use the <strong>Right</strong> and <strong>Down</strong> arguments to display the part of the page you want to see.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33cca-118"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="33cca-118"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="33cca-p103">Posición horizontal de la zona en la página, medida desde el borde izquierdo de la ventana que la contiene, que va a aparecer en el borde izquierdo de la ventana. Es obligatorio si se especifica el argumento <strong>Abajo</strong>.</span><span class="sxs-lookup"><span data-stu-id="33cca-p103">The horizontal position of the spot on the page, measured from the left edge of its containing window, that is to appear at the left edge of the window. This is required if you specify a <strong>Down</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33cca-121"><strong>Down</strong></span><span class="sxs-lookup"><span data-stu-id="33cca-121"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="33cca-p104">Posición vertical de la zona en la página, medida desde el borde superior de la ventana que la contiene, que va a aparecer en el borde superior de la ventana. Es obligatorio si se especifica el argumento <strong>Derecha</strong>.</span><span class="sxs-lookup"><span data-stu-id="33cca-p104">The vertical position of the spot on the page, measured from the top edge of its containing window, that is to appear at the top edge of the window. This is required if you specify a <strong>Right</strong> argument.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="33cca-124">[!NOTA] Los argumentos <STRONG>Derecha</STRONG> y <STRONG>Abajo</STRONG> se especifican en pulgadas o centímetros, en función de la configuración regional especificada en el Panel de control de Windows.</span><span class="sxs-lookup"><span data-stu-id="33cca-124">The <STRONG>Right</STRONG> and <STRONG>Down</STRONG> arguments are measured in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="33cca-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="33cca-125">Remarks</span></span>

<span data-ttu-id="33cca-p105">Puede usar esta acción para seleccionar el primer control (según viene definido por el orden de tabulación del formulario) de la página especificada. Use la acción **IrAControl** para moverse a un control determinado del formulario.</span><span class="sxs-lookup"><span data-stu-id="33cca-p105">You can use this action to select the first control (as defined by the form's tab order) on the specified page. Use the **GoToControl** action to move to a particular control on the form.</span></span>

<span data-ttu-id="33cca-128">Puede usar los argumentos **derecha** y **abajo** para los formularios con páginas mayores que la ventana de Access.</span><span class="sxs-lookup"><span data-stu-id="33cca-128">You can use the **Right** and **Down** arguments for forms with pages larger than the Access window.</span></span> <span data-ttu-id="33cca-129">Use el argumento **Número de página** para moverse a la página deseada y, a continuación, use los argumentos **Derecha** y **Abajo** para mostrar la parte de la página que desee ver.</span><span class="sxs-lookup"><span data-stu-id="33cca-129">Use the **Page Number** argument to move to the desired page, and then use the **Right** and **Down** arguments to display the part of the page you want to see.</span></span> <span data-ttu-id="33cca-130">Access muestra la parte de la página cuya esquina superior izquierda está a la distancia especificada de la esquina superior izquierda de la página.</span><span class="sxs-lookup"><span data-stu-id="33cca-130">Access displays the part of the page whose upper-left corner is offset the specified distance from the upper-left corner of the page.</span></span>

<span data-ttu-id="33cca-131">La acción **IrAPágina** no se puede usar en los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="33cca-131">You can't use the **GoToPage** action in the following cases:</span></span>

  - <span data-ttu-id="33cca-132">Para mover el enfoque a una página de un formulario oculto.</span><span class="sxs-lookup"><span data-stu-id="33cca-132">To move the focus to a page on a hidden form.</span></span>

  - <span data-ttu-id="33cca-133">Para mover el enfoque de una página a otra dentro del control de pestaña.</span><span class="sxs-lookup"><span data-stu-id="33cca-133">To move the focus from one page to another within the tab control.</span></span>

<span data-ttu-id="33cca-134">Para ejecutar la acción **IrAPágina** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **GoToPage** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="33cca-134">To run the **GoToPage** action in a Visual Basic for Applications (VBA) module, use the **GoToPage** method of the **DoCmd** object.</span></span>

