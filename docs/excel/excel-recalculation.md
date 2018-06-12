---
title: Actualizaci�n de Excel
manager: kelbow
ms.date: 03/09/2018
ms.audience: Developer
ms.topic: overview
keywords:
- forced calculation [excel 2007],selective recalculation [Excel 2007],functions [Excel 2007], volatile,calculation modes,recalculated cells [Excel 2007],dependence [Excel 2007],specified worksheet calculation [Excel 2007],recalculation [Excel 2007],workbook tree rebuild [Excel 2007],range calculation [Excel 2007],Excel recalculation,volatile functions [Excel 2007],functions [Excel 2007], non-volatile,active worksheet calculation [Excel 2007],dirty cells [Excel 2007],non-volatile functions [Excel 2007],forced recalculation [Excel 2007]
localization_priority: Normal
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9964f2c4282158e83891d82ba43fa19f23ab1eb6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815598"
---
# <a name="excel-recalculation"></a>Actualizaci�n de Excel

 **Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
El usuario puede desencadenar la actualizaci�n en Microsoft Excel de varias maneras, por ejemplo:
  
- Introducir nuevos datos (si Excel se encuentra en modo Actualizaci�n autom�tica, que se describe m�s adelante en este tema).
    
- Indicar expl�citamente a Excel recalcular todo o parte de un libro.
    
- Eliminar o insertar una fila o columna.
    
- Guardar un libro mientras la opci�n **Recalcular antes de guardar** est� configurada. 
    
- Realizar determinadas acciones Filtro autom�tico.
    
- Hacer doble clic en un divisor de fila o columna (en modo Actualizaci�n autom�tica).
    
- Agregar, editar o eliminar un nombre definido.
    
- Cambiar el nombre de una hoja de c�lculo.
    
- Cambiar la posici�n de una hoja de c�lculo en relaci�n a otras hojas de c�lculo.
    
- Ocultar o mostrar filas, pero no columnas.
    
> [!NOTE]
> [!NOTA] En este tema no distingue entre el usuario que presiona directamente una tecla o hace clic en el mouse, y las tareas que realiza un comando o una macro. El usuario ejecuta el comando, o hace algo para que el comando se ejecute, de modo que se considera una acci�n del usuario. Por lo tanto, la frase "el usuario" tambi�n significa "el usuario, o un comando o proceso iniciado por el usuario." 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a>Dependencia, celdas desfasadas y celdas recalculadas

En Excel, el c�lculo de hojas de c�lculo se puede ver como un proceso de tres fases:
  
1. Construcci�n de un �rbol de dependencias
    
2. Construcci�n de una cadena de c�lculo
    
3. Actualizaci�n de las celdas
    
El �rbol de dependencias informa a Excel de las celdas que dependen de otras, o de igual forma, las celdas que son precedentes para otras. Desde este �rbol, Excel construye una cadena de c�lculo. La cadena de c�lculo muestra todas las celdas que contienen f�rmulas en el orden en que se deben calcular. Durante la actualizaci�n, Excel revisa esta cadena si encuentra una f�rmula que depende de una celda que a�n no se ha calculado. En este caso, la celda que se calcula y sus dependientes se mueven hacia abajo en la cadena. Por este motivo, a menudo se pueden mejorar los tiempos de c�lculo en una hoja de c�lculo que se ha abierto en los primeros ciclos de c�lculo.
  
Cuando se realiza un cambio estructural en un libro, por ejemplo, cuando se introduce una nueva f�rmula, Excel reconstruye la cadena de c�lculo y el �rbol de dependencias. Cuando se introducen nuevos datos o f�rmulas, Excel marca todas las celdas que dependen de los nuevos datos seg�n necesiten actualizarse. Las celdas marcadas como de esta forma se conocen como  *desfasadas*  . Todos los dependientes directos e indirectos se marcan como desfasados, de modo que si B1 depende de A1 y C1 depende de B1, al cambiar A1, B1 y C1 se marcan como desfasados. 
  
