---
title: Cláusula Compute de Shape
TOCTitle: Shape Compute clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4f8dbeb97a4afdc068d635411d6035f68ba1168b
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946401"
---
# <a name="shape-compute-clause"></a><span data-ttu-id="6253e-102">Cláusula Compute de Shape</span><span class="sxs-lookup"><span data-stu-id="6253e-102">Shape Compute clause</span></span>

<span data-ttu-id="6253e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6253e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6253e-104">Una cláusula COMPUTE del comando Shape genera un objeto **Recordset** primario, cuyas columnas se componen de una referencia al objeto **Recordset** secundario; columnas opcionales cuyo contenido son columnas de capítulo, nuevas o calculadas, o bien el resultado de ejecutar funciones de agregado en el objeto **Recordset** secundario o un objeto **Recordset** al que se ha aplicado forma anteriormente; así como cualquier columna del objeto **Recordset** secundario que aparezca en la cláusula opcional BY.</span><span class="sxs-lookup"><span data-stu-id="6253e-104">A shape COMPUTE clause generates a parent **Recordset**, whose columns consist of a reference to the child **Recordset**; optional columns whose contents are chapter, new, or calculated columns, or the result of executing aggregate functions on the child **Recordset** or a previously shaped **Recordset**; and any columns from the child **Recordset** listed in the optional BY clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="6253e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6253e-105">Syntax</span></span>

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a><span data-ttu-id="6253e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6253e-106">Description</span></span>

<span data-ttu-id="6253e-107">Los elementos de esta cláusula son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="6253e-107">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="6253e-108">*comando secundario*</span><span class="sxs-lookup"><span data-stu-id="6253e-108">*child-command*</span></span>

  - <span data-ttu-id="6253e-109">Consta de uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="6253e-109">Consists of one of the following:</span></span>
    
    - <span data-ttu-id="6253e-p101">Un comando de consulta entre llaves ("{}") que devuelve un objeto **Recordset** secundario. El comando se emite al proveedor de datos subyacente y su sintaxis depende de los requisitos de ese proveedor. Suele ser el lenguaje SQL, si bien ADO no requiere ningún lenguaje de consulta en particular.</span><span class="sxs-lookup"><span data-stu-id="6253e-p101">A query command within curly braces ("{}") that returns a child **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
    - <span data-ttu-id="6253e-113">El nombre de un objeto **Recordset** con forma existente.</span><span class="sxs-lookup"><span data-stu-id="6253e-113">The name of an existing shaped **Recordset**.</span></span>
    
    - <span data-ttu-id="6253e-114">Otro comando Shape.</span><span class="sxs-lookup"><span data-stu-id="6253e-114">Another shape command.</span></span>
    
    - <span data-ttu-id="6253e-115">La palabra clave TABLE, seguida del nombre de una tabla en el proveedor de datos.</span><span class="sxs-lookup"><span data-stu-id="6253e-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="6253e-116">*alias secundario*</span><span class="sxs-lookup"><span data-stu-id="6253e-116">*child-alias*</span></span>

  - <span data-ttu-id="6253e-117">Un alias utilizado para hacer referencia al **objeto Recordset** devuelto por la *comando secundario.*</span><span class="sxs-lookup"><span data-stu-id="6253e-117">An alias used to refer to the **Recordset** returned by the *child-command.*</span></span> <span data-ttu-id="6253e-118">El *alias secundario* se requiere en la lista de columnas en la cláusula COMPUTE y define a la relación entre los objetos **Recordset** primarios y secundarios.</span><span class="sxs-lookup"><span data-stu-id="6253e-118">The *child-alias* is required in the list of columns in the COMPUTE clause and defines the relation between the parent and child **Recordset** objects.</span></span>

- <span data-ttu-id="6253e-119">*lista de columnas adjuntas*</span><span class="sxs-lookup"><span data-stu-id="6253e-119">*appended-column-list*</span></span>

  - <span data-ttu-id="6253e-p103">Una lista donde cada elemento define una columna en el objeto primario generado. Cada elemento contiene una columna de capítulo, una columna nueva, una columna calculada o un valor resultante de una función de agregado en el objeto **Recordset** secundario.</span><span class="sxs-lookup"><span data-stu-id="6253e-p103">A list in which each element defines a column in the generated parent. Each element contains either a chapter column, a new column, a calculated column, or a value resulting from an aggregate function on the child **Recordset**.</span></span>

