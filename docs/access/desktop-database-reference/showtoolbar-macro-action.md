---
title: MostrarBarraDeHerramientas (acción de macro)
TOCTitle: ShowToolbar macro action
ms:assetid: 9e53009b-1e5e-1bee-3bcc-f82dc1b0dc48
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198288(v=office.15)
ms:contentKeyID: 48546649
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm27417
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ed69a84f9b1774b7c33711a0bb8e80da54e656cc
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997933"
---
# <a name="showtoolbar-macro-action"></a>MostrarBarraDeHerramientas (acción de macro)

**Se aplica a**: Access 2013, Office 2013

La acción **MostrarBarraDeHerramientas** se utiliza para mostrar u ocultar un grupo de comandos en la ficha **Complementos**.

> [!NOTE]
> - [!NOTA] La acción **MostrarBarraDeHerramientas** no afecta a los menús contextuales.
> - [!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. 

## <a name="setting"></a>Configuración

La acción **MostrarBarraDeHerramientas** utiliza los siguientes argumentos.

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
<td><p><strong>Nombre de barra de herramientas</strong></p></td>
<td><p>El nombre del grupo de comandos en la ficha <strong>Complementos</strong> que desea mostrar u ocultar. El cuadro <strong>Nombre de la barra de herramientas</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todos los grupos disponibles que pueden verse afectados por esta acción. Este argumento es obligatorio. Si se ejecuta una macro que contiene la acción <strong>MostrarBarraDeHerramientas</strong> en una base de datos de biblioteca, Access busca el grupo con ese nombre primero en la base de datos de biblioteca y, después, en la base de datos actual.</p></td>
</tr>
<tr class="even">
<td><p><strong>Show</strong></p></td>
<td><p>Especifica si se debe mostrar u ocultar el grupo y en qué vistas se debe mostrar u ocultar. El valor predeterminado es <strong>Sí</strong> (mostrar el grupo en todo momento). Puede seleccionar <strong>Sí</strong> para mostrar el grupo en todo momento, <strong>Donde corresponda</strong> para mostrar el grupo sólo cuando el formulario o informe apropiado está activo, o <strong>No</strong> para ocultar el grupo en todo momento.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Esta acción se puede utilizar en una macro con expresiones condicionales para mostrar u ocultar un grupo si se dan ciertas condiciones.

Si desea mostrar un grupo determinado en un solo formulario o informe, asigne a la propiedad **AlActivar** del formulario o informe el nombre de una macro que contenga una acción **MostrarBarraDeHerramientas** que muestre el grupo. Luego, asigne a la propiedad **AlDesactivar** del formulario o informe el nombre de una macro que contenga una acción **MostrarBarraDeHerramientas** que oculte el grupo.

Las barras de herramientas integradas no se pueden mostrar u ocultar mediante esta acción si se asigna a la propiedad **AllowBuiltInToolbars** el valor **Falso** (0) en un módulo de Visual Basic para Aplicaciones (VBA) o si se establece la propiedad **Permitir el uso de las barras de herramientas integradas** en **Falso** en VBA mediante el método **SetOption**.

Para ejecutar la acción **MostrarBarraDeHerramientas** en un módulo de VBA, use el método **ShowToolbar** del objeto **DoCmd**.

