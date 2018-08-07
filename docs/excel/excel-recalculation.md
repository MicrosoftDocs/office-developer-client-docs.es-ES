---
title: Actualización de Excel
manager: kelbow
ms.date: 03/09/2018
ms.audience: Developer
ms.topic: overview
keywords:
- forced calculation [excel 2007],selective recalculation [Excel 2007],functions [Excel 2007], volatile,calculation modes,recalculated cells [Excel 2007],dependence [Excel 2007],specified worksheet calculation [Excel 2007],recalculation [Excel 2007],workbook tree rebuild [Excel 2007],range calculation [Excel 2007],Excel recalculation,volatile functions [Excel 2007],functions [Excel 2007], non-volatile,active worksheet calculation [Excel 2007],dirty cells [Excel 2007],non-volatile functions [Excel 2007],forced recalculation [Excel 2007]
localization_priority: Normal
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9964f2c4282158e83891d82ba43fa19f23ab1eb6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815598"
---
# <a name="excel-recalculation"></a><span data-ttu-id="12e70-104">Actualización de Excel</span><span class="sxs-lookup"><span data-stu-id="12e70-104">Excel Recalculation</span></span>

 <span data-ttu-id="12e70-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="12e70-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="12e70-106">El usuario puede desencadenar la actualización en Microsoft Excel de varias maneras, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="12e70-106">The user can trigger recalculation in Microsoft Excel in several ways, for example:</span></span>
  
- <span data-ttu-id="12e70-107">Introducir nuevos datos (si Excel se encuentra en modo Actualización automática, que se describe más adelante en este tema).</span><span class="sxs-lookup"><span data-stu-id="12e70-107">Entering new data (if Excel is in Automatic recalculation mode, described later in this topic).</span></span>
    
- <span data-ttu-id="12e70-108">Indicar explícitamente a Excel recalcular todo o parte de un libro.</span><span class="sxs-lookup"><span data-stu-id="12e70-108">Explicitly instructing Excel to recalculate all or part of a workbook.</span></span>
    
- <span data-ttu-id="12e70-109">Eliminar o insertar una fila o columna.</span><span class="sxs-lookup"><span data-stu-id="12e70-109">Deleting or inserting a row or column.</span></span>
    
- <span data-ttu-id="12e70-110">Guardar un libro mientras la opción **Recalcular antes de guardar** está configurada.</span><span class="sxs-lookup"><span data-stu-id="12e70-110">Saving a workbook while the **Recalculate before save** option is set.</span></span> 
    
- <span data-ttu-id="12e70-111">Realizar determinadas acciones Filtro automático.</span><span class="sxs-lookup"><span data-stu-id="12e70-111">Performing certain Autofilter actions.</span></span>
    
- <span data-ttu-id="12e70-112">Hacer doble clic en un divisor de fila o columna (en modo Actualización automática).</span><span class="sxs-lookup"><span data-stu-id="12e70-112">Double-clicking a row or column divider (in Automatic calculation mode).</span></span>
    
- <span data-ttu-id="12e70-113">Agregar, editar o eliminar un nombre definido.</span><span class="sxs-lookup"><span data-stu-id="12e70-113">Adding, editing, or deleting a defined name.</span></span>
    
- <span data-ttu-id="12e70-114">Cambiar el nombre de una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="12e70-114">Renaming a worksheet.</span></span>
    
- <span data-ttu-id="12e70-115">Cambiar la posición de una hoja de cálculo en relación a otras hojas de cálculo.</span><span class="sxs-lookup"><span data-stu-id="12e70-115">Changing the position of a worksheet in relation to other worksheets.</span></span>
    
- <span data-ttu-id="12e70-116">Ocultar o mostrar filas, pero no columnas.</span><span class="sxs-lookup"><span data-stu-id="12e70-116">Hiding or unhiding rows, but not columns.</span></span>
    
> [!NOTE]
> <span data-ttu-id="12e70-p101">En este tema no distingue entre el usuario que presiona directamente una tecla o hace clic en el mouse, y las tareas que realiza un comando o una macro. El usuario ejecuta el comando, o hace algo para que el comando se ejecute, de modo que se considera una acción del usuario. Por lo tanto, la frase "el usuario" también significa "el usuario, o un comando o proceso iniciado por el usuario."</span><span class="sxs-lookup"><span data-stu-id="12e70-p101">This topic does not distinguish between the user directly pressing a key or clicking the mouse, and those tasks being done by a command or macro. The user runs the command, or does something to cause the command to run so that it is still considered a user action. Therefore the phrase "the user" also means "the user, or a command or process started by the user."</span></span> 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a><span data-ttu-id="12e70-120">Dependencia, celdas desfasadas y celdas recalculadas</span><span class="sxs-lookup"><span data-stu-id="12e70-120">Dependence, Dirty Cells, and Recalculated Cells</span></span>

