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
# <a name="startnewworkflow-macro-action"></a>IniciarNuevoFlujoDeTrabajo (acción de macro)


**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **IniciarNuevoFlujoDeTrabajo** para iniciar un nuevo flujo de trabajo para un elemento en una lista de Microsoft SharePoint Foundation vinculada.

## <a name="setting"></a>Configuración

La acción **IniciarNuevoFlujoDeTrabajo** tiene el siguiente argumento.

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
<td><p>Posición del elemento en la lista de SharePoint Foundation, empezando por <strong>1</strong> para el primer elemento de la lista, <strong>2</strong> para el segundo elemento, etc. También puede escribir una expresión para este argumento.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

  - La acción **IniciarNuevoFlujoDeTrabajo** abre el cuadro de diálogo **Iniciar nuevo flujo de trabajo**. Este cuadro de diálogo muestra todos los flujos de trabajo que están disponibles para el elemento especificado. Un flujo de trabajo se debe definir para la lista en SharePoint Foundation para poder utilizarlo con esta acción.

  - La acción **IniciarNuevoFlujoDeTrabajo** sólo se puede utilizar después de que se abra y seleccione una lista de SharePoint vinculada. Para abrir y seleccionar la lista vinculada, utilice la acción **AbrirTabla**. Si la lista ya está abierta, utilice la acción **SeleccionarObjeto** para seleccionarla.

  - La acción **IniciarNuevoFlujoDeTrabajo** tienen el mismo efecto que hacer clic con el botón secundario en cualquier celda en una lista SharePoint vinculada mientras se abre en la vista Hoja de datos, ir a **Flujo de trabajo** y hacer clic en **Iniciar nuevo flujo de trabajo**.

  - Para ejecutar la acción **IniciarNuevoFlujoDeTrabajo** en un módulo de VBA, utilice el método **StartNewWorkflow** del objeto **DoCmd**.

