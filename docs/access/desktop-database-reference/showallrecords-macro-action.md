---
title: MostrarTodosRegistros (acción de macro)
TOCTitle: ShowAllRecords macro action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c4ea531de8c5b99c9ff85eacddcc79a596caebd5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922044"
---
# <a name="showallrecords-macro-action"></a><span data-ttu-id="3d811-102">MostrarTodosRegistros (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="3d811-102">ShowAllRecords macro action</span></span>


<span data-ttu-id="3d811-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d811-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="3d811-104">Puede utilizar la acción **MostrarTodosRegistros** para quitar cualquier filtro aplicado de la tabla activa, conjunto de resultados de consulta o formulario y mostrar todos los registros en la tabla o conjunto de resultados o todos los registros en el formulario de la tabla o consulta base.</span><span class="sxs-lookup"><span data-stu-id="3d811-104">You can use the **ShowAllRecords** action to remove any applied filter from the active table, query result set, or form, and display all records in the table or result set or all records in the form's underlying table or query.</span></span>

## <a name="setting"></a><span data-ttu-id="3d811-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="3d811-105">Setting</span></span>

<span data-ttu-id="3d811-106">La acción **MostrarTodosRegistros** no tiene ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="3d811-106">The **ShowAllRecords** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d811-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3d811-107">Remarks</span></span>

<span data-ttu-id="3d811-108">Puede usar esta acción para asegurarse de que se muestran todos los registros (incluidos los registros nuevos o modificados) de una tabla, un conjunto de resultados de consulta o un formulario.</span><span class="sxs-lookup"><span data-stu-id="3d811-108">You can use this action to ensure that all records (including any changed or new records) are displayed for a table, query result set, or form.</span></span> <span data-ttu-id="3d811-109">Esta acción realiza una nueva consulta de los registros de un formulario o subformulario.</span><span class="sxs-lookup"><span data-stu-id="3d811-109">This action causes a requery of the records for a form or subform.</span></span>

<span data-ttu-id="3d811-110">También puede usar esta acción para quitar cualquier filtro que se ha aplicado con la acción **AplicarFiltro** , el comando de **filtro** en la ficha **Inicio** , o el **Nombre del filtro** o el argumento **Condición Where** de la acción **AbrirFormulario** .</span><span class="sxs-lookup"><span data-stu-id="3d811-110">You can also use this action to remove any filter that was applied with the **ApplyFilter** action, the **Filter** command on the **Home** tab, or the **Filter Name** or **Where Condition** argument of the **OpenForm** action.</span></span>

<span data-ttu-id="3d811-111">Esta acción tiene el mismo efecto que hacer clic en **Alternar filtro** en la ficha **Inicio** , o bien el campo filtrado y haciendo clic en **Quitar filtro de...** en la vista formulario, vista Diseño o vista Hoja de datos.</span><span class="sxs-lookup"><span data-stu-id="3d811-111">This action has the same effect as clicking **Toggle Filter** on the **Home** tab, or right-clicking the filtered field and clicking **Clear filter from...** in Form view, Layout view, or Datasheet view.</span></span>

<span data-ttu-id="3d811-112">Para ejecutar la acción **MostrarTodosRegistros** en un módulo Visual Basic para aplicaciones (VBA), use el método **ShowAllRecords** del objeto **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="3d811-112">To run the **ShowAllRecords** action in a Visual Basic for Applications (VBA) module, use the **ShowAllRecords** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="3d811-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d811-113">Example</span></span>

<span data-ttu-id="3d811-114">**Aplicar un filtro con una macro**</span><span class="sxs-lookup"><span data-stu-id="3d811-114">**Apply a filter by using a macro**</span></span>

