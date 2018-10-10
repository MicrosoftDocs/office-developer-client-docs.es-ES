---
title: Cláusula COMPUTE del comando Shape
TOCTitle: Shape Compute Clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 634a0ea648646d95995054ce7458cea492c40e47
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486503"
---
# <a name="shape-compute-clause"></a>Cláusula COMPUTE del comando Shape

**Se aplica a**: Access 2013 | Office 2013

Una cláusula COMPUTE del comando Shape genera un objeto **Recordset** primario, cuyas columnas se componen de una referencia al objeto **Recordset** secundario; columnas opcionales cuyo contenido son columnas de capítulo, nuevas o calculadas, o bien el resultado de ejecutar funciones de agregado en el objeto **Recordset** secundario o un objeto **Recordset** al que se ha aplicado forma anteriormente; así como cualquier columna del objeto **Recordset** secundario que aparezca en la cláusula opcional BY.

## <a name="syntax"></a>Sintaxis

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a>Descripción

Los elementos de esta cláusula son los siguientes:

- *comando secundario*

  - Consta de uno de los siguientes elementos:
    
    - Un comando de consulta entre llaves ("{}") que devuelve un objeto **Recordset** secundario. El comando se emite al proveedor de datos subyacente y su sintaxis depende de los requisitos de ese proveedor. Suele ser el lenguaje SQL, si bien ADO no requiere ningún lenguaje de consulta en particular.
    
    - El nombre de un objeto **Recordset** con forma existente.
    
    - Otro comando Shape.
    
    - La palabra clave TABLE, seguida del nombre de una tabla en el proveedor de datos.

- *alias secundario*

  - Un alias utilizado para hacer referencia al **objeto Recordset** devuelto por la *comando secundario.* El *alias secundario* se requiere en la lista de columnas en la cláusula COMPUTE y define a la relación entre los objetos **Recordset** primarios y secundarios.

- *lista de columnas adjuntas*

  - Una lista donde cada elemento define una columna en el objeto primario generado. Cada elemento contiene una columna de capítulo, una columna nueva, una columna calculada o un valor resultante de una función de agregado en el objeto **Recordset** secundario.

- *lista de campos agrupados*

  - Una lista de columnas en el objeto **Recordset** primario y secundario que especifica cómo deben agruparse las filas en el objeto secundario. Para cada columna en el *campo lista agrupados,* hay una columna correspondiente en los objetos **Recordset** primarios y secundarios. Para cada fila del **objeto Recordset**primario, las columnas de la *lista de campos agrupados* tienen valores únicos, y el elemento secundario **Recordset** al que hace referencia la fila primaria consta únicamente de secundarios filas cuya *lista de campos agrupados* columnas tienen los mismos valores que el fila primaria.

Si se incluye la cláusula BY, las filas del objeto **Recordset** secundario se agruparán basándose en las columnas de la cláusula COMPUTE. El objeto **Recordset** primario contendrá una fila por cada grupo de filas en el objeto **Recordset** secundario.

Si se omite la cláusula BY, todo el objeto **Recordset** secundario se trata como un solo grupo y el objeto **Recordset** primario contendrá exactamente una fila. Esa fila hará referencia a todo el objeto **Recordset** secundario. Si se omite la cláusula BY, se podrán calcular agregados de "Total general" en todo el objeto **Recordset** secundario.

Por ejemplo:

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

Independientemente de cómo se forme el objeto **Recordset** primario (mediante COMPUTE o APPEND), contendrá una columna de capítulo que se usa para relacionarlo con un objeto **Recordset** secundario. Si lo desea, el objeto **Recordset** primario también puede contener columnas con agregados (SUMA, MIN, MAX, etc.) de las filas secundarias. Tanto el objeto **Recordset** primario como el secundario pueden incluir columnas que contienen una expresión en la fila del objeto **Recordset**, así como columnas nuevas e inicialmente vacías.

## <a name="operation"></a>Operación

El *comando a secundario* se emite al proveedor, que devuelve a un **objeto Recordset**secundario.

La cláusula COMPUTE especifica las columnas del objeto **Recordset** primario, que pueden ser una referencia al objeto **Recordset** secundario, uno o varios agregados, una expresión calculada o columnas nuevas. Si hay una cláusula BY, las columnas que define también se anexan al objeto **Recordset** primario. La cláusula BY especifica cómo se agrupan las filas del objeto **Recordset** secundario.

