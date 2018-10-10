---
title: Cláusula Append del comando Shape
TOCTitle: Shape Append Clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6460572f44e79fe4bdb30d1ca33810d610da9721
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483840"
---
# <a name="shape-append-clause"></a>Cláusula Append del comando Shape


**Se aplica a**: Access 2013 | Office 2013

La cláusula APPEND del comando Shape anexa una o varias columnas a un objeto **Recordset**. Estas columnas suelen ser columnas de capítulo, que hacen referencia a un objeto secundario de **Recordset**.

## <a name="syntax"></a>Sintaxis

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a>Descripción

Esta cláusula se compone de los siguientes elementos:

- *comando primario*

- Cero o uno de los siguientes (comandos se puede omitir el *comando a primario* en su totalidad):
    
  - Un comando de proveedor entre llaves ("{}") que devuelve un objeto **Recordset**. El comando se emite al proveedor de datos subyacente y su sintaxis depende de los requisitos de ese proveedor. Suele ser el lenguaje SQL, si bien ADO no requiere ningún lenguaje de consulta en particular.
    
  - Otro comando Shape incrustado entre paréntesis.
    
  - La palabra clave TABLE, seguida del nombre de una tabla en el proveedor de datos.

- *alias primario*

  - Alias opcional que hace referencia al objeto **Recordset** primario.

- *lista de columnas*

  - Una o varias de las siguientes columnas:
    
    - Columna agregada.
    
    - Columna calculada.
    
    - Columna nueva creada con la cláusula NEW.
    
    - Columna de capítulo. La definición de la columna de capítulo se encuentra entre paréntesis ("()"). Vea la siguiente sintaxis:


        ```vb 
        
        SHAPE [parent-command [[AS] parent-alias]] 
        APPEND (child-recordset [ [[AS] child-alias] 
        RELATE parent-column TO child-column | PARAMETER param-number, ... ]) 
        [[AS] chapter-alias] 
        [, ... ] 
        ```

- *conjunto de registros secundario*

  - Un comando de proveedor entre llaves ("{}") que devuelve un objeto **Recordset**. El comando se emite al proveedor de datos subyacente y su sintaxis depende de los requisitos de ese proveedor. Suele ser el lenguaje SQL, si bien ADO no requiere ningún lenguaje de consulta en particular.
    
  - Otro comando Shape incrustado entre paréntesis.
    
  - El nombre de un objeto **Recordset** con forma existente.
    
  - La palabra clave TABLE, seguida del nombre de una tabla en el proveedor de datos.

- *alias secundario*

  - Alias que hace referencia al objeto **Recordset** secundario.

- *columna primaria*

  - Una columna en el **conjunto de registros** devuelto por la *comando primario.*

- *columna secundaria*

  - Columna del objeto **Recordset** que devuelve el *comando secundario*.

- *número de parámetros*

  - Vea [Funcionamiento de los comandos parametrizados](operation-of-parameterized-commands.md).

- *alias de capítulo*

  - Alias que hace referencia a la columna de capítulo anexada a la columna primaria.


> [!NOTE]
> - La cláusula _"columna a primaria TO columna a secundaria"_ es en realidad una lista, donde cada relación definida viene separada por una coma.
> - [!NOTA] La cláusula situada detrás de la palabra clave APPEND es en realidad una lista donde cada cláusula viene separada por una coma y define otra columna que se va a anexar a la columna primaria.



## <a name="remarks"></a>Comentarios

Al crear comandos de proveedor a partir de datos proporcionados por el usuario como parte de un comando SHAPE, este comando tratará el comando de proveedor proporcionado por el usuario como una cadena opaca y lo pasará fielmente al proveedor. Por ejemplo en el siguiente comando SHAPE,

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

SHAPE ejecutará dos comandos: seleccione \* from t1 y (seleccione \* from t2 RELATE k1 TO k2). Si el usuario proporciona un comando compuesto formado por varios comandos de proveedor separados por signos de punto de coma, SHAPE no es capaz de discernir la diferencia. Por lo tanto, en el siguiente comando SHAPE,

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

SHAPE ejecuta select \* from t1; DROP table t1 y (seleccione \* from t2 RELATE k1 TO k2), sin darse cuenta de que drop table t1 es un independiente y en este comando de proveedor caso, peligroso. Las aplicaciones siempre deben validar los datos proporcionados por el usuario para evitar que se produzcan esos posibles ataques de piratas informáticos.

