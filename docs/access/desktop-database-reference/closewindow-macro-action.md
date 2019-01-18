---
title: CerrarVentana (acción de macro)
TOCTitle: CloseWindow macro action
ms:assetid: ba96bc26-7f3f-fd3d-8d3a-e18bfe90cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822510(v=office.15)
ms:contentKeyID: 48547377
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm64319
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4397846abdc0d10b6bfa0e6a1eb5c0c435fc862a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709855"
---
# <a name="closewindow-macro-action"></a><span data-ttu-id="5da1e-102">CerrarVentana (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="5da1e-102">CloseWindow macro action</span></span>


<span data-ttu-id="5da1e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5da1e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5da1e-104">Puede usar la acción **Cerrarventana** para cerrar una ficha de documento de acceso especificada o en la ficha del documento activo si no se especifica ninguno.</span><span class="sxs-lookup"><span data-stu-id="5da1e-104">You can use the **CloseWindow** action to close either a specified Access document tab or the active document tab if none is specified.</span></span>

## <a name="setting"></a><span data-ttu-id="5da1e-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="5da1e-105">Setting</span></span>

<span data-ttu-id="5da1e-106">La acción **CerrarVentana** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="5da1e-106">The **CloseWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5da1e-107">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="5da1e-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5da1e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5da1e-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5da1e-109"><strong>Tipo de objeto</strong></span><span class="sxs-lookup"><span data-stu-id="5da1e-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="5da1e-p101">Tipo de objeto cuya ficha de documentos se desea cerrar. Haga clic en <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Informe</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong>, en la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Para seleccionar la ficha de documentos activa, deje este argumento en blanco. 

</span><span class="sxs-lookup"><span data-stu-id="5da1e-p101">The type of object whose document tab you want to close. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To select the active document tab, leave this argument blank.</span></span></p>

> [!NOTE]
> <span data-ttu-id="5da1e-113">Si desea cerrar un módulo en el Editor de Visual Basic, debe usar **Módulo** en el argumento **Tipo de objeto**.</span><span class="sxs-lookup"><span data-stu-id="5da1e-113">If you are closing a module in the Visual Basic Editor, you must use **Module** in the **Object Type** argument.</span></span>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5da1e-114"><strong>Nombre del objeto</strong></span><span class="sxs-lookup"><span data-stu-id="5da1e-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5da1e-p102">Nombre del objeto que se va a cerrar. El cuadro <strong>Nombre del objeto</strong> muestra todos los objetos de la base de datos que tienen el tipo seleccionado en el argumento <strong>Tipo de objeto</strong>. Haga clic en el objeto que desea cerrar. Si deja en blanco el argumento <strong>Tipo de objeto</strong>, también deberá dejar en blanco este argumento.</span><span class="sxs-lookup"><span data-stu-id="5da1e-p102">The name of the object to be closed. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. Click the object to close. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5da1e-119"><strong>Save</strong></span><span class="sxs-lookup"><span data-stu-id="5da1e-119"><strong>Save</strong></span></span></p></td>
<td><p><span data-ttu-id="5da1e-p103">Indica si deben guardarse los cambios realizados en el objeto cuando se cierre. Haga clic en <strong>Sí</strong> (guardar el objeto), <strong>No</strong> (cerrar el objeto sin guardarlo) o <strong>Preguntar</strong> (preguntar al usuario si desea guardar o no el objeto). El valor predeterminado es <strong>Preguntar</strong>.</span><span class="sxs-lookup"><span data-stu-id="5da1e-p103">Whether to save changes to the object when it is closed. Click <strong>Yes</strong> (save the object), <strong>No</strong> (close the object without saving it), or <strong>Prompt</strong> (prompt the user whether or not to save the object). The default is <strong>Prompt</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5da1e-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5da1e-123">Remarks</span></span>

<span data-ttu-id="5da1e-p104">La acción **CerrarVentana** funciona en todos los objetos de base de datos que el usuario puede abrir o cerrar explícitamente. Esta acción tiene el mismo efecto que seleccionar un objeto y después cerrarlo haciendo clic con el botón secundario en la ficha de documentos del objeto y, a continuación, haciendo clic en **Cerrar** en el menú contextual, o hacer clic en el botón **Cerrar** del objeto.</span><span class="sxs-lookup"><span data-stu-id="5da1e-p104">The **CloseWindow** action works on all database objects that the user can explicitly open or close. This action has the same effect as selecting an object and then closing it by right-clicking the object's document tab and then clicking **Close** on the shortcut menu, or clicking the **Close** button for the object.</span></span>

<span data-ttu-id="5da1e-p105">Si el argumento **Guardar** se establece en **Preguntar** y el objeto todavía no se ha guardado antes de ejecutarse la acción **CerrarVentana**, un cuadro de diálogo pedirá al usuario que guarde el objeto antes de que la macro lo cierre. Si se ha establecido el argumento **Activar advertencias** de la acción **EstablecerAdvertencias** en **No**, el cuadro de diálogo no aparece y el objeto se guarda automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5da1e-p105">If the **Save** argument is set to **Prompt** and the object hasn't already been saved before the **CloseWindow** action is carried out, a dialog box prompts the user to save the object before the macro closes it. If you have set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box is not displayed and the object is automatically saved.</span></span>

<span data-ttu-id="5da1e-128">Para ejecutar la acción **CerrarVentana** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **CerrarVentana** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="5da1e-128">To run the **CloseWindow** action in a Visual Basic for Applications (VBA) module, use the **CloseWindow** method of the **DoCmd** object.</span></span>

