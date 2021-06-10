---
title: AplicarFiltro (acción de macro)
TOCTitle: ApplyFilter macro action
ms:assetid: c63988c4-4506-cc51-98f7-478d1f3fe668
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823130(v=office.15)
ms:contentKeyID: 48547623
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm79035
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e79ab56778f9429e7f1a985f0f81864ae4363606
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297000"
---
# <a name="applyfilter-macro-action"></a><span data-ttu-id="d02dc-102">AplicarFiltro (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="d02dc-102">ApplyFilter macro action</span></span>

<span data-ttu-id="d02dc-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d02dc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d02dc-p101">Puede usar la acción **AplicarFiltro** para aplicar un filtro, una consulta o una cláusula WHERE de SQL a una tabla, un formulario o un informe para restringir u ordenar los registros en la tabla, o los registros de la tabla subyacente o la consulta del formulario o informe. Para los informes, puede usar esta acción solo en una macro especificada por la propiedad del evento **OnOpen** del informe.</span><span class="sxs-lookup"><span data-stu-id="d02dc-p101">You can use the **ApplyFilter** action to apply a filter, a query, or an SQL WHERE clause to a table, form, or report to restrict or sort the records in the table, or the records from the underlying table or query of the form or report. For reports, you can use this action only in a macro specified by the report's **OnOpen** event property.</span></span>

> [!NOTE]
> <span data-ttu-id="d02dc-p102">[!NOTA] Puede usar esta acción para aplicar una cláusula WHERE de SQL cuando aplique un filtro de servidor. Un filtro de servidor no se puede aplicar a una fuente de registros de un procedimiento almacenado.</span><span class="sxs-lookup"><span data-stu-id="d02dc-p102">You can use this action to apply an SQL WHERE clause only when applying a server filter. A server filter cannot be applied to a stored procedure's record source.</span></span>

## <a name="setting"></a><span data-ttu-id="d02dc-108">Configuración</span><span class="sxs-lookup"><span data-stu-id="d02dc-108">Setting</span></span>

