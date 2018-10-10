---
title: SeleccionarObjeto (acción de macro)
TOCTitle: SelectObject Macro Action
ms:assetid: a90539a0-c5a0-e997-9c25-e0972d28f2a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821420(v=office.15)
ms:contentKeyID: 48546914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm41840
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c0e1c538f873143d3d6c7b97eda34d068761852a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483346"
---
# <a name="selectobject-macro-action"></a><span data-ttu-id="d0bf6-102">SeleccionarObjeto (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="d0bf6-102">SelectObject Macro Action</span></span>


<span data-ttu-id="d0bf6-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0bf6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d0bf6-104">Puede usar la acción **SeleccionarObjeto** para seleccionar un determinado objeto de base de datos.</span><span class="sxs-lookup"><span data-stu-id="d0bf6-104">You can use the **SelectObject** action to select a specified database object.</span></span>

## <a name="setting"></a><span data-ttu-id="d0bf6-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="d0bf6-105">Setting</span></span>

<span data-ttu-id="d0bf6-106">La acción **SeleccionarObjeto** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="d0bf6-106">The **SelectObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0bf6-107">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="d0bf6-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d0bf6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0bf6-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0bf6-109"><strong>Tipo de objeto</strong></span><span class="sxs-lookup"><span data-stu-id="d0bf6-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="d0bf6-p101">El tipo de objeto de base de datos que se desea seleccionar. Haga clic en <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Informe</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Páginas de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Este argumento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d0bf6-p101">The type of database object to select. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0bf6-113"><strong>Nombre del objeto</strong></span><span class="sxs-lookup"><span data-stu-id="d0bf6-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d0bf6-p102">Nombre del objeto que se va a seleccionar. El cuadro <strong>Nombre del objeto</strong> muestra todos los objetos del tipo seleccionado mediante el argumento <strong>Tipo de objeto</strong> que existen en la base de datos. Este argumento es obligatorio, a menos que el argumento En panel de navegación se haya establecido en <strong>Sí</strong>.</span><span class="sxs-lookup"><span data-stu-id="d0bf6-p102">The name of the object to select. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. This is a required argument, unless you set the In Navigation Pane argument to <strong>Yes</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="d0bf6-117">Los nombres de los objetos <STRONG>Vista de servidor</STRONG>, <STRONG>Diagrama</STRONG> o <STRONG>Procedimiento almacenado</STRONG> no se muestran en el cuadro <STRONG>Nombre del objeto</STRONG> de un proyecto de Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="d0bf6-117">The object names for <STRONG>Server View</STRONG>, <STRONG>Diagram</STRONG>, or <STRONG>Stored Procedure</STRONG> objects are not displayed in the <STRONG>Object Name</STRONG> box of an Access project (.adp).</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0bf6-118"><strong>En panel de navegación</strong></span><span class="sxs-lookup"><span data-stu-id="d0bf6-118"><strong>In Navigation Pane</strong></span></span></p></td>
<td><p><span data-ttu-id="d0bf6-p103">Especifica si Microsoft Access selecciona el objeto en el Panel de navegación. Haga clic en <strong>Sí</strong> (para seleccionar el objeto en el Panel de navegación) o <strong>No</strong> (para no seleccionar el objeto en el Panel de navegación). El valor predeterminado es <strong>No</strong>.</span><span class="sxs-lookup"><span data-stu-id="d0bf6-p103">Specifies whether Microsoft Access selects the object in the Navigation Pane. Click <strong>Yes</strong> (to select the object in the Navigation Pane) or <strong>No</strong> (not to select the object in the Navigation Pane). The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d0bf6-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d0bf6-122">Remarks</span></span>

<span data-ttu-id="d0bf6-p104">La acción **SeleccionarObjeto** funciona con cualquier objeto de Access capaz de recibir el enfoque. Esta acción aplica el enfoque al objeto especificado y lo muestra si está oculto. Si el objeto es un formulario, la acción **SeleccionarObjeto** establece la propiedad **Visible** del formulario en **Sí** y devuelve el formulario al modo establecido por las propiedades del formulario (por ejemplo, como formulario modal o formulario emergente).</span><span class="sxs-lookup"><span data-stu-id="d0bf6-p104">The **SelectObject** action works with any Access object that can receive the focus. This action gives the specified object the focus and shows the object if it's hidden. If the object is a form, the **SelectObject** action sets the form's **Visible** property to **Yes** and returns the form to the mode set by its form properties (for example, as a modal or pop-up form).</span></span>

<span data-ttu-id="d0bf6-p105">Si el objeto no está abierto en ninguna de las otras ventanas de Access, se puede seleccionar en el panel de navegación estableciendo previamente el argumento **En panel de navegación** en **Sí**. Si establece el argumento **En panel de navegación** en **No**, aparecerá un mensaje de error cuando intente seleccionar un objeto que no esté abierto.</span><span class="sxs-lookup"><span data-stu-id="d0bf6-p105">If the object isn't open in one of the other Access windows, you can select it in the Navigation Pane by setting the **In Navigation Pane** argument to **Yes**. If you set the **In Navigation Pane** argument to **No**, an error message appears when you try to select an object that isn't open.</span></span>

<span data-ttu-id="d0bf6-p106">Puede usar esta acción para seleccionar un objeto sobre el que desee ejecutar acciones adicionales. Por ejemplo, si Access está configurado de modo que use ventanas que se superponen en lugar de documentos con fichas, es posible restaurar un objeto minimizado (mediante la acción **RestaurarVentana** ) o maximizar una ventana que contiene un objeto con el que se desea trabajar (mediante la acción **MaximizarVentana** ).</span><span class="sxs-lookup"><span data-stu-id="d0bf6-p106">Often, you might use this action to select an object on which you want to perform additional actions. For example, if you have Access configured to use overlapping windows instead of tabbed documents, you may want to restore an object that has been minimized (by using the **RestoreWindow** action) or maximize a window that contains an object you want to work with (by using the **MaximizeWindow** action).</span></span>

<span data-ttu-id="d0bf6-p107">Si selecciona un formulario, puede utilizar las acciones **IrAControl**, **IrARegistro** e **IrAPágina** para desplazarse a determinadas áreas del formulario. La acción **IrARegistro** también funciona para hojas de datos.</span><span class="sxs-lookup"><span data-stu-id="d0bf6-p107">If you select a form, you can use the **GoToControl**, **GoToRecord**, and **GoToPage** actions to move to specific areas on the form. The **GoToRecord** action also works for datasheets.</span></span>

<span data-ttu-id="d0bf6-132">Para ejecutar la acción **SeleccionarObjeto** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **SelectObject** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="d0bf6-132">To run the **SelectObject** action in a Visual Basic for Applications (VBA) module, use the **SelectObject** method of the **DoCmd** object.</span></span>

