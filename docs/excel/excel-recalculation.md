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
# <a name="excel-recalculation"></a><span data-ttu-id="16ed0-104">Actualizaci�n de Excel</span><span class="sxs-lookup"><span data-stu-id="16ed0-104">Excel Recalculation</span></span>

 <span data-ttu-id="16ed0-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="16ed0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="16ed0-106">El usuario puede desencadenar la actualizaci�n en Microsoft Excel de varias maneras, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="16ed0-106">The user can trigger recalculation in Microsoft Excel in several ways, for example:</span></span>
  
- <span data-ttu-id="16ed0-107">Introducir nuevos datos (si Excel se encuentra en modo Actualizaci�n autom�tica, que se describe m�s adelante en este tema).</span><span class="sxs-lookup"><span data-stu-id="16ed0-107">Entering new data (if Excel is in Automatic recalculation mode, described later in this topic).</span></span>
    
- <span data-ttu-id="16ed0-108">Indicar expl�citamente a Excel recalcular todo o parte de un libro.</span><span class="sxs-lookup"><span data-stu-id="16ed0-108">Explicitly instructing Excel to recalculate all or part of a workbook.</span></span>
    
- <span data-ttu-id="16ed0-109">Eliminar o insertar una fila o columna.</span><span class="sxs-lookup"><span data-stu-id="16ed0-109">Deleting or inserting a row or column.</span></span>
    
- <span data-ttu-id="16ed0-110">Guardar un libro mientras la opci�n **Recalcular antes de guardar** est� configurada.</span><span class="sxs-lookup"><span data-stu-id="16ed0-110">Saving a workbook while the **Recalculate before save** option is set.</span></span> 
    
- <span data-ttu-id="16ed0-111">Realizar determinadas acciones Filtro autom�tico.</span><span class="sxs-lookup"><span data-stu-id="16ed0-111">Performing certain Autofilter actions.</span></span>
    
- <span data-ttu-id="16ed0-112">Hacer doble clic en un divisor de fila o columna (en modo Actualizaci�n autom�tica).</span><span class="sxs-lookup"><span data-stu-id="16ed0-112">Double-clicking a row or column divider (in Automatic calculation mode).</span></span>
    
- <span data-ttu-id="16ed0-113">Agregar, editar o eliminar un nombre definido.</span><span class="sxs-lookup"><span data-stu-id="16ed0-113">Adding, editing, or deleting a defined name.</span></span>
    
- <span data-ttu-id="16ed0-114">Cambiar el nombre de una hoja de c�lculo.</span><span class="sxs-lookup"><span data-stu-id="16ed0-114">Renaming a worksheet.</span></span>
    
- <span data-ttu-id="16ed0-115">Cambiar la posici�n de una hoja de c�lculo en relaci�n a otras hojas de c�lculo.</span><span class="sxs-lookup"><span data-stu-id="16ed0-115">Changing the position of a worksheet in relation to other worksheets.</span></span>
    
- <span data-ttu-id="16ed0-116">Ocultar o mostrar filas, pero no columnas.</span><span class="sxs-lookup"><span data-stu-id="16ed0-116">Hiding or unhiding rows, but not columns.</span></span>
    
> [!NOTE]
> <span data-ttu-id="16ed0-p101">[!NOTA] En este tema no distingue entre el usuario que presiona directamente una tecla o hace clic en el mouse, y las tareas que realiza un comando o una macro. El usuario ejecuta el comando, o hace algo para que el comando se ejecute, de modo que se considera una acci�n del usuario. Por lo tanto, la frase "el usuario" tambi�n significa "el usuario, o un comando o proceso iniciado por el usuario."</span><span class="sxs-lookup"><span data-stu-id="16ed0-p101">This topic does not distinguish between the user directly pressing a key or clicking the mouse, and those tasks being done by a command or macro. The user runs the command, or does something to cause the command to run so that it is still considered a user action. Therefore the phrase "the user" also means "the user, or a command or process started by the user."</span></span> 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a><span data-ttu-id="16ed0-120">Dependencia, celdas desfasadas y celdas recalculadas</span><span class="sxs-lookup"><span data-stu-id="16ed0-120">Dependence, Dirty Cells, and Recalculated Cells</span></span>

<span data-ttu-id="16ed0-121">En Excel, el c�lculo de hojas de c�lculo se puede ver como un proceso de tres fases:</span><span class="sxs-lookup"><span data-stu-id="16ed0-121">The calculation of worksheets in Excel can be viewed as a three-stage process:</span></span>
  
