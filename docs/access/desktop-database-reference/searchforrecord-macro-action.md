---
title: EncontrarRegistro (acción de macro)
TOCTitle: SearchForRecord macro action
ms:assetid: a3483c41-adb5-5923-55f4-1a3c4f60cb2f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821023(v=office.15)
ms:contentKeyID: 48546781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm118713
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: efa763a77250e1d5c617358f31421804c772468b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314647"
---
# <a name="searchforrecord-macro-action"></a><span data-ttu-id="df982-102">EncontrarRegistro (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="df982-102">SearchForRecord macro action</span></span>


<span data-ttu-id="df982-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df982-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df982-104">Puede usar la acción **EncontrarRegistro** para buscar un registro específico en una tabla, una consulta, un formulario o un informe.</span><span class="sxs-lookup"><span data-stu-id="df982-104">You can use the **SearchForRecord** action to search for a specific record in a table, query, form or report.</span></span>

## <a name="setting"></a><span data-ttu-id="df982-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="df982-105">Setting</span></span>

<span data-ttu-id="df982-106">La acción **EncontrarRegistro** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="df982-106">The **SearchForRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="df982-107">Argumento de acción</span><span class="sxs-lookup"><span data-stu-id="df982-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="df982-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="df982-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df982-109"><strong>Tipo de objeto</strong></span><span class="sxs-lookup"><span data-stu-id="df982-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="df982-p101">Especifique o seleccione el tipo de objeto de base de datos en el que desee realizar la búsqueda. Las opciones son <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong> o <strong>Informe</strong>.  </span><span class="sxs-lookup"><span data-stu-id="df982-p101">Enter or select the type of database object that you are searching in. You can select <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, or <strong>Report</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df982-112"><strong>Nombre del objeto</strong></span><span class="sxs-lookup"><span data-stu-id="df982-112"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="df982-p102">Especifique o seleccione el objeto específico que contenga el registro que desee buscar. En la lista desplegable se muestran todos los objetos de base de datos del tipo seleccionado para el argumento <strong>Tipo de objeto</strong>.  </span><span class="sxs-lookup"><span data-stu-id="df982-p102">Enter or select the specific object that contains the record to search for. The drop-down list shows all database objects of the type you selected for the <strong>Object Type</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df982-115"><strong>Registro</strong></span><span class="sxs-lookup"><span data-stu-id="df982-115"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="df982-116">Especifique el punto inicial y la dirección de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="df982-116">Specify the starting point and direction of the search.</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="df982-117">Configuración</span><span class="sxs-lookup"><span data-stu-id="df982-117">Setting</span></span></p></th>
<th><p><span data-ttu-id="df982-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="df982-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df982-119"><strong>Anterior</strong></span><span class="sxs-lookup"><span data-stu-id="df982-119"><strong>Previous</strong></span></span></p></td>
<td><p><span data-ttu-id="df982-120">Permite buscar hacia atrás a partir del actual registro.</span><span class="sxs-lookup"><span data-stu-id="df982-120">Search backward from the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df982-121"><strong>Siguiente</strong></span><span class="sxs-lookup"><span data-stu-id="df982-121"><strong>Next</strong></span></span></p></td>
<td><p><span data-ttu-id="df982-122">Permite buscar hacia delante a partir del actual registro.</span><span class="sxs-lookup"><span data-stu-id="df982-122">Search forward from the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df982-123"><strong>Primero</strong></span><span class="sxs-lookup"><span data-stu-id="df982-123"><strong>First</strong></span></span></p></td>
<td><p><span data-ttu-id="df982-p103">Permite buscar hacia delante a partir del primer registro. Es el valor predeterminado de este argumento.</span><span class="sxs-lookup"><span data-stu-id="df982-p103">Search forward from the first record. This is the default value for this argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df982-126"><strong>Último</strong></span><span class="sxs-lookup"><span data-stu-id="df982-126"><strong>Last</strong></span></span></p></td>
<td><p><span data-ttu-id="df982-127">Permite buscar hacia atrás a partir del último registro.</span><span class="sxs-lookup"><span data-stu-id="df982-127">Search backward from the last record.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df982-128"><strong>Condición WHERE</strong></span><span class="sxs-lookup"><span data-stu-id="df982-128"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="df982-129">Escriba los criterios para la búsqueda con la misma sintaxis que una SQL cláusula WHERE, solo sin la palabra &quot; WHERE &quot; .</span><span class="sxs-lookup"><span data-stu-id="df982-129">Enter the criteria for the search using the same syntax as an SQL WHERE clause, only without the word &quot;WHERE&quot;.</span></span> <span data-ttu-id="df982-130">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="df982-130">For example,</span></span></p>
<p>`Description = "Beverages"`</p>
<p><span data-ttu-id="df982-131">Para crear un criterio que incluya un valor de un cuadro de texto en un formulario, cree una expresión que concatene la primera parte del criterio con el nombre del cuadro de texto que contenga el valor que desee buscar.</span><span class="sxs-lookup"><span data-stu-id="df982-131">To create a criterion that includes a value from a text box on a form, you must create an expression that concatenates the first part of the criterion with the name of the text box containing the value for which to search.</span></span> <span data-ttu-id="df982-132">Por ejemplo, el siguiente criterio buscará en el campo denominado Descripción el valor del cuadro de texto denominado txtDescripción del formulario denominado frmCategorías.</span><span class="sxs-lookup"><span data-stu-id="df982-132">For example, the following criterion will search the Description field for the value in the text box named txtDescription on the form named frmCategories.</span></span> <span data-ttu-id="df982-133">Tenga en cuenta el signo igual ( ) al principio de la expresión y el uso de comillas simples ( ' ) a cada lado de la referencia <strong>=</strong> del cuadro de texto:<strong></strong></span><span class="sxs-lookup"><span data-stu-id="df982-133">Note the equal sign (<strong>=</strong>) at the beginning of the expression, and the use of single quotation marks (<strong>'</strong>) on either side of the text box reference:</span></span></p>
<p>`="Description = ' " & Forms![frmCategories]![txtDescription] & "'"`</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="df982-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="df982-134">Remarks</span></span>

