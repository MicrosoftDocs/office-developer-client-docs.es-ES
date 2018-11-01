---
title: AbrirFunción (acción de macro)
TOCTitle: OpenFunction Macro Action
ms:assetid: 0446dbb9-c342-9225-27ba-b8a6892030e1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844833(v=office.15)
ms:contentKeyID: 48543005
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89179
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d7d6c719c535dabbf4fea1267d8ce7cf9ced9326
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882101"
---
# <a name="openfunction-macro-action"></a><span data-ttu-id="0e1f2-102">AbrirFunción (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="0e1f2-102">OpenFunction Macro Action</span></span>


<span data-ttu-id="0e1f2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e1f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e1f2-p101">En un proyecto de Access, puede abrir la acción **AbrirFunción** para abrir una función definida por el usuario en la vista Hoja de datos, vista Diseño de función en línea, vista Editor de texto SQL (para una función escalar o una función de tabla definida por el usuario) o Vista preliminar. Esta acción ejecuta la función definida por el usuario cuando se abre en la vista Hoja de datos. También puede seleccionar el modo de entrada de datos para la función definida por el usuario y restringir los registros que muestra la función definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="0e1f2-p101">In an Access project, you can use the **OpenFunction** action to open a user-defined function in Datasheet view, inline function Design view, SQL Text Editor view (for a scalar or table user-defined function), or Print Preview. This action runs the user-defined function when opened in Datasheet view. You can also select the data entry mode for the user-defined function and restrict the records that the user-defined function displays.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0e1f2-p102">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.</span><span class="sxs-lookup"><span data-stu-id="0e1f2-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="0e1f2-109">Configuración</span><span class="sxs-lookup"><span data-stu-id="0e1f2-109">Setting</span></span>

<span data-ttu-id="0e1f2-110">La acción **AbrirFunción** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="0e1f2-110">The **OpenFunction** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e1f2-111">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="0e1f2-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="0e1f2-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e1f2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e1f2-113"><strong>Nombre de función</strong></span><span class="sxs-lookup"><span data-stu-id="0e1f2-113"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="0e1f2-114">El nombre de la función definida por el usuario para abrir.</span><span class="sxs-lookup"><span data-stu-id="0e1f2-114">The name of the user-defined function to open.</span></span> <span data-ttu-id="0e1f2-115">El cuadro <strong>Nombre de la función</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todas las funciones definidas por el usuario en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="0e1f2-115">The <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all user-defined functions in the current database.</span></span> <span data-ttu-id="0e1f2-116">Este es un argumento requerido. Si ejecuta una macro que contiene la acción <strong>función</strong> en una base de datos de biblioteca, Microsoft Access busca primero la función con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="0e1f2-116">This is a required argument.If you run a macro containing the <strong>Function</strong> action in a library database, Microsoft Access first looks for the function with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e1f2-117"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="0e1f2-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="0e1f2-p104">Vista en la que se va a abrir la función definida por el usuario. Haga clic en <strong>Hoja de datos</strong>, <strong>Diseño</strong>, <strong>Vista preliminar</strong>, <strong>Tabla dinámica</strong> o <strong>Gráfico dinámico</strong> en el cuadro <strong>Vista</strong>. El valor predeterminado es <strong>Hoja de datos</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e1f2-p104">The view in which the user-defined function will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e1f2-121"><strong>Modo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="0e1f2-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="0e1f2-p105">El modo de entrada de datos para la función definida por el usuario. Esto sólo se aplica a las funciones definidas por el usuario que estén abiertas en la vista Hoja de datos. Haga clic en <strong>Agregar</strong> (el usuario puede agregar nuevos registros pero no puede ver ni modificar los existentes), <strong>Modificar</strong> (el usuario puede ver o modificar los registros existentes y agregar otros nuevos) o <strong>Solo lectura</strong> (el usuario sólo puede ver los registros). El valor predeterminado es <strong>Modificar</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e1f2-p105">The data entry mode for the user-defined function. This applies only to user-defined functions opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0e1f2-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e1f2-126">Remarks</span></span>

<span data-ttu-id="0e1f2-127">Esta acción es similar a hacer doble clic en una función definida por el usuario en el panel de navegación, o bien, a hacer clic con el botón secundario en la función en el panel de navegación y, a continuación, seleccionar una vista.</span><span class="sxs-lookup"><span data-stu-id="0e1f2-127">This action is similar to double-clicking a user-defined function in the Navigation Pane, or right-clicking the function in the Navigation Pane and selecting a view.</span></span>

<span data-ttu-id="0e1f2-p106">Si se cambia a la vista Diseño mientras está abierta la función definida por el usuario, se quita el valor del argumento **Modo de datos** de la función definida por el usuario. Este valor no tiene efecto aunque el usuario vuelva a la vista Hoja de datos.</span><span class="sxs-lookup"><span data-stu-id="0e1f2-p106">Switching to Design view while the user-defined function is open removes the **Data Mode** argument setting for the user-defined function. This setting is not in effect, even if the user returns to Datasheet view.</span></span>

<span data-ttu-id="0e1f2-130">**Sugerencias**</span><span class="sxs-lookup"><span data-stu-id="0e1f2-130">**Tips**</span></span>

  - <span data-ttu-id="0e1f2-p107">Puede seleccionar una función definida por el usuario en el panel de navegación y arrastrarla hasta una fila de acción de una macro. De este modo, se crea automáticamente la acción **AbrirFunción** que abre la función definida por el usuario en la vista Hoja de datos.</span><span class="sxs-lookup"><span data-stu-id="0e1f2-p107">You can select a user-defined function in the Navigation Pane and drag it to a macro action row. This automatically creates an **OpenFunction** action that opens the user-defined function in Datasheet view.</span></span>

  - <span data-ttu-id="0e1f2-133">Si no desea que se muestren los mensajes del sistema que normalmente aparecen cuando se ejecuta una función definida por el usuario (esos mensajes indican que se trata de una función definida por el usuario y muestran cuántos registros se verán afectados), puede utilizar la acción **EstablecerAdvertencias** para suprimir la presentación de estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="0e1f2-133">If you don't want to display the system messages that normally appear when a user-defined function is run (indicating it is a user-defined function and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="0e1f2-134">Para ejecutar la acción **AbrirFunción** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **OpenFunction** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="0e1f2-134">To run the **OpenFunction** action in a Visual Basic for Applications (VBA) module, use the **OpenFunction** method of the **DoCmd** object.</span></span>

