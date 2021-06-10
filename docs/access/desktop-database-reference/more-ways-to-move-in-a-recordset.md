---
title: Más formas de moverse en un conjunto de registros
TOCTitle: More ways to move in a Recordset
ms:assetid: ae49b20e-0050-c44b-67e9-7e39de5098c4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249822(v=office.15)
ms:contentKeyID: 48547067
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2d10a493aac39934a047c6fa311233fd6c9fac4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288865"
---
# <a name="more-ways-to-move-in-a-recordset"></a>Más formas de moverse en un conjunto de registros

**Se aplica a:** Access 2013, Office 2013

Los cuatro métodos siguientes sirven para moverse o desplazarse por el **conjunto de registros**: [MoveFirst, MoveLast, MoveNext y MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) (algunos de estos métodos no están disponibles con cursores de sólo avance).

**MoveFirst** cambia la posición del registro activo al primer registro del **conjunto de registros**. **MoveLast** cambia la posición del registro activo al último registro del **conjunto de registros**. Para utilizar **MoveFirst** o **MoveLast**, el objeto **Recordset** debe admitir marcadores o movimiento de cursor hacia atrás; de lo contrario, la llamada al método generará un error.

**MoveNext** hace avanzar una posición el registro activo. Si está en el último registro cuando llama a **MoveNext**, **EOF** se establece en **True**. **MovePrevious** hace retroceder una posición el registro activo. Si está en el primer registro cuando llama a **MovePrevious**, **BOF** se establece en **True**. Es aconsejable revisar las propiedades **EOF** y **BOF** cuando se utilizan estos métodos y devolver el cursor a una posición válida de registro activo si se sale de cualquier extremo del **conjunto de registros**, como se muestra aquí:

```vb
. . . 
oRs.MoveNext 
If oRs.EOF Then oRs.MoveLast 
. . . 
```

O, en el caso del método **MovePrevious**:

```vb
. . . 
oRs.MovePrevious 
If oRs.BOF Then oRs.MoveFirst 
. . . 
```

En casos en los que se filtra u ordena el **conjunto de registros** y se cambian los datos del registro activo, es posible que también cambie la posición. En estos casos, el método **MoveNext** funciona normalmente, pero hay que tener en cuenta que la posición ha avanzado un registro respecto a la nueva posición, no respecto a la antigua. Por ejemplo, cambiar los datos del registro actual, de modo que el registro se mueva al final del objeto **Recordset** ordenado , significaría que llamar a **MoveNext** da como resultado que ADO establece el registro actual en la posición posterior al último registro del **objeto Recordset** (**EOF**  =  **True**).

El comportamiento de los diversos métodos Move del objeto **Recordset** depende, hasta cierto punto, de los datos contenidos en el **conjunto de registros**. Los nuevos registros agregados al **conjunto de registros** se agregan inicialmente en un orden determinado, que define el origen de datos y que puede depender implícita o explícitamente de los datos del nuevo registro. Por ejemplo, si se realiza una ordenación o una combinación dentro de la consulta que rellena el **conjunto de registros**, el nuevo registro se insertará en la posición apropiada en el **conjunto de registros**. Si la ordenación no se especifica explícitamente al crear el **conjunto de registros**, los cambios en la implementación del origen de datos podrían provocar que la ordenación de las filas devueltas cambiase inadvertidamente. Además, las funciones de ordenación, filtro y edición del **conjunto de registros** pueden afectar al orden y, posiblemente, a las filas del conjunto de registros que estarán visibles.

Por lo tanto, a los métodos **MoveNext**, **MovePrevious**, **MoveFirst**, **MoveLast** y **Move** les afectan otras operaciones que se realicen con el mismo **conjunto de registros**. ADO siempre tratará de mantener la posición activa hasta que usted la mueva explícitamente, pero algunos cambios que se efectúen pueden hacer que resulte difícil comprender los efectos de un movimiento posterior. Por ejemplo, si se llama a **MoveFirst** para colocarse en la primera fila de un **conjunto de registros** ordenado y se cambia la ordenación de ascendente a descendente, se seguirá estando en la misma fila, pero ahora será la última del **conjunto de registros**. **MoveFirst** le llevará a otra fila (la nueva primera fila).

Otro ejemplo: si usted se sitúa en una fila determinada en medio de un **conjunto de registros** y llama a **Delete** y, a continuación, llama a **MoveNext**, pasará a estar en el registro inmediatamente posterior al registro eliminado. Pero si llama a **MovePrevious**, el registro anterior al que se ha eliminado pasará a ser el registro activo, puesto que el registro eliminado ya no se considera perteneciente al **conjunto de registros**.

Resulta especialmente complicado definir incoherentemente la semántica de movimientos para todos los proveedores, para métodos que realizan desplazamientos respecto al registro activo (**MovePrevious**, **MoveNext** y **Move**) frente a cambiar datos del registro activo. Por ejemplo, si trabaja con un **conjunto de registros** ordenado y filtrado y cambia los datos del registro activo para que preceda a todos los demás registros, pero además, los datos modificados ya no coinciden con el filtro, no queda claro dónde le llevará una operación **MoveNext**. La conclusión más cierta es que el movimiento relativo dentro de un **conjunto de registros** es más arriesgado que el movimiento absoluto (como el uso de **MoveFirst** o **MoveLast**) cuando los datos cambian mientras se editan, agregan o eliminan registros. La ordenación y el filtrado se deberían basar en una clave principal o un identificador, ya que este tipo de valor no debería cambiar.

