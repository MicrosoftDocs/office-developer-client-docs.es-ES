---
title: Sección de SQL del archivo de personalización
TOCTitle: Customization File SQL section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ae259589cc8d4945068901c59105425599edc64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295138"
---
# <a name="customization-file-sql-section"></a>Sección de SQL del archivo de personalización


**Se aplica a:** Access 2013, Office 2013

La sección **SQL** puede contener una nueva cadena SQL que reemplaza la cadena de comandos del cliente. Si no hay ninguna cadena SQL en la sección, se omitirá la sección.

La nueva cadena SQL puede ser *parametrizada*. Es decir, los parámetros en la cadena SQL de la sección **SQL** (designada mediante el carácter '?') se pueden reemplazar con los argumentos correspondientes de un *identificador* en la cadena de comandos del cliente (designada por una lista delimitada por comas entre paréntesis). El identificador y la lista de argumentos se comportan como una llamada a función.

Por ejemplo, supongamos que la cadena de comandos de cliente es "CustomerByID(4)" , el encabezado de sección SQL es SQL CustomerByID y la nueva cadena de sección SQL es \[ \] "SELECT \* FROM Customers WHERE CustomerID = ?". El controlador generará , el encabezado de sección SQL es SQL CustomerByID y la nueva cadena de sección SQL es \[ \] "SELECT \* FROM Customers WHERE CustomerID = ?". El controlador generará "SELECT \* FROM Customers WHERE CustomerID = 4" y usará esa cadena para consultar el origen de datos.

Si la nueva instrucción SQL es la cadena null (""), se omitirá la sección.

Si la nueva instrucción SQL no es válida, se generará un error al ejecutarse la instrucción. El parámetro de cliente se omitirá de manera efectiva. Para hacerlo de manera intencionada, es preciso "desactivar" todos los comandos SQL de cliente especificando:

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a>Sintaxis

Una entrada de cadena SQL de reemplazo tiene el siguiente formato:

**SQL=*sqlString***

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parte</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>SQL</strong></p></td>
<td><p>Cadena literal que indica que se trata de una entrada de la sección SQL.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>sqlString</em></strong></p></td>
<td><p>Cadena SQL que reemplaza la cadena de cliente.</p></td>
</tr>
</tbody>
</table>

