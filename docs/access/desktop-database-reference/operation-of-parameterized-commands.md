---
title: Funcionamiento de los comandos con parámetros
TOCTitle: Operation of parameterized commands
ms:assetid: 71edbd16-21db-7afa-356b-d8e7afb92b3a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249456(v=office.15)
ms:contentKeyID: 48545596
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 145a2ee6c3d3c614eb9660350a0bb8a00d44d04c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288290"
---
# <a name="operation-of-parameterized-commands"></a>Funcionamiento de los comandos con parámetros

**Se aplica a:** Access 2013, Office 2013

Si se trabaja con un **conjunto de registros** secundario grande, especialmente en comparación con el tamaño del **conjunto de registros** principal, pero sólo se necesita obtener acceso a unos pocos capítulos secundarios, podría resultar más eficaz utilizar un comando parametrizado.

Un *comando no parametrizado* recupera los **conjuntos de registros** principal y secundario completos, anexa una columna de capítulo al principal y, a continuación, asigna una referencia al capítulo secundario relacionado para cada fila principal.

Un *comando parametrizado* recupera el **conjunto de registros** principal completo, pero sólo recupera el **conjunto de registros** del capítulo cuando se obtiene acceso a la columna del capítulo. Esta diferencia en la estrategia de recuperación puede suponer ventajas considerables en el rendimiento.

Por ejemplo, se puede especificar lo siguiente:

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

Las tablas primaria y secundaria tienen un nombre de columna en común,\_ID Cust *.* El *comando secundario* tiene un marcador de posición "?", al que hace referencia la cláusula RELATE (es decir, "...PARAMETER 0").

> [!NOTE]
> [!NOTA] La cláusula PARAMETER pertenece sólo a la sintaxis del comando Shape. No está asociada al objeto [Parameter](parameter-object-ado.md) de ADO ni a la colección [Parameters](parameters-collection-ado.md).

Cuando se ejecuta el comando parametrizado Shape, ocurre lo siguiente:

1.  El *comando principal* se ejecuta y devuelve un **conjunto de registros** principal a partir de la tabla Customers.

2.  Una columna de capítulo se anexa al **conjunto de registros** principal.

3.  Cuando se obtiene acceso a la columna de capítulo de una fila principal, el *comando secundario* se ejecuta utilizando el valor del identificador Customer.\_Cust como valor del parámetro.

4.  Todas las filas del conjunto de filas del proveedor de datos creadas en el paso 3 se usan para rellenar el **conjunto de registros** secundario. En este ejemplo, todas las filas de la tabla Orders en las que el identificador\_Cust es igual al valor de Customer. Cust\_ID. De forma predeterminada, el **conjunto de registros** secundario se almacenará en caché en el cliente hasta que se liberen todas las referencias al **conjunto de registros** principal. Para cambiar este comportamiento, establezca las**filas secundarias** de la [propiedad dinámica](ado-dynamic-property-index.md) **Recordset** en **false**.

5.  Una referencia a las filas secundarias recuperadas (es decir, el capítulo del **conjunto de registros** secundario) se coloca en la columna de capítulo de la fila activa del **conjunto de registros** principal.

6.  Los pasos 3 a 5 se repiten cuando se obtiene acceso a la columna de capítulo de otra fila.

La propiedad dinámica **Cache Child Rows** se establece de forma predeterminada en **True**. El comportamiento de almacenamiento en caché varía según los valores de los parámetros de la consulta. En una consulta con un solo parámetro, el **conjunto de registros** secundario correspondiente a un valor de parámetro determinado se almacenará en caché entre solicitudes de un secundario con ese valor. El código siguiente lo muestra:

```vb
... 
SCmd = "SHAPE {select * from customer} " & _ 
 "APPEND({select * from orders where cust_id = ?} " & _ 
 "RELATE cust_id TO PARAMETER 0) AS chpCustOrder" 
Rst1.Open sCmd, Cnn1 
Set RstChild = Rst1("chpCustOrder").Value 
Rst1.MoveNext ' Next cust_id passed to Param 0, & new rs fetched 
 ' into RstChild. 
Rst1.MovePrevious ' RstChild now holds cached rs, saving round trip. 
... 
```

En una consulta con dos o más parámetros, sólo se utiliza un secundario almacenado en caché si todos los valores de parámetros coinciden con los valores en caché.

## <a name="parameterized-commands-and-complex-parent-child-relations"></a>Comandos parametrizados y relaciones de elementos primarios y secundarios complejos

Además de utilizar comandos parametrizados para mejorar el rendimiento de una jerarquía de tipo combinación equivalente, los comandos parametrizados pueden servir para admitir relaciones principal-secundario más complejas. Por ejemplo, considere una base de datos de una liga con dos tablas: una formada por los equipos\_(identificador del\_equipo, nombre del equipo) y el otro de los\_juegos (fecha\_, equipo doméstico, visitante del equipo).

Utilizando una jerarquía no parametrizada, no hay forma de relacionar las tablas de equipos y encuentros de forma tal que el **conjunto de registros** secundario para cada equipo contenga su programación completa. Puede crear capítulos que contengan la programación de encuentros en casa o la de encuentros fuera de casa, pero no ambas. Esto se debe a que la cláusula RELATE limita a relaciones principal-secundario de la forma (pc1=cc1) AND (pc2=pc2). Por lo tanto, si el comando incluye "\_relacionar identificador\_del equipo con\_equipo local,\_identificador del equipo para visitar equipo", obtendría solo los juegos en los que un equipo se estaba reproduciendo. Lo que desea es "(identificador\_de equipo =\_equipo doméstico) o (\_identificador de equipo\_= visitar equipo)", pero el proveedor de forma no admite la cláusula OR.

Para obtener el resultado deseado, puede utilizar un comando parametrizado. Por ejemplo:

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

Este ejemplo aprovecha la mayor flexibilidad de la cláusula WHERE de SQL para obtener el resultado que necesita.