<span data-ttu-id="3d811-p102">La siguiente macro contiene un conjunto de acciones, cada una de las cuales filtra los registros para un formulario Lista de teléfonos de clientes. La macro muestra el uso de las acciones **AplicarFiltro**, **MostrarTodosRegistros** e **IrAControl**. También muestra el uso de condiciones para determinar qué botón de alternar en un grupo de opciones se seleccionó en el formulario. Cada fila de acción está asociada con un botón de alternar que selecciona el conjunto de registros que comienzan con A, B, C, y así sucesivamente. Esta macro se debe adjuntar al evento **DespuésDeActualizar** del grupo de opción FiltroNombreCompañía.</span><span class="sxs-lookup"><span data-stu-id="3d811-p102">The following macro contains a set of actions, each of which filters the records for a Customer Phone List form. It shows the use of the **ApplyFilter**, **ShowAllRecords**, and **GoToControl** actions. It also shows the use of conditions to determine which toggle button in an option group has been selected on the form. Each action row is associated with a toggle button that selects the set of records starting with A, B, C, and so on, or all records. This macro should be attached to the **AfterUpdate** event of the CompanyNameFilter option group.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d811-120">Condición</span><span class="sxs-lookup"><span data-stu-id="3d811-120">Condition</span></span></p></th>
<th><p><span data-ttu-id="3d811-121">Acción</span><span class="sxs-lookup"><span data-stu-id="3d811-121">Action</span></span></p></th>
<th><p><span data-ttu-id="3d811-122">Argumentos: Configuración</span><span class="sxs-lookup"><span data-stu-id="3d811-122">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="3d811-123">Comentario</span><span class="sxs-lookup"><span data-stu-id="3d811-123">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d811-124">[Filtros de nombres de compañía] = 1</span><span class="sxs-lookup"><span data-stu-id="3d811-124">[Company Name Filters] =1</span></span></p></td>
<td><p><span data-ttu-id="3d811-125"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="3d811-125"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="3d811-126"><strong>Condición WHERE</strong>: [nombre de compañía] como &quot;[AÀÁÂÃÄ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="3d811-126"><strong>Where Condition</strong>: [Company Name] Like &quot;[AÀÁÂÃÄ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="3d811-127">Filtrar por nombres de compañías que comienzan con A, À, Á, Â, Ã o Ä.</span><span class="sxs-lookup"><span data-stu-id="3d811-127">Filter for company names that start with A, À, Á, Â, Ã, or Ä.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d811-128">[Filtros de nombres de compañía] = 2</span><span class="sxs-lookup"><span data-stu-id="3d811-128">[Company Name Filters] =2</span></span></p></td>
<td><p><span data-ttu-id="3d811-129"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="3d811-129"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="3d811-130"><strong>Condición WHERE</strong>: [nombre de compañía] como &quot;B \*&quot;</span><span class="sxs-lookup"><span data-stu-id="3d811-130"><strong>Where Condition</strong>: [Company Name] Like &quot;B\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="3d811-131">Filtrar por nombres de compañías que empiecen con B.</span><span class="sxs-lookup"><span data-stu-id="3d811-131">Filter for company names that start with B.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d811-132">[Filtros de nombres de compañía] = 3</span><span class="sxs-lookup"><span data-stu-id="3d811-132">[Company Name Filters] =3</span></span></p></td>
<td><p><span data-ttu-id="3d811-133"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="3d811-133"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="3d811-134"><strong>Condición WHERE</strong>: [nombre de compañía] como &quot;[CÇ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="3d811-134"><strong>Where Condition</strong>: [Company Name] Like &quot;[CÇ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="3d811-135">Filtrar por nombres de compañía que empiecen por C o Ç.</span><span class="sxs-lookup"><span data-stu-id="3d811-135">Filter for company names that start with C or Ç.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d811-136">... Las filas de acciones de la D a la Y tienen el mismo formato que las de la A a la C ...</span><span class="sxs-lookup"><span data-stu-id="3d811-136">... Action rows for D through Y have the same format as A through C ...</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d811-137">[Filtros de nombres de compañía] = 26</span><span class="sxs-lookup"><span data-stu-id="3d811-137">[Company Name Filters] =26</span></span></p></td>
<td><p><span data-ttu-id="3d811-138"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="3d811-138"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="3d811-139"><strong>Condición WHERE</strong>: [nombre de compañía] como &quot;[ZÆØÅ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="3d811-139"><strong>Where Condition</strong>: [Company Name] Like &quot;[ZÆØÅ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="3d811-140">Filtrar por nombres de compañías que empiecen por Z, Æ, Ø o Å.</span><span class="sxs-lookup"><span data-stu-id="3d811-140">Filter for company names that start with Z, Æ, Ø, or Å.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d811-141">[Filtros de nombres de compañía] = 27</span><span class="sxs-lookup"><span data-stu-id="3d811-141">[Company Name Filters] =27</span></span></p></td>
<td><p><span data-ttu-id="3d811-142"><strong>ShowAllRecords</strong></span><span class="sxs-lookup"><span data-stu-id="3d811-142"><strong>ShowAllRecords</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3d811-143">Mostrar todos los registros.</span><span class="sxs-lookup"><span data-stu-id="3d811-143">Show all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d811-144">[RecordsetClone]. [RecordCount] &gt;0</span><span class="sxs-lookup"><span data-stu-id="3d811-144">[RecordsetClone].[RecordCount]&gt;0</span></span></p></td>
<td><p><span data-ttu-id="3d811-145"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="3d811-145"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="3d811-146"><strong>Nombre del control</strong>: NombreDeEmpresa</span><span class="sxs-lookup"><span data-stu-id="3d811-146"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="3d811-147">Si se devuelven registros para la letra seleccionada, mueve el enfoque al control NombreCompañía.</span><span class="sxs-lookup"><span data-stu-id="3d811-147">If records are returned for the selected letter, move focus to the CompanyName control.</span></span></p></td>
</tr>
</tbody>
</table>

