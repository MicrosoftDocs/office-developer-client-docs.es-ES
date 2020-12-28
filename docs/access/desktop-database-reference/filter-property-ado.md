---
description: Filter (propiedad)
title: Filter (propiedad, ADO)
TOCTitle: Filter property (ADO)
ms:assetid: 5abc528a-a6ee-34de-5d44-a3249194b0a0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249314(v=office.15)
ms:contentKeyID: 48545053
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9d3234f1d5f41fd9f07b8d98bf3df395067780ae
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734199"
---
# <a name="filter-property-ado"></a>Filter (propiedad, ADO)


**Se aplica a:** Access 2013, Office 2013

Indica un filtro para datos en un objeto [ Recordset ](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Valores de configuración y devueltos

Establece o devuelve un valor de tipo **Variant** que puede contener uno de los siguientes:

  - **Cadena de criterios**: una cadena compuesta por una o más cláusulas concatenadas mediante operadores **AND** u **OR**.

  - **Matriz de marcadores**: una matriz de valores de marcador exclusivos que señalan a registros del objeto **Recordset**.

  - Un valor [FilterGroupEnum](filtergroupenum.md).

## <a name="remarks"></a>Comentarios

Use la propiedad **Filter** para seleccionar registros de un objeto **Recordset**. El objeto **Recordset** filtrado se convierte en el cursor actual. Esto afecta a otras propiedades que devuelven valores basados en el cursor actual, como [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [RecordCount](recordcount-property-ado.md) y [PageCount](pagecount-property-ado.md). Esto se debe a que al establecer la propiedad **Filter** en un valor específico, se moverá el registro actual al primer registro que satisfaga el nuevo valor.

La cadena de criterios se compone de cláusulas con el formato *NombreCampo-operador-valor* (por ejemplo, "LastName = ' Smith '"). Puede crear cláusulas compuestas mediante la concatenación de cláusulas individuales con **and** (por ejemplo, "LastName = ' Smith ' and FirstName = ' John '") u **or** (por ejemplo, "). Puede crear cláusulas compuestas mediante la concatenación de cláusulas individuales con **and** (por ejemplo, "LastName = ' Smith ' and FirstName = ' John '") u **or** (por ejemplo, "LastName = ' Smith ' or LastName = ' Jones '"). Utilice las siguientes directrices para las cadenas de criterios:

  - *NombreCampo* debe ser un nombre de campo válido del objeto **Recordset**. Si el nombre de campo contiene espacios, debe ir entre corchetes.

  - *Operador* debe ser uno de los siguientes: \<, \> , \<=, \> =, \<\> , = o **like**.

  - *Value* es el valor con el que se comparan los valores de campo (por ejemplo, ' Smith ', \# 8/24/95 \# , 12,345 o $50,00). Use comillas sencillas con las cadenas y los signos de almohadilla ( \# ) con las fechas. Con los números puede utilizar comas decimales, signos de dólar y notación científica. Si *Operador* es **LIKE**, *Valor* puede utilizar comodines. Solo el asterisco ( \* ) y el signo de porcentaje (%) se permiten los caracteres comodín y deben ser el último carácter de la cadena. *Valor* no puede ser nulo.

    > [!NOTE]
    > [!NOTA] Para incluir comillas sencillas (') en el filtro Valor, utilice dos comillas sencillas para representar una. Por ejemplo, para filtrar por O'Malley, la cadena de criterios debería ser "col1 = 'O''Malley'". Para incluir comillas sencillas al principio y al final del valor de filtrado, incluya la cadena entre signos de número (#). Por ejemplo, para filtrar por '1', la cadena de criterios debería ser "col1 = #'1'#".

-   No hay ninguna preferencia entre **AND** y **OR**. Las cláusulas se pueden agrupar entre paréntesis. Sin embargo, no puede agrupar cláusulas Unidas mediante **or** y, a continuación, unir el grupo a otra cláusula con un **y**, como en el siguiente fragmento de código:  
 `(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John'`  
  
-   Este filtro se construiría como  
 `(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John')`  

  - En una cláusula **like** , puede usar un carácter comodín al principio y al final del patrón (por ejemplo, LastName like ' \* MIT \* ') o sólo al final del patrón (por ejemplo, LastName like ' Smit \* ').

Las constantes del filtro facilitan la resolución de conflictos de registros individuales durante el modo de actualización por lotes al permitir ver, por ejemplo, sólo aquellos registros afectados durante la última llamada al método [UpdateBatch](updatebatch-method-ado.md).

El establecimiento de la propiedad **Filter** por sí misma puede dar lugar a un error a causa de un conflicto con los datos subyacentes (por ejemplo, en el caso de que un registro ya haya sido eliminado por otro usuario). En este caso, el proveedor devuelve advertencias a la colección [Errors](errors-collection-ado.md) pero no detiene la ejecución del programa. Solo se produce un error en tiempo de ejecución si existen conflictos en todos los registros solicitados. Use la propiedad [Status](status-property-ado-recordset.md) para buscar registros con conflictos.

El establecimiento de la propiedad **Filter** en una cadena de longitud cero ("") tiene el mismo efecto que el uso de la constante **adFilterNone**.

Siempre que se establece la propiedad **Filter**, la posición del registro actual se mueve al primer registro del subconjunto filtrado de registros del objeto **Recordset**. Igualmente, cuando se borra la propiedad **Filter**, la posición del registro actual se mueve al primer registro del objeto **Recordset**.

Vea la propiedad [Bookmark](bookmark-property-ado.md) para obtener una explicación de los valores de marcador a partir de los que se puede construir una matriz para utilizarla con la propiedad **Filter**.

Solo los **filtros** en forma de cadenas de criterios (por ejemplo, OrderDate \> ' 12/31/1999 ') afectan al contenido de un **objeto Recordset** persistente. Los **filtros** creados con una matriz de **marcadores** o mediante un valor de **FilterGroupEnum** no afectarán al contenido del objeto Recordset persistente. Estas reglas se aplican a los objetos **Recordset** creados con cursores cliente o servidor.

> [!NOTE]
> [!NOTA] Cuando se aplica la marca **adFilterPendingRecords** a un objeto **Recordset** filtrado y modificado en el modo de actualización por lotes, el objeto **Recordset** resultante estará vacío si el filtrado se ha basado en el campo clave de una tabla de una única clave y la modificación se ha realizado en los valores del campo clave. El objeto **Recordset** resultante no estará vacío si se cumple una de las siguientes condiciones:
> - El filtrado se ha basado en campos sin clave de una tabla con una única clave.
> - El filtrado se ha basado en cualquier campo de una tabla con varias claves.
> - Las modificaciones se han realizado en campos sin clave de una tabla con una única clave.
> - Las modificaciones se han realizado en cualquier campo de una tabla con varias claves.

En la siguiente tabla se resumen los efectos de **adFilterPendingRecords** sobre diferentes combinaciones de filtrado y modificaciones. En la columna de la izquierda se muestran las posibles modificaciones; éstas se pueden realizar en cualquiera de los campos sin clave, en el campo clave de una tabla con una única clave o en cualquiera de los campos clave de una tabla con varias claves. En la fila superior se muestra el criterio de filtrado; éste puede basarse en cualquiera de los campos sin clave, en el campo clave de una tabla con una única clave o en cualquiera de los campos clave de una tabla con varias claves. En las celdas de intersección se muestran los resultados: + significa que la aplicación de **adFilterPendingRecords** da lugar a un objeto **Recordset** no vacío; **-** significa un objeto **Recordset** vacío.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
</p></th>
<th><p>Sin clave</p></th>
<th><p>Clave única</p></th>
<th><p>Varias claves</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Sin clave</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
</tr>
<tr class="even">
<td><p>Clave única</p></td>
<td><p>+</p></td>
<td><p>-</p></td>
<td><p>N/D</p></td>
</tr>
<tr class="odd">
<td><p>Varias claves</p></td>
<td><p>+</p></td>
<td><p>N/D</p></td>
<td><p>+</p></td>
</tr>
</tbody>
</table>