<span data-ttu-id="12e70-121">En Excel, el cálculo de hojas de cálculo se puede ver como un proceso de tres fases:</span><span class="sxs-lookup"><span data-stu-id="12e70-121">The calculation of worksheets in Excel can be viewed as a three-stage process:</span></span>
  
1. <span data-ttu-id="12e70-122">Construcción de un árbol de dependencias</span><span class="sxs-lookup"><span data-stu-id="12e70-122">Construction of a dependency tree</span></span>
    
2. <span data-ttu-id="12e70-123">Construcción de una cadena de cálculo</span><span class="sxs-lookup"><span data-stu-id="12e70-123">Construction of a calculation chain</span></span>
    
3. <span data-ttu-id="12e70-124">Actualización de las celdas</span><span class="sxs-lookup"><span data-stu-id="12e70-124">Recalculation of cells</span></span>
    
<span data-ttu-id="12e70-p102">El árbol de dependencias informa a Excel de las celdas que dependen de otras, o de igual forma, las celdas que son precedentes para otras. Desde este árbol, Excel construye una cadena de cálculo. La cadena de cálculo muestra todas las celdas que contienen fórmulas en el orden en que se deben calcular. Durante la actualización, Excel revisa esta cadena si encuentra una fórmula que depende de una celda que aún no se ha calculado. En este caso, la celda que se calcula y sus dependientes se mueven hacia abajo en la cadena. Por este motivo, a menudo se pueden mejorar los tiempos de cálculo en una hoja de cálculo que se ha abierto en los primeros ciclos de cálculo.</span><span class="sxs-lookup"><span data-stu-id="12e70-p102">The dependency tree informs Excel about which cells depend on which others, or equivalently, which cells are precedents for which others. From this tree, Excel constructs a calculation chain. The calculation chain lists all the cells that contain formulas in the order in which they should be calculated. During recalculation, Excel revises this chain if it comes across a formula that depends on a cell that has not yet been calculated. In this case, the cell that is being calculated and its dependents are moved down the chain. For this reason, calculation times can often improve in a worksheet that has just been opened in the first few calculation cycles.</span></span>
  
<span data-ttu-id="12e70-p103">Cuando se realiza un cambio estructural en un libro, por ejemplo, cuando se introduce una nueva fórmula, Excel reconstruye la cadena de cálculo y el árbol de dependencias. Cuando se introducen nuevos datos o fórmulas, Excel marca todas las celdas que dependen de los nuevos datos según necesiten actualizarse. Las celdas marcadas como de esta forma se conocen como  *desfasadas*  . Todos los dependientes directos e indirectos se marcan como desfasados, de modo que si B1 depende de A1 y C1 depende de B1, al cambiar A1, B1 y C1 se marcan como desfasados.</span><span class="sxs-lookup"><span data-stu-id="12e70-p103">When a structural change is made to a workbook, for example, when a new formula is entered, Excel reconstructs the dependency tree and calculation chain. When new data or new formulas are entered, Excel marks all the cells that depend on that new data as needing recalculation. Cells that are marked in this way are known as  *dirty*  . All direct and indirect dependents are marked as dirty so that if B1 depends on A1, and C1 depends on B1, when A1 is changed, both B1 and C1 are marked as dirty.</span></span> 
  
<span data-ttu-id="12e70-p104">Si una celda depende, directa o indirectamente, de sí misma, Excel detecta la referencia circular y advierte al usuario. Normalmente es una condición de error que el usuario debe corregir y Excel proporciona herramientas gráficas y navegación muy útiles para ayudar a los usuarios a encontrar el origen de la dependencia circular. En algunos casos, es posible que quiera que esta condición exista deliberadamente. Por ejemplo, puede que quiera ejecutar un cálculo iterativo donde el punto de inicio para la siguiente iteración sea el resultado de la iteración anterior. Excel admite el control de los cálculos iterativos mediante el cuadro de diálogo Opciones de cálculo.</span><span class="sxs-lookup"><span data-stu-id="12e70-p104">If a cell depends, directly or indirectly, on itself, Excel detects the circular reference and warns the user. This is usually an error condition that the user must fix, and Excel provides very helpful graphical and navigational tools to help the user to find the source of the circular dependency. In some cases, you might deliberately want this condition to exist. For example, you might want to run an iterative calculation where the starting point for the next iteration is the result of the previous iteration. Excel supports control of iterative calculations through the calculation options dialog box.</span></span>
  