1. <span data-ttu-id="16ed0-122">Construcci�n de un �rbol de dependencias</span><span class="sxs-lookup"><span data-stu-id="16ed0-122">Construction of a dependency tree</span></span>
    
2. <span data-ttu-id="16ed0-123">Construcci�n de una cadena de c�lculo</span><span class="sxs-lookup"><span data-stu-id="16ed0-123">Construction of a calculation chain</span></span>
    
3. <span data-ttu-id="16ed0-124">Actualizaci�n de las celdas</span><span class="sxs-lookup"><span data-stu-id="16ed0-124">Recalculation of cells</span></span>
    
<span data-ttu-id="16ed0-p102">El �rbol de dependencias informa a Excel de las celdas que dependen de otras, o de igual forma, las celdas que son precedentes para otras. Desde este �rbol, Excel construye una cadena de c�lculo. La cadena de c�lculo muestra todas las celdas que contienen f�rmulas en el orden en que se deben calcular. Durante la actualizaci�n, Excel revisa esta cadena si encuentra una f�rmula que depende de una celda que a�n no se ha calculado. En este caso, la celda que se calcula y sus dependientes se mueven hacia abajo en la cadena. Por este motivo, a menudo se pueden mejorar los tiempos de c�lculo en una hoja de c�lculo que se ha abierto en los primeros ciclos de c�lculo.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p102">The dependency tree informs Excel about which cells depend on which others, or equivalently, which cells are precedents for which others. From this tree, Excel constructs a calculation chain. The calculation chain lists all the cells that contain formulas in the order in which they should be calculated. During recalculation, Excel revises this chain if it comes across a formula that depends on a cell that has not yet been calculated. In this case, the cell that is being calculated and its dependents are moved down the chain. For this reason, calculation times can often improve in a worksheet that has just been opened in the first few calculation cycles.</span></span>
  
<span data-ttu-id="16ed0-p103">Cuando se realiza un cambio estructural en un libro, por ejemplo, cuando se introduce una nueva f�rmula, Excel reconstruye la cadena de c�lculo y el �rbol de dependencias. Cuando se introducen nuevos datos o f�rmulas, Excel marca todas las celdas que dependen de los nuevos datos seg�n necesiten actualizarse. Las celdas marcadas como de esta forma se conocen como  *desfasadas*  . Todos los dependientes directos e indirectos se marcan como desfasados, de modo que si B1 depende de A1 y C1 depende de B1, al cambiar A1, B1 y C1 se marcan como desfasados.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p103">When a structural change is made to a workbook, for example, when a new formula is entered, Excel reconstructs the dependency tree and calculation chain. When new data or new formulas are entered, Excel marks all the cells that depend on that new data as needing recalculation. Cells that are marked in this way are known as  *dirty*  . All direct and indirect dependents are marked as dirty so that if B1 depends on A1, and C1 depends on B1, when A1 is changed, both B1 and C1 are marked as dirty.</span></span> 
  
<span data-ttu-id="16ed0-p104">Si una celda depende, directa o indirectamente, de s� misma, Excel detecta la referencia circular y advierte al usuario. Normalmente es una condici�n de error que el usuario debe corregir y Excel proporciona herramientas gr�ficas y navegaci�n muy �tiles para ayudar a los usuarios a encontrar el origen de la dependencia circular. En algunos casos, es posible que quiera que esta condici�n exista deliberadamente. Por ejemplo, puede que quiera ejecutar un c�lculo iterativo donde el punto de inicio para la siguiente iteraci�n sea el resultado de la iteraci�n anterior. Excel admite el control de los c�lculos iterativos mediante el cuadro de di�logo Opciones de c�lculo.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p104">If a cell depends, directly or indirectly, on itself, Excel detects the circular reference and warns the user. This is usually an error condition that the user must fix, and Excel provides very helpful graphical and navigational tools to help the user to find the source of the circular dependency. In some cases, you might deliberately want this condition to exist. For example, you might want to run an iterative calculation where the starting point for the next iteration is the result of the previous iteration. Excel supports control of iterative calculations through the calculation options dialog box.</span></span>
  
<span data-ttu-id="16ed0-p105">Despu�s de marcar las celdas como desfasadas, despu�s de realizar la actualizaci�n a continuaci�n, Excel vuelve a evaluar el contenido de cada celda desfasada en el orden determinado por la cadena de c�lculo. En el ejemplo anterior, esto significa que B1 es la primera y C1 la siguiente. Esta actualizaci�n ocurre inmediatamente despu�s de que Excel termine de marcar las celdas como desfasadas si el modo de actualizaci�n es autom�tico; de lo contrario, ocurre posteriormente.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p105">After marking cells as dirty, when a recalculation is next done, Excel reevaluates the contents of each dirty cell in the order dictated by the calculation chain. In the example given earlier, this means B1 is first, and then C1. This recalculation occurs immediately after Excel finishes marking cells as dirty if the recalculation mode is automatic; otherwise, it occurs later.</span></span>
  
