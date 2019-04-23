---
title: Funciones escalares ODBC
TOCTitle: ODBC scalar functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 33443fda474b3785d34d457719e49f5e358bb254
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288514"
---
# <a name="odbc-scalar-functions"></a>Funciones escalares ODBC

**Se aplica a:** Access 2013, Office 2013

Microsoft Access SQL admite el uso de la sintaxis definida de ODBC para las funciones escalares. 

Por ejemplo, la consulta `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` devolverá todas las filas en las que el valor absoluto del cambio en el precio de una cotización sea mayor que cinco.

Se admite un subconjunto de las funciones escalares definidas por ODBC. En la siguiente tabla, se enumeran las funciones admitidas.

Para obtener una descripción de los argumentos y una explicación completa de la sintaxis de escape para incluir funciones en una instrucción SQL, vea la documentación de ODBC.

## <a name="string-functions"></a>Funciones de cadena

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>ASCII</p></td>
<td><p>LARGOS</p></td>
<td><p>RTRIM</p></td>
</tr>
<tr class="even">
<td><p>CHAR</p></td>
<td><p>HALLAR</p></td>
<td><p>ESPACIO</p></td>
</tr>
<tr class="odd">
<td><p>CONCAT</p></td>
<td><p>FUNCIONES LTrim</p></td>
<td><p>SUBCADENA</p></td>
</tr>
<tr class="even">
<td><p>LCASE</p></td>
<td><p>DERECHA</p></td>
<td><p>UCASE</p></td>
</tr>
<tr class="odd">
<td><p>DEJARON</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a>Funciones numéricas

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>ABS</p></td>
<td><p>INFERIORES</p></td>
<td><p>PIN</p></td>
</tr>
<tr class="even">
<td><p>ATAR</p></td>
<td><p>CONECTARSE</p></td>
<td><p>RAIZ</p></td>
</tr>
<tr class="odd">
<td><p>FIJADO</p></td>
<td><p>ALIMENTA</p></td>
<td><p>BRONCE</p></td>
</tr>
<tr class="even">
<td><p>Co</p></td>
<td><p>ALEA</p></td>
<td><p>MODULACIÓN</p></td>
</tr>
<tr class="odd">
<td><p>EXP</p></td>
<td><p>Inicio</p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a>Funciones de fecha y hora &

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>CURDATE</p></td>
<td><p>DAYOFYEAR</p></td>
<td><p>MES</p></td>
</tr>
<tr class="even">
<td><p>CURTIME</p></td>
<td><p>AÑO</p></td>
<td><p>BISEMANAL</p></td>
</tr>
<tr class="odd">
<td><p>VERSIÓN</p></td>
<td><p>CORRESPONDIENTE</p></td>
<td><p>Trim</p></td>
</tr>
<tr class="even">
<td><p>DAYOFMONTH</p></td>
<td><p>MINUTO</p></td>
<td><p>MONTHNAME</p></td>
</tr>
<tr class="odd">
<td><p>ODB</p></td>
<td><p>PUJA</p></td>
<td><p>DAYNAME</p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a>Conversión de tipos de datos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>VERSIONES</p></td>
<td><p>Los literales de cadena se pueden convertir a los siguientes tipos de datos: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR y SQL_DATETIME.</p></td>
</tr>
</tbody>
</table>