<span data-ttu-id="d02dc-109">La acción **AplicarFiltro** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="d02dc-109">The **ApplyFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d02dc-110">Argumento de acción</span><span class="sxs-lookup"><span data-stu-id="d02dc-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d02dc-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d02dc-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d02dc-112">Nombre del filtro</span><span class="sxs-lookup"><span data-stu-id="d02dc-112">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="d02dc-p103">El nombre de un filtro o una consulta que restringe u ordena los registros de una tabla, un formulario o un informe. Puede escribir el nombre de una consulta existente o un filtro que se guardó como una consulta en el cuadro <strong>Nombre del filtro</strong> de la sección <strong>Argumentos de acciones</strong> del panel <strong>Generador de macros</strong>.  </span><span class="sxs-lookup"><span data-stu-id="d02dc-p103">The name of a filter or query that restricts or sorts the records of the table, form, or report. You can enter the name of either an existing query or a filter that has been saved as a query in the <strong>Filter Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane.</span></span></p><p><span data-ttu-id="d02dc-115"><strong>NOTA:</strong>Cuando se usa esta acción para aplicar un filtro de servidor, el argumento Filter Name debe estar en blanco.</span><span class="sxs-lookup"><span data-stu-id="d02dc-115"><strong>NOTE</strong>: When you are using this action to apply a server filter, the Filter Name argument must be blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d02dc-116">Condición WHERE</span><span class="sxs-lookup"><span data-stu-id="d02dc-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="d02dc-117">Una cláusula WHERE válida de SQL (sin la palabra WHERE) o una expresión que restringe los registros de la tabla, el formulario o el informe.</span><span class="sxs-lookup"><span data-stu-id="d02dc-117">A valid SQL WHERE clause (without the word WHERE) or an expression that restricts the records of the table, form, or report.</span></span></p>
<p><span data-ttu-id="d02dc-118"><b>NOTA</b>: En una expresión de argumento Where Condition, el lado izquierdo de la expresión normalmente contiene un nombre de campo de la tabla o consulta subyacente para el formulario o informe.</span><span class="sxs-lookup"><span data-stu-id="d02dc-118"><b>NOTE</b>: In a Where Condition argument expression, the left side of the expression typically contains a field name from the underlying table or query for the form or report.</span></span> <span data-ttu-id="d02dc-119">The right side of the expression typically contains the criteria you want to apply to this field to restrict or sort the records.</span><span class="sxs-lookup"><span data-stu-id="d02dc-119">The right side of the expression typically contains the criteria you want to apply to this field to restrict or sort the records.</span></span> <span data-ttu-id="d02dc-120">Por ejemplo, los criterios pueden ser el nombre de un control en otro formulario que contenga el valor con el que desea que coincidan los registros en el primer formulario.</span><span class="sxs-lookup"><span data-stu-id="d02dc-120">For example, the criteria can be the name of a control on another form that contains the value you want the records in the first form to match.</span></span> <span data-ttu-id="d02dc-121">El nombre del control debe ser completo, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d02dc-121">The name of the control should be fully qualified, for example:</span></span></p>
<p><span data-ttu-id="d02dc-122"><strong>Forms</strong>! <em>formname</em>! <em>controlname</em> Los nombres de campo deben estar entre comillas dobles y los literales de cadena deben estar entre comillas simples.</span><span class="sxs-lookup"><span data-stu-id="d02dc-122"><strong>Forms</strong>!<em>formname</em>!<em>controlname</em> Field names should be surrounded by double quotation marks and string literals should be surrounded by single quotation marks.</span></span> <span data-ttu-id="d02dc-123">La longitud máxima del argumento Where Condition es de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d02dc-123">The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="d02dc-124">If you need to enter a longer SQL WHERE clause, use the <strong>ApplyFilter</strong> method of the <strong>DoCmd</strong> object in a Visual Basic for Applications (VBA) module.</span><span class="sxs-lookup"><span data-stu-id="d02dc-124">If you need to enter a longer SQL WHERE clause, use the <strong>ApplyFilter</strong> method of the <strong>DoCmd</strong> object in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="d02dc-125">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span><span class="sxs-lookup"><span data-stu-id="d02dc-125">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d02dc-126">Puede usar el argumento Nombre de filtro si ya ha definido un filtro que proporciona los datos adecuados.</span><span class="sxs-lookup"><span data-stu-id="d02dc-126">You can use the Filter Name argument if you have already defined a filter that provides the appropriate data.</span></span> <span data-ttu-id="d02dc-127">El argumento WhereCondition puede usarlo para especificar directamente los criterios de restricción.</span><span class="sxs-lookup"><span data-stu-id="d02dc-127">You can use the Where Condition argument to enter the restriction criteria directly.</span></span> <span data-ttu-id="d02dc-128">Si usa ambos argumentos, Microsoft Office Access 2007 aplica la cláusula WHERE a los resultados del filtro.</span><span class="sxs-lookup"><span data-stu-id="d02dc-128">If you use both arguments, Microsoft Office Access 2007 applies the WHERE clause to the results of the filter.</span></span> <span data-ttu-id="d02dc-129">Debe usar uno o ambos argumentos.</span><span class="sxs-lookup"><span data-stu-id="d02dc-129">You must use one or both arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="d02dc-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d02dc-130">Remarks</span></span>

<span data-ttu-id="d02dc-131">Puede aplicar un filtro o una consulta a un formulario en la vista Formulario o la vista Hoja de datos.</span><span class="sxs-lookup"><span data-stu-id="d02dc-131">You can apply a filter or query to a form in Form view or Datasheet view.</span></span>

<span data-ttu-id="d02dc-132">El filtro y la condición WHERE que aplica se convierten en la configuración de la propiedad **Filter** o **ServerFilter** del formulario o el informe.</span><span class="sxs-lookup"><span data-stu-id="d02dc-132">The filter and WHERE condition you apply become the setting of the form's or report's **Filter** or **ServerFilter** property.</span></span>

<span data-ttu-id="d02dc-p107">Para las tablas y los formularios, esta acción es similar a hacer clic en **Aplicar filtro u orden** o **Aplicar filtro de servidor** en el menú **Registros**. El comando de menú aplica el filtro creado más recientemente a la tabla o el formulario, mientras que la acción **AplicarFiltro** aplica un filtro o una consulta especificada.</span><span class="sxs-lookup"><span data-stu-id="d02dc-p107">For tables and forms, this action is similar to clicking **Apply Filter/Sort** or **Apply Server Filter** on the **Records** menu. The menu command applies the most recently created filter to the table or form, whereas the **ApplyFilter** action applies a specified filter or query.</span></span>

