---
title: Funcionamiento de comandos parametrizados
TOCTitle: Operation of parameterized commands
ms:assetid: 71edbd16-21db-7afa-356b-d8e7afb92b3a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249456(v=office.15)
ms:contentKeyID: 48545596
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1623b32a5ec52acd086bf028a5c1775daae989e8
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997052"
---
# <a name="operation-of-parameterized-commands"></a><span data-ttu-id="da7f9-102">Funcionamiento de comandos parametrizados</span><span class="sxs-lookup"><span data-stu-id="da7f9-102">Operation of parameterized commands</span></span>

<span data-ttu-id="da7f9-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="da7f9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="da7f9-104">Si se trabaja con un **conjunto de registros** secundario grande, especialmente en comparación con el tamaño del **conjunto de registros** principal, pero sólo se necesita obtener acceso a unos pocos capítulos secundarios, podría resultar más eficaz utilizar un comando parametrizado.</span><span class="sxs-lookup"><span data-stu-id="da7f9-104">If you are working with a large child **Recordset**, especially compared to the size of the parent **Recordset**, but need to access only a few child chapters, you might find it more efficient to use a parameterized command.</span></span>

<span data-ttu-id="da7f9-105">Un *comando no parametrizado* recupera los **conjuntos de registros**secundarios y principal completo, anexa una columna de capítulo al principal y, a continuación, asigna una referencia al capítulo secundario relacionado para cada fila principal.</span><span class="sxs-lookup"><span data-stu-id="da7f9-105">A *non-parameterized command* retrieves both the entire parent and child **Recordsets**, appends a chapter column to the parent, and then assigns a reference to the related child chapter for each parent row.</span></span>

<span data-ttu-id="da7f9-106">Un *comando parametrizado* recupera al **conjunto de registros**principal completo, pero sólo recupera el **conjunto de registros** cuando se obtiene acceso a la columna de capítulo.</span><span class="sxs-lookup"><span data-stu-id="da7f9-106">A *parameterized command* retrieves the entire parent **Recordset**, but retrieves only the chapter **Recordset** when the chapter column is accessed.</span></span> <span data-ttu-id="da7f9-107">Esta diferencia en la estrategia de recuperación puede suponer ventajas considerables en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="da7f9-107">This difference in retrieval strategy can yield significant performance benefits.</span></span>

<span data-ttu-id="da7f9-108">Por ejemplo, se puede especificar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="da7f9-108">For example, you can specify the following:</span></span>

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

