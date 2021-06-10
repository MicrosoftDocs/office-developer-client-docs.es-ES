---
title: AbrirTabla (acción de macro)
TOCTitle: OpenTable macro action
ms:assetid: 4220ad3a-d064-0034-2806-ec1a447cebac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192909(v=office.15)
ms:contentKeyID: 48544469
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm149011
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 48a3797c2008f261eda8acc3391b39561fec05f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288297"
---
# <a name="opentable-macro-action"></a><span data-ttu-id="d27ed-102">AbrirTabla (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="d27ed-102">OpenTable macro action</span></span>

<span data-ttu-id="d27ed-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d27ed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d27ed-p101">Puede usar la acción **AbrirTabla** para abrir una tabla en la vista Hoja de datos, vista Diseño o Vista preliminar. También puede seleccionar un modo de entrada de datos para la tabla.</span><span class="sxs-lookup"><span data-stu-id="d27ed-p101">You can use the **OpenTable** action to open a table in Datasheet view, Design view, or Print Preview. You can also select a data entry mode for the table.</span></span>

## <a name="setting"></a><span data-ttu-id="d27ed-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="d27ed-106">Setting</span></span>

<span data-ttu-id="d27ed-107">La acción **AbrirTabla** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="d27ed-107">The **OpenTable** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d27ed-108">Argumento de acción</span><span class="sxs-lookup"><span data-stu-id="d27ed-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d27ed-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d27ed-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d27ed-110"><strong>Nombre de la tabla</strong></span><span class="sxs-lookup"><span data-stu-id="d27ed-110"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d27ed-111">Nombre de la tabla que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="d27ed-111">The name of the table to open.</span></span> <span data-ttu-id="d27ed-112">El cuadro <strong>Nombre de la tabla</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todas las tablas de la base de datos activa.</span><span class="sxs-lookup"><span data-stu-id="d27ed-112">The <strong>Table Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all tables in the current database.</span></span> <span data-ttu-id="d27ed-113">Éste es un argumento requerido.</span><span class="sxs-lookup"><span data-stu-id="d27ed-113">This is a required argument.</span></span> <span data-ttu-id="d27ed-114">Si ejecuta una macro que contiene la acción <strong>AbrirTabla</strong> en una base de datos de biblioteca, Microsoft Access primero busca la tabla con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos activa.</span><span class="sxs-lookup"><span data-stu-id="d27ed-114">If you run a macro containing the <strong>OpenTable</strong> action in a library database, Microsoft Microsoft Access looks for the table with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d27ed-115"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="d27ed-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="d27ed-p103">Vista en la que se va a abrir la tabla. Haga clic en <strong>Hoja de datos</strong>, <strong>Diseño</strong>, <strong>Vista preliminar</strong>, <strong>Tabla dinámica</strong> o <strong>Gráfico dinámico</strong> en el cuadro <strong>Vista</strong>. El valor predeterminado es <strong>Hoja de datos</strong>.</span><span class="sxs-lookup"><span data-stu-id="d27ed-p103">The view in which the table will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d27ed-119"><strong>Modo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="d27ed-119"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="d27ed-p104">Modo de entrada de datos para la tabla. Sólo se aplica a las tablas abiertas en la vista Hoja de datos. Haga clic en <strong>Agregar</strong> (el usuario puede agregar nuevos registros, pero no puede modificar los existentes), <strong>Modificar</strong> (el usuario puede modificar los registros existentes y agregar registros nuevos) o <strong>Solo lectura</strong> (el usuario sólo puede ver los registros). El valor predeterminado es <strong>Modificar</strong>.</span><span class="sxs-lookup"><span data-stu-id="d27ed-p104">The data entry mode for the table. This applies only to tables opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="d27ed-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d27ed-124">Remarks</span></span>

<span data-ttu-id="d27ed-125">Esta acción es similar a hacer doble clic en una tabla en el panel de navegación, o bien, a hacer clic con el botón secundario en la tabla en el panel de navegación y, a continuación, seleccionar una vista.</span><span class="sxs-lookup"><span data-stu-id="d27ed-125">This action is similar to double-clicking the table in the Navigation Pane, or right-clicking the table in the Navigation Pane and selecting a view.</span></span>

> [!TIP]
> <span data-ttu-id="d27ed-p105">[!SUGERENCIA] Puede arrastrar una tabla desde el panel de navegación hasta una fila de acción de una macro. De este modo, se crea automáticamente una acción **AbrirTabla** que abre la tabla en la vista Hoja de datos.</span><span class="sxs-lookup"><span data-stu-id="d27ed-p105">You can drag a table from the Navigation Pane to a macro action row. This automatically creates an **OpenTable** action that opens the table in Datasheet view.</span></span>

<span data-ttu-id="d27ed-128">Para ejecutar la acción **AbrirTabla** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **OpenTable** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="d27ed-128">To run the **OpenTable** action in a Visual Basic for Applications (VBA) module, use the **OpenTable** method of the **DoCmd** object.</span></span>