<span data-ttu-id="16ed0-p106">A partir de Microsoft Excel 2002, el objeto **Range** de Microsoft Visual Basic para aplicaciones (VBA) admite un m�todo, **Range.Dirty**, que marca las celdas como que necesitan un c�lculo. Cuando se usa junto con el m�todo **Range.Calculate** (consulte la siguiente secci�n), permite la actualizaci�n forzada de las celdas de un rango determinado. Esto resulta �til al realizar un c�lculo limitado durante una macro, donde se configura el modo de c�lculo manual, para evitar la sobrecarga de celdas de c�lculo no relacionadas con la funci�n de la macro. Los m�todos de c�lculo del rango no est�n disponibles a trav�s de la API de C.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p106">Starting in Microsoft Excel 2002, the **Range** object in Microsoft Visual Basic for Applications (VBA) supports a method, **Range.Dirty**, which marks cells as needing calculation. When it is used together with the **Range.Calculate** method (see next section), it enables forced recalculation of cells in a given range. This is useful when you are performing a limited calculation during a macro, where the calculation mode is set to manual, to avoid the overhead of calculating cells unrelated to the macro function. Range calculation methods are not available through the C API.</span></span> 
  
<span data-ttu-id="16ed0-p107">En Excel 2002 y versiones anteriores, Excel compila una cadena de c�lculo para cada hoja de c�lculo de cada libro abierto. Esto resultaba complejo en la forma en que se gestionaban los v�nculos entre hojas de c�lculo y necesitaba cierto cuidado para garantizar una actualizaci�n eficaz. En concreto, en Excel 2000, deber�a minimizar las dependencias entre hojas de c�lculo y las hojas de c�lculo de nombres en orden alfab�tico para que las hojas que depend�an de otras hojas aparecieran alfab�ticamente despu�s de las hojas de las que depend�an.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p107">In Excel 2002 and earlier versions, Excel built a calculation chain for each worksheet in each open workbook. This resulted in some complexity in the way links between worksheets were handled, and required some care to ensure efficient recalculation. In particular, in Excel 2000, you should minimize cross-worksheet dependencies and name worksheets in alphabetical order so that sheets that depend on other sheets come alphabetically after the sheets they depend on.</span></span>
  
<span data-ttu-id="16ed0-p108">En Excel 2007, se ha mejorado la l�gica para habilitar la actualizaci�n en varios subprocesos para que las secciones de la cadena de c�lculo no sean interdependientes y se puedan calcular a la vez. Puede configurar Excel para usar varios subprocesos en un equipo con procesador �nico o en un �nico subproceso de un equipo con varios procesadores o varios n�cleos.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p108">In Excel 2007, the logic was improved to enable recalculation on multiple threads so that sections of the calculation chain are not interdependent and can be calculated at the same time. You can configure Excel to use multiple threads on a single processor computer, or a single thread on a multi-processor or multi-core computer.</span></span> 
  
## <a name="asynchronous-user-defined-functions-udfs"></a><span data-ttu-id="16ed0-152">Funciones asincr�nicas definidas por el usuario (UDF)</span><span class="sxs-lookup"><span data-stu-id="16ed0-152">Asynchronous User Defined Functions (UDFs)</span></span>

<span data-ttu-id="16ed0-p109">Cuando un c�lculo encuentra un UDF asincr�nico, guarda el estado de la f�rmula actual, inicia la UDF y sigue evaluando el resto de celdas. Cuando el c�lculo finaliza la evaluaci�n de las celdas, Excel espera a que las funciones asincr�nicas se completen, si hay funciones asincr�nicas en ejecuci�n. Ya que cada funci�n asincr�nica informa de los resultados, Excel finaliza la f�rmula y ejecuta un nuevo paso de c�lculo para volver a calcular las celdas que usan la celda con la referencia a la funci�n asincr�nica.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p109">When a calculation encounters an asynchronous UDF, it saves the state of the current formula, starts the UDF and continues evaluating the rest of the cells. When the calculation finishes evaluating the cells Excel waits for the asynchronous functions to complete if there are still asynchronous functions running. As each asynchronous function reports results, Excel finishes the formula, and then runs a new calculation pass to re-compute cells that use the cell with the reference to the asynchronous function.</span></span>
  
