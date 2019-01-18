---
title: CambiarNombreDeObjeto (acción de macro)
TOCTitle: RenameObject macro action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ce16b86ea06e041d490d0c68917daf18bd80dbb6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698389"
---
# <a name="renameobject-macro-action"></a><span data-ttu-id="7bbcd-102">CambiarNombreDeObjeto (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="7bbcd-102">RenameObject macro action</span></span>

<span data-ttu-id="7bbcd-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7bbcd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7bbcd-104">Puede usar la acción **CambiarNombreDeObjeto** para cambiar el nombre de un objeto de base de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-104">You can use the **RenameObject** action to rename a specified database object.</span></span>

> [!NOTE]
> <span data-ttu-id="7bbcd-105">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-105">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="7bbcd-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="7bbcd-106">Setting</span></span>

<span data-ttu-id="7bbcd-107">La acción **CambiarNombreDeObjeto** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-107">The **RenameObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7bbcd-108">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="7bbcd-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="7bbcd-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bbcd-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bbcd-110"><strong>Nombre nuevo</strong></span><span class="sxs-lookup"><span data-stu-id="7bbcd-110"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="7bbcd-p101">Nombre nuevo del objeto de la base de datos. Escriba el nombre del objeto en el cuadro <strong>Nombre nuevo</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Éste es un argumento requerido.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-p101">A new name for the database object. Enter the object name in the <strong>New Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bbcd-114"><strong>Tipo de objeto</strong></span><span class="sxs-lookup"><span data-stu-id="7bbcd-114"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="7bbcd-p102">Tipo del objeto cuyo nombre se desea cambiar. Haga clic en <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Informe</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong>. Para cambiar el nombre del objeto seleccionado en el panel de navegación, deje este argumento en blanco.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-p102">The type of object you want to rename. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>. To rename the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bbcd-118"><strong>Nombre anterior</strong></span><span class="sxs-lookup"><span data-stu-id="7bbcd-118"><strong>Old Name</strong></span></span></p></td>
<td><p><span data-ttu-id="7bbcd-p103">Nombre del objeto cuyo nombre se va a cambiar. En el cuadro <strong>Nombre anterior</strong> se muestran todos los objetos de la base de datos del tipo seleccionado mediante el argumento <strong>Tipo de objeto</strong>. Si deja en blanco el argumento <strong>Tipo de objeto</strong>, deje también en blanco este argumento. 

</span><span class="sxs-lookup"><span data-stu-id="7bbcd-p103">The name of the object to be renamed. The <strong>Old Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p><p><span data-ttu-id="7bbcd-122"><strong>Nota</strong>: si ejecuta una macro que contiene la acción <STRONG>CambiarNombre</STRONG> en una base de datos de biblioteca, Microsoft Access busca primero el objeto con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-122"><strong>NOTE</strong>: If you run a macro containing the <STRONG>Rename</STRONG> action in a library database, Microsoft Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7bbcd-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7bbcd-123">Remarks</span></span>

<span data-ttu-id="7bbcd-124">El nuevo nombre del objeto de base de datos debe cumplir las convenciones de nomenclatura estándar para los objetos de Access.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-124">The new name of the database object must follow the standard naming conventions for Access objects.</span></span>

<span data-ttu-id="7bbcd-125">No se puede cambiar el nombre de un objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-125">You can't rename an open object.</span></span>

<span data-ttu-id="7bbcd-p104">Si se dejan en blanco los argumentos **Tipo de objeto** y **Nombre anterior**, Access cambia el nombre del objeto seleccionado en el panel de navegación. Para seleccionar un objeto en el panel de navegación, se puede utilizar la acción **SeleccionarObjeto** con el valor del argumento\*\* En panel de navegación\*\* establecido en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-p104">If you leave the **Object Type** and **Old Name** arguments blank, Access renames the object selected in the Navigation Pane. To select an object in the Navigation Pane, you can use the **SelectObject** action with the **In Navigation Pane** argument set to **Yes**.</span></span>

<span data-ttu-id="7bbcd-p105">Para cambiar el nombre de un objeto, también se puede hacer clic con el botón secundario en dicho botón en el panel de navegación, hacer clic en **Cambiar nombre** y escribir un nombre nuevo. Con la acción **CambiarNombreDeObjeto**, no es preciso seleccionar primero el objeto en el panel de navegación y tampoco hay que detener la macro para escribir el nuevo nombre.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-p105">You can also rename an object by right-clicking it in the Navigation Pane, clicking **Rename**, and entering a new name. With the **RenameObject** action, you don't have to select the object first in the Navigation Pane, and you don't have to stop the macro to enter the new name.</span></span>

<span data-ttu-id="7bbcd-130">Esta acción se diferencia de la acción **CopiarObjeto**, con la que se crea una copia del objeto con un nombre nuevo.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-130">This action differs from the **CopyObject** action, which creates a copy of the object under a new name.</span></span>

<span data-ttu-id="7bbcd-131">Para ejecutar la acción **CambiarNombreDeObjeto** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **Rename** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="7bbcd-131">To run the **RenameObject** action in a Visual Basic for Applications (VBA) module, use the **Rename** method of the **DoCmd** object.</span></span>

