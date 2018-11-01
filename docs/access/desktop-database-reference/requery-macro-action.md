---
title: NuevaConsulta (acción de macro)
TOCTitle: Requery Macro Action
ms:assetid: 6dbdcae5-81b6-9925-4cad-64b178c23060
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195544(v=office.15)
ms:contentKeyID: 48545499
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm30402
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e8e5a25b8770f3542fade53d206ff20400ebf350
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885944"
---
# <a name="requery-macro-action"></a><span data-ttu-id="f8e58-102">NuevaConsulta (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="f8e58-102">Requery Macro Action</span></span>


<span data-ttu-id="f8e58-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8e58-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f8e58-p101">Puede usar la acción **NuevaConsulta** para actualizar los datos de un control especificado del objeto activo consultando de nuevo el origen del control. Si no se especifica ningún control, con esta acción se vuelve a consultar el origen del propio objeto. Utilice esta acción para asegurarse de que el objeto activo o uno de sus controles muestra los datos más actualizados.</span><span class="sxs-lookup"><span data-stu-id="f8e58-p101">You can use the **Requery** action to update the data in a specified control on the active object by requerying the source of the control. If no control is specified, this action requeries the source of the object itself. Use this action to ensure that the active object or one of its controls displays the most current data.</span></span>

## <a name="setting"></a><span data-ttu-id="f8e58-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="f8e58-107">Setting</span></span>

<span data-ttu-id="f8e58-108">La acción **NuevaConsulta** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="f8e58-108">The **Requery** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f8e58-109">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="f8e58-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f8e58-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8e58-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8e58-111"><strong>Nombre del control</strong></span><span class="sxs-lookup"><span data-stu-id="f8e58-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e58-p102">Nombre del control que se desea actualizar. Escriba el nombre del control en el cuadro <strong>Nombre del control</strong> de la sección <strong>Argumentos de acción</strong> en el panel Generador de macros. Sólo debe utilizar el nombre del control y no el identificador completo (como <strong>Formularios</strong>!<em>nombreDelFormulario</em>!<em>nombreDelControl</em>). Deje este argumento en blanco para consultar de nuevo el origen del objeto activo. Si el objeto activo es una hoja de datos o un conjunto de resultados de una consulta, debe dejar este argumento en blanco.</span><span class="sxs-lookup"><span data-stu-id="f8e58-p102">The name of the control you want to update. Enter the control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You should use only the name of the control, not the fully qualified identifier (such as <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>). Leave this argument blank to requery the source of the active object. If the active object is a datasheet or a query result set, you must leave this argument blank.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f8e58-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8e58-117">Remarks</span></span>

<span data-ttu-id="f8e58-118">La acción **NuevaConsulta** realiza alguna de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="f8e58-118">The **Requery** action does one of the following:</span></span>

  - <span data-ttu-id="f8e58-119">Ejecuta de nuevo la consulta en la que está basada el control o el objeto.</span><span class="sxs-lookup"><span data-stu-id="f8e58-119">Reruns the query on which the control or object is based.</span></span>

  - <span data-ttu-id="f8e58-120">Presenta cualquier registro nuevo o modificado y quita cualquier registro eliminado de la tabla en la que está basado el control o el objeto.</span><span class="sxs-lookup"><span data-stu-id="f8e58-120">Displays any new or changed records, and removes any deleted records from the table on which the control or object is based.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f8e58-121">[!NOTA] La acción <STRONG>NuevaConsulta</STRONG> no afecta a la posición del puntero de registro.</span><span class="sxs-lookup"><span data-stu-id="f8e58-121">The <STRONG>Requery</STRONG> action does not affect the position of the record pointer.</span></span></P>