## <a name="volatile-and-non-volatile-functions"></a><span data-ttu-id="16ed0-156">Funciones vol�tiles y no vol�tiles</span><span class="sxs-lookup"><span data-stu-id="16ed0-156">Volatile and Non-Volatile Functions</span></span>

<span data-ttu-id="16ed0-p110">Excel admite el concepto de una funci�n vol�til, es decir, una cuyo valor no se puede suponer que sea el mismo que la de la siguiente, incluso si ninguno de los argumentos (si toma alguno) ha cambiado. Excel vuelve a evaluar las celdas que contienen funciones vol�tiles, junto con todos los dependientes, cada vez que actualiza. Por este motivo, confiar demasiado en las funciones vol�tiles puede hacer que los tiempos de actualizaci�n sean lentos. �selas con moderaci�n.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p110">Excel supports the concept of a volatile function, that is, one whose value cannot be assumed to be the same from one moment to the next even if none of its arguments (if it takes any) has changed. Excel reevaluates cells that contain volatile functions, together with all dependents, every time that it recalculates. For this reason, too much reliance on volatile functions can make recalculation times slow. Use them sparingly.</span></span>
  
<span data-ttu-id="16ed0-161">Las siguientes funciones de Excel son vol�tiles:</span><span class="sxs-lookup"><span data-stu-id="16ed0-161">The following Excel functions are volatile:</span></span>
  
- <span data-ttu-id="16ed0-162">**NOW**</span><span class="sxs-lookup"><span data-stu-id="16ed0-162">**NOW**</span></span>
    
- <span data-ttu-id="16ed0-163">**TODAY**</span><span class="sxs-lookup"><span data-stu-id="16ed0-163">**TODAY**</span></span>
    
- <span data-ttu-id="16ed0-164">**RANDBETWEEN**</span><span class="sxs-lookup"><span data-stu-id="16ed0-164">**RANDBETWEEN**</span></span>
    
- <span data-ttu-id="16ed0-165">**OFFSET**</span><span class="sxs-lookup"><span data-stu-id="16ed0-165">**OFFSET**</span></span>
    
- <span data-ttu-id="16ed0-166">**INDIRECT**</span><span class="sxs-lookup"><span data-stu-id="16ed0-166">**INDIRECT**</span></span>
    
- <span data-ttu-id="16ed0-167">**INFO** (en funci�n de sus argumentos)</span><span class="sxs-lookup"><span data-stu-id="16ed0-167">**INFO** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="16ed0-168">**CELL** (en funci�n de sus argumentos)</span><span class="sxs-lookup"><span data-stu-id="16ed0-168">**CELL** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="16ed0-169">**SUMIF** (en función de sus argumentos)</span><span class="sxs-lookup"><span data-stu-id="16ed0-169">**SUMIF** (depending on its arguments)</span></span> 
    
<span data-ttu-id="16ed0-p111">La API de C y VBA admiten maneras para informar a Excel que una funci�n definida por el usuario (UDF) debe tratarse como vol�til. Con VBA, UDF se declara como vol�til del siguiente modo.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p111">Both the VBA and C API support ways to inform Excel that a user-defined function (UDF) should be handled as volatile. By using VBA, the UDF is declared as volatile as follows.</span></span>
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

<span data-ttu-id="16ed0-p112">De forma predeterminada, Excel asume que las UDF de VBA no son vol�tiles. Excel solo descubre que una UDF es vol�til cuando la llama en primer lugar. Una UDF vol�til se puede volver a cambiar a no vol�til, como en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p112">By default, Excel assumes that VBA UDFs are not volatile. Excel only learns that a UDF is volatile when it first calls it. A volatile UDF can be changed back to non-volatile as in this example.</span></span>
  
<span data-ttu-id="16ed0-p113">Con la API de C, puede registrar una funci�n XLL como vol�til antes de la primera llamada. Tambi�n le permite alternar el estado vol�til de una funci�n de hoja de c�lculo.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p113">Using the C API, you can register an XLL function as volatile before its first call. It also enables you to switch on and off the volatile status of a worksheet function.</span></span>
  