- <span data-ttu-id="6253e-122">*lista de campos agrupados*</span><span class="sxs-lookup"><span data-stu-id="6253e-122">*grp-field-list*</span></span>

  - <span data-ttu-id="6253e-123">Una lista de columnas en el objeto **Recordset** primario y secundario que especifica cómo deben agruparse las filas en el objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="6253e-123">A list of columns in the parent and child **Recordset** objects that specifies how rows should be grouped in the child.</span></span> <span data-ttu-id="6253e-124">Para cada columna en el *campo lista agrupados,* hay una columna correspondiente en los objetos **Recordset** primarios y secundarios.</span><span class="sxs-lookup"><span data-stu-id="6253e-124">For each column in the *grp-field-list,* there is a corresponding column in the child and parent **Recordset** objects.</span></span> <span data-ttu-id="6253e-125">Para cada fila del **objeto Recordset**primario, las columnas de la *lista de campos agrupados* tienen valores únicos, y el elemento secundario **Recordset** al que hace referencia la fila primaria consta únicamente de secundarios filas cuya *lista de campos agrupados* columnas tienen los mismos valores que el fila primaria.</span><span class="sxs-lookup"><span data-stu-id="6253e-125">For each row in the parent **Recordset**, the *grp-field-list* columns have unique values, and the child **Recordset** referenced by the parent row consists solely of child rows whose *grp-field-list* columns have the same values as the parent row.</span></span>

<span data-ttu-id="6253e-p105">Si se incluye la cláusula BY, las filas del objeto **Recordset** secundario se agruparán basándose en las columnas de la cláusula COMPUTE. El objeto **Recordset** primario contendrá una fila por cada grupo de filas en el objeto **Recordset** secundario.</span><span class="sxs-lookup"><span data-stu-id="6253e-p105">If the BY clause is included, the child **Recordset**'s rows will be grouped based on the columns in the COMPUTE clause. The parent **Recordset** will contain one row for each group of rows in the child **Recordset**.</span></span>

<span data-ttu-id="6253e-p106">Si se omite la cláusula BY, todo el objeto **Recordset** secundario se trata como un solo grupo y el objeto **Recordset** primario contendrá exactamente una fila. Esa fila hará referencia a todo el objeto **Recordset** secundario. Si se omite la cláusula BY, se podrán calcular agregados de "Total general" en todo el objeto **Recordset** secundario.</span><span class="sxs-lookup"><span data-stu-id="6253e-p106">If the BY clause is omitted, the entire child **Recordset** is treated as a single group and the parent **Recordset** will contain exactly one row. That row will reference the entire child **Recordset**. Omitting the BY clause allows you to compute "grand total" aggregates over the entire child **Recordset**.</span></span>

<span data-ttu-id="6253e-131">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6253e-131">For example:</span></span>

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

<span data-ttu-id="6253e-p107">Independientemente de cómo se forme el objeto **Recordset** primario (mediante COMPUTE o APPEND), contendrá una columna de capítulo que se usa para relacionarlo con un objeto **Recordset** secundario. Si lo desea, el objeto **Recordset** primario también puede contener columnas con agregados (SUMA, MIN, MAX, etc.) de las filas secundarias. Tanto el objeto **Recordset** primario como el secundario pueden incluir columnas que contienen una expresión en la fila del objeto **Recordset**, así como columnas nuevas e inicialmente vacías.</span><span class="sxs-lookup"><span data-stu-id="6253e-p107">Regardless of which way the parent **Recordset** is formed (using COMPUTE or using APPEND), it will contain a chapter column that is used to relate it to a child **Recordset**. If you wish, the parent **Recordset** may also contain columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows. Both the parent and the child **Recordset** may contain columns that contain an expression on the row in the **Recordset**, as well as columns that are new and initially empty.</span></span>

## <a name="operation"></a><span data-ttu-id="6253e-135">Operación</span><span class="sxs-lookup"><span data-stu-id="6253e-135">Operation</span></span>

<span data-ttu-id="6253e-136">El *comando a secundario* se emite al proveedor, que devuelve a un **objeto Recordset**secundario.</span><span class="sxs-lookup"><span data-stu-id="6253e-136">The *child-command* is issued to the provider, which returns a child **Recordset**.</span></span>

