---
title: EstablecerElementoDelMenú (acción de macro)
TOCTitle: SetMenuItem macro action
ms:assetid: 503b3635-e721-1b99-3249-626e5dccdb8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193803(v=office.15)
ms:contentKeyID: 48544789
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm16614
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fe61a3368813ba3420920909f818beee2029d993
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308683"
---
# <a name="setmenuitem-macro-action"></a><span data-ttu-id="2003e-102">EstablecerElementoDelMenú (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="2003e-102">SetMenuItem macro action</span></span>

<span data-ttu-id="2003e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2003e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2003e-104">La acción **EstablecerElementoDelMenú** sirve para establecer el estado de los elementos de menú (habilitado o deshabilitado, seleccionado o no seleccionado) en los menús globales o personalizados de la ficha **Complementos**.</span><span class="sxs-lookup"><span data-stu-id="2003e-104">You can use the **SetMenuItem** action to set the state of menu items (enabled or disabled, selected or unselected) on custom or global menus on the **Add-Ins** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="2003e-p101">[!NOTA] La acción **EstablecerElementoDelMenú** solo funciona con menús globales y personalizados creados mediante macros de menús. La acción **EstablecerElementoDelMenú** está incluida en Microsoft Access sólo a efectos de compatibilidad con versiones anteriores. No se puede usar con la funcionalidad de las barras de comandos. Sin embargo, puede usar las propiedades **Enabled** y **State** en un módulo de Visual Basic para Aplicaciones (VBA) con el fin de habilitar, deshabilitar, seleccionar o cancelar la selección de elementos de menús contextuales o menús globales o personalizados.</span><span class="sxs-lookup"><span data-stu-id="2003e-p101">The **SetMenuItem** action works only with custom and global menus created by using menu macros. The **SetMenuItem** action is included in Microsoft Access only for compatibility with previous versions. It does not work with the command bar functionality. However, you can use the **Enabled** and **State** properties in a Visual Basic for Applications (VBA) module to disable or enable and select or unselect items on shortcut menus or custom or global menus.</span></span>

## <a name="setting"></a><span data-ttu-id="2003e-109">Configuración</span><span class="sxs-lookup"><span data-stu-id="2003e-109">Setting</span></span>

