---
title: MostrarBarraDeHerramientas (acción de macro)
TOCTitle: ShowToolbar macro action
ms:assetid: 9e53009b-1e5e-1bee-3bcc-f82dc1b0dc48
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198288(v=office.15)
ms:contentKeyID: 48546649
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm27417
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 01ba59ce0898068788adb9269b3203794d1f31d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306478"
---
# <a name="showtoolbar-macro-action"></a><span data-ttu-id="13ff5-102">MostrarBarraDeHerramientas (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="13ff5-102">ShowToolbar macro action</span></span>

<span data-ttu-id="13ff5-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="13ff5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="13ff5-104">La acción **MostrarBarraDeHerramientas** se utiliza para mostrar u ocultar un grupo de comandos en la ficha **Complementos**.</span><span class="sxs-lookup"><span data-stu-id="13ff5-104">You can use the **ShowToolbar** action to display or hide a group of commands on the **Add-Ins** tab.</span></span>

> [!NOTE]
> - <span data-ttu-id="13ff5-105">[!NOTA] La acción **MostrarBarraDeHerramientas** no afecta a los menús contextuales.</span><span class="sxs-lookup"><span data-stu-id="13ff5-105">The **ShowToolbar** action does not affect shortcut menus.</span></span>
> - <span data-ttu-id="13ff5-106">Esta acción no se permitirá si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="13ff5-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="13ff5-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="13ff5-107">Setting</span></span>

<span data-ttu-id="13ff5-108">La acción **MostrarBarraDeHerramientas** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="13ff5-108">The **ShowToolbar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13ff5-109">Argumento de acción</span><span class="sxs-lookup"><span data-stu-id="13ff5-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="13ff5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="13ff5-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13ff5-111"><strong>Nombre de barra de herramientas</strong></span><span class="sxs-lookup"><span data-stu-id="13ff5-111"><strong>Toolbar Name</strong></span></span></p></td>
<td><p><span data-ttu-id="13ff5-112">Nombre del grupo de comandos de la ficha <strong>Complementos</strong> que se desea mostrar u ocultar.</span><span class="sxs-lookup"><span data-stu-id="13ff5-112">The name of the command group on the <strong>Add-Ins</strong> tab you want to display or hide.</span></span> <span data-ttu-id="13ff5-113">El cuadro <strong>Nombre de barra de herramientas</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todos los grupos disponibles a los que afecta esta acción.</span><span class="sxs-lookup"><span data-stu-id="13ff5-113">The <strong>Toolbar Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane shows all the available groups that can be affected by this action.</span></span> <span data-ttu-id="13ff5-114">Este argumento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="13ff5-114">This is a required argument.</span></span> <span data-ttu-id="13ff5-115">Si se ejecuta una macro que contiene la acción <strong>MostrarBarraDeHerramientas</strong> en una base de datos de biblioteca, Access busca el grupo con ese nombre primero en la base de datos de biblioteca y, después, en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="13ff5-115">If you run a macro containing the <strong>ShowToolbar</strong> action in a library database, Access first looks for the group with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13ff5-116"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="13ff5-116"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="13ff5-117">Especifica si se debe mostrar u ocultar el grupo de comandos y en qué vistas hacerlo.</span><span class="sxs-lookup"><span data-stu-id="13ff5-117">Specifies whether to display or hide the group and in which views to display or hide it.</span></span> <span data-ttu-id="13ff5-118">El valor predeterminado es <strong>Sí</strong> (mostrar el grupo en todo momento).</span><span class="sxs-lookup"><span data-stu-id="13ff5-118">The default is <strong>Yes</strong> (show the group at all times).</span></span> <span data-ttu-id="13ff5-119">Puede seleccionar <strong>Sí para</strong> mostrar el grupo en todo momento, Cuando corresponda para mostrar el grupo solo cuando el formulario o informe adecuado esté activo, o <strong>No</strong> para ocultar el grupo en todo momento. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="13ff5-119">You can select <strong>Yes</strong> to display the group at all times, <strong>Where Appropriate</strong> to display the group only when the appropriate form or report is active, or <strong>No</strong> to hide the group at all times.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="13ff5-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13ff5-120">Remarks</span></span>

<span data-ttu-id="13ff5-121">Esta acción se puede utilizar en una macro con expresiones condicionales para mostrar u ocultar un grupo si se dan ciertas condiciones.</span><span class="sxs-lookup"><span data-stu-id="13ff5-121">You can use this action in a macro with conditional expressions to display or hide a group depending on certain conditions.</span></span>

<span data-ttu-id="13ff5-p103">Si desea mostrar un grupo determinado en un solo formulario o informe, asigne a la propiedad **AlActivar** del formulario o informe el nombre de una macro que contenga una acción **MostrarBarraDeHerramientas** que muestre el grupo. Luego, asigne a la propiedad **AlDesactivar** del formulario o informe el nombre de una macro que contenga una acción **MostrarBarraDeHerramientas** que oculte el grupo.</span><span class="sxs-lookup"><span data-stu-id="13ff5-p103">If you want to show a particular group on just one form or report, you can set the **OnActivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to show the group. Then set the **OnDeactivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to hide the group.</span></span>

<span data-ttu-id="13ff5-124">Las barras de herramientas integradas no se pueden mostrar u ocultar mediante esta acción si se asigna a la propiedad **AllowBuiltInToolbars** el valor **Falso** (0) en un módulo de Visual Basic para Aplicaciones (VBA) o si se establece la propiedad **Permitir el uso de las barras de herramientas integradas** en **Falso** en VBA mediante el método **SetOption**.</span><span class="sxs-lookup"><span data-stu-id="13ff5-124">The built-in toolbars are not available to display or hide by using this action if you set the **AllowBuiltInToolbars** property to **False** (0) in a Visual Basic for Applications (VBA) module, or if you set the **Allow Built-in Toolbars** option to **False** in VBA by using the **SetOption** method.</span></span>

<span data-ttu-id="13ff5-125">Para ejecutar la acción **MostrarBarraDeHerramientas** en un módulo de VBA, use el método **ShowToolbar** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="13ff5-125">To run the **ShowToolbar** action in a VBA module, use the **ShowToolbar** method of the **DoCmd** object.</span></span>

