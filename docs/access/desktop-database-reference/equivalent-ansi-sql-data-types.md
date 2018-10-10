---
title: Tipos de datos equivalentes de ANSI SQL
TOCTitle: Equivalent ANSI SQL Data Types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7eae567d2787e60f84c8020d80e1c15c9b02928f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485313"
---
# <a name="equivalent-ansi-sql-data-types"></a>Tipos de datos equivalentes de ANSI SQL


**Se aplica a**: Access 2013 | Office 2013

En la siguiente tabla se incluyen los tipos de datos ANSI SQL, los tipos de datos SQL equivalentes del motor de base de datos de Microsoft Access y sus sinónimos válidos. También se incluyen los tipos de datos equivalentes de Microsoft® SQL Server.

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
<th><p>
Sinónimo</p></th>
<th><p>Tipo de datos de Microsoft SQL Server</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BIT, BIT VARYING</p></td>
<td><p>BINARY (vea las Notas)</p></td>
<td><p>VARBINARY, BINARIO DEBIDO A DISTINTOS DEBIDO A DISTINTOS BITS</p></td>
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
<td><p>DATE, TIME (vea las notas)</p></td>
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
<td><p>No admitido</p></td>
</tr>
<tr class="even">
<td><p>No admitido</p></td>
<td><p>IMAGE</p></td>
<td><p>LONGBINARY, GENERAL, OLEOBJECT</p></td>
<td><p>IMAGE</p></td>
</tr>
<tr class="odd">
<td><p>No admitido</p></td>
<td><p>TEXTO (vea las notas)</p></td>
<td><p>LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (vea las Notas)</p></td>
<td><p>TEXT</p></td>
</tr>
<tr class="even">
<td><p>CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</p></td>
<td><p>CHAR (vea las Notas)</p></td>
<td><p>Text (n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (vea las notas)</p></td>
<td><p>CHAR, VARCHAR, NCHAR, NVARCHAR</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <UL>
> <LI>
> <P>El tipo de datos BIT de ANSI SQL no se corresponde con el tipo de datos BIT de Microsoft Access SQL. En su lugar, se corresponde con el tipo de datos BINARY. No hay equivalente en ANSI SQL para el tipo de datos BIT de Microsoft Access SQL.</P>
> <LI>
> <P>TIMESTAMP ya no se admite como sinónimo de DATETIME.</P>
> <LI>
> <P>NUMERIC ya no se admite como sinónimo de FLOAT o DOUBLE. Ahora, NUMERIC se usa como sinónimo de DECIMAL.</P>
> <LI>
> <P>Los campos LONGTEXT siempre se almacenan en el formato de representación Unicode.</P>
> <LI>
> <P>Si se usa el nombre de tipo de datos TEXT sin especificar la longitud opcional, por ejemplo TEXT(25), se crea un campo LONGTEXT. Esto permite escribir <A href="create-table-statement-microsoft-access-sql.md">instrucciones CREATE TABLE</A> que produzcan tipos de datos coherentes con Microsoft SQL Server.</P>
> <LI>
> <P>Los campos CHAR siempre se almacenan en el formato de representación Unicode, que es el equivalente del tipo de datos NATIONAL CHAR de ANSI SQL.</P>
> <LI>
> <P>Si se usa el nombre de tipo de datos TEXT y se especifica la longitud opcional, por ejemplo TEXT(25), el tipo de datos del campo es equivalente al tipo de datos CHAR. Esto conserva la compatibilidad con versiones anteriores para la mayoría de las aplicaciones de Microsoft Jet a la vez que permite conciliar el tipo de datos TEXT (sin especificar la longitud) con Microsoft SQL Server.</P></LI></UL>


