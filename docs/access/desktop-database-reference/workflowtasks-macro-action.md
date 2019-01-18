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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721860"
---
# <a name="workflowtasks-macro-action"></a><span data-ttu-id="4442c-102">TareasFlujoTrabajo (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="4442c-102">WorkflowTasks macro action</span></span>


<span data-ttu-id="4442c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4442c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4442c-104">Puede usar la acción **TareasFlujoTrabajo** para mostrar el cuadro de diálogo **Tarea de flujo de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="4442c-104">You can use the **WorkflowTasks** action to display the **Workflow Task** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="4442c-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="4442c-105">Setting</span></span>

<span data-ttu-id="4442c-106">La acción **TareasFlujoTrabajo** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="4442c-106">The **WorkflowTasks** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4442c-107">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="4442c-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4442c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4442c-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4442c-109"><strong>Número de registro</strong></span><span class="sxs-lookup"><span data-stu-id="4442c-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="4442c-110">La posición del elemento en la lista de Microsoft SharePoint Foundation, comenzando por <strong>1</strong> para el primer elemento de la lista, <strong>2</strong> para el segundo elemento, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="4442c-110">The position of the item in the Microsoft SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="4442c-111">También puede escribir una expresión para este argumento.</span><span class="sxs-lookup"><span data-stu-id="4442c-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4442c-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4442c-112">Remarks</span></span>

  - <span data-ttu-id="4442c-p102">La acción **TareasFlujoTrabajo** abre el cuadro de diálogo **Tareas de flujo de trabajo**. Este cuadro de diálogo muestra todas las tareas que están disponibles para el elemento especificado. Se debe definir un flujo de trabajo para la lista en SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="4442c-p102">The **WorkflowTasks** action opens the **Workflow Tasks** dialog box. This dialog box displays all tasks that are available for the specified item. A workflow must be defined for the list in SharePoint Foundation.</span></span>

  - <span data-ttu-id="4442c-p103">La acción **TareasFlujoTrabajo** solo se puede utilizar después de que se haya abierto y seleccionado una lista vinculada de SharePoint Foundation. Para abrir y seleccionar la lista vinculada, utilice la acción **AbrirTabla**. Si la lista ya está abierta, utilice la acción **SeleccionarObjeto** para seleccionarla.</span><span class="sxs-lookup"><span data-stu-id="4442c-p103">The **WorkflowTasks** action can only be used after a linked SharePoint Foundation list has been opened and selected. To open and select the linked list, use the **OpenTable** action. If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="4442c-119">La acción **TareasFlujoTrabajo** tiene el mismo efecto que hacer clic con el botón secundario en cualquier celda en una lista SharePoint Foundation vinculada mientras está abierta en la vista de hoja de datos, ir a **Flujo de trabajo** y hacer clic en **Tareas de flujo de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="4442c-119">The **WorkflowTasks** action has the same effect as right-clicking any cell in a linked SharePoint Foundation list while it is open in datasheet view, pointing to **Workflow**, and then clicking **Workflow Tasks**.</span></span>

  - <span data-ttu-id="4442c-120">Para ejecutar la acción **TareasFlujoTrabajo** en un módulo de VBA, utilice el método **WorkflowTasks** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="4442c-120">To run the **WorkflowTasks** action in a VBA module, use the **WorkflowTasks** method of the **DoCmd** object.</span></span>