<span data-ttu-id="16ed0-p114">De forma predeterminada, Excel trata las UDF de XLL que toman argumentos de rango y que se declaran como equivalentes de hojas macros como vol�tiles. Puede desactivar este estado predeterminado con la funci�n **xlfVolatile** al llamar a la UDF por primera vez.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p114">By default, Excel handles XLL UDFs that take range arguments and that are declared as macro-sheet equivalents as volatile. You can turn this default state off using the **xlfVolatile** function when the UDF is first called.</span></span> 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a><span data-ttu-id="16ed0-179">Modos de c�lculo, comandos, actualizaci�n selectiva y tablas de datos</span><span class="sxs-lookup"><span data-stu-id="16ed0-179">Calculation Modes, Commands, Selective Recalculation, and Data Tables</span></span>

<span data-ttu-id="16ed0-180">Excel tiene tres modos de c�lculo:</span><span class="sxs-lookup"><span data-stu-id="16ed0-180">Excel has three calculation modes:</span></span>
  
- <span data-ttu-id="16ed0-181">Autom�tico</span><span class="sxs-lookup"><span data-stu-id="16ed0-181">Automatic</span></span>
    
- <span data-ttu-id="16ed0-182">Autom�tico excepto en tablas</span><span class="sxs-lookup"><span data-stu-id="16ed0-182">Automatic Except Tables</span></span>
    
- <span data-ttu-id="16ed0-183">Manual</span><span class="sxs-lookup"><span data-stu-id="16ed0-183">Manual</span></span>
    
<span data-ttu-id="16ed0-p115">Cuando se configura el c�lculo en autom�tico, la actualizaci�n ocurre despu�s de cada entrada de datos y de determinados eventos, como los ejemplos de la secci�n anterior. Los libros grandes, el tiempo de actualizaci�n podr�a ser tan largo que los usuarios deber�an limitar el momento en que esto ocurre, es decir, actualizar solo cuando sea necesario. Para habilitarlo, Excel admite el modo manual. El usuario puede seleccionar el modo en el sistema de men�s de Excel o mediante programaci�n con la API de C, COM o VBA.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p115">When calculation is set to automatic, recalculation occurs after every data input and after certain events such as the examples given in the previous section. For very large workbooks, recalculation time might be so long that users must limit when this happens, that is, only recalculating when they need to. To enable this, Excel supports the manual mode. The user can select the mode through the Excel menu system, or programmatically using VBA, COM, or the C API.</span></span>
  
<span data-ttu-id="16ed0-p116">Las tablas de datos son estructuras especiales de una hoja de c�lculo. En primer lugar, el usuario configura el c�lculo de un resultado de una hoja de c�lculo. Esto depende de una o dos entradas modificables clave y otros par�metros. Luego, el usuario puede crear una tabla de resultados para un conjunto de valores para una o ambas entradas clave. La tabla se crea con el **Asistente para tablas de datos**. Despu�s de configurar la tabla, Excel inserta las entradas de una en una en el c�lculo y copia el valor resultante en la tabla. Como se pueden usar una o dos entradas, las tablas de datos pueden ser de una o dos dimensiones.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p116">Data tables are special structures in a worksheet. First, the user sets up the calculation of a result on a worksheet. This depends on one or two key changeable inputs and other parameters. The user can then create a table of results for a set of values for one or both of the key inputs. The table is created by using the **Data Table Wizard**. After the table is set up, Excel plugs the inputs one-by-one into the calculation and copies the resulting value into the table. As one or two inputs can be used, data tables can be one- or two-dimensional.</span></span> 
  
<span data-ttu-id="16ed0-195">La actualizaci�n de las tablas de datos se trata de manera diferente:</span><span class="sxs-lookup"><span data-stu-id="16ed0-195">Recalculation of data tables is handled slightly differently:</span></span>
  
- <span data-ttu-id="16ed0-196">La actualizaci�n se controla de forma asincr�nica para la actualizaci�n de libros normales de modo que las tablas de gran tama�o pueden tardar m�s en actualizarse que el resto del libro.</span><span class="sxs-lookup"><span data-stu-id="16ed0-196">Recalculation is handled asynchronously to regular workbook recalculation so that large tables might take longer to recalculate than the rest of the workbook.</span></span>
    
- <span data-ttu-id="16ed0-p117">Se toleran las referencias circulares. Si el c�lculo que se usa para obtener el resultado depende de uno o varios valores de la tabla de datos, Excel no devuelve un error para la dependencia circular.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p117">Circular references are tolerated. If the calculation that is used to get the result depends on one or more values from the data table, Excel does not return an error for the circular dependency.</span></span> 
    