<span data-ttu-id="6253e-p108">La cláusula COMPUTE especifica las columnas del objeto **Recordset** primario, que pueden ser una referencia al objeto **Recordset** secundario, uno o varios agregados, una expresión calculada o columnas nuevas. Si hay una cláusula BY, las columnas que define también se anexan al objeto **Recordset** primario. La cláusula BY especifica cómo se agrupan las filas del objeto **Recordset** secundario.</span><span class="sxs-lookup"><span data-stu-id="6253e-p108">The COMPUTE clause specifies the columns of the parent **Recordset**, which may be a reference to the child **Recordset**, one or more aggregates, a calculated expression, or new columns. If there is a BY clause, the columns it defines are also appended to the parent **Recordset**. The BY clause specifies how the rows of the child **Recordset** are grouped.</span></span>

<span data-ttu-id="6253e-140">Por ejemplo, supongamos que tenemos una tabla denominada Demographics (Datos demográficos) que consta de los campos Estado, Ciudad y Población (los datos de población son a título ilustrativo).</span><span class="sxs-lookup"><span data-stu-id="6253e-140">For example, assume you have a table — Demographics — consisting of State, City, and Population fields (the population figures are solely for illustration).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6253e-141">Estado</span><span class="sxs-lookup"><span data-stu-id="6253e-141">State</span></span></p></th>
<th><p><span data-ttu-id="6253e-142">Ciudad</span><span class="sxs-lookup"><span data-stu-id="6253e-142">City</span></span></p></th>
<th><p><span data-ttu-id="6253e-143">Población</span><span class="sxs-lookup"><span data-stu-id="6253e-143">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6253e-144">WA</span><span class="sxs-lookup"><span data-stu-id="6253e-144">WA</span></span></p></td>
<td><p><span data-ttu-id="6253e-145">Seattle</span><span class="sxs-lookup"><span data-stu-id="6253e-145">Seattle</span></span></p></td>
<td><p><span data-ttu-id="6253e-146">700.000</span><span class="sxs-lookup"><span data-stu-id="6253e-146">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6253e-147">OR</span><span class="sxs-lookup"><span data-stu-id="6253e-147">OR</span></span></p></td>
<td><p><span data-ttu-id="6253e-148">Medford</span><span class="sxs-lookup"><span data-stu-id="6253e-148">Medford</span></span></p></td>
<td><p><span data-ttu-id="6253e-149">200.000</span><span class="sxs-lookup"><span data-stu-id="6253e-149">200,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6253e-150">OR</span><span class="sxs-lookup"><span data-stu-id="6253e-150">OR</span></span></p></td>
<td><p><span data-ttu-id="6253e-151">Portland</span><span class="sxs-lookup"><span data-stu-id="6253e-151">Portland</span></span></p></td>
<td><p><span data-ttu-id="6253e-152">400.000</span><span class="sxs-lookup"><span data-stu-id="6253e-152">400,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6253e-153">CA</span><span class="sxs-lookup"><span data-stu-id="6253e-153">CA</span></span></p></td>
<td><p><span data-ttu-id="6253e-154">Los Ángeles</span><span class="sxs-lookup"><span data-stu-id="6253e-154">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="6253e-155">800.000</span><span class="sxs-lookup"><span data-stu-id="6253e-155">800,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6253e-156">CA</span><span class="sxs-lookup"><span data-stu-id="6253e-156">CA</span></span></p></td>
<td><p><span data-ttu-id="6253e-157">San Diego</span><span class="sxs-lookup"><span data-stu-id="6253e-157">San Diego</span></span></p></td>
<td><p><span data-ttu-id="6253e-158">600.000</span><span class="sxs-lookup"><span data-stu-id="6253e-158">600,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6253e-159">WA</span><span class="sxs-lookup"><span data-stu-id="6253e-159">WA</span></span></p></td>
<td><p><span data-ttu-id="6253e-160">Tacoma</span><span class="sxs-lookup"><span data-stu-id="6253e-160">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="6253e-161">500.000</span><span class="sxs-lookup"><span data-stu-id="6253e-161">500,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6253e-162">OR</span><span class="sxs-lookup"><span data-stu-id="6253e-162">OR</span></span></p></td>
<td><p><span data-ttu-id="6253e-163">Corvallis</span><span class="sxs-lookup"><span data-stu-id="6253e-163">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="6253e-164">300.000</span><span class="sxs-lookup"><span data-stu-id="6253e-164">300,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6253e-165">Emita ahora este comando Shape:</span><span class="sxs-lookup"><span data-stu-id="6253e-165">Now, issue this shape command:</span></span>

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