Por ejemplo, supongamos que tenemos una tabla denominada Demographics (Datos demográficos) que consta de los campos Estado, Ciudad y Población (los datos de población son a título ilustrativo).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Estado</p></th>
<th><p>Ciudad</p></th>
<th><p>Población</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WA</p></td>
<td><p>Seattle</p></td>
<td><p>700.000</p></td>
</tr>
<tr class="even">
<td><p>OR</p></td>
<td><p>Medford</p></td>
<td><p>200.000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Portland</p></td>
<td><p>400.000</p></td>
</tr>
<tr class="even">
<td><p>CA</p></td>
<td><p>Los Ángeles</p></td>
<td><p>800.000</p></td>
</tr>
<tr class="odd">
<td><p>CA</p></td>
<td><p>San Diego</p></td>
<td><p>600.000</p></td>
</tr>
<tr class="even">
<td><p>WA</p></td>
<td><p>Tacoma</p></td>
<td><p>500.000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Corvallis</p></td>
<td><p>300.000</p></td>
</tr>
</tbody>
</table>


Emita ahora este comando Shape:

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

Este comando abre un objeto **Recordset** con forma que consta de dos niveles. El nivel primario es un **conjunto de registros** de generado con una columna agregada (SUM(rs.population)), una columna que hace referencia al elemento secundario de **Recordset** (rs) y una columna para agrupar al **objeto Recordset** (estado) secundario. El nivel secundario es el **objeto Recordset** devuelto por el comando de consulta (), una columna que hace referencia al elemento secundario de **Recordset** (rs) y una columna para agrupar al **objeto Recordset** (estado) secundario. El nivel secundario es el **objeto Recordset** devuelto por el comando de consulta (seleccione \* de datos demográficos).

Las filas de detalle del objeto **Recordset** secundario se agruparán por estado, pero por lo demás en ningún orden particular. Es decir, los grupos no estarán en orden alfabético ni numérico. Si desea ordenar el objeto **Recordset** primario, podrá utilizar el método **Sort** del objeto **Recordset** para ordenar el objeto **Recordset** primario.

Ahora, puede navegar por el objeto **Recordset** primario abierto y obtener acceso a los objetos **Recordset** secundarios de detalle. Para obtener más información, vea [ Obtener acceso a las filas de un objeto Recordset jerárquico ](accessing-rows-in-a-hierarchical-recordset.md).

**Objetos Recordset primarios y secundarios de detalle resultantes**

**Primario**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>SUM (rs.Population)</p></th>
<th><p>rs</p></th>
<th><p>Estado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1,300,000</p></td>
<td><p>Referencia a secundario1</p></td>
<td><p>CA</p></td>
</tr>
<tr class="even">
<td><p>1,200,000</p></td>
<td><p>Referencia a secundario2</p></td>
<td><p>WA</p></td>
</tr>
<tr class="odd">
<td><p>1,100,000</p></td>
<td><p>Referencia a secundario3</p></td>
<td><p>OR</p></td>
</tr>
</tbody>
</table>


**Secundario1**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Estado</p></th>
<th><p>Ciudad</p></th>
<th><p>Población</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CA</p></td>
<td><p>Los Ángeles</p></td>
<td><p>800.000</p></td>
</tr>
<tr class="even">
<td><p>CA</p></td>
<td><p>San Diego</p></td>
<td><p>600.000</p></td>
</tr>
</tbody>
</table>


**Secundario2**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Estado</p></th>
<th><p>Ciudad</p></th>
<th><p>Población</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WA</p></td>
<td><p>Seattle</p></td>
<td><p>700.000</p></td>
</tr>
<tr class="even">
<td><p>WA</p></td>
<td><p>Tacoma</p></td>
<td><p>500.000</p></td>
</tr>
</tbody>
</table>


**Secundario3**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Estado</p></th>
<th><p>Ciudad</p></th>
<th><p>Población</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Medford</p></td>
<td><p>200.000</p></td>
</tr>
<tr class="even">
<td><p>OR</p></td>
<td><p>Portland</p></td>
<td><p>400.000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Corvallis</p></td>
<td><p>300.000</p></td>
</tr>
</tbody>
</table>