<span data-ttu-id="da7f9-109">Las tablas primarias y secundarias tienen un nombre de columna en común, cliente\_identificador *.*</span><span class="sxs-lookup"><span data-stu-id="da7f9-109">The parent and child tables have a column name in common, cust\_id *.*</span></span> <span data-ttu-id="da7f9-110">El *comando secundario* tiene un marcador de posición "?", a la que hace referencia la cláusula RELATE (es decir, "..." PARÁMETRO 0").</span><span class="sxs-lookup"><span data-stu-id="da7f9-110">The *child-command* has a "?" placeholder, to which the RELATE clause refers (that is, "...PARAMETER 0").</span></span>

> [!NOTE]
> <span data-ttu-id="da7f9-p103">[!NOTA] La cláusula PARAMETER pertenece sólo a la sintaxis del comando Shape. No está asociada al objeto [Parameter](parameter-object-ado.md) de ADO ni a la colección [Parameters](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="da7f9-p103">The PARAMETER clause pertains solely to the shape command syntax. It is not associated with either the ADO [Parameter](parameter-object-ado.md) object or the [Parameters](parameters-collection-ado.md) collection.</span></span>

<span data-ttu-id="da7f9-113">Cuando se ejecuta el comando parametrizado Shape, ocurre lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="da7f9-113">When the parameterized shape command is executed, the following occurs:</span></span>

1.  <span data-ttu-id="da7f9-114">El *comando a principal* se ejecuta y devuelve a un **objeto Recordset** primario de la tabla Customers.</span><span class="sxs-lookup"><span data-stu-id="da7f9-114">The *parent-command* is executed and returns a parent **Recordset** from the Customers table.</span></span>

2.  <span data-ttu-id="da7f9-115">Una columna de capítulo se anexa al **conjunto de registros** principal.</span><span class="sxs-lookup"><span data-stu-id="da7f9-115">A chapter column is appended to the parent **Recordset**.</span></span>

3.  <span data-ttu-id="da7f9-116">Cuando se obtiene acceso a la columna de capítulo de una fila principal, el *comando secundario* se ejecuta utilizando el valor de la customer.cust\_id como el valor del parámetro.</span><span class="sxs-lookup"><span data-stu-id="da7f9-116">When the chapter column of a parent row is accessed, the *child-command* is executed using the value of the customer.cust\_id as the value of the parameter.</span></span>

4.  <span data-ttu-id="da7f9-117">Todas las filas del conjunto de filas del proveedor de datos creadas en el paso 3 se usan para rellenar el **conjunto de registros** secundario.</span><span class="sxs-lookup"><span data-stu-id="da7f9-117">All rows in the data provider rowset created in step 3 are used to populate the child **Recordset**.</span></span> <span data-ttu-id="da7f9-118">En este ejemplo, que es todas las filas de la tabla Orders en el que el cliente\_identificador es igual al valor de customer.cust\_id.</span><span class="sxs-lookup"><span data-stu-id="da7f9-118">In this example, that is all the rows in the Orders table in which the cust\_id equals the value of customer.cust\_id.</span></span> <span data-ttu-id="da7f9-119">De forma predeterminada, el elemento secundario s de **conjunto de registros**se almacenarán en caché en el cliente hasta que se suelten todas las referencias al **conjunto de registros** principal.</span><span class="sxs-lookup"><span data-stu-id="da7f9-119">By default, the child **Recordset**s will be cached on the client until all references to the parent **Recordset** are released.</span></span> <span data-ttu-id="da7f9-120">Para cambiar este comportamiento, establezca la [propiedad dinámica](ado-dynamic-property-index.md)de **Recordset** **Cache Child Rows** en **False**.</span><span class="sxs-lookup"><span data-stu-id="da7f9-120">To change this behavior, set the **Recordset** [dynamic property](ado-dynamic-property-index.md)**Cache Child Rows** to **False**.</span></span>

5.  <span data-ttu-id="da7f9-121">Una referencia a las filas secundarias recuperadas (es decir, el capítulo del **conjunto de registros** secundario) se coloca en la columna de capítulo de la fila activa del **conjunto de registros** principal.</span><span class="sxs-lookup"><span data-stu-id="da7f9-121">A reference to the retrieved child rows (that is, the chapter of the child **Recordset**) is placed in the chapter column of the current row of the parent **Recordset**.</span></span>

6.  <span data-ttu-id="da7f9-122">Los pasos 3 a 5 se repiten cuando se obtiene acceso a la columna de capítulo de otra fila.</span><span class="sxs-lookup"><span data-stu-id="da7f9-122">Steps 3–5 are repeated when the chapter column of another row is accessed.</span></span>

<span data-ttu-id="da7f9-p105">La propiedad dinámica **Cache Child Rows** se establece de forma predeterminada en **True**. El comportamiento de almacenamiento en caché varía según los valores de los parámetros de la consulta. En una consulta con un solo parámetro, el **conjunto de registros** secundario correspondiente a un valor de parámetro determinado se almacenará en caché entre solicitudes de un secundario con ese valor. El código siguiente lo muestra:</span><span class="sxs-lookup"><span data-stu-id="da7f9-p105">The **Cache Child Rows** dynamic property is set to **True** by default. The caching behavior varies depending upon the parameter values of the query. In a query with a single parameter, the child **Recordset** for a given parameter value will be cached between requests for a child with that value. The following code demonstrates this:</span></span>

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

<span data-ttu-id="da7f9-127">En una consulta con dos o más parámetros, sólo se utiliza un secundario almacenado en caché si todos los valores de parámetros coinciden con los valores en caché.</span><span class="sxs-lookup"><span data-stu-id="da7f9-127">In a query with two or more parameters, a cached child is used only if all the parameter values match the cached values.</span></span>

## <a name="parameterized-commands-and-complex-parent-child-relations"></a><span data-ttu-id="da7f9-128">Comandos parametrizados y relaciones secundarias de complejas entre principal</span><span class="sxs-lookup"><span data-stu-id="da7f9-128">Parameterized commands and complex parent child relations</span></span>

<span data-ttu-id="da7f9-129">Además de utilizar comandos parametrizados para mejorar el rendimiento de una jerarquía de tipo combinación equivalente, los comandos parametrizados pueden servir para admitir relaciones principal-secundario más complejas.</span><span class="sxs-lookup"><span data-stu-id="da7f9-129">In addition to using parameterized commands to improve performance of an equi-join type hierarchy, parameterized commands can be used to support more complex parent-child relationships.</span></span> <span data-ttu-id="da7f9-130">Por ejemplo, considere la posibilidad de una base de datos de poca deportiva con dos tablas: uno que consta de los equipos (equipo\_identificador, equipo\_nombre) y la otra de juegos (fecha, página principal\_equipo, visite\_equipo).</span><span class="sxs-lookup"><span data-stu-id="da7f9-130">For example, consider a Little League database with two tables: one consisting of the teams (team\_id, team\_name) and the other of games (date, home\_team, visiting\_team).</span></span>

<span data-ttu-id="da7f9-131">Utilizando una jerarquía no parametrizada, no hay forma de relacionar las tablas de equipos y encuentros de forma tal que el **conjunto de registros** secundario para cada equipo contenga su programación completa.</span><span class="sxs-lookup"><span data-stu-id="da7f9-131">Using a non-parameterized hierarchy, there is no way to relate the teams and games tables in such a way that the child **Recordset** for each team contains its complete schedule.</span></span> <span data-ttu-id="da7f9-132">Puede crear capítulos que contengan la programación de encuentros en casa o la de encuentros fuera de casa, pero no ambas.</span><span class="sxs-lookup"><span data-stu-id="da7f9-132">You can create chapters that contain the home schedule or the road schedule, but not both.</span></span> <span data-ttu-id="da7f9-133">Esto se debe a que la cláusula RELATE limita a relaciones principal-secundario de la forma (pc1=cc1) AND (pc2=pc2).</span><span class="sxs-lookup"><span data-stu-id="da7f9-133">This is because the RELATE clause limits you to parent-child relationships of the form (pc1=cc1) AND (pc2=pc2).</span></span> <span data-ttu-id="da7f9-134">Por lo tanto, si el comando incluye "equipo relacionar\_principal de identificador para\_team, equipo de\_identificador a visitar\_equipo", obtendría sólo juegos donde estaba reproduciendo un equipo propio.</span><span class="sxs-lookup"><span data-stu-id="da7f9-134">So, if your command included "RELATE team\_id TO home\_team, team\_id TO visiting\_team", you would get only games where a team was playing itself.</span></span> <span data-ttu-id="da7f9-135">Lo que desea es "(equipo\_id = home\_equipo) o (equipo\_identificador = visitar\_equipo)", pero el proveedor Shape no admite la cláusula OR.</span><span class="sxs-lookup"><span data-stu-id="da7f9-135">What you want is "(team\_id=home\_team) OR (team\_id=visiting\_team)", but the Shape provider does not support the OR clause.</span></span>

<span data-ttu-id="da7f9-p108">Para obtener el resultado deseado, puede utilizar un comando parametrizado. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="da7f9-p108">To obtain the desired result, you can use a parameterized command. For example:</span></span>

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

<span data-ttu-id="da7f9-138">Este ejemplo aprovecha la mayor flexibilidad de la cláusula WHERE de SQL para obtener el resultado que necesita.</span><span class="sxs-lookup"><span data-stu-id="da7f9-138">This example exploits the greater flexibility of the SQL WHERE clause to get the result you need.</span></span>

