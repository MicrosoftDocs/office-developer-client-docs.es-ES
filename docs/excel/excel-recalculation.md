---
title: Actualización de Excel
manager: kelbow
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- forced calculation [excel 2007],selective recalculation [Excel 2007],functions [Excel 2007], volatile,calculation modes,recalculated cells [Excel 2007],dependence [Excel 2007],specified worksheet calculation [Excel 2007],recalculation [Excel 2007],workbook tree rebuild [Excel 2007],range calculation [Excel 2007],Excel recalculation,volatile functions [Excel 2007],functions [Excel 2007], non-volatile,active worksheet calculation [Excel 2007],dirty cells [Excel 2007],non-volatile functions [Excel 2007],forced recalculation [Excel 2007]
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: c4b6dbad7a31b7155d1bec3a5c867b6c74d0ff42
ms.sourcegitcommit: 35b723efe168ae4bad461bd16b26f9a2412656f2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "53139096"
---
# <a name="excel-recalculation"></a>Actualización de Excel

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
El usuario puede desencadenar la actualización en Microsoft Excel de varias maneras, por ejemplo:
  
- Introducir nuevos datos (si Excel se encuentra en modo Actualización automática, que se describe más adelante en este tema).
    
- Indicar explícitamente a Excel recalcular todo o parte de un libro.
    
- Eliminar o insertar una fila o columna.
    
- Guardar un libro mientras la opción **Recalcular antes de guardar** está configurada. 
    
- Realizar determinadas acciones Filtro automático.
    
- Hacer doble clic en un divisor de fila o columna (en modo Actualización automática).
    
- Agregar, editar o eliminar un nombre definido.
    
- Cambiar el nombre de una hoja de cálculo.
    
- Cambiar la posición de una hoja de cálculo en relación a otras hojas de cálculo.
    
- Ocultar o mostrar filas, pero no columnas.
    
> [!NOTE]
> En este tema no distingue entre el usuario que presiona directamente una tecla o hace clic en el mouse, y las tareas que realiza un comando o una macro. El usuario ejecuta el comando, o hace algo para que el comando se ejecute, de modo que se considera una acción del usuario. Por lo tanto, la frase "el usuario" también significa "el usuario, o un comando o proceso iniciado por el usuario." 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a>Dependencia, celdas desfasadas y celdas recalculadas

En Excel, el cálculo de hojas de cálculo se puede ver como un proceso de tres fases:
  
1. Construcción de un árbol de dependencias
    
2. Construcción de una cadena de cálculo
    
3. Actualización de las celdas
    
El árbol de dependencias informa a Excel de las celdas que dependen de otras, o de igual forma, las celdas que son precedentes para otras. Desde este árbol, Excel construye una cadena de cálculo. La cadena de cálculo muestra todas las celdas que contienen fórmulas en el orden en que se deben calcular. Durante la actualización, Excel revisa esta cadena si encuentra una fórmula que depende de una celda que aún no se ha calculado. En este caso, la celda que se calcula y sus dependientes se mueven hacia abajo en la cadena. Por este motivo, a menudo se pueden mejorar los tiempos de cálculo en una hoja de cálculo que se ha abierto en los primeros ciclos de cálculo.
  
Cuando se realiza un cambio estructural en un libro, por ejemplo, cuando se introduce una nueva fórmula, Excel reconstruye la cadena de cálculo y el árbol de dependencias. Cuando se introducen nuevos datos o fórmulas, Excel marca todas las celdas que dependen de los nuevos datos según necesiten actualizarse. Las celdas marcadas como de esta forma se conocen como  *desfasadas*  . Todos los dependientes directos e indirectos se marcan como desfasados, de modo que si B1 depende de A1 y C1 depende de B1, al cambiar A1, B1 y C1 se marcan como desfasados. 
  
