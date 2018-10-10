---
title: Sección SQL del archivo de personalización
TOCTitle: Customization File SQL Section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09be671ba15727e3612ade78c5b54af12b1d1c57
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483675"
---
# <a name="customization-file-sql-section"></a>Sección SQL del archivo de personalización


**Se aplica a**: Access 2013 | Office 2013

La sección **SQL** puede contener una nueva cadena SQL que reemplaza la cadena de comandos del cliente. Si no hay ninguna cadena SQL en la sección, se omitirá la sección.

La nueva cadena SQL puede ser *parametrizada*. Es decir, los parámetros en la cadena SQL de la sección **SQL** (designada mediante el carácter '?') se pueden reemplazar con los argumentos correspondientes de un *identificador* en la cadena de comandos del cliente (designada por una lista delimitada por comas entre paréntesis). El identificador y la lista de argumentos se comportan como una llamada a función.

Por ejemplo, supongamos que la cadena de comandos de cliente es "CustomerById (4)", el encabezado de sección SQL es \[SQL CustomerByID\] , y la nueva cadena de la sección SQL es "seleccione \* FROM Customers WHERE CustomerID = ?". El controlador generará, el encabezado de sección SQL es \[SQL CustomerByID\] , y la nueva cadena de la sección SQL es "seleccione \* FROM Customers WHERE CustomerID = ?". El controlador generará "seleccione \* FROM Customers WHERE CustomerID = 4" y utilizará dicha cadena para consultar el origen de datos.

Si la nueva instrucción SQL es la cadena null (""), se omitirá la sección.

Si la nueva instrucción SQL no es válida, se generará un error al ejecutarse la instrucción. El parámetro de cliente se omitirá de manera efectiva. Para hacerlo de manera intencionada, es preciso "desactivar" todos los comandos SQL de cliente especificando:

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a>Sintaxis

Una entrada de cadena SQL de reemplazo tiene el siguiente formato:

**SQL = * cadenasql***

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
<td><p><strong><em>cadenasql</em></strong></p></td>
<td><p>Cadena SQL que reemplaza la cadena de cliente.</p></td>
</tr>
</tbody>
</table>