<span data-ttu-id="f8e58-122">Los controles basados en una consulta o tabla son:</span><span class="sxs-lookup"><span data-stu-id="f8e58-122">Controls based on a query or table include:</span></span>

  - <span data-ttu-id="f8e58-123">Cuadros de lista y cuadros combinados.</span><span class="sxs-lookup"><span data-stu-id="f8e58-123">List boxes and combo boxes.</span></span>

  - <span data-ttu-id="f8e58-124">Controles de subformulario.</span><span class="sxs-lookup"><span data-stu-id="f8e58-124">Subform controls.</span></span>

  - <span data-ttu-id="f8e58-125">Objetos OLE, por ejemplo, gráficos.</span><span class="sxs-lookup"><span data-stu-id="f8e58-125">OLE objects, such as charts.</span></span>

  - <span data-ttu-id="f8e58-126">Controles que contienen funciones de agregado de dominio, como **DSuma**.</span><span class="sxs-lookup"><span data-stu-id="f8e58-126">Controls containing domain aggregate functions, such as **DSum**.</span></span>

<span data-ttu-id="f8e58-127">Si el control especificado no está basado en una consulta o tabla, esta acción hace que se vuelva a calcular el control.</span><span class="sxs-lookup"><span data-stu-id="f8e58-127">If the specified control isn't based on a query or table, this action forces a recalculation of the control.</span></span>

<span data-ttu-id="f8e58-p103">Si deja en blanco el argumento **Nombre del control**, la acción **NuevaConsulta** tiene el mismo efecto que presionar MAYÚS+F9 cuando el objeto tiene el enfoque. Si un control de subformulario tiene el enfoque, esta acción vuelve a consultar sólo el origen del subformulario (al igual que cuando se presionan MAYÚS+F9).</span><span class="sxs-lookup"><span data-stu-id="f8e58-p103">If you leave the **Control Name** argument blank, the **Requery** action has the same effect as pressing SHIFT+F9 when the object has the focus. If a subform control has the focus, this action requeries only the source of the subform (just as pressing SHIFT+F9 does).</span></span>


> [!NOTE]
> <P><span data-ttu-id="f8e58-p104">[!NOTA] La acción <STRONG>NuevaConsulta</STRONG> vuelve a consultar el origen del control u objeto. En cambio, la acción <STRONG>RepintarObjeto</STRONG> vuelve a pintar los controles del objeto especificado pero no vuelve a consultar la base de datos ni muestra los nuevos registros. La acción <STRONG>MostrarTodosRegistros</STRONG> no sólo vuelve a consultar el objeto activo sino que también quita todos los filtros que se hayan aplicado, a diferencia de la acción <STRONG>NuevaConsulta</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f8e58-p104">The <STRONG>Requery</STRONG> action requeries the source of the control or object. In contrast, the <STRONG>RepaintObject</STRONG> action repaints controls in the specified object but doesn't requery the database or display new records. The <STRONG>ShowAllRecords</STRONG> action not only requeries the active object, but it also removes any applied filters, which the <STRONG>Requery</STRONG> action doesn't do.</span></span></P>



<span data-ttu-id="f8e58-p105">Si desea volver a consultar un control que no esté en el objeto activo, deberá utilizar el método **Requery** en un módulo de Visual Basic para Aplicaciones (VBA), en lugar de la acción **NuevaConsulta** o su correspondiente método **Requery** del objeto **DoCmd**. El método **Requery** en VBA es más rápido que la acción **NuevaConsulta** o el método **DoCmd.Requery**. Además, cuando se utiliza la acción **NuevaConsulta** o el método **DoCmd.Requery**, Microsoft Access cierra la consulta y vuelve a cargarla desde la base de datos, pero cuando se utiliza el método **Requery**, Access ejecuta de nuevo la consulta sin cerrarla ni cargarla. Observe que el método **Requery** de ActiveX Data Object (ADO) funciona de la misma manera que el método **Requery** de Access.</span><span class="sxs-lookup"><span data-stu-id="f8e58-p105">If you want to requery a control that isn't on the active object, you must use the **Requery** method in a Visual Basic for Applications (VBA) module, not the **Requery** action or its corresponding **Requery** method of the **DoCmd** object. The **Requery** method in VBA is faster than the **Requery** action or the **DoCmd.Requery** method. In addition, when you use the **Requery** action or the **DoCmd.Requery** method, Microsoft Access closes the query and reloads it from the database, but when you use the **Requery** method, Access reruns the query without closing and reloading it. Note that the ActiveX Data Object (ADO) **Requery** method works the same way as the Access **Requery** method.</span></span>

