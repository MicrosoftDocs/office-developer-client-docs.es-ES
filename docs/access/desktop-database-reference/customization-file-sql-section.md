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
# <a name="customization-file-sql-section"></a><span data-ttu-id="7944f-102">Sección de SQL del archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="7944f-102">Customization File SQL section</span></span>


<span data-ttu-id="7944f-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7944f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7944f-p101">La sección **SQL** puede contener una nueva cadena SQL que reemplaza la cadena de comandos del cliente. Si no hay ninguna cadena SQL en la sección, se omitirá la sección.</span><span class="sxs-lookup"><span data-stu-id="7944f-p101">The **sql** section can contain a new SQL string that replaces the client command string. If there is no SQL string in the section, the section will be ignored.</span></span>

<span data-ttu-id="7944f-p102">La nueva cadena SQL puede ser *parametrizada*. Es decir, los parámetros en la cadena SQL de la sección **SQL** (designada mediante el carácter '?') se pueden reemplazar con los argumentos correspondientes de un *identificador* en la cadena de comandos del cliente (designada por una lista delimitada por comas entre paréntesis). El identificador y la lista de argumentos se comportan como una llamada a función.</span><span class="sxs-lookup"><span data-stu-id="7944f-p102">The new SQL string may be *parameterized*. That is, parameters in the **sql** section SQL string (designated by the '?' character) can be replaced by corresponding arguments in an *identifier* in the client command string (designated by a comma-delimited list in parentheses). The identifier and argument list behave like a function call.</span></span>

<span data-ttu-id="7944f-109">Por ejemplo, supongamos que la cadena de comandos del cliente es "CustomerByID (4)", \[el encabezado\] de la sección SQL es SQL CustomerByID y la nueva \* cadena de la sección SQL es "SELECT FROM Customers WHERE CustomerID = ?".</span><span class="sxs-lookup"><span data-stu-id="7944f-109">For example, assume the client command string is "CustomerByID(4)" , the SQL section header is \[SQL CustomerByID\] , and the new SQL section string is "SELECT \* FROM Customers WHERE CustomerID = ?".</span></span> <span data-ttu-id="7944f-110">El controlador generará, el encabezado de la sección \[SQL es\] SQL CustomerByID y la nueva cadena de la sección SQL \* es "SELECT FROM Customers WHERE CustomerID = ?".</span><span class="sxs-lookup"><span data-stu-id="7944f-110">The Handler will generate , the SQL section header is \[SQL CustomerByID\] , and the new SQL section string is "SELECT \* FROM Customers WHERE CustomerID = ?".</span></span> <span data-ttu-id="7944f-111">El controlador generará "SELECT \* FROM Customers WHERE CustomerID = 4" y use esa cadena para consultar el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="7944f-111">The Handler will generate "SELECT \* FROM Customers WHERE CustomerID = 4" and use that string to query the data source.</span></span>

<span data-ttu-id="7944f-112">Si la nueva instrucción SQL es la cadena null (""), se omitirá la sección.</span><span class="sxs-lookup"><span data-stu-id="7944f-112">If the new SQL statement is the null string (""), then the section is ignored.</span></span>

<span data-ttu-id="7944f-p104">Si la nueva instrucción SQL no es válida, se generará un error al ejecutarse la instrucción. El parámetro de cliente se omitirá de manera efectiva. Para hacerlo de manera intencionada, es preciso "desactivar" todos los comandos SQL de cliente especificando:</span><span class="sxs-lookup"><span data-stu-id="7944f-p104">If the new SQL statement string is not valid, then the execution of the statement will fail. The client parameter is effectively ignored. You can do this intentionally to "turn off" all client SQL commands by specifying:</span></span>

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a><span data-ttu-id="7944f-116">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7944f-116">Syntax</span></span>

<span data-ttu-id="7944f-117">Una entrada de cadena SQL de reemplazo tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="7944f-117">A replacement SQL string entry is of the form:</span></span>

<span data-ttu-id="7944f-118">**SQL = \* sqlString**\*</span><span class="sxs-lookup"><span data-stu-id="7944f-118">**SQL=\*sqlString**\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7944f-119">Parte</span><span class="sxs-lookup"><span data-stu-id="7944f-119">Part</span></span></p></th>
<th><p><span data-ttu-id="7944f-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="7944f-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7944f-121"><strong>SQL</strong></span><span class="sxs-lookup"><span data-stu-id="7944f-121"><strong>SQL</strong></span></span></p></td>
<td><p><span data-ttu-id="7944f-122">Cadena literal que indica que se trata de una entrada de la sección SQL.</span><span class="sxs-lookup"><span data-stu-id="7944f-122">A literal string that indicates this is an SQL section entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7944f-123"><strong><em>Cadenasql</em></strong></span><span class="sxs-lookup"><span data-stu-id="7944f-123"><strong><em>sqlString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="7944f-124">Cadena SQL que reemplaza la cadena de cliente.</span><span class="sxs-lookup"><span data-stu-id="7944f-124">An SQL string that replaces the client string.</span></span></p></td>
</tr>
</tbody>
</table>