Si una celda depende, directa o indirectamente, de s� misma, Excel detecta la referencia circular y advierte al usuario. Normalmente es una condici�n de error que el usuario debe corregir y Excel proporciona herramientas gr�ficas y navegaci�n muy �tiles para ayudar a los usuarios a encontrar el origen de la dependencia circular. En algunos casos, es posible que quiera que esta condici�n exista deliberadamente. Por ejemplo, puede que quiera ejecutar un c�lculo iterativo donde el punto de inicio para la siguiente iteraci�n sea el resultado de la iteraci�n anterior. Excel admite el control de los c�lculos iterativos mediante el cuadro de di�logo Opciones de c�lculo.
  
Despu�s de marcar las celdas como desfasadas, despu�s de realizar la actualizaci�n a continuaci�n, Excel vuelve a evaluar el contenido de cada celda desfasada en el orden determinado por la cadena de c�lculo. En el ejemplo anterior, esto significa que B1 es la primera y C1 la siguiente. Esta actualizaci�n ocurre inmediatamente despu�s de que Excel termine de marcar las celdas como desfasadas si el modo de actualizaci�n es autom�tico; de lo contrario, ocurre posteriormente.
  
A partir de Microsoft Excel 2002, el objeto **Range** de Microsoft Visual Basic para aplicaciones (VBA) admite un m�todo, **Range.Dirty**, que marca las celdas como que necesitan un c�lculo. Cuando se usa junto con el m�todo **Range.Calculate** (consulte la siguiente secci�n), permite la actualizaci�n forzada de las celdas de un rango determinado. Esto resulta �til al realizar un c�lculo limitado durante una macro, donde se configura el modo de c�lculo manual, para evitar la sobrecarga de celdas de c�lculo no relacionadas con la funci�n de la macro. Los m�todos de c�lculo del rango no est�n disponibles a trav�s de la API de C. 
  
En Excel 2002 y versiones anteriores, Excel compila una cadena de c�lculo para cada hoja de c�lculo de cada libro abierto. Esto resultaba complejo en la forma en que se gestionaban los v�nculos entre hojas de c�lculo y necesitaba cierto cuidado para garantizar una actualizaci�n eficaz. En concreto, en Excel 2000, deber�a minimizar las dependencias entre hojas de c�lculo y las hojas de c�lculo de nombres en orden alfab�tico para que las hojas que depend�an de otras hojas aparecieran alfab�ticamente despu�s de las hojas de las que depend�an.
  
En Excel 2007, se ha mejorado la l�gica para habilitar la actualizaci�n en varios subprocesos para que las secciones de la cadena de c�lculo no sean interdependientes y se puedan calcular a la vez. Puede configurar Excel para usar varios subprocesos en un equipo con procesador �nico o en un �nico subproceso de un equipo con varios procesadores o varios n�cleos. 
  
## <a name="asynchronous-user-defined-functions-udfs"></a>Funciones asincr�nicas definidas por el usuario (UDF)

Cuando un c�lculo encuentra un UDF asincr�nico, guarda el estado de la f�rmula actual, inicia la UDF y sigue evaluando el resto de celdas. Cuando el c�lculo finaliza la evaluaci�n de las celdas, Excel espera a que las funciones asincr�nicas se completen, si hay funciones asincr�nicas en ejecuci�n. Ya que cada funci�n asincr�nica informa de los resultados, Excel finaliza la f�rmula y ejecuta un nuevo paso de c�lculo para volver a calcular las celdas que usan la celda con la referencia a la funci�n asincr�nica.
  
## <a name="volatile-and-non-volatile-functions"></a>Funciones vol�tiles y no vol�tiles

Excel admite el concepto de una funci�n vol�til, es decir, una cuyo valor no se puede suponer que sea el mismo que la de la siguiente, incluso si ninguno de los argumentos (si toma alguno) ha cambiado. Excel vuelve a evaluar las celdas que contienen funciones vol�tiles, junto con todos los dependientes, cada vez que actualiza. Por este motivo, confiar demasiado en las funciones vol�tiles puede hacer que los tiempos de actualizaci�n sean lentos. �selas con moderaci�n.
  
Las siguientes funciones de Excel son vol�tiles:
  
- **NOW**
    
- **TODAY**
    
- **RANDBETWEEN**
    
- **OFFSET**
    
- **INDIRECT**
    
