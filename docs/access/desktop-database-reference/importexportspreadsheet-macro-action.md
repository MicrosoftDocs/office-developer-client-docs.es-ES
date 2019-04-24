---
title: ImportarExportarHojaDeCálculo (acción de macro)
TOCTitle: ImportExportSpreadsheet macro action
ms:assetid: 526aef41-8329-5335-9d16-4d332542a297
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193927(v=office.15)
ms:contentKeyID: 48544846
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm31446
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: f910393c6d7a64258e5afc7545641fc5c6778b03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291876"
---
# <a name="importexportspreadsheet-macro-action"></a>ImportarExportarHojaDeCálculo (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **ImportarExportarHojaDeCálculo** para importar o exportar datos entre la base de datos de Access activa (.mdb o .accdb) o un proyecto de Access (.adp) y un archivo de hoja de cálculo. También puede vincular los datos en una hoja de cálculo de Microsoft Excel a la base de datos de Microsoft Access. Con una hoja de cálculo vinculada, puede ver y editar los datos de la hoja de cálculo con Access y a su vez tener un acceso total a los datos desde el programa de hoja de cálculo Excel. También puede vincular a datos en un archivo de hoja de cálculo de Lotus 1-2-3, pero estos datos son de solo lectura en Access.

> [!NOTE]
> Esta acción no se permitirá si la base de datos no es de confianza. 

## <a name="setting"></a>Configuración

La acción **TransferirHojaCálculo** tiene los siguientes argumentos.

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
<td><p><strong>Tipo de transferencia</strong></p></td>
<td><p>El tipo de transferencia que se desea realizar. Seleccione <strong>Importar</strong>, <strong>Exportar</strong> o <strong>Vincular</strong> en el cuadro <strong>Tipo de transferencia</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. La opción predeterminada es <strong>Importar</strong>.  </p><p><strong>Nota</strong>: el tipo de transferencia <STRONG>Link</STRONG> no se admite en los proyectos de Access (.adp).</p></td>
</tr>
<tr class="even">
<td><p><strong>Tipo hoja de cálculo</strong></p></td>
<td><p>El tipo de hoja de cálculo que se va a importar, exportar o vincular. Puede seleccionar uno entre varios tipos de hojas de cálculo en el cuadro. El valor predeterminado es <strong>Libro de Excel</strong>.  </p><p><strong>Nota</strong>: puede importar y vincular (solo lectura) archivos Lotus .WK4, pero no puede exportar datos de Access a este formato de hoja de cálculo. Access ya no admite importar, exportar o vincular datos de hojas de cálculo de Excel versión 2.0 o Lotus .WKS con esta acción. Si quiere importar o vincular datos de hoja de cálculo de Excel versión 2.0 o formato de Lotus .WKS, convierta los datos de la hoja de cálculo a una versión posterior de Excel o de Lotus 1-2-3 antes de importar o vincular los datos en Access.</p>
</td>
</tr>
<tr class="odd">
<td><p><strong>Nombre de la tabla</strong></p></td>
<td><p>El nombre de la tabla de Access a la que importar los datos de la hoja de cálculo, desde la que exportar los datos de la hoja de cálculo, o a la que vincular los datos de la hoja de cálculo. También puede escribir el nombre de la consulta de selección de Access desde la que quiera exportar los datos. Se trata de un argumento obligatorio. Si selecciona <strong>Importar</strong> en el argumento <strong>Tipo de transferencia</strong>, Access anexa los datos de la hoja de cálculo a esta tabla, si existe. De lo contrario, Access crea una nueva tabla que contiene los datos de la hoja de cálculo. En Access, no puede usar una instrucción SQL para especificar los datos para exportar al usar la acción <strong>ImportarExportarHojaDeCálculo</strong>. En lugar de usar una instrucción SQL, debe crear primero una consulta y, luego, especificar el nombre de la consulta en el argumento <strong>Nombre de tabla</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre del archivo</strong></p></td>
<td><p>El nombre del archivo de la hoja de cálculo desde la que importar, exportar o vincular. Incluir la ruta de acceso completa. Se trata de un argumento obligatorio. Access crea una nueva hoja de cálculo al exportar datos desde Access. Si el nombre del archivo es el mismo que el nombre de una hoja de cálculo existente, Access reemplaza la hoja de cálculo existente, a menos que exporte a un libro de Excel versión 5.0 o posterior. En este caso, Access copia los datos exportados a la siguiente nueva hoja de cálculo disponible del libro. Si importa desde o vincula a una hoja de cálculo de Excel versión 5.0 o posterior, puede especificar una hoja cálculo concreta con el argumento <strong>Rango</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Contiene nombres de campo</strong></p></td>
<td><p>Especifica si la primera fila de la hoja de cálculo contiene los nombres de los campos. Si selecciona <strong>Sí</strong>, Access usa los nombres de esta fila como los nombres de campo en la tabla de Access al importar o vincular los datos de la hoja de cálculo. Si selecciona <strong>No</strong>, Access trata la primera fila como una fila de datos normal. El valor predeterminado es <strong>No</strong>. Al exportar una tabla de Access o al seleccionar una consulta para una hoja de cálculo, se insertan los nombres de campo en la primera fila de la hoja de cálculo, independientemente de lo que seleccione en este argumento.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Range</strong></p></td>
<td><p>Rango de celdas que se van a importar o vincular. Deje este argumento en blanco para importar o vincular la hoja de cálculo completa. Puede escribir el nombre de un rango de la hoja de cálculo o especificar un rango de celdas para importar o vincular, tal como A1:E25 (observe que la sintaxis A1..E25 no funciona en Access 97 o en una versión posterior). Si importa o vincula con una hoja de cálculo de Excel versión 5.0 o posterior, puede anteponer al rango el nombre de la hoja de cálculo y un signo de exclamación (por ejemplo, Presupuesto!A1:C7).</p><p><strong>Nota</strong>: al exportar una hoja de cálculo, debe dejar este argumento en blanco. Si especifica un rango, se producirá un error en la exportación.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Los datos de las consultas de selección de Access se pueden exportar a hojas de cálculo. Access exporta el conjunto de resultados de la consulta tratándolo como si fuera una tabla.