<span data-ttu-id="16ed0-p118">Dada la forma distinta en que Excel gestiona la actualizaci�n de las tablas de datos, y el hecho de que las tablas de gran tama�o que dependen de c�lculos largos o complejos pueden tardar mucho tiempo en calcularse, Excel permite deshabilitar el c�lculo autom�tico de tablas de datos. Para ello, configure el modo de c�lculo en Autom�tico excepto en tablas de datos. Cuando el c�lculo se encuentra en este modo, el usuario actualiza las tablas de datos presionando F9 o alguna operaci�n de programaci�n equivalente.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p118">Given the different way that Excel handles recalculation of data tables, and the fact that large tables that depend on complex or lengthy calculations can take a long time to calculate, Excel lets you disable the automatic calculation of data tables. To do this, set the calculation mode to Automatic except Data Tables. When calculation is in this mode, the user recalculates the data tables by pressing F9 or some equivalent programmatic operation.</span></span>
  
<span data-ttu-id="16ed0-p119">Excel expone m�todos a trav�s de los cuales puede modificar el modo de actualizaci�n y controlarla. Estos m�todos se han mejorado de versi�n a versi�n para permitir un control m�s preciso. En este sentido, las capacidades de la API de C reflejan las que estaban disponibles en la versi�n 5 de Excel y, por lo tanto, no proporcionan el mismo control que ten�a con VBA en las versiones m�s recientes.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p119">Excel exposes methods through which you can alter the recalculation mode and control recalculation. These methods have been improved from version to version to allow for finer control. The capabilities of the C API in this regard reflect those that were available in Excel version 5, and so do not give you the same control that you have using VBA in more recent versions.</span></span> 
  
<span data-ttu-id="16ed0-205">Estos m�todos, que se usan con m�s frecuencia cuando Excel est� en modo de c�lculo manual, permiten el c�lculo selectivo de libros, hojas de c�lculo y rangos, una actualizaci�n completa de todos los libros abiertos e incluso completar la recompilaci�n de la cadena de c�lculo y del �rbol de dependencias.</span><span class="sxs-lookup"><span data-stu-id="16ed0-205">Most frequently used when Excel is in manual calculation mode, these methods allow selective calculation of workbooks, worksheets, and ranges, complete recalculation of all open workbooks, and even complete rebuild of the dependency tree and calculation chain.</span></span>
  
### <a name="range-calculation"></a><span data-ttu-id="16ed0-206">C�lculo de rango</span><span class="sxs-lookup"><span data-stu-id="16ed0-206">Range Calculation</span></span>

<span data-ttu-id="16ed0-207">Pulsaci�n de tecla: ninguno</span><span class="sxs-lookup"><span data-stu-id="16ed0-207">Keystroke: None</span></span>
  