- **INFO** (en funci�n de sus argumentos) 
    
- **CELL** (en funci�n de sus argumentos) 
    
- **SUMIF** (en función de sus argumentos) 
    
La API de C y VBA admiten maneras para informar a Excel que una funci�n definida por el usuario (UDF) debe tratarse como vol�til. Con VBA, UDF se declara como vol�til del siguiente modo.
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

De forma predeterminada, Excel asume que las UDF de VBA no son vol�tiles. Excel solo descubre que una UDF es vol�til cuando la llama en primer lugar. Una UDF vol�til se puede volver a cambiar a no vol�til, como en este ejemplo.
  
Con la API de C, puede registrar una funci�n XLL como vol�til antes de la primera llamada. Tambi�n le permite alternar el estado vol�til de una funci�n de hoja de c�lculo.
  
De forma predeterminada, Excel trata las UDF de XLL que toman argumentos de rango y que se declaran como equivalentes de hojas macros como vol�tiles. Puede desactivar este estado predeterminado con la funci�n **xlfVolatile** al llamar a la UDF por primera vez. 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a>Modos de c�lculo, comandos, actualizaci�n selectiva y tablas de datos

Excel tiene tres modos de c�lculo:
  
- Autom�tico
    
- Autom�tico excepto en tablas
    
- Manual
    
Cuando se configura el c�lculo en autom�tico, la actualizaci�n ocurre despu�s de cada entrada de datos y de determinados eventos, como los ejemplos de la secci�n anterior. Los libros grandes, el tiempo de actualizaci�n podr�a ser tan largo que los usuarios deber�an limitar el momento en que esto ocurre, es decir, actualizar solo cuando sea necesario. Para habilitarlo, Excel admite el modo manual. El usuario puede seleccionar el modo en el sistema de men�s de Excel o mediante programaci�n con la API de C, COM o VBA.
  
Las tablas de datos son estructuras especiales de una hoja de c�lculo. En primer lugar, el usuario configura el c�lculo de un resultado de una hoja de c�lculo. Esto depende de una o dos entradas modificables clave y otros par�metros. Luego, el usuario puede crear una tabla de resultados para un conjunto de valores para una o ambas entradas clave. La tabla se crea con el **Asistente para tablas de datos**. Despu�s de configurar la tabla, Excel inserta las entradas de una en una en el c�lculo y copia el valor resultante en la tabla. Como se pueden usar una o dos entradas, las tablas de datos pueden ser de una o dos dimensiones. 
  
La actualizaci�n de las tablas de datos se trata de manera diferente:
  
- La actualizaci�n se controla de forma asincr�nica para la actualizaci�n de libros normales de modo que las tablas de gran tama�o pueden tardar m�s en actualizarse que el resto del libro.
    
- Se toleran las referencias circulares. Si el c�lculo que se usa para obtener el resultado depende de uno o varios valores de la tabla de datos, Excel no devuelve un error para la dependencia circular. 
    
Dada la forma distinta en que Excel gestiona la actualizaci�n de las tablas de datos, y el hecho de que las tablas de gran tama�o que dependen de c�lculos largos o complejos pueden tardar mucho tiempo en calcularse, Excel permite deshabilitar el c�lculo autom�tico de tablas de datos. Para ello, configure el modo de c�lculo en Autom�tico excepto en tablas de datos. Cuando el c�lculo se encuentra en este modo, el usuario actualiza las tablas de datos presionando F9 o alguna operaci�n de programaci�n equivalente.
  
Excel expone m�todos a trav�s de los cuales puede modificar el modo de actualizaci�n y controlarla. Estos m�todos se han mejorado de versi�n a versi�n para permitir un control m�s preciso. En este sentido, las capacidades de la API de C reflejan las que estaban disponibles en la versi�n 5 de Excel y, por lo tanto, no proporcionan el mismo control que ten�a con VBA en las versiones m�s recientes. 
  
Estos m�todos, que se usan con m�s frecuencia cuando Excel est� en modo de c�lculo manual, permiten el c�lculo selectivo de libros, hojas de c�lculo y rangos, una actualizaci�n completa de todos los libros abiertos e incluso completar la recompilaci�n de la cadena de c�lculo y del �rbol de dependencias.
  
