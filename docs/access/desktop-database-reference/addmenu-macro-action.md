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
localization_priority: Normal
ms.openlocfilehash: 119e824cae71d54bb398aa68f476a667f14a6888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280276"
---
# <a name="addmenu-macro-action"></a><span data-ttu-id="7a095-102">AgregarMenú (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="7a095-102">AddMenu macro action</span></span>


<span data-ttu-id="7a095-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a095-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7a095-104">Este artículo describe la operación básica de la acción de macro **AgregarMenú**.</span><span class="sxs-lookup"><span data-stu-id="7a095-104">This article describes the basic operation of the **AddMenu** macro action.</span></span>

<span data-ttu-id="7a095-105">Puede usar la acción **AgregarMenú** para crear:</span><span class="sxs-lookup"><span data-stu-id="7a095-105">You can use the **AddMenu** action to create:</span></span>

- <span data-ttu-id="7a095-106">Menús personalizados en la ficha **Complementos** para un formulario o informe particular.</span><span class="sxs-lookup"><span data-stu-id="7a095-106">Custom menus on the **Add-Ins** tab for a particular form or report.</span></span>

- <span data-ttu-id="7a095-p101">Un menú contextual personalizado para un formulario, un informe o un control. El menú contextual personalizado reemplaza el menú contextual integrado para el formulario, el informe o el control.</span><span class="sxs-lookup"><span data-stu-id="7a095-p101">A custom shortcut menu for a form, report, or control. The custom shortcut menu replaces the built-in shortcut menu for the form, report, or control.</span></span>

- <span data-ttu-id="7a095-p102">Un menú contextual global. El menú contextual global reemplaza el menú contextual integrado para los campos en las hojas de datos de tabla y consulta, los formularios y los informes, excepto donde se agregó un menú contextual personalizado para un formulario, un informe o un control.</span><span class="sxs-lookup"><span data-stu-id="7a095-p102">A global shortcut menu. The global shortcut menu replaces the built-in shortcut menu for fields in table and query datasheets, forms, and reports, except where you've added a custom shortcut menu for a form, report, or control.</span></span>

## <a name="setting"></a><span data-ttu-id="7a095-111">Setting</span><span class="sxs-lookup"><span data-stu-id="7a095-111">Setting</span></span>

<span data-ttu-id="7a095-112">La acción **AgregarMenú** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="7a095-112">The **AddMenu** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7a095-113">Argumento de acción</span><span class="sxs-lookup"><span data-stu-id="7a095-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="7a095-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a095-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a095-115"><strong>Nombre del menú</strong></span><span class="sxs-lookup"><span data-stu-id="7a095-115"><strong>Menu Name</strong></span></span></p></td>
<td><p><span data-ttu-id="7a095-116">El nombre del menú, por ejemplo, &quot; Comandos de informe o Herramientas &quot; &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="7a095-116">The name of the menu, for example, &quot;Report Commands&quot; or &quot;Tools&quot;.</span></span> <span data-ttu-id="7a095-117">Para crear una tecla de acceso para que pueda usar el teclado para elegir el menú, escriba una y comercial ( ) antes de la letra que desea que <strong>&amp;</strong> sea la tecla de acceso.</span><span class="sxs-lookup"><span data-stu-id="7a095-117">To create an access key so that you can use the keyboard to choose the menu, type an ampersand (<strong>&amp;</strong>) before the letter you want to be the access key.</span></span> <span data-ttu-id="7a095-118">Esta letra se subrayará en el nombre del menú en la ficha <strong>Complementos</strong>.</span><span class="sxs-lookup"><span data-stu-id="7a095-118">This letter will be underlined in the menu name on the <strong>Add-Ins</strong> tab.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a095-119"><strong>Nombre de macro de menú</strong></span><span class="sxs-lookup"><span data-stu-id="7a095-119"><strong>Menu Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="7a095-120">El nombre del grupo de macros que contiene las macros para los comandos del menú.</span><span class="sxs-lookup"><span data-stu-id="7a095-120">The name of the macro group that contains the macros for the menu's commands.</span></span> <span data-ttu-id="7a095-121">Es un argumento obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7a095-121">This is a required argument.</span></span></p>
<p><span data-ttu-id="7a095-122"><strong>NOTA:</strong>Si ejecuta una macro <strong></strong> que contiene la acción AgregarMenú en una base de datos de biblioteca, Microsoft Office Access 2007 solo busca el grupo de macros con este nombre en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="7a095-122"><strong>NOTE</strong>: If you run a macro containing the <strong>AddMenu</strong> action in a library database, Microsoft Office Access 2007 looks for the macro group with this name in the current database only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a095-123"><strong>Texto de la barra de estado</strong></span><span class="sxs-lookup"><span data-stu-id="7a095-123"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="7a095-124">El texto que se muestra en la barra de estado cuando se selecciona el menú.</span><span class="sxs-lookup"><span data-stu-id="7a095-124">The text to display in the status bar when the menu is selected.</span></span> <span data-ttu-id="7a095-125">Este argumento se pasa por alto para los menús contextuales.</span><span class="sxs-lookup"><span data-stu-id="7a095-125">This argument is ignored for shortcut menus.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7a095-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7a095-126">Remarks</span></span>

<span data-ttu-id="7a095-p106">Para ejecutar la acción **AgregarMenú** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **AddMenu** del objeto **DoCmd**. También puede establecer la propiedad **MenuBar** o **ShortcutMenuBar** en VBA para crear un menú personalizado en la ficha **Complementos** o para asociar un menú contextual personalizado a un formulario, un informe o un control. Puede establecer la propiedad **ShortcutMenuBar** del objeto **Application** para crear un menú contextual global.</span><span class="sxs-lookup"><span data-stu-id="7a095-p106">To run the **AddMenu** action in a Visual Basic for Applications (VBA) module, use the **AddMenu** method of the **DoCmd** object. You can also set the **MenuBar** or **ShortcutMenuBar** property in VBA to create a custom menu on the **Add-Ins** tab or to attach a custom shortcut menu to a form, report, or control. You can set the **ShortcutMenuBar** property of the **Application** object to create a global shortcut menu.</span></span>

