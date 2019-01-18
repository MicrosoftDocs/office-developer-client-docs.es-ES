---
title: EstablecerElementoDelMenú (acción de macro)
TOCTitle: SetMenuItem macro action
ms:assetid: 503b3635-e721-1b99-3249-626e5dccdb8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193803(v=office.15)
ms:contentKeyID: 48544789
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm16614
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fe61a3368813ba3420920909f818beee2029d993
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709428"
---
# <a name="setmenuitem-macro-action"></a>EstablecerElementoDelMenú (acción de macro)

**Se aplica a**: Access 2013, Office 2013

La acción **EstablecerElementoDelMenú** sirve para establecer el estado de los elementos de menú (habilitado o deshabilitado, seleccionado o no seleccionado) en los menús globales o personalizados de la ficha **Complementos**.

> [!NOTE]
> [!NOTA] La acción **EstablecerElementoDelMenú** solo funciona con menús globales y personalizados creados mediante macros de menús. La acción **EstablecerElementoDelMenú** está incluida en Microsoft Access sólo a efectos de compatibilidad con versiones anteriores. No se puede usar con la funcionalidad de las barras de comandos. Sin embargo, puede usar las propiedades **Enabled** y **State** en un módulo de Visual Basic para Aplicaciones (VBA) con el fin de habilitar, deshabilitar, seleccionar o cancelar la selección de elementos de menús contextuales o menús globales o personalizados.

## <a name="setting"></a>Configuración

La acción **EstablecerElementoDelMenú** utiliza los siguientes argumentos.

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
<td><p><strong>Índice del menú</strong></p></td>
<td><p>El índice del menú que contiene el comando para el que desea establecer el estado. Escriba un valor entero, comenzando desde 0, para el índice del menú que desea en el menú global o personalizado. Escriba el valor de índice en el cuadro <strong>Índice del menú</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros. El índice es con relación a la posición del menú en la macro de menú para el menú global o personalizado (la posición de la acción <strong>AgregarMenú</strong> de este menú en la macro de menú, contando desde 0). La presentación del menú puede ser algo diferente, ya que se pueden utilizar expresiones condicionales en la macro de menú para ocultar o mostrar elementos de menú personalizados. Este argumento es obligatorio. Si selecciona un menú con este argumento y deja en blanco los argumentos <strong>Índice del comando</strong> e <strong>Índice de subcomando</strong> , puede habilitar o deshabilitar el propio nombre del menú. Sin embargo, no se puede seleccionar o anular la selección de un nombre de menú (Access omite la configuración de <strong>Activar</strong> y <strong>desactivar</strong> del argumento <strong>indicador</strong> para nombres de menús).</p></td>
</tr>
<tr class="even">
<td><p><strong>Índice del comando</strong></p></td>
<td><p>El índice del comando para el que se desea establecer el estado. Especifique un valor entero, empezando desde 0, para el índice del comando deseado dentro del menú seleccionado mediante el argumento <strong>Índice del menú</strong>. El índice es relativo a la posición del comando en el grupo de macros que define el menú seleccionado para el menú global o personalizado (la posición de la macro de este comando en el grupo de macros, contando desde 0). La presentación del menú puede ser algo diferente, ya que se pueden utilizar expresiones condicionales en el grupo de macros del menú para ocultar o mostrar comandos de menú personalizados.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Índice de subcomando</strong></p></td>
<td><p>El índice del subcomando para el que se desea establecer el estado. Esto sólo es de aplicación si el comando deseado tiene un submenú. En el submenú seleccionado por el argumento <strong>Índice del comando</strong>, escriba un valor Entero, comenzando desde 0, para el índice del subcomando deseado. El índice es relativo a la posición del subcomando en el grupo de macros que define al submenú seleccionado para el menú global o personalizado (la posición de la macro de este subcomando en el grupo de macros, contando desde 0).</p></td>
</tr>
<tr class="even">
<td><p><strong>Flag</strong></p></td>
<td><p>El estado que desea establecer para el comando o subcomando. Haga clic en <strong>Sombrear</strong>, para deshabilitar el comando (éste aparecerá atenuado), <strong>Quitar sombreado</strong>, para habilitarlo, <strong>Activar</strong>, para colocar una marca junto al comando que indica que ha sido activado, o <strong>Desactivar</strong>, para quitar la marca. La opción predeterminada es <strong>Quitar sombreado</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

La acción **EstablecerElementoDelMenú** sólo funciona para un menú global o personalizado. Si la ventana activa no contiene un menú global o personalizado y se ejecuta una macro que contenga la acción **EstablecerElementoDelMenú**, se genera un error en tiempo de ejecución.

Esta acción se puede utilizar para establecer el estado de los comandos y subcomandos de menú, aunque no el de los subcomandos de subcomandos.

Para ejecutar la acción **EstablecerElementoDelMenú** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **SetMenuItem** del objeto **DoCmd**.