### <a name="range-calculation"></a>C�lculo de rango

Pulsaci�n de tecla: ninguno
  
VBA: **Range.Calculate** (a partir de Excel 2000, modificado en Excel 2007) y **Range.CalculateRowMajorOrder** (a partir de Excel 2007) 
  
API de C: no se admite
  
- **Modo manual**
    
    Actualiza solo las celdas del rango especificado independientemente de si est�n desfasadas o no. El comportamiento del m�todo **Range.Calculate** ha cambiado en Excel 2007; sin embargo, el m�todo **Range.CalculateRowMajorOrder** sigue admitiendo el comportamiento anterior. 
    
- **Modos Autom�tico o Autom�tico excepto en tablas**
    
    Actualiza el libro pero no fuerza la actualizaci�n del rango o de las celdas del rango.
    
### <a name="active-worksheet-calculation"></a>C�lculo de la hoja de c�lculo activa

Pulsaci�n de tecla: MAY�S+F9
  
VBA: **ActiveSheet.Calculate**
  
API DE C: **xlcCalculateDocument**
  
- **Todos los modos**
    
    Actualiza las celdas marcadas para el c�lculo solo en la hoja de c�lculo activa.
    
### <a name="specified-worksheet-calculation"></a>C�lculo de la hoja de c�lculo especificada

Pulsaci�n de tecla: ninguno
  
VBA: **Worksheets(** referencia **).Calculate**
  
API de C: no se admite
  
- **Todos los modos**
    
    Actualiza las celdas desfasadas y sus dependientes solo dentro de la hoja de c�lculo especificada. La referencia es el nombre de la hoja de c�lculo como una cadena o el n�mero de �ndice del libro relevante.
    
    Excel 2000 y las versiones posteriores exponen una propiedad **Boolean** de hoja de c�lculo, la propiedad **EnableCalculation**. Si se configura en **True** desde **False** desfasa todas las celdas de la hoja de c�lculo especificada. En los modos autom�ticos, tambi�n desencadena la actualizaci�n de todo el libro. 
    
    En el modo manual, el siguiente c�digo provoca la actualizaci�n solo de la hoja activa.
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a>Recompilaci�n y actualizaci�n forzada del �rbol de libro

Pulsaci�n de tecla: CTRL+ALT+MAY�S+F9 (a partir de Excel 2002)
  
VBA: **Workbooks(** referencia **).ForceFullCalculation** (a partir de Excel 2007) 
  
API de C: no se admite
  
- **Todos los modos**
    
    Hace que Excel recompile el �rbol de dependencias y la cadena de c�lculo de un libro determinado y fuerza una actualizaci�n de todas las celdas que contienen f�rmulas.
    
### <a name="all-open-workbooks"></a>Todos los libros abiertos

Pulsaci�n de tecla: F9
  
VBA: **Application.Calculate**
  
API de C: **xlcCalculateNow**
  
- **Todos los modos**
    
    Actualiza todas las celdas que Excel marca como desfasadas, es decir, los dependientes de datos vol�tiles o modificados, y las celdas marcadas mediante programaci�n como desfasadas. Si el modo de c�lculo es Autom�tico excepto en tablas, se calculan las tablas que necesiten una actualizaci�n y tambi�n todas las funciones vol�tiles y sus dependientes.
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a>Recompilaci�n y c�lculo forzado de todos �rboles de libros

Pulsaci�n de tecla: CTRL+ALT+F9
  
VBA: **Application.CalculateFull**
  
API de C: no se admite
  
- **Todos los modos**
    
    Actualiza todas las celdas de todos los libros abiertos. Si el modo de c�lculo es Autom�tico excepto en tablas, fuerza la actualizaci�n de las tablas.
    
## <a name="see-also"></a>Vea tambi�n



[Nuevo c�lculo multiproceso en Excel](multithreaded-recalculation-in-excel.md)
  
[Tipos de datos utilizados por Excel](data-types-used-by-excel.md)
  
[Administraci�n de memoria en Excel](memory-management-in-excel.md)
  
[Conceptos de programaci�n de Excel](excel-programming-concepts.md)