<span data-ttu-id="12e70-p105">Después de marcar las celdas como desfasadas, después de realizar la actualización a continuación, Excel vuelve a evaluar el contenido de cada celda desfasada en el orden determinado por la cadena de cálculo. En el ejemplo anterior, esto significa que B1 es la primera y C1 la siguiente. Esta actualización ocurre inmediatamente después de que Excel termine de marcar las celdas como desfasadas si el modo de actualización es automático; de lo contrario, ocurre posteriormente.</span><span class="sxs-lookup"><span data-stu-id="12e70-p105">After marking cells as dirty, when a recalculation is next done, Excel reevaluates the contents of each dirty cell in the order dictated by the calculation chain. In the example given earlier, this means B1 is first, and then C1. This recalculation occurs immediately after Excel finishes marking cells as dirty if the recalculation mode is automatic; otherwise, it occurs later.</span></span>
  
<span data-ttu-id="12e70-p106">A partir de Microsoft Excel 2002, el objeto **Range** de Microsoft Visual Basic para aplicaciones (VBA) admite un método, **Range.Dirty**, que marca las celdas como que necesitan un cálculo. Cuando se usa junto con el método **Range.Calculate** (consulte la siguiente sección), permite la actualización forzada de las celdas de un rango determinado. Esto resulta útil al realizar un cálculo limitado durante una macro, donde se configura el modo de cálculo manual, para evitar la sobrecarga de celdas de cálculo no relacionadas con la función de la macro. Los métodos de cálculo del rango no están disponibles a través de la API de C.</span><span class="sxs-lookup"><span data-stu-id="12e70-p106">Starting in Microsoft Excel 2002, the **Range** object in Microsoft Visual Basic for Applications (VBA) supports a method, **Range.Dirty**, which marks cells as needing calculation. When it is used together with the **Range.Calculate** method (see next section), it enables forced recalculation of cells in a given range. This is useful when you are performing a limited calculation during a macro, where the calculation mode is set to manual, to avoid the overhead of calculating cells unrelated to the macro function. Range calculation methods are not available through the C API.</span></span> 
  
<span data-ttu-id="12e70-p107">En Excel 2002 y versiones anteriores, Excel compila una cadena de cálculo para cada hoja de cálculo de cada libro abierto. Esto resultaba complejo en la forma en que se gestionaban los vínculos entre hojas de cálculo y necesitaba cierto cuidado para garantizar una actualización eficaz. En concreto, en Excel 2000, debería minimizar las dependencias entre hojas de cálculo y las hojas de cálculo de nombres en orden alfabético para que las hojas que dependían de otras hojas aparecieran alfabéticamente después de las hojas de las que dependían.</span><span class="sxs-lookup"><span data-stu-id="12e70-p107">In Excel 2002 and earlier versions, Excel built a calculation chain for each worksheet in each open workbook. This resulted in some complexity in the way links between worksheets were handled, and required some care to ensure efficient recalculation. In particular, in Excel 2000, you should minimize cross-worksheet dependencies and name worksheets in alphabetical order so that sheets that depend on other sheets come alphabetically after the sheets they depend on.</span></span>
  
<span data-ttu-id="12e70-p108">En Excel 2007, se ha mejorado la lógica para habilitar la actualización en varios subprocesos para que las secciones de la cadena de cálculo no sean interdependientes y se puedan calcular a la vez. Puede configurar Excel para usar varios subprocesos en un equipo con procesador único o en un único subproceso de un equipo con varios procesadores o varios núcleos.</span><span class="sxs-lookup"><span data-stu-id="12e70-p108">In Excel 2007, the logic was improved to enable recalculation on multiple threads so that sections of the calculation chain are not interdependent and can be calculated at the same time. You can configure Excel to use multiple threads on a single processor computer, or a single thread on a multi-processor or multi-core computer.</span></span> 
  
## <a name="asynchronous-user-defined-functions-udfs"></a><span data-ttu-id="12e70-152">Funciones asincrónicas definidas por el usuario (UDF)</span><span class="sxs-lookup"><span data-stu-id="12e70-152">Asynchronous User Defined Functions (UDFs)</span></span>