- <span data-ttu-id="df982-135">En los casos en los que más de un registro coincida con los criterios del argumento **Condición Where**, los siguientes factores determinarán el registro encontrado:</span><span class="sxs-lookup"><span data-stu-id="df982-135">In cases where more than one record matches the criteria in the **Where Condition** argument, the following factors determine which record is found:</span></span>
    
  - <span data-ttu-id="df982-136">**El valor del argumento Registro** Vea la tabla que figura en la sección Valor para obtener más información sobre el argumento **Registro**.</span><span class="sxs-lookup"><span data-stu-id="df982-136">**The Record argument setting** See the table in the Settings section for more information about the **Record** argument.</span></span>
    
  - <span data-ttu-id="df982-137">**El criterio de ordenación de los registros** Por ejemplo, si el argumento **Registro** está establecido en **Primero**, un cambio del criterio de ordenación de los registros podría cambiar el registro que se va a encontrar.</span><span class="sxs-lookup"><span data-stu-id="df982-137">**The sort order of the records** For example, if the **Record** argument is set to **First**, changing the sort order of the records might change which record is found.</span></span>

- <span data-ttu-id="df982-p106">El objeto especificado en el argumento **Nombre del objeto** debe estar abierto antes de que se ejecute esta acción. En caso contrario, se genera un error.</span><span class="sxs-lookup"><span data-stu-id="df982-p106">The object specified in the **Object Name** argument must be open before this action is run. Otherwise, an error occurs.</span></span>

- <span data-ttu-id="df982-140">Si no se cumplen los criterios del argumento **Condición Where**, no se genera ningún error y el foco permanece en el actual registro.</span><span class="sxs-lookup"><span data-stu-id="df982-140">If the criteria in the **Where Condition** argument are not met, no error occurs and the focus remains on the current record.</span></span>

- <span data-ttu-id="df982-p107">Cuando se busca el registro anterior o siguiente, la búsqueda no se "ajusta" al alcanzar el final de los datos. Si no hay registros que cumplan los criterios, no se genera ningún error y el foco permanece en el actual registro. Para confirmar que se ha encontrado una coincidencia, se puede especificar una condición para la siguiente acción y equiparar la condición a los criterios del argumento **Condición Where**.</span><span class="sxs-lookup"><span data-stu-id="df982-p107">When searching for the previous or next record, the search does not "wrap" when it reaches the end of the data. If there are no further records that match the criteria, no error occurs and the focus remains on the current record. To confirm that a match was found, you can enter a condition for the next action, and make the condition the same as the criteria in the **Where Condition** argument.</span></span>

- <span data-ttu-id="df982-144">Para ejecutar la acción **EncontrarRegistro** en un módulo de VBA, use el método **SearchForRecord** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="df982-144">To run the **SearchForRecord** action in a VBA module, use the **SearchForRecord** method of the **DoCmd** object.</span></span>