<span data-ttu-id="d02dc-135">En una base de datos de Access, si va a **Filtro** en el menú **Registros** y hace clic en **Filtro u orden avanzado** después de ejecutar la acción **AplicarFiltro**, la ventana Filtro u orden avanzado muestra los criterios de filtro que seleccionó con esta acción.</span><span class="sxs-lookup"><span data-stu-id="d02dc-135">In an Access database, if you point to **Filter** on the **Records** menu and then click **Advanced Filter/Sort** after running the **ApplyFilter** action, the Advanced Filter/Sort window shows the filter criteria you have selected with this action.</span></span>

<span data-ttu-id="d02dc-p108">Para quitar un filtro y mostrar todos los registros para una tabla o un formulario en una Office Access 2007 base de datos, puede utilizar la acción **MostrarTodosRegistros** o el comando **Quitar filtro u orden** en el menú **Registros**. Para quitar un filtro en un proyecto de Access (.adp), puede volver a la ventana Filtro de servidor por formulario y quitar todos los criterios de filtros, y hacer clic en **Aplicar filtro de servidor** en el menú **Registros** de la barra de herramientas, o establecer la propiedad **ServerFilterByForm** a **False** (0).</span><span class="sxs-lookup"><span data-stu-id="d02dc-p108">To remove a filter and display all of the records for a table or form in an Office Access 2007 database, you can use the **ShowAllRecords** action or the **Remove Filter/Sort** command on the **Records** menu. To remove a filter in an Access project (.adp), you can return to the Server Filter By Form window and remove all filter criteria and then click **Apply Server Filter** on the **Records** menu on the toolbar, or set the **ServerFilterByForm** property to **False** (0).</span></span>

<span data-ttu-id="d02dc-p109">Cuando guarda una tabla o un formulario, Access guarda cualquier filtro definido actualmente en ese objeto, pero no aplica el filtro automáticamente la próxima vez que se abre el objeto (aunque aplicará automáticamente cualquier orden que usted aplicó al objeto antes de guardarlo). Si desea aplicar un filtro automáticamente cuando se abre un formulario por primera vez, especifique una macro que contenga la acción **AplicarFiltro** o un procedimiento de evento que contenga el método **ApplyFilter** del objeto **DoCmd** como la configuración de la propiedad de evento **OnOpen** del formulario. También puede aplicar un filtro al utilizar la acción **AbrirFormulario** o **AbrirInforme**, o sus correspondientes métodos. Para aplicar un filtro automáticamente cuando se abre una tabla por primera vez, puede abrir la tabla con una macro que contenga la acción **AbrirTabla**, seguida inmediatamente por la acción **AplicarFiltro**.</span><span class="sxs-lookup"><span data-stu-id="d02dc-p109">When you save a table or form, Access saves any filter currently defined in that object, but won't apply the filter automatically the next time the object is opened (although it will automatically apply any sort you applied to the object before it was saved). If you want to apply a filter automatically when a form is first opened, specify a macro containing the **ApplyFilter** action or an event procedure containing the **ApplyFilter** method of the **DoCmd** object as the **OnOpen** event property setting of the form. You can also apply a filter by using the **OpenForm** or **OpenReport** action, or their corresponding methods. To apply a filter automatically when a table is first opened, you can open the table by using a macro containing the **OpenTable** action, followed immediately by the **ApplyFilter** action.</span></span>

## <a name="example"></a><span data-ttu-id="d02dc-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d02dc-142">Example</span></span>

<span data-ttu-id="d02dc-143">En el ejemplo siguiente se muestra cómo usar la acción ApplyFilter para filtrar el formulario frmFoods cuando se abre.</span><span class="sxs-lookup"><span data-stu-id="d02dc-143">The following example shows how to use the ApplyFilter action to filter the frmFoods form as it is opened.</span></span>

<span data-ttu-id="d02dc-144">**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="d02dc-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    ApplyFilter
        Filter Name
        Where Condition=[display_name] Link "*cheese*"
        Control Name
```