<span data-ttu-id="12e70-p109">Cuando un cálculo encuentra un UDF asincrónico, guarda el estado de la fórmula actual, inicia la UDF y sigue evaluando el resto de celdas. Cuando el cálculo finaliza la evaluación de las celdas, Excel espera a que las funciones asincrónicas se completen, si hay funciones asincrónicas en ejecución. Ya que cada función asincrónica informa de los resultados, Excel finaliza la fórmula y ejecuta un nuevo paso de cálculo para volver a calcular las celdas que usan la celda con la referencia a la función asincrónica.</span><span class="sxs-lookup"><span data-stu-id="12e70-p109">When a calculation encounters an asynchronous UDF, it saves the state of the current formula, starts the UDF and continues evaluating the rest of the cells. When the calculation finishes evaluating the cells Excel waits for the asynchronous functions to complete if there are still asynchronous functions running. As each asynchronous function reports results, Excel finishes the formula, and then runs a new calculation pass to re-compute cells that use the cell with the reference to the asynchronous function.</span></span>
  
## <a name="volatile-and-non-volatile-functions"></a><span data-ttu-id="12e70-156">Funciones volátiles y no volátiles</span><span class="sxs-lookup"><span data-stu-id="12e70-156">Volatile and Non-Volatile Functions</span></span>

<span data-ttu-id="12e70-p110">Excel admite el concepto de una función volátil, es decir, una cuyo valor no se puede suponer que sea el mismo que la de la siguiente, incluso si ninguno de los argumentos (si toma alguno) ha cambiado. Excel vuelve a evaluar las celdas que contienen funciones volátiles, junto con todos los dependientes, cada vez que actualiza. Por este motivo, confiar demasiado en las funciones volátiles puede hacer que los tiempos de actualización sean lentos. Úselas con moderación.</span><span class="sxs-lookup"><span data-stu-id="12e70-p110">Excel supports the concept of a volatile function, that is, one whose value cannot be assumed to be the same from one moment to the next even if none of its arguments (if it takes any) has changed. Excel reevaluates cells that contain volatile functions, together with all dependents, every time that it recalculates. For this reason, too much reliance on volatile functions can make recalculation times slow. Use them sparingly.</span></span>
  
<span data-ttu-id="12e70-161">Las siguientes funciones de Excel son volátiles:</span><span class="sxs-lookup"><span data-stu-id="12e70-161">The following Excel functions are volatile:</span></span>
  
- <span data-ttu-id="12e70-162">**NOW**</span><span class="sxs-lookup"><span data-stu-id="12e70-162">**NOW**</span></span>
    
- <span data-ttu-id="12e70-163">**TODAY**</span><span class="sxs-lookup"><span data-stu-id="12e70-163">**TODAY**</span></span>
    
- <span data-ttu-id="12e70-164">**RANDBETWEEN**</span><span class="sxs-lookup"><span data-stu-id="12e70-164">**RandBetween**</span></span>
    
- <span data-ttu-id="12e70-165">**OFFSET**</span><span class="sxs-lookup"><span data-stu-id="12e70-165">**OFFSET**</span></span>
    
- <span data-ttu-id="12e70-166">**INDIRECT**</span><span class="sxs-lookup"><span data-stu-id="12e70-166">**INDIRECT**</span></span>
    
- <span data-ttu-id="12e70-167">**INFO** (en función de sus argumentos)</span><span class="sxs-lookup"><span data-stu-id="12e70-167">**INFO** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="12e70-168">**CELL** (en función de sus argumentos)</span><span class="sxs-lookup"><span data-stu-id="12e70-168">**CELL** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="12e70-169">**SUMIF** (en función de sus argumentos)</span><span class="sxs-lookup"><span data-stu-id="12e70-169">**CELL** (depending on its arguments)</span></span> 
    
<span data-ttu-id="12e70-p111">La API de C y VBA admiten maneras para informar a Excel que una función definida por el usuario (UDF) debe tratarse como volátil. Con VBA, UDF se declara como volátil del siguiente modo.</span><span class="sxs-lookup"><span data-stu-id="12e70-p111">Both the VBA and C API support ways to inform Excel that a user-defined function (UDF) should be handled as volatile. By using VBA, the UDF is declared as volatile as follows.</span></span>
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

<span data-ttu-id="12e70-p112">De forma predeterminada, Excel asume que las UDF de VBA no son volátiles. Excel solo descubre que una UDF es volátil cuando la llama en primer lugar. Una UDF volátil se puede volver a cambiar a no volátil, como en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="12e70-p112">By default, Excel assumes that VBA UDFs are not volatile. Excel only learns that a UDF is volatile when it first calls it. A volatile UDF can be changed back to non-volatile as in this example.</span></span>
  
<span data-ttu-id="12e70-p113">Con la API de C, puede registrar una función XLL como volátil antes de la primera llamada. También le permite alternar el estado volátil de una función de hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="12e70-p113">Using the C API, you can register an XLL function as volatile before its first call. It also enables you to switch on and off the volatile status of a worksheet function.</span></span>
  