Si una celda depende, directa o indirectamente, de sí misma, Excel detecta la referencia circular y advierte al usuario. Normalmente es una condición de error que el usuario debe corregir y Excel proporciona herramientas gráficas y navegación muy útiles para ayudar a los usuarios a encontrar el origen de la dependencia circular. En algunos casos, es posible que quiera que esta condición exista deliberadamente. Por ejemplo, puede que quiera ejecutar un cálculo iterativo donde el punto de inicio para la siguiente iteración sea el resultado de la iteración anterior. Excel admite el control de los cálculos iterativos mediante el cuadro de diálogo Opciones de cálculo.
  
Después de marcar las celdas como desfasadas, después de realizar la actualización a continuación, Excel vuelve a evaluar el contenido de cada celda desfasada en el orden determinado por la cadena de cálculo. En el ejemplo anterior, esto significa que B1 es la primera y C1 la siguiente. Esta actualización ocurre inmediatamente después de que Excel termine de marcar las celdas como desfasadas si el modo de actualización es automático; de lo contrario, ocurre posteriormente.
  
A partir de Microsoft Excel 2002, el objeto **Range** de Microsoft Visual Basic para aplicaciones (VBA) admite un método, **Range.Dirty**, que marca las celdas como que necesitan un cálculo. Cuando se usa junto con el método **Range.Calculate** (consulte la siguiente sección), permite la actualización forzada de las celdas de un rango determinado. Esto resulta útil al realizar un cálculo limitado durante una macro, donde se configura el modo de cálculo manual, para evitar la sobrecarga de celdas de cálculo no relacionadas con la función de la macro. Los métodos de cálculo del rango no están disponibles a través de la API de C. 
  
En Excel 2002 y versiones anteriores, Excel compila una cadena de cálculo para cada hoja de cálculo de cada libro abierto. Esto resultaba complejo en la forma en que se gestionaban los vínculos entre hojas de cálculo y necesitaba cierto cuidado para garantizar una actualización eficaz. En concreto, en Excel 2000, debería minimizar las dependencias entre hojas de cálculo y las hojas de cálculo de nombres en orden alfabético para que las hojas que dependían de otras hojas aparecieran alfabéticamente después de las hojas de las que dependían.
  
En Excel 2007, se ha mejorado la lógica para habilitar la actualización en varios subprocesos para que las secciones de la cadena de cálculo no sean interdependientes y se puedan calcular a la vez. Puede configurar Excel para usar varios subprocesos en un equipo con procesador único o en un único subproceso de un equipo con varios procesadores o varios núcleos. 
  
## <a name="asynchronous-user-defined-functions-udfs"></a>Funciones asincrónicas definidas por el usuario (UDF)

Cuando un cálculo encuentra un UDF asincrónico, guarda el estado de la fórmula actual, inicia la UDF y sigue evaluando el resto de celdas. Cuando el cálculo finaliza la evaluación de las celdas, Excel espera a que las funciones asincrónicas se completen, si hay funciones asincrónicas en ejecución. Ya que cada función asincrónica informa de los resultados, Excel finaliza la fórmula y ejecuta un nuevo paso de cálculo para volver a calcular las celdas que usan la celda con la referencia a la función asincrónica.
  
## <a name="volatile-and-non-volatile-functions"></a>Funciones volátiles y no volátiles

Excel admite el concepto de una función volátil, es decir, una cuyo valor no se puede suponer que sea el mismo que la de la siguiente, incluso si ninguno de los argumentos (si toma alguno) ha cambiado. Excel vuelve a evaluar las celdas que contienen funciones volátiles, junto con todos los dependientes, cada vez que actualiza. Por este motivo, confiar demasiado en las funciones volátiles puede hacer que los tiempos de actualización sean lentos. Úselas con moderación.
  
Las siguientes funciones de Excel son volátiles:
  
- **NOW**
    
- **TODAY**
    
- **RANDBETWEEN**
    
- **OFFSET**
    
- **INDIRECT**
    
