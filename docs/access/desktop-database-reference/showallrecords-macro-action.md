---
title: MostrarTodosRegistros (acción de macro)
TOCTitle: ShowAllRecords macro action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 201b284a56fbd3030b41a95424b41c73ee13e385
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308648"
---
# <a name="showallrecords-macro-action"></a><span data-ttu-id="7612e-102">MostrarTodosRegistros (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="7612e-102">ShowAllRecords macro action</span></span>


<span data-ttu-id="7612e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7612e-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="7612e-104">Puede usar la acción **MostrarTodosRegistros** para quitar cualquier filtro aplicado de la tabla activa, el conjunto de resultados de la consulta o el formulario, y Mostrar todos los registros de la tabla o el conjunto de resultados o todos los registros de la tabla o consulta subyacente del formulario.</span><span class="sxs-lookup"><span data-stu-id="7612e-104">You can use the **ShowAllRecords** action to remove any applied filter from the active table, query result set, or form, and display all records in the table or result set or all records in the form's underlying table or query.</span></span>

## <a name="setting"></a><span data-ttu-id="7612e-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="7612e-105">Setting</span></span>

<span data-ttu-id="7612e-106">La acción **MostrarTodosRegistros** no tiene argumentos.</span><span class="sxs-lookup"><span data-stu-id="7612e-106">The **ShowAllRecords** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="7612e-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7612e-107">Remarks</span></span>

<span data-ttu-id="7612e-108">Puede usar esta acción para asegurarse de que todos los registros (incluidos los registros nuevos o modificados) se muestran para una tabla, un conjunto de resultados de una consulta o un formulario.</span><span class="sxs-lookup"><span data-stu-id="7612e-108">You can use this action to ensure that all records (including any changed or new records) are displayed for a table, query result set, or form.</span></span> <span data-ttu-id="7612e-109">Esta acción produce una nueva consulta de los registros de un formulario o subformulario.</span><span class="sxs-lookup"><span data-stu-id="7612e-109">This action causes a requery of the records for a form or subform.</span></span>

<span data-ttu-id="7612e-110">También puede usar esta acción para quitar cualquier filtro que se haya aplicado con la acción **AplicarFiltro** , el comando **filtrar** en la ficha **Inicio** o el argumento **nombre del filtro** o **Condición Where** de la acción **AbrirFormulario** .</span><span class="sxs-lookup"><span data-stu-id="7612e-110">You can also use this action to remove any filter that was applied with the **ApplyFilter** action, the **Filter** command on the **Home** tab, or the **Filter Name** or **Where Condition** argument of the **OpenForm** action.</span></span>

<span data-ttu-id="7612e-111">Esta acción tiene el mismo efecto que hacer clic en **alternar filtro** en la ficha **Inicio** o hacer clic con el botón secundario en el campo filtrado y hacer clic en **Borrar filtro de...** en la vista formulario, vista Diseño o vista Hoja de información.</span><span class="sxs-lookup"><span data-stu-id="7612e-111">This action has the same effect as clicking **Toggle Filter** on the **Home** tab, or right-clicking the filtered field and clicking **Clear filter from...** in Form view, Layout view, or Datasheet view.</span></span>

<span data-ttu-id="7612e-112">Para ejecutar la acción **MostrarTodosRegistros** en un módulo de Visual Basic para aplicaciones (VBA), use el método **ShowAllRecords** del objeto **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="7612e-112">To run the **ShowAllRecords** action in a Visual Basic for Applications (VBA) module, use the **ShowAllRecords** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="7612e-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7612e-113">Example</span></span>

<span data-ttu-id="7612e-114">**Aplicar un filtro con una macro**</span><span class="sxs-lookup"><span data-stu-id="7612e-114">**Apply a filter by using a macro**</span></span>

