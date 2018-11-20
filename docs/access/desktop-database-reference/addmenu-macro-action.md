---
title: AgregarMenú (acción de macro)
TOCTitle: AddMenu macro action
ms:assetid: 4eb2afa0-ed1f-41b1-d27f-b3ce7a73d2bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193760(v=office.15)
ms:contentKeyID: 48544762
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm37891
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d04c98da0ecef1c2323930c74588b7a6a07c2e29
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026270"
---
# <a name="addmenu-macro-action"></a><span data-ttu-id="70468-102">AgregarMenú (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="70468-102">AddMenu macro action</span></span>


<span data-ttu-id="70468-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70468-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70468-104">Este artículo describe la operación básica de la acción de macro **AgregarMenú**.</span><span class="sxs-lookup"><span data-stu-id="70468-104">This article describes the basic operation of the **AddMenu** macro action.</span></span>

<span data-ttu-id="70468-105">Puede usar la acción **AgregarMenú** para crear:</span><span class="sxs-lookup"><span data-stu-id="70468-105">You can use the **AddMenu** action to create:</span></span>

- <span data-ttu-id="70468-106">Menús personalizados en la ficha **Complementos** para un formulario o informe particular.</span><span class="sxs-lookup"><span data-stu-id="70468-106">Custom menus on the **Add-Ins** tab for a particular form or report.</span></span>

- <span data-ttu-id="70468-p101">Un menú contextual personalizado para un formulario, un informe o un control. El menú contextual personalizado reemplaza el menú contextual integrado para el formulario, el informe o el control.</span><span class="sxs-lookup"><span data-stu-id="70468-p101">A custom shortcut menu for a form, report, or control. The custom shortcut menu replaces the built-in shortcut menu for the form, report, or control.</span></span>

- <span data-ttu-id="70468-p102">Un menú contextual global. El menú contextual global reemplaza el menú contextual integrado para los campos en las hojas de datos de tabla y consulta, los formularios y los informes, excepto donde se agregó un menú contextual personalizado para un formulario, un informe o un control.</span><span class="sxs-lookup"><span data-stu-id="70468-p102">A global shortcut menu. The global shortcut menu replaces the built-in shortcut menu for fields in table and query datasheets, forms, and reports, except where you've added a custom shortcut menu for a form, report, or control.</span></span>

## <a name="setting"></a><span data-ttu-id="70468-111">Configuración</span><span class="sxs-lookup"><span data-stu-id="70468-111">Setting</span></span>

<span data-ttu-id="70468-112">La acción **AgregarMenú** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="70468-112">The **AddMenu** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70468-113">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="70468-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="70468-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="70468-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70468-115"><strong>Nombre del menú</strong></span><span class="sxs-lookup"><span data-stu-id="70468-115"><strong>Menu Name</strong></span></span></p></td>
<td><p><span data-ttu-id="70468-116">El nombre del menú, por ejemplo, &quot;comandos de informe&quot; o &quot;herramientas&quot;.</span><span class="sxs-lookup"><span data-stu-id="70468-116">The name of the menu, for example, &quot;Report Commands&quot; or &quot;Tools&quot;.</span></span> <span data-ttu-id="70468-117">Para crear una tecla de acceso para que puede utilizar el teclado para elegir el menú, escriba una y comercial (<strong>&amp;</strong>) antes de la letra que desea que sean la tecla de acceso.</span><span class="sxs-lookup"><span data-stu-id="70468-117">To create an access key so that you can use the keyboard to choose the menu, type an ampersand (<strong>&amp;</strong>) before the letter you want to be the access key.</span></span> <span data-ttu-id="70468-118">Esta letra aparecerá subrayada en el nombre del menú en la ficha <strong>Complementos</strong> .</span><span class="sxs-lookup"><span data-stu-id="70468-118">This letter will be underlined in the menu name on the <strong>Add-Ins</strong> tab.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70468-119"><strong>Nombre de macro de menú</strong></span><span class="sxs-lookup"><span data-stu-id="70468-119"><strong>Menu Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="70468-p104">El nombre del grupo de macros que contiene las macros para los comandos del menú. Es un argumento obligatorio. 

</span><span class="sxs-lookup"><span data-stu-id="70468-p104">The name of the macro group that contains the macros for the menu's commands. This is a required argument.</span></span></p>
<p><span data-ttu-id="70468-122"><strong>Nota</strong>: si ejecuta una macro que contiene la acción <strong>AgregarMenú</strong> en una base de datos de biblioteca, Microsoft Office Access 2007 busca el grupo de macros con este nombre en sólo la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="70468-122"><strong>NOTE</strong>: If you run a macro containing the <strong>AddMenu</strong> action in a library database, Microsoft Office Access 2007 looks for the macro group with this name in the current database only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70468-123"><strong>Texto de la barra de estado</strong></span><span class="sxs-lookup"><span data-stu-id="70468-123"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="70468-p105">El texto que se muestra en la barra de estado cuando se selecciona el menú. Este argumento se pasa por alto para los menús contextuales.</span><span class="sxs-lookup"><span data-stu-id="70468-p105">The text to display in the status bar when the menu is selected. This argument is ignored for shortcut menus.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="70468-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="70468-126">Remarks</span></span>

<span data-ttu-id="70468-p106">Para ejecutar la acción **AgregarMenú** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **AddMenu** del objeto **DoCmd**. También puede establecer la propiedad **MenuBar** o **ShortcutMenuBar** en VBA para crear un menú personalizado en la ficha **Complementos** o para asociar un menú contextual personalizado a un formulario, un informe o un control. Puede establecer la propiedad **ShortcutMenuBar** del objeto **Application** para crear un menú contextual global.</span><span class="sxs-lookup"><span data-stu-id="70468-p106">To run the **AddMenu** action in a Visual Basic for Applications (VBA) module, use the **AddMenu** method of the **DoCmd** object. You can also set the **MenuBar** or **ShortcutMenuBar** property in VBA to create a custom menu on the **Add-Ins** tab or to attach a custom shortcut menu to a form, report, or control. You can set the **ShortcutMenuBar** property of the **Application** object to create a global shortcut menu.</span></span>

