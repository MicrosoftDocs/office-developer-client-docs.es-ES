---
title: AbrirConsulta (acción de macro)
TOCTitle: OpenQuery Macro Action
ms:assetid: 64bfce73-aeaf-9a78-895c-492e5da43ded
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195094(v=office.15)
ms:contentKeyID: 48545298
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89069
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3a718355f8305c7182ba2bc1196e0099205f6da1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880274"
---
# <a name="openquery-macro-action"></a><span data-ttu-id="6bed2-102">AbrirConsulta (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="6bed2-102">OpenQuery Macro Action</span></span>


<span data-ttu-id="6bed2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6bed2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6bed2-p101">Puede usar la acción **AbrirConsulta** para abrir una consulta de selección o de tabla de referencias cruzadas en la vista Hoja de datos, vista Diseño o Vista preliminar. Esta acción ejecuta una consulta de acción. También puede seleccionar un modo de entrada de datos para la consulta.</span><span class="sxs-lookup"><span data-stu-id="6bed2-p101">You can use the **OpenQuery** action to open a select or crosstab query in Datasheet view, Design view, or Print Preview. This action runs an action query. You can also select a data entry mode for the query.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6bed2-p102">[!NOTA] Esta acción sólo está disponible en el entorno de bases de datos de Access (.mdb o .accdb). Vea las acciones <STRONG>AbrirVista</STRONG>, <STRONG>AbrirProcedimientoAlmacenado</STRONG> o <STRONG>AbrirFunción</STRONG> si utiliza el entorno de proyectos de Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="6bed2-p102">This action is only available in the Access database environment (.mdb or .accdb). See the <STRONG>OpenView</STRONG>, <STRONG>OpenStoredProcedure</STRONG>, or <STRONG>OpenFunction</STRONG> actions if you are using the Access project environment (.adp).</span></span></P>



## <a name="setting"></a><span data-ttu-id="6bed2-109">Configuración</span><span class="sxs-lookup"><span data-stu-id="6bed2-109">Setting</span></span>

<span data-ttu-id="6bed2-110">La acción **AbrirConsulta** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="6bed2-110">The **OpenQuery** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6bed2-111">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="6bed2-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6bed2-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6bed2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6bed2-113"><strong>Nombre de la consulta</strong></span><span class="sxs-lookup"><span data-stu-id="6bed2-113"><strong>Query Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6bed2-114">El nombre de la consulta para abrir.</span><span class="sxs-lookup"><span data-stu-id="6bed2-114">The name of the query to open.</span></span> <span data-ttu-id="6bed2-115">El cuadro <strong>Nombre de la consulta</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todas las consultas en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="6bed2-115">The <strong>Query Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all queries in the current database.</span></span> <span data-ttu-id="6bed2-116">Este es un argumento requerido. Si ejecuta una macro que contiene la acción <strong>AbrirConsulta</strong> en una base de datos de biblioteca, Microsoft Access busca primero la consulta con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="6bed2-116">This is a required argument.If you run a macro containing the <strong>OpenQuery</strong> action in a library database, Microsoft Access first looks for the query with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bed2-117"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="6bed2-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="6bed2-p104">Vista en la que se va a abrir la consulta. Haga clic en <strong>Hoja de datos</strong>, <strong>Diseño</strong>, <strong>Vista preliminar</strong>, <strong>Tabla dinámica</strong> o <strong>Gráfico dinámico</strong> en el cuadro <strong>Vista</strong>. El valor predeterminado es <strong>Hoja de datos</strong>.</span><span class="sxs-lookup"><span data-stu-id="6bed2-p104">The view in which the query will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bed2-121"><strong>Modo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="6bed2-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="6bed2-p105">Modo de entrada de datos de la consulta. Esto sólo se aplica a las consultas abiertas en la vista Hoja de datos. Haga clic en <strong>Agregar</strong> (el usuario puede agregar nuevos registros pero no puede modificar los existentes), <strong>Modificar</strong> (el usuario puede modificar los registros existentes y agregar otros nuevos) o <strong>Solo lectura</strong> (el usuario sólo puede ver los registros). El valor predeterminado es <strong>Modificar</strong>.</span><span class="sxs-lookup"><span data-stu-id="6bed2-p105">The data entry mode for the query. This applies only to queries opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6bed2-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6bed2-126">Remarks</span></span>

<span data-ttu-id="6bed2-127">Si usa **Hoja de datos** para el argumento **Vista**, Access muestra el conjunto de resultados si la consulta es una consulta de selección, de tabla de referencias cruzadas, de combinación o de paso a través cuya propiedad **DevuelveRegistros** está establecida en **Sí** y ejecuta la consulta si es una consulta de acción, de definición de datos o de paso a través cuya propiedad **DevuelveRegistros** está establecida en **No**.</span><span class="sxs-lookup"><span data-stu-id="6bed2-127">If you use **Datasheet** for the **View** argument, Access displays the result set if the query is a select, crosstab, union, or pass-through query whose **ReturnsRecords** property is set to **Yes**; and it runs the query if it is an action, data-definition, or pass-through query whose **ReturnsRecords** property is set to **No**.</span></span>

<span data-ttu-id="6bed2-p106">La acción **AbrirConsulta** es similar a hacer doble clic en la consulta en el panel de navegación o hacer clic con el botón secundario en la consulta en el panel de navegación y seleccionar una vista. Con esta acción, se pueden seleccionar opciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="6bed2-p106">The **OpenQuery** action is similar to double-clicking the query in the Navigation Pane, or right-clicking the query in the Navigation Pane and selecting a view. With this action you can select additional options.</span></span>

<span data-ttu-id="6bed2-130">**Sugerencias**</span><span class="sxs-lookup"><span data-stu-id="6bed2-130">**Tips**</span></span>

  - <span data-ttu-id="6bed2-p107">Puede arrastrar una consulta desde el panel de navegación hasta una fila de acción de una macro. De este modo, se crea automáticamente una acción **AbrirConsulta** que abre la consulta en la vista Hoja de datos. Al cambiar a la vista Diseño mientras está abierta la consulta, se quita el valor del argumento **Modo de datos** de la consulta. Este valor no tiene efecto, incluso si el usuario vuelve a la vista Hoja de datos.</span><span class="sxs-lookup"><span data-stu-id="6bed2-p107">You can drag a query from the Navigation Pane to a macro action row. This automatically creates an **OpenQuery** action that opens the query in Datasheet view. Switching to Design view while the query is open removes the **Data Mode** argument setting for the query. This setting isn't in effect even if the user returns to Datasheet view.</span></span>

  - <span data-ttu-id="6bed2-135">Si no desea que se muestren los mensajes del sistema que normalmente aparecen cuando se ejecuta una consulta de acción (que indican que es una consulta de acción y muestran cuántos registros se verán afectados), puede utilizar la acción **EstablecerAdvertencias** para suprimir la presentación de estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="6bed2-135">If you don't want to display the system messages that normally appear when an action query is run (indicating it is an action query and showing how many records will be affected), you can use the **SetWarnings** action to suppress the display of these messages.</span></span>

<span data-ttu-id="6bed2-136">Para ejecutar la acción **AbrirConsulta** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **OpenQuery** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="6bed2-136">To run the **OpenQuery** action in a Visual Basic for Applications (VBA) module, use the **OpenQuery** method of the **DoCmd** object.</span></span>