<span data-ttu-id="12e70-p114">De forma predeterminada, Excel trata las UDF de XLL que toman argumentos de rango y que se declaran como equivalentes de hojas macros como volátiles. Puede desactivar este estado predeterminado con la función **xlfVolatile** al llamar a la UDF por primera vez.</span><span class="sxs-lookup"><span data-stu-id="12e70-p114">By default, Excel handles XLL UDFs that take range arguments and that are declared as macro-sheet equivalents as volatile. You can turn this default state off using the **xlfVolatile** function when the UDF is first called.</span></span> 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a><span data-ttu-id="12e70-179">Modos de cálculo, comandos, actualización selectiva y tablas de datos</span><span class="sxs-lookup"><span data-stu-id="12e70-179">Calculation Modes, Commands, Selective Recalculation, and Data Tables</span></span>

<span data-ttu-id="12e70-180">Excel tiene tres modos de cálculo:</span><span class="sxs-lookup"><span data-stu-id="12e70-180">Excel has three calculation modes:</span></span>
  
- <span data-ttu-id="12e70-181">Automatic</span><span class="sxs-lookup"><span data-stu-id="12e70-181">Automatic</span></span>
    
- <span data-ttu-id="12e70-182">Automático excepto en tablas</span><span class="sxs-lookup"><span data-stu-id="12e70-182">Automatic Except Tables</span></span>
    
- <span data-ttu-id="12e70-183">Manual</span><span class="sxs-lookup"><span data-stu-id="12e70-183">Manual</span></span>
    
<span data-ttu-id="12e70-p115">Cuando se configura el cálculo en automático, la actualización ocurre después de cada entrada de datos y de determinados eventos, como los ejemplos de la sección anterior. Los libros grandes, el tiempo de actualización podría ser tan largo que los usuarios deberían limitar el momento en que esto ocurre, es decir, actualizar solo cuando sea necesario. Para habilitarlo, Excel admite el modo manual. El usuario puede seleccionar el modo en el sistema de menús de Excel o mediante programación con la API de C, COM o VBA.</span><span class="sxs-lookup"><span data-stu-id="12e70-p115">When calculation is set to automatic, recalculation occurs after every data input and after certain events such as the examples given in the previous section. For very large workbooks, recalculation time might be so long that users must limit when this happens, that is, only recalculating when they need to. To enable this, Excel supports the manual mode. The user can select the mode through the Excel menu system, or programmatically using VBA, COM, or the C API.</span></span>
  
<span data-ttu-id="12e70-p116">Las tablas de datos son estructuras especiales de una hoja de cálculo. En primer lugar, el usuario configura el cálculo de un resultado de una hoja de cálculo. Esto depende de una o dos entradas modificables clave y otros parámetros. Luego, el usuario puede crear una tabla de resultados para un conjunto de valores para una o ambas entradas clave. La tabla se crea con el **Asistente para tablas de datos**. Después de configurar la tabla, Excel inserta las entradas de una en una en el cálculo y copia el valor resultante en la tabla. Como se pueden usar una o dos entradas, las tablas de datos pueden ser de una o dos dimensiones.</span><span class="sxs-lookup"><span data-stu-id="12e70-p116">Data tables are special structures in a worksheet. First, the user sets up the calculation of a result on a worksheet. This depends on one or two key changeable inputs and other parameters. The user can then create a table of results for a set of values for one or both of the key inputs. The table is created by using the **Data Table Wizard**. After the table is set up, Excel plugs the inputs one-by-one into the calculation and copies the resulting value into the table. As one or two inputs can be used, data tables can be one- or two-dimensional.</span></span> 
  
<span data-ttu-id="12e70-195">La actualización de las tablas de datos se trata de manera diferente:</span><span class="sxs-lookup"><span data-stu-id="12e70-195">Recalculation of data tables is handled slightly differently:</span></span>
  
- <span data-ttu-id="12e70-196">La actualización se controla de forma asincrónica para la actualización de libros normales de modo que las tablas de gran tamaño pueden tardar más en actualizarse que el resto del libro.</span><span class="sxs-lookup"><span data-stu-id="12e70-196">Recalculation is handled asynchronously to regular workbook recalculation so that large tables might take longer to recalculate than the rest of the workbook.</span></span>
    
- <span data-ttu-id="12e70-p117">Se toleran las referencias circulares. Si el cálculo que se usa para obtener el resultado depende de uno o varios valores de la tabla de datos, Excel no devuelve un error para la dependencia circular.</span><span class="sxs-lookup"><span data-stu-id="12e70-p117">Circular references are tolerated. If the calculation that is used to get the result depends on one or more values from the data table, Excel does not return an error for the circular dependency.</span></span> 
    