- **INFO** (en función de sus argumentos) 
    
- **CELL** (en función de sus argumentos) 
    
- **SUMIF** (en función de sus argumentos) 
    
La API de C y VBA admiten maneras para informar a Excel que una función definida por el usuario (UDF) debe tratarse como volátil. Con VBA, UDF se declara como volátil del siguiente modo.
  
```vba
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile MakeMeVolatile
   MyUDF = Now
End Function

```

De forma predeterminada, Excel asume que las UDF de VBA no son volátiles. Excel solo descubre que una UDF es volátil cuando la llama en primer lugar. Una UDF volátil se puede volver a cambiar a no volátil, como en este ejemplo.
  
Con la API de C, puede registrar una función XLL como volátil antes de la primera llamada. También le permite alternar el estado volátil de una función de hoja de cálculo.
  
De forma predeterminada, Excel trata las UDF de XLL que toman argumentos de rango y que se declaran como equivalentes de hojas macros como volátiles. Puede desactivar este estado predeterminado con la función **xlfVolatile** al llamar a la UDF por primera vez. 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a>Modos de cálculo, comandos, actualización selectiva y tablas de datos

Excel tiene tres modos de cálculo:
  
- Automatic
    
- Automático excepto en tablas
    
- Manual
    
Cuando se configura el cálculo en automático, la actualización ocurre después de cada entrada de datos y de determinados eventos, como los ejemplos de la sección anterior. Los libros grandes, el tiempo de actualización podría ser tan largo que los usuarios deberían limitar el momento en que esto ocurre, es decir, actualizar solo cuando sea necesario. Para habilitarlo, Excel admite el modo manual. El usuario puede seleccionar el modo en el sistema de menús de Excel o mediante programación con la API de C, COM o VBA.
  
Las tablas de datos son estructuras especiales de una hoja de cálculo. En primer lugar, el usuario configura el cálculo de un resultado de una hoja de cálculo. Esto depende de una o dos entradas modificables clave y otros parámetros. Luego, el usuario puede crear una tabla de resultados para un conjunto de valores para una o ambas entradas clave. La tabla se crea con el **Asistente para tablas de datos**. Después de configurar la tabla, Excel inserta las entradas de una en una en el cálculo y copia el valor resultante en la tabla. Como se pueden usar una o dos entradas, las tablas de datos pueden ser de una o dos dimensiones. 
  
La actualización de las tablas de datos se trata de manera diferente:
  
- La actualización se controla de forma asincrónica para la actualización de libros normales de modo que las tablas de gran tamaño pueden tardar más en actualizarse que el resto del libro.
    
- Se toleran las referencias circulares. Si el cálculo que se usa para obtener el resultado depende de uno o varios valores de la tabla de datos, Excel no devuelve un error para la dependencia circular. 

- Las tablas de datos no usan cálculos multiproceso.
    
Dada la forma distinta en que Excel gestiona la actualización de las tablas de datos, y el hecho de que las tablas de gran tamaño que dependen de cálculos largos o complejos pueden tardar mucho tiempo en calcularse, Excel permite deshabilitar el cálculo automático de tablas de datos. Para ello, configure el modo de cálculo en Automático excepto en tablas de datos. Cuando el cálculo se encuentra en este modo, el usuario actualiza las tablas de datos presionando F9 o alguna operación de programación equivalente.
  
Excel expone métodos a través de los cuales puede modificar el modo de actualización y controlarla. Estos métodos se han mejorado de versión a versión para permitir un control más preciso. En este sentido, las capacidades de la API de C reflejan las que estaban disponibles en la versión 5 de Excel y, por lo tanto, no proporcionan el mismo control que tenía con VBA en las versiones más recientes. 
  
Estos métodos, que se usan con más frecuencia cuando Excel está en modo de cálculo manual, permiten el cálculo selectivo de libros, hojas de cálculo y rangos, una actualización completa de todos los libros abiertos e incluso completar la recompilación de la cadena de cálculo y del árbol de dependencias.
  