Los datos de una hoja de cálculo que se anexan a una tabla de Access existente deben ser compatibles con la estructura de la tabla.

- Cada campo de la hoja de cálculo debe contener el mismo tipo de datos que el campo correspondiente de la tabla.

- Los campos deben estar en el mismo orden (a menos que haya establecido el argumento **Contiene nombres de campo** en **Sí**, en cuyo caso los nombres de los campos de la hoja de cálculo deben coincidir con los nombres de los campos de la tabla).

Esta acción es similar a hacer clic en la pestaña **Datos externos** y hacer clic en **Excel** en el grupo **Importar** o **Exportar**, o bien, hacer clic en **Más** en el grupo **Importar** o **Exportar** y hacer clic en **Archivo de Lotus 1-2-3**. Estos comandos se usan para seleccionar un origen de datos, tal como Access o un tipo de base de datos, hoja de cálculo o archivo de texto. Si selecciona una hoja de cálculo, aparecerán una serie de cuadros de diálogo, o se ejecutará un asistente de Access, donde se puede seleccionar el nombre de la hoja de cálculo y otras opciones. Los argumentos de la acción **ImportarExportarHojaDeCálculo** reflejan las opciones de estos cuadros de diálogo o de los asistentes.

> [!NOTE]
> Si consulta o filtra una hoja de cálculo vinculada, la consulta o el filtro distinguen entre mayúsculas y minúsculas.

Si crea un vínculo a una hoja de cálculo de Excel que está abierta en modo Edición, Access esperará hasta que la hoja de cálculo de Excel salga del modo Edición antes de completar el vínculo. No existe un tiempo máximo para esta espera.

Para ejecutar la acción **ImportarExportarHojaDeCálculo** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **TransferSpreadsheet** del objeto **DoCmd**.