<span data-ttu-id="16ed0-208">VBA: **Range.Calculate** (a partir de Excel 2000, modificado en Excel 2007) y **Range.CalculateRowMajorOrder** (a partir de Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="16ed0-208">VBA: **Range.Calculate** (introduced in Excel 2000, changed in Excel 2007) and **Range.CalculateRowMajorOrder** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="16ed0-209">API de C: no se admite</span><span class="sxs-lookup"><span data-stu-id="16ed0-209">C API: Not supported</span></span>
  
- <span data-ttu-id="16ed0-210">**Modo manual**</span><span class="sxs-lookup"><span data-stu-id="16ed0-210">**Manual mode**</span></span>
    
    <span data-ttu-id="16ed0-p120">Actualiza solo las celdas del rango especificado independientemente de si est�n desfasadas o no. El comportamiento del m�todo **Range.Calculate** ha cambiado en Excel 2007; sin embargo, el m�todo **Range.CalculateRowMajorOrder** sigue admitiendo el comportamiento anterior.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p120">Recalculates just the cells in the given range regardless of whether they are dirty or not. Behavior of the **Range.Calculate** method changed in Excel 2007; however, the old behavior is still supported by the **Range.CalculateRowMajorOrder** method.</span></span> 
    
- <span data-ttu-id="16ed0-213">**Modos Autom�tico o Autom�tico excepto en tablas**</span><span class="sxs-lookup"><span data-stu-id="16ed0-213">**Automatic or Automatic Except Tables modes**</span></span>
    
    <span data-ttu-id="16ed0-214">Actualiza el libro pero no fuerza la actualizaci�n del rango o de las celdas del rango.</span><span class="sxs-lookup"><span data-stu-id="16ed0-214">Recalculates the workbook but does not force recalculation of the range or any cells in the range.</span></span>
    
### <a name="active-worksheet-calculation"></a><span data-ttu-id="16ed0-215">C�lculo de la hoja de c�lculo activa</span><span class="sxs-lookup"><span data-stu-id="16ed0-215">Active Worksheet Calculation</span></span>

<span data-ttu-id="16ed0-216">Pulsaci�n de tecla: MAY�S+F9</span><span class="sxs-lookup"><span data-stu-id="16ed0-216">Keystroke: SHIFT+F9</span></span>
  
<span data-ttu-id="16ed0-217">VBA: **ActiveSheet.Calculate**</span><span class="sxs-lookup"><span data-stu-id="16ed0-217">VBA: **ActiveSheet.Calculate**</span></span>
  
<span data-ttu-id="16ed0-218">API DE C: **xlcCalculateDocument**</span><span class="sxs-lookup"><span data-stu-id="16ed0-218">C API: **xlcCalculateDocument**</span></span>
  
- <span data-ttu-id="16ed0-219">**Todos los modos**</span><span class="sxs-lookup"><span data-stu-id="16ed0-219">**All modes**</span></span>
    
    <span data-ttu-id="16ed0-220">Actualiza las celdas marcadas para el c�lculo solo en la hoja de c�lculo activa.</span><span class="sxs-lookup"><span data-stu-id="16ed0-220">Recalculates the cells marked for calculation in the active worksheet only.</span></span>
    
### <a name="specified-worksheet-calculation"></a><span data-ttu-id="16ed0-221">C�lculo de la hoja de c�lculo especificada</span><span class="sxs-lookup"><span data-stu-id="16ed0-221">Specified Worksheet Calculation</span></span>

<span data-ttu-id="16ed0-222">Pulsaci�n de tecla: ninguno</span><span class="sxs-lookup"><span data-stu-id="16ed0-222">Keystroke: None</span></span>
  
<span data-ttu-id="16ed0-223">VBA: **Worksheets(** referencia **).Calculate**</span><span class="sxs-lookup"><span data-stu-id="16ed0-223">VBA: **Worksheets(** reference **).Calculate**</span></span>
  
<span data-ttu-id="16ed0-224">API de C: no se admite</span><span class="sxs-lookup"><span data-stu-id="16ed0-224">C API: Not supported</span></span>
  
- <span data-ttu-id="16ed0-225">**Todos los modos**</span><span class="sxs-lookup"><span data-stu-id="16ed0-225">**All modes**</span></span>
    
    <span data-ttu-id="16ed0-p121">Actualiza las celdas desfasadas y sus dependientes solo dentro de la hoja de c�lculo especificada. La referencia es el nombre de la hoja de c�lculo como una cadena o el n�mero de �ndice del libro relevante.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p121">Recalculates the dirty cells and their dependents within the specified worksheet only. Reference is the name of the worksheet as a string or the index number in the relevant workbook.</span></span>
    
    <span data-ttu-id="16ed0-p122">Excel 2000 y las versiones posteriores exponen una propiedad **Boolean** de hoja de c�lculo, la propiedad **EnableCalculation**. Si se configura en **True** desde **False** desfasa todas las celdas de la hoja de c�lculo especificada. En los modos autom�ticos, tambi�n desencadena la actualizaci�n de todo el libro.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p122">Excel 2000 and later versions expose a **Boolean** worksheet property, the **EnableCalculation** property. Setting this to **True** from **False** dirties all cells in the specified worksheet. In automatic modes, this also triggers a recalculation of the whole workbook.</span></span> 
    
    <span data-ttu-id="16ed0-231">En el modo manual, el siguiente c�digo provoca la actualizaci�n solo de la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="16ed0-231">In manual mode, the following code causes recalculation of the active sheet only.</span></span>
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a><span data-ttu-id="16ed0-232">Recompilaci�n y actualizaci�n forzada del �rbol de libro</span><span class="sxs-lookup"><span data-stu-id="16ed0-232">Workbook Tree Rebuild and Forced Recalculation</span></span>

<span data-ttu-id="16ed0-233">Pulsaci�n de tecla: CTRL+ALT+MAY�S+F9 (a partir de Excel 2002)</span><span class="sxs-lookup"><span data-stu-id="16ed0-233">Keystroke: CTRL+ALT+SHIFT+F9 (introduced in Excel 2002)</span></span>
  
<span data-ttu-id="16ed0-234">VBA: **Workbooks(** referencia **).ForceFullCalculation** (a partir de Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="16ed0-234">VBA: **Workbooks(** reference **).ForceFullCalculation** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="16ed0-235">API de C: no se admite</span><span class="sxs-lookup"><span data-stu-id="16ed0-235">C API: Not supported</span></span>
  
- <span data-ttu-id="16ed0-236">**Todos los modos**</span><span class="sxs-lookup"><span data-stu-id="16ed0-236">**All modes**</span></span>
    
    <span data-ttu-id="16ed0-237">Hace que Excel recompile el �rbol de dependencias y la cadena de c�lculo de un libro determinado y fuerza una actualizaci�n de todas las celdas que contienen f�rmulas.</span><span class="sxs-lookup"><span data-stu-id="16ed0-237">Causes Excel to rebuild the dependency tree and the calculation chain for a given workbook and forces a recalculation of all cells that contain formulas.</span></span>
    
### <a name="all-open-workbooks"></a><span data-ttu-id="16ed0-238">Todos los libros abiertos</span><span class="sxs-lookup"><span data-stu-id="16ed0-238">All Open Workbooks</span></span>

<span data-ttu-id="16ed0-239">Pulsaci�n de tecla: F9</span><span class="sxs-lookup"><span data-stu-id="16ed0-239">Keystroke: F9</span></span>
  
<span data-ttu-id="16ed0-240">VBA: **Application.Calculate**</span><span class="sxs-lookup"><span data-stu-id="16ed0-240">VBA: **Application.Calculate**</span></span>
  
<span data-ttu-id="16ed0-241">API de C: **xlcCalculateNow**</span><span class="sxs-lookup"><span data-stu-id="16ed0-241">C API: **xlcCalculateNow**</span></span>
  
- <span data-ttu-id="16ed0-242">**Todos los modos**</span><span class="sxs-lookup"><span data-stu-id="16ed0-242">**All modes**</span></span>
    
    <span data-ttu-id="16ed0-p123">Actualiza todas las celdas que Excel marca como desfasadas, es decir, los dependientes de datos vol�tiles o modificados, y las celdas marcadas mediante programaci�n como desfasadas. Si el modo de c�lculo es Autom�tico excepto en tablas, se calculan las tablas que necesiten una actualizaci�n y tambi�n todas las funciones vol�tiles y sus dependientes.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p123">Recalculates all cells that Excel has marked as dirty, that is, dependents of volatile or changed data, and cells programmatically marked as dirty. If the calculation mode is Automatic Except Tables, this calculates those tables that require updating and also all volatile functions and their dependents.</span></span>
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a><span data-ttu-id="16ed0-245">Recompilaci�n y c�lculo forzado de todos �rboles de libros</span><span class="sxs-lookup"><span data-stu-id="16ed0-245">All Open Workbooks Tree Rebuild and Forced Calculation</span></span>

<span data-ttu-id="16ed0-246">Pulsaci�n de tecla: CTRL+ALT+F9</span><span class="sxs-lookup"><span data-stu-id="16ed0-246">Keystroke: CTRL+ALT+F9</span></span>
  
<span data-ttu-id="16ed0-247">VBA: **Application.CalculateFull**</span><span class="sxs-lookup"><span data-stu-id="16ed0-247">VBA: **Application.CalculateFull**</span></span>
  
<span data-ttu-id="16ed0-248">API de C: no se admite</span><span class="sxs-lookup"><span data-stu-id="16ed0-248">C API: Not supported</span></span>
  
- <span data-ttu-id="16ed0-249">**Todos los modos**</span><span class="sxs-lookup"><span data-stu-id="16ed0-249">**All modes**</span></span>
    
    <span data-ttu-id="16ed0-p124">Actualiza todas las celdas de todos los libros abiertos. Si el modo de c�lculo es Autom�tico excepto en tablas, fuerza la actualizaci�n de las tablas.</span><span class="sxs-lookup"><span data-stu-id="16ed0-p124">Recalculates all cells in all open workbooks. If the calculation mode is Automatic Except Tables, it forces the tables to be recalculated.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="16ed0-252">Vea tambi�n</span><span class="sxs-lookup"><span data-stu-id="16ed0-252">See also</span></span>



[<span data-ttu-id="16ed0-253">Nuevo c�lculo multiproceso en Excel</span><span class="sxs-lookup"><span data-stu-id="16ed0-253">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="16ed0-254">Tipos de datos utilizados por Excel</span><span class="sxs-lookup"><span data-stu-id="16ed0-254">Data Types Used by Excel</span></span>](data-types-used-by-excel.md)
  
[<span data-ttu-id="16ed0-255">Administraci�n de memoria en Excel</span><span class="sxs-lookup"><span data-stu-id="16ed0-255">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="16ed0-256">Conceptos de programaci�n de Excel</span><span class="sxs-lookup"><span data-stu-id="16ed0-256">Excel Programming Concepts</span></span>](excel-programming-concepts.md)

