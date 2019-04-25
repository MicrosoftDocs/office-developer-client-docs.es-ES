---
title: Tipos de datos equivalentes de ANSI SQL
TOCTitle: Equivalent ANSI SQL data types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 3ea0641c7325bfcb4339572bc8b50724115af8d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293514"
---
# <a name="equivalent-ansi-sql-data-types"></a>Tipos de datos equivalentes de ANSI SQL


**Se aplica a:** Access 2013, Office 2013

La siguiente tabla enumera los tipos de datos de ANSI SQL, los tipos de datos equivalentes del motor de base de datos de Microsoft Access y sus sinónimos válidos. También se incluyen los tipos de datos equivalentes de Microsoft SQL Server™.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de datos de ANSI SQL</p></th>
<th><p>Tipo de datos de Microsoft Access SQL</p></th>
<th><p>Sinónimo</p></th>
<th><p>Tipo de datos de Microsoft SQL Server</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BIT, BIT VARYING</p></td>
<td><p>BINARY (vea las Notas)</p></td>
<td><p>VARBINARY, BINARY VARYING BIT VARYING</p></td>
<td><p>BINARY, VARBINARY</p></td>
</tr>
<tr class="even">
<td><p>No admitido</p></td>
<td><p>BIT (vea las Notas)</p></td>
<td><p>BOOLEAN, LOGICAL, LOGICAL1, YESNO</p></td>
<td><p>BIT</p></td>
</tr>
<tr class="odd">
<td><p>No admitido</p></td>
<td><p>TINYINT</p></td>
<td><p>INTEGER1, BYTE</p></td>
<td><p>TINYINT</p></td>
</tr>
<tr class="even">
<td><p>No admitido</p></td>
<td><p>COUNTER (vea las Notas)</p></td>
<td><p>AUTOINCREMENT</p></td>
<td><p>(vea las Notas)</p></td>
</tr>
<tr class="odd">
<td><p>No admitido</p></td>
<td><p>MONEY</p></td>
<td><p>CURRENCY</p></td>
<td><p>MONEY</p></td>
</tr>
<tr class="even">
<td><p>DATE, TIME, TIMESTAMP</p></td>
<td><p>DATETIME</p></td>
<td><p>DATE, TIME (See Notes)</p></td>
<td><p>DATETIME</p></td>
</tr>
<tr class="odd">
<td><p>No admitido</p></td>
<td><p>UNIQUEIDENTIFIER</p></td>
<td><p>GUID</p></td>
<td><p>UNIQUEIDENTIFIER</p></td>
</tr>
<tr class="even">
<td><p>DECIMAL</p></td>
<td><p>DECIMAL</p></td>
<td><p>NUMERIC, DEC</p></td>
<td><p>DECIMAL</p></td>
</tr>
<tr class="odd">
<td><p>REAL</p></td>
<td><p>REAL</p></td>
<td><p>SINGLE, FLOAT4, IEEESINGLE</p></td>
<td><p>REAL</p></td>
</tr>
<tr class="even">
<td><p>DOUBLE PRECISION, FLOAT</p></td>
<td><p>FLOAT</p></td>
<td><p>DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (vea las Notas)</p></td>
<td><p>FLOAT</p></td>
</tr>
<tr class="odd">
<td><p>SMALLINT</p></td>
<td><p>SMALLINT</p></td>
<td><p>SHORT, INTEGER2</p></td>
<td><p>SMALLINT</p></td>
</tr>
<tr class="even">
<td><p>INTEGER</p></td>
<td><p>INTEGER</p></td>
<td><p>LONG, INT, INTEGER4</p></td>
<td><p>INTEGER</p></td>
</tr>
<tr class="odd">
<td><p>INTERVAL</p></td>
<td><p>No admitido</p></td>
<td><p></p></td>
<td><p>Incompatible</p></td>
</tr>
<tr class="even">
<td><p>No admitido</p></td>
<td><p>IMAGE</p></td>
<td><p>LONGBINARY, GENERAL, OLEOBJECT</p></td>
<td><p>IMAGE</p></td>
</tr>
<tr class="odd">
<td><p>No admitido</p></td>
<td><p>TEXT (ver notas)</p></td>
<td><p>LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (vea las Notas)</p></td>
<td><p>TEXT</p></td>
</tr>
<tr class="even">
<td><p>CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</p></td>
<td><p>CHAR (vea las Notas)</p></td>
<td><p>TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (ver notas)</p></td>
<td><p>CHAR, VARCHAR, NCHAR, NVARCHAR</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - El tipo de datos BIT de ANSI SQL no se corresponde con el tipo de datos BIT de Microsoft Access SQL. En su lugar, se corresponde con el tipo de datos BINARY. No hay equivalente en ANSI SQL para el tipo de datos BIT de Microsoft Access SQL.
> - TIMESTAMP ya no se admite como sinónimo de DATETIME.
> - NUMERIC ya no se admite como sinónimo de FLOAT o DOUBLE. Ahora, NUMERIC se usa como sinónimo de DECIMAL.
> - Los campos LONGTEXT siempre se almacenan en el formato de representación Unicode.
> - Si se usa el nombre de tipo de datos TEXT sin especificar la longitud opcional, por ejemplo TEXT(25), se crea un campo LONGTEXT. Esto permite escribir [instrucciones CREATE TABLE](create-table-statement-microsoft-access-sql.md) que produzcan tipos de datos coherentes con Microsoft SQL Server.
> - Los campos CHAR siempre se almacenan en el formato de representación Unicode, que es el equivalente del tipo de datos NATIONAL CHAR de ANSI SQL.
> - Si se usa el nombre de tipo de datos TEXT y se especifica la longitud opcional, por ejemplo TEXT(25), el tipo de datos del campo es equivalente al tipo de datos CHAR. Esto conserva la compatibilidad con versiones anteriores para la mayoría de las aplicaciones de Microsoft Jet a la vez que permite conciliar el tipo de datos TEXT (sin especificar la longitud) con Microsoft SQL Server.