<span data-ttu-id="2003e-110">La acción **EstablecerElementoDelMenú** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="2003e-110">The **SetMenuItem** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2003e-111">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="2003e-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="2003e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2003e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2003e-113"><strong>Índice del menú</strong></span><span class="sxs-lookup"><span data-stu-id="2003e-113"><strong>Menu Index</strong></span></span></p></td>
<td><p><span data-ttu-id="2003e-114">El índice del menú que contiene el comando para el que se desea establecer el estado.</span><span class="sxs-lookup"><span data-stu-id="2003e-114">The index of the menu that contains the command for which you want to set the state.</span></span> <span data-ttu-id="2003e-115">Especifique un valor Entero, contando desde 0, para el índice del elemento de menú deseado dentro del menú global o personalizado.</span><span class="sxs-lookup"><span data-stu-id="2003e-115">Enter an integer value, starting from 0, for the index of the desired menu in the custom or global menu.</span></span> <span data-ttu-id="2003e-116">Escriba el valor del índice en el cuadro <strong>Índice del menú</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros.</span><span class="sxs-lookup"><span data-stu-id="2003e-116">Enter the index value in the <strong>Menu Index</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="2003e-117">El índice es relativo a la posición del menú en la macro de menú para el menú global o personalizado (la posición de la acción <strong>AgregarMenú</strong> de este menú dentro de la macro de menú, contando desde 0).</span><span class="sxs-lookup"><span data-stu-id="2003e-117">The index is relative to the menu's position in the menu macro for the custom or global menu (the position of this menu's <strong>AddMenu</strong> action in the menu macro, counting from 0).</span></span> <span data-ttu-id="2003e-118">La presentación del menú puede ser algo diferente, ya que se pueden utilizar expresiones condicionales en la macro de menú para ocultar o mostrar elementos de menú personalizados.</span><span class="sxs-lookup"><span data-stu-id="2003e-118">The menu's display may be somewhat different, because you can use conditional expressions in the menu macro to hide or display custom menu items.</span></span> <span data-ttu-id="2003e-119">Este argumento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2003e-119">This is a required argument.</span></span> <span data-ttu-id="2003e-120">Si selecciona un menú con este argumento y deja en blanco los argumentos <strong>Índice del comando</strong> e <strong>Índice de subcomando</strong>, entonces puede habilitar o deshabilitar el propio nombre del menú.</span><span class="sxs-lookup"><span data-stu-id="2003e-120">If you select a menu with this argument and leave the <strong>Command Index</strong> and <strong>Subcommand Index</strong> arguments blank, you can enable or disable the menu name itself.</span></span> <span data-ttu-id="2003e-121">Sin embargo, no se puede seleccionar o anular la selección de un nombre de menú (Access no tiene en cuenta los valores <strong>Activar</strong> y <strong>Desactivar</strong> del argumento <strong>Marca</strong> para nombres de menús).</span><span class="sxs-lookup"><span data-stu-id="2003e-121">You cannot, however, select or unselect a menu name (Access ignores the <strong>Check</strong> and <strong>Uncheck</strong> settings for the <strong>Flag</strong> argument for menu names).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2003e-122"><strong>Índice del comando</strong></span><span class="sxs-lookup"><span data-stu-id="2003e-122"><strong>Command Index</strong></span></span></p></td>
<td><p><span data-ttu-id="2003e-p103">El índice del comando para el que se desea establecer el estado. Especifique un valor entero, empezando desde 0, para el índice del comando deseado dentro del menú seleccionado mediante el argumento <strong>Índice del menú</strong>. El índice es relativo a la posición del comando en el grupo de macros que define el menú seleccionado para el menú global o personalizado (la posición de la macro de este comando en el grupo de macros, contando desde 0). La presentación del menú puede ser algo diferente, ya que se pueden utilizar expresiones condicionales en el grupo de macros del menú para ocultar o mostrar comandos de menú personalizados.</span><span class="sxs-lookup"><span data-stu-id="2003e-p103">The index of the command for which you want to set the state. Enter an integer value, starting from 0, for the index of the desired command in the menu selected by the <strong>Menu Index</strong> argument. The index is relative to the command's position in the macro group that defines the selected menu for the custom or global menu (the position of this command's macro in the macro group, counting from 0). The menu's display may be somewhat different, because you can use conditional expressions in the menu's macro group to hide or display custom menu commands.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2003e-127"><strong>Índice de subcomando</strong></span><span class="sxs-lookup"><span data-stu-id="2003e-127"><strong>Subcommand Index</strong></span></span></p></td>
<td><p><span data-ttu-id="2003e-p104">El índice del subcomando para el que se desea establecer el estado. Esto sólo es de aplicación si el comando deseado tiene un submenú. En el submenú seleccionado por el argumento <strong>Índice del comando</strong>, escriba un valor Entero, comenzando desde 0, para el índice del subcomando deseado. El índice es relativo a la posición del subcomando en el grupo de macros que define al submenú seleccionado para el menú global o personalizado (la posición de la macro de este subcomando en el grupo de macros, contando desde 0).</span><span class="sxs-lookup"><span data-stu-id="2003e-p104">The index of the subcommand for which you want to set the state. This applies only if the desired command has a submenu. Enter an integer value, starting from 0, for the index of the desired subcommand in the submenu selected by the <strong>Command Index</strong> argument. The index is relative to the subcommand's position in the macro group that defines the selected submenu for the custom or global menu (the position of this subcommand's macro in the macro group, counting from 0).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2003e-132"><strong>Flag</strong></span><span class="sxs-lookup"><span data-stu-id="2003e-132"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="2003e-p105">El estado que desea establecer para el comando o subcomando. Haga clic en <strong>Sombrear</strong>, para deshabilitar el comando (éste aparecerá atenuado), <strong>Quitar sombreado</strong>, para habilitarlo, <strong>Activar</strong>, para colocar una marca junto al comando que indica que ha sido activado, o <strong>Desactivar</strong>, para quitar la marca. La opción predeterminada es <strong>Quitar sombreado</strong>.</span><span class="sxs-lookup"><span data-stu-id="2003e-p105">The state you want to set the command or subcommand to. Click <strong>Gray</strong> (to disable the command — it appears dimmed), <strong>Ungray</strong> (to enable it), <strong>Check</strong> (to place a check by the command — typically indicating it has been selected or toggled), or <strong>Uncheck</strong> (to remove the check). The default is <strong>Ungray</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2003e-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2003e-136">Remarks</span></span>

<span data-ttu-id="2003e-p106">La acción **EstablecerElementoDelMenú** sólo funciona para un menú global o personalizado. Si la ventana activa no contiene un menú global o personalizado y se ejecuta una macro que contenga la acción**EstablecerElementoDelMenú**, se genera un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2003e-p106">The **SetMenuItem** action works only on a custom or global menu. If the active window does not have a custom or global menu, running a macro containing the **SetMenuItem** action causes a run-time error.</span></span>

<span data-ttu-id="2003e-139">Esta acción se puede utilizar para establecer el estado de los comandos y subcomandos de menú, aunque no el de los subcomandos de subcomandos.</span><span class="sxs-lookup"><span data-stu-id="2003e-139">You can use this action to set the state of menu commands and subcommands, but not subcommands of subcommands.</span></span>

<span data-ttu-id="2003e-140">Para ejecutar la acción **EstablecerElementoDelMenú** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **SetMenuItem** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="2003e-140">To run the **SetMenuItem** action in a Visual Basic for Applications (VBA) module, use the **SetMenuItem** method of the **DoCmd** object.</span></span>

