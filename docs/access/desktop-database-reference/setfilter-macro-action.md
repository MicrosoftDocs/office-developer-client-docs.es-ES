---
title: EstablecerFiltro (acción de macro)
TOCTitle: SetFilter macro action
ms:assetid: dee699e2-0840-1612-23ce-199ef8d30566
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835438(v=office.15)
ms:contentKeyID: 48548203
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm122943
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ac1a2c8a603fb74b56d71f73605455ecdbc87035
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308697"
---
# <a name="setfilter-macro-action"></a><span data-ttu-id="3b36d-102">EstablecerFiltro (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="3b36d-102">SetFilter macro action</span></span>

<span data-ttu-id="3b36d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b36d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b36d-104">Puede utilizar la acción **EstablecerFiltro** para aplicar un filtro a los registros de la hoja de datos, formulario, informe o tabla que esté activo.</span><span class="sxs-lookup"><span data-stu-id="3b36d-104">You can use the **SetFilter** action to apply a filter to the records in the active datasheet, form, report, or table.</span></span>

## <a name="setting"></a><span data-ttu-id="3b36d-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="3b36d-105">Setting</span></span>

<span data-ttu-id="3b36d-106">La acción **EstablecerFiltro** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="3b36d-106">The **SetFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b36d-107">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="3b36d-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3b36d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b36d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b36d-109">Nombre del filtro</span><span class="sxs-lookup"><span data-stu-id="3b36d-109">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="3b36d-110">Si se proporciona, el nombre de una consulta o de un filtro guardado como consulta.</span><span class="sxs-lookup"><span data-stu-id="3b36d-110">If provided, the name of a query or of a filter saved as a query.</span></span> <span data-ttu-id="3b36d-111">Este argumento o el argumento CondiciónWhere es necesario en una base de datos cliente.</span><span class="sxs-lookup"><span data-stu-id="3b36d-111">This argument or the WhereCondition argument is required in a client database.</span></span> <span data-ttu-id="3b36d-112">En una base de datos Web, este argumento no está disponible.</span><span class="sxs-lookup"><span data-stu-id="3b36d-112">In a web database, this argument is not available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b36d-113">Condición WHERE</span><span class="sxs-lookup"><span data-stu-id="3b36d-113">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="3b36d-114">Si se proporciona, una cláusula WHERE de SQL que restringe los registros en la hoja de datos, formulario, informe o tabla.</span><span class="sxs-lookup"><span data-stu-id="3b36d-114">If provided, a SQL WHERE clause that restricts the records in the datasheet, form, report, or table.</span></span> <span data-ttu-id="3b36d-115">En una base de datos Web, este argumento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3b36d-115">In a web database, this argument is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b36d-116">Nombre del control</span><span class="sxs-lookup"><span data-stu-id="3b36d-116">Control Name</span></span></p></td>
<td><p><span data-ttu-id="3b36d-p103">Si se proporciona, es el nombre del control que corresponde al subformulario o subinforme que se va a filtrar. Si está vacío, se filtra el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="3b36d-p103">If provided, the name of the control that corresponds to the subform or subreport to be filtered. If empty, the current object is filtered.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3b36d-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3b36d-119">Remarks</span></span>

<span data-ttu-id="3b36d-120">En una base de datos web, el argumento Condición WHERE no puede empezar con un signo igual (=).</span><span class="sxs-lookup"><span data-stu-id="3b36d-120">In a web database, the Where Condition argument cannot begin with an equal sign (=).</span></span>

<span data-ttu-id="3b36d-121">Al ejecutar esta acción, el filtro se aplica a la tabla, formulario, informe u hoja de datos (por ejemplo, el resultado de consulta) que está activo y tiene el enfoque.</span><span class="sxs-lookup"><span data-stu-id="3b36d-121">When you run this action, the filter is applied to the table, form, report or datasheet (for example, query result) that is active and has the focus.</span></span>

<span data-ttu-id="3b36d-p104">La propiedad **Filtro** del objeto activo se utiliza para guardar el argumento CondiciónWhere y aplicarlo en un momento posterior. Los filtros se guardan con los objetos en los que se crean. Se cargan automáticamente cuando se abre el objeto, pero no se aplican automáticamente.</span><span class="sxs-lookup"><span data-stu-id="3b36d-p104">The **Filter** property of the active object is used to save the WhereCondition argument and apply it at a later time. Filters are saved with the objects in which they are created. They are automatically loaded when the object is opened, but they are not automatically applied.</span></span>

<span data-ttu-id="3b36d-125">En una base de datos cliente, para aplicar un filtro automáticamente cuando se abre el objeto, establezca la propiedad **FiltrarAlCargar** en Verdadero.</span><span class="sxs-lookup"><span data-stu-id="3b36d-125">In a client database, to automatically apply a filter when the object is opened, set the **FilterOnLoad** property to True.</span></span>

<span data-ttu-id="3b36d-126">En una base de datos web, para aplicar un filtro cuando se abre el objeto, agregue la acción **EstablecerFiltro** a una macro y agregue la macro al evento \*\*AlCargar \*\* del objeto.</span><span class="sxs-lookup"><span data-stu-id="3b36d-126">In a web database, to automatically apply a filter when the object is opened, add the **SetFilter** action to a macro, and add the macro to the object's **OnLoad** event.</span></span>

## <a name="example"></a><span data-ttu-id="3b36d-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3b36d-127">Example</span></span>

<span data-ttu-id="3b36d-128">En el siguiente ejemplo, se muestra cómo usar la acción SetFilter para filtrar el formulario en el que se define la macro.</span><span class="sxs-lookup"><span data-stu-id="3b36d-128">The following example shows how to use the SetFilter action to filter the form in which the macro is defined.</span></span>

<span data-ttu-id="3b36d-129">**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="3b36d-129">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    SetFilter
        Filter Name
        Where Condtion =[display_name] Like "*cheese*"
        Control Name
```