<span data-ttu-id="6253e-166">Este comando abre un objeto **Recordset** con forma que consta de dos niveles.</span><span class="sxs-lookup"><span data-stu-id="6253e-166">This command opens a shaped **Recordset** with two levels.</span></span> <span data-ttu-id="6253e-167">El nivel primario es un **conjunto de registros** de generado con una columna agregada (SUM(rs.population)), una columna que hace referencia al elemento secundario de **Recordset** (rs) y una columna para agrupar al **objeto Recordset** (estado) secundario.</span><span class="sxs-lookup"><span data-stu-id="6253e-167">The parent level is a generated **Recordset** with an aggregate column (SUM(rs.population) ), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="6253e-168">El nivel secundario es el **objeto Recordset** devuelto por el comando de consulta (), una columna que hace referencia al elemento secundario de **Recordset** (rs) y una columna para agrupar al **objeto Recordset** (estado) secundario.</span><span class="sxs-lookup"><span data-stu-id="6253e-168">The child level is the **Recordset** returned by the query command (), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="6253e-169">El nivel secundario es el **objeto Recordset** devuelto por el comando de consulta (seleccione \* de datos demográficos).</span><span class="sxs-lookup"><span data-stu-id="6253e-169">The child level is the **Recordset** returned by the query command (select \* from demographics ).</span></span>

<span data-ttu-id="6253e-p110">Las filas de detalle del objeto **Recordset** secundario se agruparán por estado, pero por lo demás en ningún orden particular. Es decir, los grupos no estarán en orden alfabético ni numérico. Si desea ordenar el objeto **Recordset** primario, podrá utilizar el método **Sort** del objeto **Recordset** para ordenar el objeto **Recordset** primario.</span><span class="sxs-lookup"><span data-stu-id="6253e-p110">The child **Recordset** detail rows will be grouped by state, but otherwise in no particular order. That is, the groups will not be in alphabetical or numerical order. If you want the parent **Recordset** to be ordered, you can use the **Recordset** **Sort** method to order the parent **Recordset**.</span></span>

