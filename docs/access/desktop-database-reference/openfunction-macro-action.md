---
title: AbrirFunción (acción de macro)
TOCTitle: OpenFunction macro action
ms:assetid: 0446dbb9-c342-9225-27ba-b8a6892030e1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844833(v=office.15)
ms:contentKeyID: 48543005
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89179
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b13d21ef1bd8a95587eb78cd448f19f9fd0c24c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288367"
---
# <a name="openfunction-macro-action"></a><span data-ttu-id="65fff-102">AbrirFunción (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="65fff-102">OpenFunction macro action</span></span>

<span data-ttu-id="65fff-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="65fff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="65fff-p101">En un proyecto de Access, puede abrir la acción **AbrirFunción** para abrir una función definida por el usuario en la vista Hoja de datos, vista Diseño de función en línea, vista Editor de texto SQL (para una función escalar o una función de tabla definida por el usuario) o Vista preliminar. Esta acción ejecuta la función definida por el usuario cuando se abre en la vista Hoja de datos. También puede seleccionar el modo de entrada de datos para la función definida por el usuario y restringir los registros que muestra la función definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="65fff-p101">In an Access project, you can use the **OpenFunction** action to open a user-defined function in Datasheet view, inline function Design view, SQL Text Editor view (for a scalar or table user-defined function), or Print Preview. This action runs the user-defined function when opened in Datasheet view. You can also select the data entry mode for the user-defined function and restrict the records that the user-defined function displays.</span></span>

> [!NOTE]
> <span data-ttu-id="65fff-107">Esta acción no se permitirá si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="65fff-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="65fff-108">Configuración</span><span class="sxs-lookup"><span data-stu-id="65fff-108">Setting</span></span>

<span data-ttu-id="65fff-109">La acción **AbrirFunción** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="65fff-109">The **OpenFunction** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65fff-110">Argumento de acción</span><span class="sxs-lookup"><span data-stu-id="65fff-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="65fff-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="65fff-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65fff-112"><strong>Nombre de función</strong></span><span class="sxs-lookup"><span data-stu-id="65fff-112"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="65fff-113">Nombre de la función definida por el usuario que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="65fff-113">The name of the user-defined function to open.</span></span> <span data-ttu-id="65fff-114">El cuadro <strong>Nombre de función</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todas las funciones definidas por el usuario de la base de datos activa.</span><span class="sxs-lookup"><span data-stu-id="65fff-114">The <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all user-defined functions in the current database.</span></span> <span data-ttu-id="65fff-115">Este argumento es obligatorio. Si ejecuta una macro <strong></strong> que contiene la acción Función en una base de datos de biblioteca, Microsoft Access busca primero la función con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="65fff-115">This is a required argument.If you run a macro containing the <strong>Function</strong> action in a library database, Microsoft Access first looks for the function with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65fff-116"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="65fff-116"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="65fff-p103">Vista en la que se va a abrir la función definida por el usuario. Haga clic en <strong>Hoja de datos</strong>, <strong>Diseño</strong>, <strong>Vista preliminar</strong>, <strong>Tabla dinámica</strong> o <strong>Gráfico dinámico</strong> en el cuadro <strong>Vista</strong>. El valor predeterminado es <strong>Hoja de datos</strong>.</span><span class="sxs-lookup"><span data-stu-id="65fff-p103">The view in which the user-defined function will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65fff-120"><strong>Modo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="65fff-120"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="65fff-p104">El modo de entrada de datos para la función definida por el usuario. Esto sólo se aplica a las funciones definidas por el usuario que estén abiertas en la vista Hoja de datos. Haga clic en <strong>Agregar</strong> (el usuario puede agregar nuevos registros pero no puede ver ni modificar los existentes), <strong>Modificar</strong> (el usuario puede ver o modificar los registros existentes y agregar otros nuevos) o <strong>Solo lectura</strong> (el usuario sólo puede ver los registros). El valor predeterminado es <strong>Modificar</strong>.</span><span class="sxs-lookup"><span data-stu-id="65fff-p104">The data entry mode for the user-defined function. This applies only to user-defined functions opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="65fff-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="65fff-125">Remarks</span></span>

<span data-ttu-id="65fff-126">Esta acción es similar a hacer doble clic en una función definida por el usuario en el panel de navegación, o bien, a hacer clic con el botón secundario en la función en el panel de navegación y, a continuación, seleccionar una vista.</span><span class="sxs-lookup"><span data-stu-id="65fff-126">This action is similar to double-clicking a user-defined function in the Navigation Pane, or right-clicking the function in the Navigation Pane and selecting a view.</span></span>

<span data-ttu-id="65fff-p105">Si se cambia a la vista Diseño mientras está abierta la función definida por el usuario, se quita el valor del argumento **Modo de datos** de la función definida por el usuario. Este valor no tiene efecto aunque el usuario vuelva a la vista Hoja de datos.</span><span class="sxs-lookup"><span data-stu-id="65fff-p105">Switching to Design view while the user-defined function is open removes the **Data Mode** argument setting for the user-defined function. This setting is not in effect, even if the user returns to Datasheet view.</span></span>

> [!TIP]
> - <span data-ttu-id="65fff-p106">Puede seleccionar una función definida por el usuario en el panel de navegación y arrastrarla hasta una fila de acción de una macro. De este modo, se crea automáticamente la acción **AbrirFunción** que abre la función definida por el usuario en la vista Hoja de datos.</span><span class="sxs-lookup"><span data-stu-id="65fff-p106">You can select a user-defined function in the Navigation Pane and drag it to a macro action row. This automatically creates an **OpenFunction** action that opens the user-defined function in Datasheet view.</span></span>
> - <span data-ttu-id="65fff-131">Si no desea que se muestren los mensajes del sistema que normalmente aparecen cuando se ejecuta una función definida por el usuario (esos mensajes indican que se trata de una función definida por el usuario y muestran cuántos registros se verán afectados), puede utilizar la acción **EstablecerAdvertencias** para suprimir la presentación de estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="65fff-131">If you don't want to display the system messages that normally appear when a user-defined function is run (indicating it is a user-defined function and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="65fff-132">Para ejecutar la acción **AbrirFunción** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **OpenFunction** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="65fff-132">To run the **OpenFunction** action in a Visual Basic for Applications (VBA) module, use the **OpenFunction** method of the **DoCmd** object.</span></span>

