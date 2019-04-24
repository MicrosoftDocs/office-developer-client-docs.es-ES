---
title: TareasFlujoTrabajo (acción de macro)
TOCTitle: WorkflowTasks macro action
ms:assetid: 4b299681-b45b-f6d1-2cfe-ebf01712bfc1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193503(v=office.15)
ms:contentKeyID: 48544684
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm8454
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 921396edd480e06194d1c3dcbb683aa8556553e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306009"
---
# <a name="workflowtasks-macro-action"></a>TareasFlujoTrabajo (acción de macro)


**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **TareasFlujoTrabajo** para mostrar el cuadro de diálogo **Tarea de flujo de trabajo**.

## <a name="setting"></a>Configuración

La acción **TareasFlujoTrabajo** tiene el siguiente argumento.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de la acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Número de registro</strong></p></td>
<td><p>La posición del elemento en la lista de Microsoft SharePoint Foundation, empezando por <strong>1</strong> para el primer elemento de la lista, <strong>2</strong> para el segundo elemento, etc. También puede escribir una expresión para este argumento.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

  - La acción **TareasFlujoTrabajo** abre el cuadro de diálogo **Tareas de flujo de trabajo**. Este cuadro de diálogo muestra todas las tareas que están disponibles para el elemento especificado. Se debe definir un flujo de trabajo para la lista en SharePoint Foundation.

  - La acción **TareasFlujoTrabajo** solo se puede utilizar después de que se haya abierto y seleccionado una lista vinculada de SharePoint Foundation. Para abrir y seleccionar la lista vinculada, utilice la acción **AbrirTabla**. Si la lista ya está abierta, utilice la acción **SeleccionarObjeto** para seleccionarla.

  - La acción **TareasFlujoTrabajo** tiene el mismo efecto que hacer clic con el botón secundario en cualquier celda en una lista SharePoint Foundation vinculada mientras está abierta en la vista de hoja de datos, ir a **Flujo de trabajo** y hacer clic en **Tareas de flujo de trabajo**.

  - Para ejecutar la acción **TareasFlujoTrabajo** en un módulo de VBA, utilice el método **WorkflowTasks** del objeto **DoCmd**.

