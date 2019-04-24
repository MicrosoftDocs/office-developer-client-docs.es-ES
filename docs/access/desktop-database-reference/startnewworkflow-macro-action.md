---
title: IniciarNuevoFlujoDeTrabajo (acción de macro)
TOCTitle: StartNewWorkflow macro action
ms:assetid: b3e81a11-b816-0eef-fc70-6d6da7a5a845
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822054(v=office.15)
ms:contentKeyID: 48547206
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm198223
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1e37d72754531fc4dd51427eefb355a057d08073
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306401"
---
# <a name="startnewworkflow-macro-action"></a><span data-ttu-id="edbfe-102">IniciarNuevoFlujoDeTrabajo (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="edbfe-102">StartNewWorkflow macro action</span></span>


<span data-ttu-id="edbfe-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="edbfe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="edbfe-104">Puede usar la acción **IniciarNuevoFlujoDeTrabajo** para iniciar un nuevo flujo de trabajo para un elemento en una lista de Microsoft SharePoint Foundation vinculada.</span><span class="sxs-lookup"><span data-stu-id="edbfe-104">You can use the **StartNewWorkflow** action to start a new workflow for an item in a linked Microsoft SharePoint Foundation list.</span></span>

## <a name="setting"></a><span data-ttu-id="edbfe-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="edbfe-105">Setting</span></span>

<span data-ttu-id="edbfe-106">La acción **IniciarNuevoFlujoDeTrabajo** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="edbfe-106">The **StartNewWorkflow** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="edbfe-107">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="edbfe-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="edbfe-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="edbfe-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edbfe-109"><strong>Número de registro</strong></span><span class="sxs-lookup"><span data-stu-id="edbfe-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="edbfe-110">Posición del elemento en la lista de SharePoint Foundation, empezando por <strong>1</strong> para el primer elemento de la lista, <strong>2</strong> para el segundo elemento, etc.</span><span class="sxs-lookup"><span data-stu-id="edbfe-110">The position of the item in the SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="edbfe-111">También puede escribir una expresión para este argumento.</span><span class="sxs-lookup"><span data-stu-id="edbfe-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="edbfe-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edbfe-112">Remarks</span></span>

  - <span data-ttu-id="edbfe-p102">La acción **IniciarNuevoFlujoDeTrabajo** abre el cuadro de diálogo **Iniciar nuevo flujo de trabajo**. Este cuadro de diálogo muestra todos los flujos de trabajo que están disponibles para el elemento especificado. Un flujo de trabajo se debe definir para la lista en SharePoint Foundation para poder utilizarlo con esta acción.</span><span class="sxs-lookup"><span data-stu-id="edbfe-p102">The **StartNewWorkflow** action opens the **Start New Workflow** dialog box. This dialog box displays all workflows that are available for the specified item. A workflow must be defined for the list in SharePoint Foundation before you can start it using this action.</span></span>

  - <span data-ttu-id="edbfe-p103">La acción **IniciarNuevoFlujoDeTrabajo** sólo se puede utilizar después de que se abra y seleccione una lista de SharePoint vinculada. Para abrir y seleccionar la lista vinculada, utilice la acción **AbrirTabla**. Si la lista ya está abierta, utilice la acción **SeleccionarObjeto** para seleccionarla.</span><span class="sxs-lookup"><span data-stu-id="edbfe-p103">The **StartNewWorkflow** action can only be used after a linked SharePoint list has been opened and selected. To open and select the linked list, use the **OpenTable** action. If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="edbfe-119">La acción **IniciarNuevoFlujoDeTrabajo** tienen el mismo efecto que hacer clic con el botón secundario en cualquier celda en una lista SharePoint vinculada mientras se abre en la vista Hoja de datos, ir a **Flujo de trabajo** y hacer clic en **Iniciar nuevo flujo de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="edbfe-119">The **StartNewWorkflow** action has the same effect as right-clicking any cell in a linked SharePoint list while it is open in Datasheet view, pointing to **Workflow**, and then clicking **Start New Workflow**.</span></span>

  - <span data-ttu-id="edbfe-120">Para ejecutar la acción **IniciarNuevoFlujoDeTrabajo** en un módulo de VBA, utilice el método **StartNewWorkflow** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="edbfe-120">To run the **StartNewWorkflow** action in a VBA module, use the **StartNewWorkflow** method of the **DoCmd** object.</span></span>