<span data-ttu-id="12e70-p118">Dada la forma distinta en que Excel gestiona la actualización de las tablas de datos, y el hecho de que las tablas de gran tamaño que dependen de cálculos largos o complejos pueden tardar mucho tiempo en calcularse, Excel permite deshabilitar el cálculo automático de tablas de datos. Para ello, configure el modo de cálculo en Automático excepto en tablas de datos. Cuando el cálculo se encuentra en este modo, el usuario actualiza las tablas de datos presionando F9 o alguna operación de programación equivalente.</span><span class="sxs-lookup"><span data-stu-id="12e70-p118">Given the different way that Excel handles recalculation of data tables, and the fact that large tables that depend on complex or lengthy calculations can take a long time to calculate, Excel lets you disable the automatic calculation of data tables. To do this, set the calculation mode to Automatic except Data Tables. When calculation is in this mode, the user recalculates the data tables by pressing F9 or some equivalent programmatic operation.</span></span>
  
<span data-ttu-id="12e70-p119">Excel expone métodos a través de los cuales puede modificar el modo de actualización y controlarla. Estos métodos se han mejorado de versión a versión para permitir un control más preciso. En este sentido, las capacidades de la API de C reflejan las que estaban disponibles en la versión 5 de Excel y, por lo tanto, no proporcionan el mismo control que tenía con VBA en las versiones más recientes.</span><span class="sxs-lookup"><span data-stu-id="12e70-p119">Excel exposes methods through which you can alter the recalculation mode and control recalculation. These methods have been improved from version to version to allow for finer control. The capabilities of the C API in this regard reflect those that were available in Excel version 5, and so do not give you the same control that you have using VBA in more recent versions.</span></span> 
  
<span data-ttu-id="12e70-205">Estos métodos, que se usan con más frecuencia cuando Excel está en modo de cálculo manual, permiten el cálculo selectivo de libros, hojas de cálculo y rangos, una actualización completa de todos los libros abiertos e incluso completar la recompilación de la cadena de cálculo y del árbol de dependencias.</span><span class="sxs-lookup"><span data-stu-id="12e70-205">Most frequently used when Excel is in manual calculation mode, these methods allow selective calculation of workbooks, worksheets, and ranges, complete recalculation of all open workbooks, and even complete rebuild of the dependency tree and calculation chain.</span></span>
  
### <a name="range-calculation"></a><span data-ttu-id="12e70-206">Cálculo de rango</span><span class="sxs-lookup"><span data-stu-id="12e70-206">Range Calculation</span></span>

<span data-ttu-id="12e70-207">Pulsación de tecla: ninguno</span><span class="sxs-lookup"><span data-stu-id="12e70-207">Keystroke: None</span></span>
  
