---
title: DefinirCategoríasMostradas (acción de macro)
TOCTitle: SetDisplayedCategories macro action
ms:assetid: e8bf39a6-c639-2232-7b21-3b0badf37e4b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836053(v=office.15)
ms:contentKeyID: 48548429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm20026
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f08b9a8980fc6f08a9f91366d38f65e4365a037e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314629"
---
# <a name="setdisplayedcategories-macro-action"></a>DefinirCategoríasMostradas (acción de macro)


**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **DefinirCategoríasMostradas** para especificar las categorías que se van a mostrar bajo **Desplazarse a la categoría** en la barra de título del panel de navegación. Por ejemplo, si desea impedir que los usuarios puedan cambiar el panel de navegación de modo que muestre los objetos ordenados por **Fecha de creación**, puede usar esta acción para ocultar esa opción en la lista desplegable de la barra de título.

## <a name="setting"></a>Configuración

La acción **DefinirCategoríasMostradas** tiene los siguientes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Show</strong></p></td>
<td><p>Seleccione <strong>Sí</strong> para que se muestren las categorías. Seleccione <strong>No</strong> para ocultarlas.</p></td>
</tr>
<tr class="even">
<td><p><strong>Categoría</strong></p></td>
<td><p>Especifique o seleccione el nombre de la categoría que desee mostrar u ocultar. Deje este argumento en blanco para mostrar u ocultar todas las categorías.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

  - El título en la barra de título del panel de navegación indica, si procede, el filtro actualmente activo. Haga clic en cualquier punto de la barra para mostrar la lista desplegable. Los elementos controlados por esta acción de macro aparecen bajo **Desplazarse a la categoría**.

  - Esta acción sólo activa o desactiva la presentación de las categorías especificadas; no cambia la presentación del panel de navegación. Por ejemplo, si se muestran objetos ordenados por **Fecha de creación** y se usa la acción **DefinirCategoríasMostradas** para deshabilitar la opción **Fecha de creación**, Access no cambia el panel de navegación a otra categoría.

  - Para ejecutar la acción **DefinirCategoríasMostradas** en un módulo de VBA, use el método **SetDisplayedCategories** del objeto **DoCmd**.