<span data-ttu-id="7612e-115">La siguiente macro contiene un conjunto de acciones, cada una de las cuales filtra los registros de un formulario de lista de teléfonos de clientes.</span><span class="sxs-lookup"><span data-stu-id="7612e-115">The following macro contains a set of actions, each of which filters the records for a Customer Phone List form.</span></span> <span data-ttu-id="7612e-116">Muestra el uso de las acciones **AplicarFiltro**, **MostrarTodosRegistros**e **IrAControl** .</span><span class="sxs-lookup"><span data-stu-id="7612e-116">It shows the use of the **ApplyFilter**, **ShowAllRecords**, and **GoToControl** actions.</span></span> <span data-ttu-id="7612e-117">También muestra el uso de condiciones para determinar qué botón de alternancia de un grupo de opciones se ha seleccionado en el formulario.</span><span class="sxs-lookup"><span data-stu-id="7612e-117">It also shows the use of conditions to determine which toggle button in an option group has been selected on the form.</span></span> <span data-ttu-id="7612e-118">Cada fila de acción se asocia a un botón de alternancia que selecciona el conjunto de registros que comienzan con A, B, C, etc. o todos los registros.</span><span class="sxs-lookup"><span data-stu-id="7612e-118">Each action row is associated with a toggle button that selects the set of records starting with A, B, C, and so on, or all records.</span></span> <span data-ttu-id="7612e-119">Esta macro se debe adjuntar al evento **AfterUpdate** del grupo de opciones CompanyNameFilter.</span><span class="sxs-lookup"><span data-stu-id="7612e-119">This macro should be attached to the **AfterUpdate** event of the CompanyNameFilter option group.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7612e-120">Condición</span><span class="sxs-lookup"><span data-stu-id="7612e-120">Condition</span></span></p></th>
<th><p><span data-ttu-id="7612e-121">Acción</span><span class="sxs-lookup"><span data-stu-id="7612e-121">Action</span></span></p></th>
<th><p><span data-ttu-id="7612e-122">Argumentos: Configuración</span><span class="sxs-lookup"><span data-stu-id="7612e-122">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="7612e-123">Comment</span><span class="sxs-lookup"><span data-stu-id="7612e-123">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7612e-124">[Filtros de nombre de la compañía] = 1</span><span class="sxs-lookup"><span data-stu-id="7612e-124">[Company Name Filters] =1</span></span></p></td>
<td><p><span data-ttu-id="7612e-125"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="7612e-125"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="7612e-126"><strong>Condición Where</strong>: [nombre de la compañía &quot;] like [AÀÁÂÃÄ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="7612e-126"><strong>Where Condition</strong>: [Company Name] Like &quot;[AÀÁÂÃÄ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="7612e-127">Filtrar por nombres de compañías que empiecen por A, À, Á, Â, Ã o Ä.</span><span class="sxs-lookup"><span data-stu-id="7612e-127">Filter for company names that start with A, À, Á, Â, Ã, or Ä.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7612e-128">[Filtros de nombre de compañía] = 2</span><span class="sxs-lookup"><span data-stu-id="7612e-128">[Company Name Filters] =2</span></span></p></td>
<td><p><span data-ttu-id="7612e-129"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="7612e-129"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="7612e-130"><strong>Condición Where</strong>: [nombre de la compañía &quot;] like B \*&quot;</span><span class="sxs-lookup"><span data-stu-id="7612e-130"><strong>Where Condition</strong>: [Company Name] Like &quot;B\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="7612e-131">Filtrar por nombres de compañías que empiecen por B.</span><span class="sxs-lookup"><span data-stu-id="7612e-131">Filter for company names that start with B.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7612e-132">[Filtros de nombre de la compañía] = 3</span><span class="sxs-lookup"><span data-stu-id="7612e-132">[Company Name Filters] =3</span></span></p></td>
<td><p><span data-ttu-id="7612e-133"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="7612e-133"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="7612e-134"><strong>Condición Where</strong>: [nombre de la compañía &quot;] like [cç] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="7612e-134"><strong>Where Condition</strong>: [Company Name] Like &quot;[CÇ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="7612e-135">Filtrar por nombres de compañías que empiecen por C o Ç.</span><span class="sxs-lookup"><span data-stu-id="7612e-135">Filter for company names that start with C or Ç.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7612e-136">... Las filas de acción de la D a la Y tienen el mismo formato que a hasta C...</span><span class="sxs-lookup"><span data-stu-id="7612e-136">... Action rows for D through Y have the same format as A through C ...</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7612e-137">[Filtros de nombre de compañía] = 26</span><span class="sxs-lookup"><span data-stu-id="7612e-137">[Company Name Filters] =26</span></span></p></td>
<td><p><span data-ttu-id="7612e-138"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="7612e-138"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="7612e-139"><strong>Condición Where</strong>: [nombre de la compañía &quot;] like [ZÆØÅ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="7612e-139"><strong>Where Condition</strong>: [Company Name] Like &quot;[ZÆØÅ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="7612e-140">Filtrar por nombres de compañías que empiecen por Z, Æ, Ø o Å.</span><span class="sxs-lookup"><span data-stu-id="7612e-140">Filter for company names that start with Z, Æ, Ø, or Å.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7612e-141">[Filtros de nombre de la compañía] = 27</span><span class="sxs-lookup"><span data-stu-id="7612e-141">[Company Name Filters] =27</span></span></p></td>
<td><p><span data-ttu-id="7612e-142"><strong>ShowAllRecords</strong></span><span class="sxs-lookup"><span data-stu-id="7612e-142"><strong>ShowAllRecords</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7612e-143">Mostrar todos los registros.</span><span class="sxs-lookup"><span data-stu-id="7612e-143">Show all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7612e-144">[RecordsetClone]. RecordCount &gt;0</span><span class="sxs-lookup"><span data-stu-id="7612e-144">[RecordsetClone].[RecordCount]&gt;0</span></span></p></td>
<td><p><span data-ttu-id="7612e-145"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="7612e-145"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="7612e-146"><strong>Nombre del control</strong>: NombreDeEmpresa</span><span class="sxs-lookup"><span data-stu-id="7612e-146"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="7612e-147">Si se devuelven registros para la carta seleccionada, desplace el foco al control CompanyName.</span><span class="sxs-lookup"><span data-stu-id="7612e-147">If records are returned for the selected letter, move focus to the CompanyName control.</span></span></p></td>
</tr>
</tbody>
</table>

