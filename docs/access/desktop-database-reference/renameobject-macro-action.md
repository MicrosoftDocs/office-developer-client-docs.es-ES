---
title: CambiarNombreDeObjeto (acción de macro)
TOCTitle: RenameObject Macro Action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6522e85aa0407800ea0aade039a65c79a25c1419
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484386"
---
# <a name="renameobject-macro-action"></a><span data-ttu-id="4d92a-102">CambiarNombreDeObjeto (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="4d92a-102">RenameObject Macro Action</span></span>


<span data-ttu-id="4d92a-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d92a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4d92a-104">Puede usar la acción **CambiarNombreDeObjeto** para cambiar el nombre de un objeto de base de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="4d92a-104">You can use the **RenameObject** action to rename a specified database object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4d92a-p101">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.</span><span class="sxs-lookup"><span data-stu-id="4d92a-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="4d92a-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="4d92a-107">Setting</span></span>

<span data-ttu-id="4d92a-108">La acción **CambiarNombreDeObjeto** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="4d92a-108">The **RenameObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4d92a-109">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="4d92a-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4d92a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d92a-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d92a-111"><strong>Nombre nuevo</strong></span><span class="sxs-lookup"><span data-stu-id="4d92a-111"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="4d92a-p102">Nombre nuevo del objeto de la base de datos. Escriba el nombre del objeto en el cuadro <strong>Nombre nuevo</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Éste es un argumento requerido.</span><span class="sxs-lookup"><span data-stu-id="4d92a-p102">A new name for the database object. Enter the object name in the <strong>New Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d92a-115"><strong>Tipo de objeto</strong></span><span class="sxs-lookup"><span data-stu-id="4d92a-115"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="4d92a-p103">Tipo del objeto cuyo nombre se desea cambiar. Haga clic en <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Informe</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong>. Para cambiar el nombre del objeto seleccionado en el panel de navegación, deje este argumento en blanco.</span><span class="sxs-lookup"><span data-stu-id="4d92a-p103">The type of object you want to rename. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>. To rename the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d92a-119"><strong>Nombre anterior</strong></span><span class="sxs-lookup"><span data-stu-id="4d92a-119"><strong>Old Name</strong></span></span></p></td>
<td><p><span data-ttu-id="4d92a-p104">Nombre del objeto cuyo nombre se va a cambiar. En el cuadro <strong>Nombre anterior</strong> se muestran todos los objetos de la base de datos del tipo seleccionado mediante el argumento <strong>Tipo de objeto</strong>. Si deja en blanco el argumento <strong>Tipo de objeto</strong>, deje también en blanco este argumento. 

</span><span class="sxs-lookup"><span data-stu-id="4d92a-p104">The name of the object to be renamed. The <strong>Old Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="4d92a-123">Si ejecuta una macro que contiene la acción <STRONG>CambiarNombre</STRONG> en una base de datos de biblioteca, Microsoft Access primero busca el objeto con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos activa.</span><span class="sxs-lookup"><span data-stu-id="4d92a-123">If you run a macro containing the <STRONG>Rename</STRONG> action in a library database, Microsoft Access first looks for the object with this name in the library database, and then in the current database.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4d92a-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d92a-124">Remarks</span></span>

<span data-ttu-id="4d92a-125">El nuevo nombre del objeto de base de datos debe cumplir las convenciones de nomenclatura estándar para los objetos de Access.</span><span class="sxs-lookup"><span data-stu-id="4d92a-125">The new name of the database object must follow the standard naming conventions for Access objects.</span></span>

<span data-ttu-id="4d92a-126">No se puede cambiar el nombre de un objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="4d92a-126">You can't rename an open object.</span></span>

<span data-ttu-id="4d92a-p105">Si se dejan en blanco los argumentos **Tipo de objeto** y **Nombre anterior**, Access cambia el nombre del objeto seleccionado en el panel de navegación. Para seleccionar un objeto en el panel de navegación, se puede utilizar la acción **SeleccionarObjeto** con el valor del argumento\*\* En panel de navegación\*\* establecido en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="4d92a-p105">If you leave the **Object Type** and **Old Name** arguments blank, Access renames the object selected in the Navigation Pane. To select an object in the Navigation Pane, you can use the **SelectObject** action with the **In Navigation Pane** argument set to **Yes**.</span></span>

<span data-ttu-id="4d92a-p106">Para cambiar el nombre de un objeto, también se puede hacer clic con el botón secundario en dicho botón en el panel de navegación, hacer clic en **Cambiar nombre** y escribir un nombre nuevo. Con la acción **CambiarNombreDeObjeto**, no es preciso seleccionar primero el objeto en el panel de navegación y tampoco hay que detener la macro para escribir el nuevo nombre.</span><span class="sxs-lookup"><span data-stu-id="4d92a-p106">You can also rename an object by right-clicking it in the Navigation Pane, clicking **Rename**, and entering a new name. With the **RenameObject** action, you don't have to select the object first in the Navigation Pane, and you don't have to stop the macro to enter the new name.</span></span>

<span data-ttu-id="4d92a-131">Esta acción se diferencia de la acción **CopiarObjeto**, con la que se crea una copia del objeto con un nombre nuevo.</span><span class="sxs-lookup"><span data-stu-id="4d92a-131">This action differs from the **CopyObject** action, which creates a copy of the object under a new name.</span></span>

<span data-ttu-id="4d92a-132">Para ejecutar la acción **CambiarNombreDeObjeto** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **Rename** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="4d92a-132">To run the **RenameObject** action in a Visual Basic for Applications (VBA) module, use the **Rename** method of the **DoCmd** object.</span></span>