- <span data-ttu-id="df982-p108">La acción **EncontrarRegistro** es similar a la acción **[BuscarRegistro](findrecord-macro-action.md)**, pero **EncontrarRegistro** tiene características de búsqueda más eficaces. La acción **BuscarRegistro** se usa principalmente para buscar cadenas y duplica la funcionalidad del cuadro de diálogo **Buscar**. La acción **EncontrarRegistro** usa criterios más similares a las de un filtro o una consulta SQL. En la siguiente lista se muestran algunas de las operaciones que se pueden realizar con la acción **EncontrarRegistro**:</span><span class="sxs-lookup"><span data-stu-id="df982-p108">The **SearchForRecord** action is similar to the **[FindRecord](findrecord-macro-action.md)** action, but **SearchForRecord** has more powerful search features. The **FindRecord** action is primarily used for finding strings, and it duplicates the functionality of the **Find** dialog box. The **SearchForRecord** action uses criteria that are more like those of a filter or an SQL query. The following list demonstrates some things you can do with the **SearchForRecord** action:</span></span>
    
  - <span data-ttu-id="df982-149">Se pueden usar criterios complejos en el argumento **Condición Where**, como</span><span class="sxs-lookup"><span data-stu-id="df982-149">You can use complex criteria in the **Where Condition** argument, such as</span></span>
        
    `Description = "Beverages" and CategoryID = 11`
    
  - <span data-ttu-id="df982-p109">Se puede hacer referencia a campos del origen de registros de un formulario o informe que no se muestran en el formulario o informe. En el ejemplo anterior, ni Description ni CategoryID pueden aparecer en el formulario o informe para que funcionen los criterios.</span><span class="sxs-lookup"><span data-stu-id="df982-p109">You can refer to fields that are in the record source of a form or report but aren't displayed on the form or report. In the preceding example, neither Description nor CategoryID must be displayed on the form or report for the criteria to work.</span></span>
    
  - <span data-ttu-id="df982-p110">Se pueden usar operadores lógicos, como **\<**, **\>**, **Y**, **O** y **ENTRE**. La acción **BuscarRegistro** sólo busca las cadenas que sean iguales, comiencen o contengan la cadena que se está buscando.</span><span class="sxs-lookup"><span data-stu-id="df982-p110">You can use logical operators, such as **\<**, **\>**, **AND**, **OR**, and **BETWEEN**. The **FindRecord** action only matches strings that equal, start with, or contain the string being searched for.</span></span>

## <a name="example"></a><span data-ttu-id="df982-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="df982-154">Example</span></span>

<span data-ttu-id="df982-p111">En la siguiente macro se abre primero la tabla Categorías mediante la acción **AbrirTabla**. A continuación, se usa la acción **EncontrarRegistro** para buscar el primer registro de la tabla donde el campo Descripción sea igual a "Bebidas".</span><span class="sxs-lookup"><span data-stu-id="df982-p111">The following macro first opens the Categories table by using the **OpenTable** action. The macro then uses the **SearchForRecord** action to find the first record in the table where the Description field equals "Beverages."</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="df982-157">Acción</span><span class="sxs-lookup"><span data-stu-id="df982-157">Action</span></span></p></th>
<th><p><span data-ttu-id="df982-158">Argumentos</span><span class="sxs-lookup"><span data-stu-id="df982-158">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df982-159"><strong>OpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="df982-159"><strong>OpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="df982-160"><strong>Nombre de tabla</strong>: Vista<strong>Categorías</strong>: <strong>Modo DatasheetData</strong>: <strong>Editar</strong></span><span class="sxs-lookup"><span data-stu-id="df982-160"><strong>Table Name</strong>: Categories<strong>View</strong>: <strong>DatasheetData Mode</strong>: <strong>Edit</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df982-161"><strong>SearchForRecord</strong></span><span class="sxs-lookup"><span data-stu-id="df982-161"><strong>SearchForRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="df982-162"><strong>Tipo de objeto</strong>: <strong>TableObject Name</strong>: Categories<strong>Record</strong>: <strong>FirstWhere Condition</strong>: Description = &quot; Beverages&quot;</span><span class="sxs-lookup"><span data-stu-id="df982-162"><strong>Object Type</strong>: <strong>TableObject Name</strong>: Categories<strong>Record</strong>: <strong>FirstWhere Condition</strong>: Description = &quot;Beverages&quot;</span></span></p></td>
</tr>
</tbody>
</table>

