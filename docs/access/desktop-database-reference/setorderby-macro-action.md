---
title: ConfigurarOrdenarPor (acción de macro)
TOCTitle: SetOrderBy Macro Action
ms:assetid: 78f65ce9-b56f-f476-3bd6-f3307bc22a08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196152(v=office.15)
ms:contentKeyID: 48545765
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98639
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ac911110d313243879d6dff993061d58c208cd34
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876221"
---
# <a name="setorderby-macro-action"></a><span data-ttu-id="a03c6-102">ConfigurarOrdenarPor (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="a03c6-102">SetOrderBy Macro Action</span></span>


<span data-ttu-id="a03c6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a03c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a03c6-104">Puede utilizar la acción **ConfigurarOrdenarPor** para especificar cómo desea ordenar los registros en un formulario, informe, tabla o resultado de consulta.</span><span class="sxs-lookup"><span data-stu-id="a03c6-104">You can use the **SetOrderBy** action to specify how you want to sort records in a form, report, table, or query result.</span></span>

## <a name="setting"></a><span data-ttu-id="a03c6-105">Valores</span><span class="sxs-lookup"><span data-stu-id="a03c6-105">Setting</span></span>

<span data-ttu-id="a03c6-106">La acción **ConfigurarOrdenarPor** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="a03c6-106">The **SetOrderBy** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a03c6-107">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="a03c6-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a03c6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a03c6-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a03c6-109"><strong>Ordenar por</strong></span><span class="sxs-lookup"><span data-stu-id="a03c6-109"><strong>Order By</strong></span></span></p></td>
<td><p><span data-ttu-id="a03c6-110">Una expresión de cadena que incluye el nombre del campo o campos en los que se van a ordenar los registros y las palabras clave ASC o DESC opcionales.</span><span class="sxs-lookup"><span data-stu-id="a03c6-110">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a03c6-111"><strong>Nombre del control</strong></span><span class="sxs-lookup"><span data-stu-id="a03c6-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="a03c6-p101">Si se proporciona y el objeto activo es un formulario o informe, es el nombre del control que corresponde al subformulario o subinforme que se va a ordenar. Si está vacío y el objeto activo es un formulario o informe, el formulario o el informe primario se ordena.</span><span class="sxs-lookup"><span data-stu-id="a03c6-p101">If provided and the active object is a form or report, the name of the control that corresponds to the subform or subreport that will be sorted. If empty and the active object is a form or report, the parent form or report is sorted..</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a03c6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a03c6-114">Remarks</span></span>

<span data-ttu-id="a03c6-115">Al ejecutar esta acción de macro, la ordenación se aplica a la tabla, formulario, informe u hoja de datos (resultado de consulta) que está activo y tiene el enfoque.</span><span class="sxs-lookup"><span data-stu-id="a03c6-115">When you run this macro action, the sort is applied to the table, form, report or datasheet (query result) that is active and has the focus.</span></span>

<span data-ttu-id="a03c6-p102">El argumento OrdenarPor es el nombre del campo o los campos por los que desea ordenar los registros. Cuando utilice más de un nombre de campo, separe los nombres con una coma (,). La propiedad **OrdenarPor** del objeto activo se utiliza para guardar el valor de orden y aplicarlo en un momento posterior. Los valores de OrdenarPor se guardan con los objetos en los que se crean. Se cargan automáticamente cuando se abre el objeto, pero no se aplican automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a03c6-p102">The Order By argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,). The **OrderBy** property of the active object is used to save the ordering value and apply it at a later time. OrderBy values are saved with the objects in which they are created. They are automatically loaded when the object is opened, but they aren't automatically applied.</span></span>

<span data-ttu-id="a03c6-121">Si se establece el argumento OrdenarPor especificando uno o más nombres de campo y ejecutando la macro a continuación, los registros se ordenan en orden ascendente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a03c6-121">When you set the Order By argument by entering one or more field names and then run the macro, the records are sorted by default in ascending order.</span></span>

<span data-ttu-id="a03c6-p103">Para ordenar los registros en orden descendente, escriba DESC al final de la expresión de argumento Ordenar Por. Por ejemplo, para ordenar los registros de clientes en orden descendente por nombre de contacto, establezca el argumento Ordenar Por en "NombreDeContacto DESC". Para ordenar los nombres de forma descendente por Apellido y de forma ascendente por Nombre, establezca el argumento Ordenar Por en "Apellido DESC, Nombre ASC".</span><span class="sxs-lookup"><span data-stu-id="a03c6-p103">To sort records in descending order, type DESC at the end of the Order By argument expression. For example, to sort customer records in descending order by contact name, set the Order By argument to "ContactName DESC". To sort names by LastName descending, and FirstName ascending, set the Order By argument to "LastName DESC, FirstName ASC".</span></span>