### <a name="range-calculation"></a>Cálculo de rango

Pulsación de tecla: ninguno
  
VBA: **Range.Calculate** (a partir de Excel 2000, modificado en Excel 2007) y **Range.CalculateRowMajorOrder** (a partir de Excel 2007) 
  
API de C: no se admite
  
- **Modo manual**
    
    Actualiza solo las celdas del rango especificado independientemente de si están desfasadas o no. El comportamiento del método **Range.Calculate** ha cambiado en Excel 2007; sin embargo, el método **Range.CalculateRowMajorOrder** sigue admitiendo el comportamiento anterior. 
    
- **Modos Automático o Automático excepto en tablas**
    
    Actualiza el libro pero no fuerza la actualización del rango o de las celdas del rango.
    
### <a name="active-worksheet-calculation"></a>Cálculo de la hoja de cálculo activa

Pulsación de tecla: MAYÚS+F9
  
VBA: **ActiveSheet.Calculate**
  
API DE C: **xlcCalculateDocument**
  
- **Todos los modos**
    
    Actualiza las celdas marcadas para el cálculo solo en la hoja de cálculo activa.
    
### <a name="specified-worksheet-calculation"></a>Cálculo de la hoja de cálculo especificada

Pulsación de tecla: ninguno
  
VBA: **Worksheets(** referencia **).Calculate**
  
API de C: no se admite
  
- **Todos los modos**
    
    Actualiza las celdas desfasadas y sus dependientes solo dentro de la hoja de cálculo especificada. La referencia es el nombre de la hoja de cálculo como una cadena o el número de índice del libro relevante.
    
    Excel 2000 y las versiones posteriores exponen una propiedad **Boolean** de hoja de cálculo, la propiedad **EnableCalculation**. Si se configura en **True** desde **False** desfasa todas las celdas de la hoja de cálculo especificada. En los modos automáticos, también desencadena la actualización de todo el libro. 
    
    En el modo manual, el siguiente código provoca la actualización solo de la hoja activa.
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a>Recompilación y actualización forzada del árbol de libro

Pulsación de tecla: CTRL+ALT+MAYÚS+F9 (a partir de Excel 2002)
  
VBA: **Workbooks(** referencia **).ForceFullCalculation** (a partir de Excel 2007) 
  
API de C: no se admite
  
- **Todos los modos**
    
    Hace que Excel recompile el árbol de dependencias y la cadena de cálculo de un libro determinado y fuerza una actualización de todas las celdas que contienen fórmulas.
    
### <a name="all-open-workbooks"></a>Todos los libros abiertos

Pulsación de tecla: F9
  
VBA: **Application.Calculate**
  
API de C: **xlcCalculateNow**
  
- **Todos los modos**
    
    Actualiza todas las celdas que Excel marca como desfasadas, es decir, los dependientes de datos volátiles o modificados, y las celdas marcadas mediante programación como desfasadas. Si el modo de cálculo es Automático excepto en tablas, se calculan las tablas que necesiten una actualización y también todas las funciones volátiles y sus dependientes.
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a>Recompilación y cálculo forzado de todos árboles de libros

Pulsación de tecla: CTRL+ALT+F9
  
VBA: **Application.CalculateFull**
  
API de C: no se admite
  
- **Todos los modos**
    
    Actualiza todas las celdas de todos los libros abiertos. Si el modo de cálculo es Automático excepto en tablas, fuerza la actualización de las tablas.
    
## <a name="see-also"></a>Vea también



[Actualización multiproceso en Excel](multithreaded-recalculation-in-excel.md)
  
[Tipos de datos utilizados por Excel](data-types-used-by-excel.md)
  
[Administración de memoria en Excel](memory-management-in-excel.md)
  
[Conceptos de programación de Excel](excel-programming-concepts.md)