<span data-ttu-id="12e70-208">VBA: **Range.Calculate** (a partir de Excel 2000, modificado en Excel 2007) y **Range.CalculateRowMajorOrder** (a partir de Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="12e70-208">VBA: **Range.Calculate** (introduced in Excel 2000, changed in Excel 2007) and **Range.CalculateRowMajorOrder** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="12e70-209">API de C: no se admite</span><span class="sxs-lookup"><span data-stu-id="12e70-209">C API: Not supported</span></span>
  
- <span data-ttu-id="12e70-210">**Modo manual**</span><span class="sxs-lookup"><span data-stu-id="12e70-210">**Manual mode**</span></span>
    
    <span data-ttu-id="12e70-p120">Actualiza solo las celdas del rango especificado independientemente de si están desfasadas o no. El comportamiento del método **Range.Calculate** ha cambiado en Excel 2007; sin embargo, el método **Range.CalculateRowMajorOrder** sigue admitiendo el comportamiento anterior.</span><span class="sxs-lookup"><span data-stu-id="12e70-p120">Recalculates just the cells in the given range regardless of whether they are dirty or not. Behavior of the **Range.Calculate** method changed in Excel 2007; however, the old behavior is still supported by the **Range.CalculateRowMajorOrder** method.</span></span> 
    
- <span data-ttu-id="12e70-213">**Modos Automático o Automático excepto en tablas**</span><span class="sxs-lookup"><span data-stu-id="12e70-213">**Automatic or Automatic Except Tables modes**</span></span>
    
    <span data-ttu-id="12e70-214">Actualiza el libro pero no fuerza la actualización del rango o de las celdas del rango.</span><span class="sxs-lookup"><span data-stu-id="12e70-214">Recalculates the workbook but does not force recalculation of the range or any cells in the range.</span></span>
    
### <a name="active-worksheet-calculation"></a><span data-ttu-id="12e70-215">Cálculo de la hoja de cálculo activa</span><span class="sxs-lookup"><span data-stu-id="12e70-215">Active Worksheet Calculation</span></span>

<span data-ttu-id="12e70-216">Pulsación de tecla: MAYÚS+F9</span><span class="sxs-lookup"><span data-stu-id="12e70-216">Keystroke: SHIFT+F9</span></span>
  
<span data-ttu-id="12e70-217">VBA: **ActiveSheet.Calculate**</span><span class="sxs-lookup"><span data-stu-id="12e70-217">VBA: **ActiveSheet.Calculate**</span></span>
  
<span data-ttu-id="12e70-218">API DE C: **xlcCalculateDocument**</span><span class="sxs-lookup"><span data-stu-id="12e70-218">C API: **xlcCalculateDocument**</span></span>
  
- <span data-ttu-id="12e70-219">**Todos los modos**</span><span class="sxs-lookup"><span data-stu-id="12e70-219">**All modes**</span></span>
    
    <span data-ttu-id="12e70-220">Actualiza las celdas marcadas para el cálculo solo en la hoja de cálculo activa.</span><span class="sxs-lookup"><span data-stu-id="12e70-220">Recalculates the cells marked for calculation in the active worksheet only.</span></span>
    
### <a name="specified-worksheet-calculation"></a><span data-ttu-id="12e70-221">Cálculo de la hoja de cálculo especificada</span><span class="sxs-lookup"><span data-stu-id="12e70-221">Specified Worksheet Calculation</span></span>

<span data-ttu-id="12e70-222">Pulsación de tecla: ninguno</span><span class="sxs-lookup"><span data-stu-id="12e70-222">Keystroke: None</span></span>
  
<span data-ttu-id="12e70-223">VBA: **Worksheets(** referencia **).Calculate**</span><span class="sxs-lookup"><span data-stu-id="12e70-223">VBA: **Worksheets(** reference **).Calculate**</span></span>
  
<span data-ttu-id="12e70-224">API de C: no se admite</span><span class="sxs-lookup"><span data-stu-id="12e70-224">C API: Not supported</span></span>
  
- <span data-ttu-id="12e70-225">**Todos los modos**</span><span class="sxs-lookup"><span data-stu-id="12e70-225">**All modes**</span></span>
    
    <span data-ttu-id="12e70-p121">Actualiza las celdas desfasadas y sus dependientes solo dentro de la hoja de cálculo especificada. La referencia es el nombre de la hoja de cálculo como una cadena o el número de índice del libro relevante.</span><span class="sxs-lookup"><span data-stu-id="12e70-p121">Recalculates the dirty cells and their dependents within the specified worksheet only. Reference is the name of the worksheet as a string or the index number in the relevant workbook.</span></span>
    
    <span data-ttu-id="12e70-p122">Excel 2000 y las versiones posteriores exponen una propiedad **Boolean** de hoja de cálculo, la propiedad **EnableCalculation**. Si se configura en **True** desde **False** desfasa todas las celdas de la hoja de cálculo especificada. En los modos automáticos, también desencadena la actualización de todo el libro.</span><span class="sxs-lookup"><span data-stu-id="12e70-p122">Excel 2000 and later versions expose a **Boolean** worksheet property, the **EnableCalculation** property. Setting this to **True** from **False** dirties all cells in the specified worksheet. In automatic modes, this also triggers a recalculation of the whole workbook.</span></span> 
    
    <span data-ttu-id="12e70-231">En el modo manual, el siguiente código provoca la actualización solo de la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="12e70-231">In manual mode, the following code causes recalculation of the active sheet only.</span></span>
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a><span data-ttu-id="12e70-232">Recompilación y actualización forzada del árbol de libro</span><span class="sxs-lookup"><span data-stu-id="12e70-232">Workbook Tree Rebuild and Forced Recalculation</span></span>

<span data-ttu-id="12e70-233">Pulsación de tecla: CTRL+ALT+MAYÚS+F9 (a partir de Excel 2002)</span><span class="sxs-lookup"><span data-stu-id="12e70-233">Keystroke: CTRL+ALT+SHIFT+F9 (introduced in Excel 2002)</span></span>
  
<span data-ttu-id="12e70-234">VBA: **Workbooks(** referencia **).ForceFullCalculation** (a partir de Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="12e70-234">VBA: **Workbooks(** reference **).ForceFullCalculation** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="12e70-235">API de C: no se admite</span><span class="sxs-lookup"><span data-stu-id="12e70-235">C API: Not supported</span></span>
  
- <span data-ttu-id="12e70-236">**Todos los modos**</span><span class="sxs-lookup"><span data-stu-id="12e70-236">**All modes**</span></span>
    
    <span data-ttu-id="12e70-237">Hace que Excel recompile el árbol de dependencias y la cadena de cálculo de un libro determinado y fuerza una actualización de todas las celdas que contienen fórmulas.</span><span class="sxs-lookup"><span data-stu-id="12e70-237">Causes Excel to rebuild the dependency tree and the calculation chain for a given workbook and forces a recalculation of all cells that contain formulas.</span></span>
    
### <a name="all-open-workbooks"></a><span data-ttu-id="12e70-238">Todos los libros abiertos</span><span class="sxs-lookup"><span data-stu-id="12e70-238">All Open Workbooks</span></span>

<span data-ttu-id="12e70-239">Pulsación de tecla: F9</span><span class="sxs-lookup"><span data-stu-id="12e70-239">Keystroke: F9</span></span>
  
<span data-ttu-id="12e70-240">VBA: **Application.Calculate**</span><span class="sxs-lookup"><span data-stu-id="12e70-240">VBA: **Application.Calculate**</span></span>
  
<span data-ttu-id="12e70-241">API de C: **xlcCalculateNow**</span><span class="sxs-lookup"><span data-stu-id="12e70-241">C API: **xlcCalculateNow**</span></span>
  
- <span data-ttu-id="12e70-242">**Todos los modos**</span><span class="sxs-lookup"><span data-stu-id="12e70-242">**All modes**</span></span>
    
    <span data-ttu-id="12e70-p123">Actualiza todas las celdas que Excel marca como desfasadas, es decir, los dependientes de datos volátiles o modificados, y las celdas marcadas mediante programación como desfasadas. Si el modo de cálculo es Automático excepto en tablas, se calculan las tablas que necesiten una actualización y también todas las funciones volátiles y sus dependientes.</span><span class="sxs-lookup"><span data-stu-id="12e70-p123">Recalculates all cells that Excel has marked as dirty, that is, dependents of volatile or changed data, and cells programmatically marked as dirty. If the calculation mode is Automatic Except Tables, this calculates those tables that require updating and also all volatile functions and their dependents.</span></span>
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a><span data-ttu-id="12e70-245">Recompilación y cálculo forzado de todos árboles de libros</span><span class="sxs-lookup"><span data-stu-id="12e70-245">All Open Workbooks Tree Rebuild and Forced Calculation</span></span>

<span data-ttu-id="12e70-246">Pulsación de tecla: CTRL+ALT+F9</span><span class="sxs-lookup"><span data-stu-id="12e70-246">Keystroke: CTRL+ALT+F9</span></span>
  
<span data-ttu-id="12e70-247">VBA: **Application.CalculateFull**</span><span class="sxs-lookup"><span data-stu-id="12e70-247">VBA: **Application.CalculateFull**</span></span>
  
<span data-ttu-id="12e70-248">API de C: no se admite</span><span class="sxs-lookup"><span data-stu-id="12e70-248">C API: Not supported</span></span>
  
- <span data-ttu-id="12e70-249">**Todos los modos**</span><span class="sxs-lookup"><span data-stu-id="12e70-249">**All modes**</span></span>
    
    <span data-ttu-id="12e70-p124">Actualiza todas las celdas de todos los libros abiertos. Si el modo de cálculo es Automático excepto en tablas, fuerza la actualización de las tablas.</span><span class="sxs-lookup"><span data-stu-id="12e70-p124">Recalculates all cells in all open workbooks. If the calculation mode is Automatic Except Tables, it forces the tables to be recalculated.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12e70-252">Vea también</span><span class="sxs-lookup"><span data-stu-id="12e70-252">See also</span></span>



[<span data-ttu-id="12e70-253">Actualización multiproceso en Excel</span><span class="sxs-lookup"><span data-stu-id="12e70-253">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="12e70-254">Tipos de datos utilizados por Excel</span><span class="sxs-lookup"><span data-stu-id="12e70-254">Data Types Used by Excel</span></span>](data-types-used-by-excel.md)
  
[<span data-ttu-id="12e70-255">Administración de memoria en Excel</span><span class="sxs-lookup"><span data-stu-id="12e70-255">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="12e70-256">Conceptos de programación de Excel</span><span class="sxs-lookup"><span data-stu-id="12e70-256">Excel Programming Concepts</span></span>](excel-programming-concepts.md)

