---
title: AbrirVista (acción de macro)
TOCTitle: OpenView Macro Action
ms:assetid: 4d3b7e6d-4b81-4fbe-7222-24d745350321
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193569(v=office.15)
ms:contentKeyID: 48544726
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50135
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ad607f852f5af21bc2979bd635286b86d18489a5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484589"
---
# <a name="openview-macro-action"></a><span data-ttu-id="4ecac-102">AbrirVista (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="4ecac-102">OpenView Macro Action</span></span>


<span data-ttu-id="4ecac-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ecac-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4ecac-p101">En un proyecto de Access, puede utilizar la acción **AbrirVista** para abrir una vista en la vista Hoja de datos, vista Diseño o Vista preliminar. Esta acción ejecuta la vista especificada cuando se abre en la vista Hoja de datos. Puede seleccionar un modo de entrada de datos para la vista y restringir los registros que muestra la vista.</span><span class="sxs-lookup"><span data-stu-id="4ecac-p101">In an Access project, you can use the **OpenView** action to open a view in Datasheet view, Design view, or Print Preview. This action runs the named view when opened in Datasheet view. You can select data entry for the view and restrict the records that the view displays.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4ecac-p102">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.</span><span class="sxs-lookup"><span data-stu-id="4ecac-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="4ecac-109">Configuración</span><span class="sxs-lookup"><span data-stu-id="4ecac-109">Setting</span></span>

<span data-ttu-id="4ecac-110">La acción **AbrirVista** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="4ecac-110">The **OpenView** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ecac-111">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="4ecac-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4ecac-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ecac-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ecac-113"><strong>Nombre de vista</strong></span><span class="sxs-lookup"><span data-stu-id="4ecac-113"><strong>View Name</strong></span></span></p></td>
<td><p><span data-ttu-id="4ecac-114">El nombre de la vista que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="4ecac-114">The name of the view to open.</span></span> <span data-ttu-id="4ecac-115">El cuadro <strong>Nombre de la vista</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todas las vistas en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="4ecac-115">The <strong>View Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all views in the current database.</span></span> <span data-ttu-id="4ecac-116">Este argumento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4ecac-116">This is a required argument.</span></span> <span data-ttu-id="4ecac-117">Si ejecuta una macro que contiene la acción <strong>AbrirVista</strong> en una base de datos de biblioteca, Microsoft Access primero busca la vista con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos activa.</span><span class="sxs-lookup"><span data-stu-id="4ecac-117">If you run a macro containing the <strong>OpenView</strong> action in a library database, Microsoft Access first looks for the view with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ecac-118"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="4ecac-118"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="4ecac-p104">Vista en la que se abrirá la vista. Haga clic en <strong>Hoja de datos</strong>, <strong>Diseño</strong>, <strong>Vista preliminar</strong>, <strong>Tabla dinámica</strong> o <strong>Gráfico dinámico</strong> en el cuadro <strong>Vista</strong>. El valor predeterminado es <strong>Hoja de datos</strong>.</span><span class="sxs-lookup"><span data-stu-id="4ecac-p104">The view in which the view will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ecac-122"><strong>Modo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="4ecac-122"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="4ecac-p105">Modo de entrada de datos para la vista. Sólo se aplica a las vistas abiertas en la vista Hoja de datos. Haga clic en <strong>Agregar</strong> (el usuario puede agregar registros nuevos, pero no puede ver ni modificar los existentes), <strong>Modificar</strong> (el usuario puede ver o modificar los registros existentes y agregar registros nuevos) o <strong>Solo lectura</strong> (el usuario sólo puede ver los registros). El valor predeterminado es <strong>Modificar</strong>.</span><span class="sxs-lookup"><span data-stu-id="4ecac-p105">The data entry mode for the view. This applies only to views opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4ecac-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ecac-127">Remarks</span></span>

<span data-ttu-id="4ecac-128">Esta acción es similar a hacer doble clic en una vista en el panel de navegación, o bien, a hacer clic con el botón secundario en la vista en el panel de navegación y, a continuación, hacer clic en el comando deseado.</span><span class="sxs-lookup"><span data-stu-id="4ecac-128">This action is similar to double-clicking a view in the Navigation Pane, or right-clicking the view in the Navigation Pane and then clicking the command you want.</span></span>

<span data-ttu-id="4ecac-129">**Sugerencias**</span><span class="sxs-lookup"><span data-stu-id="4ecac-129">**Tips**</span></span>

  - <span data-ttu-id="4ecac-p106">Puede arrastrar una vista desde el panel de navegación hasta una fila de acción de una macro. De este modo, se crea automáticamente una acción **AbrirVista** que abre la vista en la vista Hoja de datos.</span><span class="sxs-lookup"><span data-stu-id="4ecac-p106">You can drag a view from the Navigation Pane to a macro action row. This automatically creates an **OpenView** action that opens the view in Datasheet view.</span></span>

  - <span data-ttu-id="4ecac-132">Si no desea que se muestren los mensajes del sistema que normalmente aparecen cuando se ejecuta una vista (esos mensajes indican que se trata de una vista y muestran cuántos registros se verán afectados), puede utilizar la acción **EstablecerAdvertencias** para suprimir la presentación de estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="4ecac-132">If you don't want to display the system messages that normally appear when a view is run (indicating it is a view and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="4ecac-133">Para ejecutar la acción **AbrirVista** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **OpenView** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="4ecac-133">To run the **OpenView** action in a Visual Basic for Applications (VBA) module, use the **OpenView** method of the **DoCmd** object.</span></span>