<span data-ttu-id="6253e-p111">Ahora, puede navegar por el objeto **Recordset** primario abierto y obtener acceso a los objetos **Recordset** secundarios de detalle. Para obtener más información, vea [ Obtener acceso a las filas de un objeto Recordset jerárquico ](accessing-rows-in-a-hierarchical-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="6253e-p111">You can now navigate the opened parent **Recordset** and access the child detail **Recordset** objects. For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="6253e-175">**Objetos Recordset primarios y secundarios de detalle resultantes**</span><span class="sxs-lookup"><span data-stu-id="6253e-175">**Resultant Parent and Child Detail Recordsets**</span></span>

<span data-ttu-id="6253e-176">**Primario**</span><span class="sxs-lookup"><span data-stu-id="6253e-176">**Parent**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6253e-177">SUM (rs.Population)</span><span class="sxs-lookup"><span data-stu-id="6253e-177">SUM (rs.Population)</span></span></p></th>
<th><p><span data-ttu-id="6253e-178">rs</span><span class="sxs-lookup"><span data-stu-id="6253e-178">rs</span></span></p></th>
<th><p><span data-ttu-id="6253e-179">Estado</span><span class="sxs-lookup"><span data-stu-id="6253e-179">State</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6253e-180">1,300,000</span><span class="sxs-lookup"><span data-stu-id="6253e-180">1,300,000</span></span></p></td>
<td><p><span data-ttu-id="6253e-181">Referencia a secundario1</span><span class="sxs-lookup"><span data-stu-id="6253e-181">Reference to child1</span></span></p></td>
<td><p><span data-ttu-id="6253e-182">CA</span><span class="sxs-lookup"><span data-stu-id="6253e-182">CA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6253e-183">1,200,000</span><span class="sxs-lookup"><span data-stu-id="6253e-183">1,200,000</span></span></p></td>
<td><p><span data-ttu-id="6253e-184">Referencia a secundario2</span><span class="sxs-lookup"><span data-stu-id="6253e-184">Reference to child2</span></span></p></td>
<td><p><span data-ttu-id="6253e-185">WA</span><span class="sxs-lookup"><span data-stu-id="6253e-185">WA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6253e-186">1,100,000</span><span class="sxs-lookup"><span data-stu-id="6253e-186">1,100,000</span></span></p></td>
<td><p><span data-ttu-id="6253e-187">Referencia a secundario3</span><span class="sxs-lookup"><span data-stu-id="6253e-187">Reference to child3</span></span></p></td>
<td><p><span data-ttu-id="6253e-188">OR</span><span class="sxs-lookup"><span data-stu-id="6253e-188">OR</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6253e-189">**Secundario1**</span><span class="sxs-lookup"><span data-stu-id="6253e-189">**Child1**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6253e-190">Estado</span><span class="sxs-lookup"><span data-stu-id="6253e-190">State</span></span></p></th>
<th><p><span data-ttu-id="6253e-191">Ciudad</span><span class="sxs-lookup"><span data-stu-id="6253e-191">City</span></span></p></th>
<th><p><span data-ttu-id="6253e-192">Población</span><span class="sxs-lookup"><span data-stu-id="6253e-192">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6253e-193">CA</span><span class="sxs-lookup"><span data-stu-id="6253e-193">CA</span></span></p></td>
<td><p><span data-ttu-id="6253e-194">Los Ángeles</span><span class="sxs-lookup"><span data-stu-id="6253e-194">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="6253e-195">800.000</span><span class="sxs-lookup"><span data-stu-id="6253e-195">800,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6253e-196">CA</span><span class="sxs-lookup"><span data-stu-id="6253e-196">CA</span></span></p></td>
<td><p><span data-ttu-id="6253e-197">San Diego</span><span class="sxs-lookup"><span data-stu-id="6253e-197">San Diego</span></span></p></td>
<td><p><span data-ttu-id="6253e-198">600.000</span><span class="sxs-lookup"><span data-stu-id="6253e-198">600,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6253e-199">**Secundario2**</span><span class="sxs-lookup"><span data-stu-id="6253e-199">**Child2**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6253e-200">Estado</span><span class="sxs-lookup"><span data-stu-id="6253e-200">State</span></span></p></th>
<th><p><span data-ttu-id="6253e-201">Ciudad</span><span class="sxs-lookup"><span data-stu-id="6253e-201">City</span></span></p></th>
<th><p><span data-ttu-id="6253e-202">Población</span><span class="sxs-lookup"><span data-stu-id="6253e-202">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6253e-203">WA</span><span class="sxs-lookup"><span data-stu-id="6253e-203">WA</span></span></p></td>
<td><p><span data-ttu-id="6253e-204">Seattle</span><span class="sxs-lookup"><span data-stu-id="6253e-204">Seattle</span></span></p></td>
<td><p><span data-ttu-id="6253e-205">700.000</span><span class="sxs-lookup"><span data-stu-id="6253e-205">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6253e-206">WA</span><span class="sxs-lookup"><span data-stu-id="6253e-206">WA</span></span></p></td>
<td><p><span data-ttu-id="6253e-207">Tacoma</span><span class="sxs-lookup"><span data-stu-id="6253e-207">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="6253e-208">500.000</span><span class="sxs-lookup"><span data-stu-id="6253e-208">500,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6253e-209">**Secundario3**</span><span class="sxs-lookup"><span data-stu-id="6253e-209">**Child3**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6253e-210">Estado</span><span class="sxs-lookup"><span data-stu-id="6253e-210">State</span></span></p></th>
<th><p><span data-ttu-id="6253e-211">Ciudad</span><span class="sxs-lookup"><span data-stu-id="6253e-211">City</span></span></p></th>
<th><p><span data-ttu-id="6253e-212">Población</span><span class="sxs-lookup"><span data-stu-id="6253e-212">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6253e-213">OR</span><span class="sxs-lookup"><span data-stu-id="6253e-213">OR</span></span></p></td>
<td><p><span data-ttu-id="6253e-214">Medford</span><span class="sxs-lookup"><span data-stu-id="6253e-214">Medford</span></span></p></td>
<td><p><span data-ttu-id="6253e-215">200.000</span><span class="sxs-lookup"><span data-stu-id="6253e-215">200,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6253e-216">OR</span><span class="sxs-lookup"><span data-stu-id="6253e-216">OR</span></span></p></td>
<td><p><span data-ttu-id="6253e-217">Portland</span><span class="sxs-lookup"><span data-stu-id="6253e-217">Portland</span></span></p></td>
<td><p><span data-ttu-id="6253e-218">400.000</span><span class="sxs-lookup"><span data-stu-id="6253e-218">400,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6253e-219">OR</span><span class="sxs-lookup"><span data-stu-id="6253e-219">OR</span></span></p></td>
<td><p><span data-ttu-id="6253e-220">Corvallis</span><span class="sxs-lookup"><span data-stu-id="6253e-220">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="6253e-221">300.000</span><span class="sxs-lookup"><span data-stu-id="6253e-221">300,000</span></span></p></td>
</tr>
</tbody>
</table>

