---
title: Funcionamiento de comandos parametrizados
TOCTitle: Operation of Parameterized Commands
ms:assetid: 71edbd16-21db-7afa-356b-d8e7afb92b3a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249456(v=office.15)
ms:contentKeyID: 48545596
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 42f0e8ffc7472dbf8a8c03fa320d3ae2b4a2e21b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486622"
---
# <a name="operation-of-parameterized-commands"></a>Funcionamiento de comandos parametrizados


**Se aplica a**: Access 2013 | Office 2013

Si se trabaja con un **conjunto de registros** secundario grande, especialmente en comparación con el tamaño del **conjunto de registros** principal, pero sólo se necesita obtener acceso a unos pocos capítulos secundarios, podría resultar más eficaz utilizar un comando parametrizado.

Un *comando no parametrizado* recupera los **conjuntos de registros**secundarios y principal completo, anexa una columna de capítulo al principal y, a continuación, asigna una referencia al capítulo secundario relacionado para cada fila principal.

Un *comando parametrizado* recupera al **conjunto de registros**principal completo, pero sólo recupera el **conjunto de registros** cuando se obtiene acceso a la columna de capítulo. Esta diferencia en la estrategia de recuperación puede suponer ventajas considerables en el rendimiento.

Por ejemplo, se puede especificar lo siguiente:

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

Las tablas primarias y secundarias tienen un nombre de columna en común, cliente\_identificador *.* El *comando secundario* tiene un marcador de posición "?", a la que hace referencia la cláusula RELATE (es decir, "..." PARÁMETRO 0").


> [!NOTE]
> <P>[!NOTA] La cláusula PARAMETER pertenece sólo a la sintaxis del comando Shape. No está asociada al objeto <A href="parameter-object-ado.md">Parameter</A> de ADO ni a la colección <A href="parameters-collection-ado.md">Parameters</A>.</P>



Cuando se ejecuta el comando parametrizado Shape, ocurre lo siguiente:

1.  El *comando a principal* se ejecuta y devuelve a un **objeto Recordset** primario de la tabla Customers.

2.  Una columna de capítulo se anexa al **conjunto de registros** principal.

3.  Cuando se obtiene acceso a la columna de capítulo de una fila principal, el *comando secundario* se ejecuta utilizando el valor de la customer.cust\_id como el valor del parámetro.

4.  Todas las filas del conjunto de filas del proveedor de datos creadas en el paso 3 se usan para rellenar el **conjunto de registros** secundario. En este ejemplo, que es todas las filas de la tabla Orders en el que el cliente\_identificador es igual al valor de customer.cust\_id. De forma predeterminada, el elemento secundario s de **conjunto de registros**se almacenarán en caché en el cliente hasta que se suelten todas las referencias al **conjunto de registros** principal. Para cambiar este comportamiento, establezca la [propiedad dinámica](ado-dynamic-property-index.md)de **Recordset** **Cache Child Rows** en **False**.

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

## <a name="parameterized-commands-and-complex-parent-child-relations"></a>Comandos parametrizados y relaciones complejas entre principal y secundario

Además de utilizar comandos parametrizados para mejorar el rendimiento de una jerarquía de tipo combinación equivalente, los comandos parametrizados pueden servir para admitir relaciones principal-secundario más complejas. Por ejemplo, considere la posibilidad de una base de datos de poca deportiva con dos tablas: uno que consta de los equipos (equipo\_identificador, equipo\_nombre) y la otra de juegos (fecha, página principal\_equipo, visite\_equipo).

Utilizando una jerarquía no parametrizada, no hay forma de relacionar las tablas de equipos y encuentros de forma tal que el **conjunto de registros** secundario para cada equipo contenga su programación completa. Puede crear capítulos que contengan la programación de encuentros en casa o la de encuentros fuera de casa, pero no ambas. Esto se debe a que la cláusula RELATE limita a relaciones principal-secundario de la forma (pc1=cc1) AND (pc2=pc2). Por lo tanto, si el comando incluye "equipo relacionar\_principal de identificador para\_team, equipo de\_identificador a visitar\_equipo", obtendría sólo juegos donde estaba reproduciendo un equipo propio. Lo que desea es "(equipo\_id = home\_equipo) o (equipo\_identificador = visitar\_equipo)", pero el proveedor Shape no admite la cláusula OR.

Para obtener el resultado deseado, puede utilizar un comando parametrizado. Por ejemplo:

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

Este ejemplo aprovecha la mayor flexibilidad de la cláusula WHERE de SQL para obtener el resultado que necesita.

