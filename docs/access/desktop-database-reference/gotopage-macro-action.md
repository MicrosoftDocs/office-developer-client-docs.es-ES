---
title: IrAPágina (acción de macro)
TOCTitle: GoToPage macro action
ms:assetid: 611aadff-83b7-e74d-4093-93fb5ce6e3ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194858(v=office.15)
ms:contentKeyID: 48545199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm129285
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 10d55b435a59594eaf3e8380b6690ebbda63a258
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712375"
---
# <a name="gotopage-macro-action"></a>IrAPágina (acción de macro)

**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **IrAPágina** para mover el enfoque del formulario activo al primer control de una página especificada. Puede usar esta acción si ha creado un formulario con saltos de página que contenga grupos de información relacionada. Por ejemplo, podría tener un formulario Empleados con información personal en una página, información de la oficina en otra e información de las ventas en una tercera. Puede usar la acción **IrAPágina** para moverse a la página deseada. También puede presentar varias páginas de información en un único formulario mediante controles de pestaña.

## <a name="setting"></a>Configuración

La acción **IrAPágina** tiene los siguientes argumentos.

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
<td><p><strong>Número de página</strong></p></td>
<td><p>Número de la página a la que se desea trasladar el enfoque. Especifique el número de página en el cuadro <strong>Número de página</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Si deja este argumento en blanco, el enfoque permanece en la página activa. Puede usar los argumentos <strong>Derecho</strong> y <strong>Abajo</strong> para mostrar la parte de la página que desea ver.</p></td>
</tr>
<tr class="even">
<td><p><strong>Right</strong></p></td>
<td><p>Posición horizontal de la zona en la página, medida desde el borde izquierdo de la ventana que la contiene, que va a aparecer en el borde izquierdo de la ventana. Es obligatorio si se especifica el argumento <strong>Abajo</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Down</strong></p></td>
<td><p>Posición vertical de la zona en la página, medida desde el borde superior de la ventana que la contiene, que va a aparecer en el borde superior de la ventana. Es obligatorio si se especifica el argumento <strong>Derecha</strong>.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!NOTA] Los argumentos **Derecha** y **Abajo** se especifican en pulgadas o centímetros, en función de la configuración regional especificada en el Panel de control de Windows.

## <a name="remarks"></a>Comentarios

Puede usar esta acción para seleccionar el primer control (según viene definido por el orden de tabulación del formulario) de la página especificada. Use la acción **IrAControl** para moverse a un control determinado del formulario.

Puede usar los argumentos **derecha** y **abajo** para los formularios con páginas mayores que la ventana de Access. Use el argumento **Número de página** para moverse a la página deseada y, a continuación, use los argumentos **Derecha** y **Abajo** para mostrar la parte de la página que desee ver. Access muestra la parte de la página cuya esquina superior izquierda está a la distancia especificada de la esquina superior izquierda de la página.

La acción **IrAPágina** no se puede usar en los siguientes casos:

- Para mover el enfoque a una página de un formulario oculto.

- Para mover el enfoque de una página a otra dentro del control de pestaña.

Para ejecutar la acción **IrAPágina** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **GoToPage** del objeto **DoCmd**.

