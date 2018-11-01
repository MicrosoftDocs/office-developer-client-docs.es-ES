---
title: BloquearPanelDeExploración (acción de macro)
TOCTitle: LockNavigationPane Macro Action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2db34ee9ea56c5fcb4c5aff6afa57c3f59d1f17c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870334"
---
# <a name="locknavigationpane-macro-action"></a>BloquearPanelDeExploración (acción de macro)


**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **BloquearPanelDeExploración** para impedir que los usuarios eliminen objetos de base de datos que se muestran en el Panel de navegación.

## <a name="setting"></a>Configuración

La acción **BloquearPanelDeExploración** tiene el siguiente argumento.

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
<td><p><strong>Lock</strong></p></td>
<td><p>Seleccione <strong>Sí</strong> para bloquear el panel de navegación, o bien, <strong>No</strong> para desbloquearlo.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Al bloquear el panel de navegación, se impide que se eliminen objetos de la base de datos o se corten y se peguen objetos de la base de datos en el portapapeles. Lo hace *no* le impida llevar a cabo cualquiera de las siguientes operaciones:

  - Copiar objetos de base de datos en el Portapapeles

  - Pegar objetos de base de datos del Portapapeles

  - Mostrar u ocultar el Panel de navegación

  - Seleccionar esquemas de organización diferentes en el Panel de navegación

  - Mostrar u ocultar secciones del Panel de navegación

Para ejecutar la acción **BloquearPanelDeExploración** en un módulo de VBA, use el método **LockNavigationPane** del objeto **DoCmd**.

