---
title: Cláusula de forma Append
TOCTitle: Shape Append clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40c35e8b2c3fb3f0b92bf261b62c252a61a367b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306450"
---
# <a name="shape-append-clause"></a>Cláusula de forma Append


**Se aplica a:** Access 2013, Office 2013

La cláusula APPEND del comando Shape anexa una o varias columnas a un objeto **Recordset**. Estas columnas suelen ser columnas de capítulo, que hacen referencia a un objeto secundario de **Recordset**.

## <a name="syntax"></a>Sintaxis

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a>Descripción

Esta cláusula se compone de los siguientes elementos:

- *comando primario*

- Cero o uno de los siguientes comandos (se puede omitir el *comando primario* en su totalidad):
    
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

  - Columna del objeto **Recordset** que devuelve el *comando primario*.

- *columna secundaria*

  - Columna del objeto **Recordset** que devuelve el *comando secundario*.

- *número de parámetros*

  - Vea [Funcionamiento de los comandos parametrizados](operation-of-parameterized-commands.md).

- *alias de capítulo*

  - Alias que hace referencia a la columna de capítulo anexada a la columna primaria.


> [!NOTE]
> - La cláusula _"columna primaria TO columna secundaria"_ es en realidad una lista, donde cada relación definida viene separada por una coma.
> - La cláusula situada detrás de la palabra clave APPEND es en realidad una lista donde cada cláusula viene separada por una coma y define otra columna que se va a anexar a la columna primaria.



## <a name="remarks"></a>Comentarios

Al crear comandos de proveedor a partir de datos proporcionados por el usuario como parte de un comando SHAPE, este comando tratará el comando de proveedor proporcionado por el usuario como una cadena opaca y lo pasará fielmente al proveedor. Por ejemplo en el siguiente comando SHAPE,

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

SHAPE ejecutará dos comandos: seleccione \* de t1 y (seleccione \* de t2 RELATE k1 A k2). Si el usuario proporciona un comando compuesto formado por varios comandos de proveedor separados por signos de punto de coma, SHAPE no es capaz de discernir la diferencia. Por lo tanto, en el siguiente comando SHAPE,

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

SHAPE ejecuta select \* from t1; drop table t1 and (select \* from t2 RELATE k1 TO k2), not inging that drop table t1 is a separate and in this case, dangerous, provider command. Las aplicaciones siempre deben validar los datos proporcionados por el usuario para evitar que se produzcan esos posibles ataques de piratas informáticos.

Esta sección incluye los siguientes temas:

- [Operación de comandos sin parámetros](operation-of-non-parameterized-commands.md)

- [Operación de comandos parametrizados](operation-of-parameterized-commands.md)

- [Comandos híbridos](hybrid-commands.md)

- [Cláusulas COMPUTE de formas intervenidas](intervening-shape-compute-clauses.md)
