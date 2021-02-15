---
title: Cláusula de forma Compute
TOCTitle: Shape Compute clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eadc448d59814f0573a959c6c1038f9c4afdbac9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306457"
---
# <a name="shape-compute-clause"></a><span data-ttu-id="18c57-102">Cláusula de forma Compute</span><span class="sxs-lookup"><span data-stu-id="18c57-102">Shape Compute clause</span></span>

<span data-ttu-id="18c57-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="18c57-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18c57-104">Una cláusula COMPUTE del comando Shape genera un objeto **Recordset** primario, cuyas columnas se componen de una referencia al objeto **Recordset** secundario; columnas opcionales cuyo contenido son columnas de capítulo, nuevas o calculadas, o bien el resultado de ejecutar funciones de agregado en el objeto **Recordset** secundario o un objeto **Recordset** al que se ha aplicado forma anteriormente; así como cualquier columna del objeto **Recordset** secundario que aparezca en la cláusula opcional BY.</span><span class="sxs-lookup"><span data-stu-id="18c57-104">A shape COMPUTE clause generates a parent **Recordset**, whose columns consist of a reference to the child **Recordset**; optional columns whose contents are chapter, new, or calculated columns, or the result of executing aggregate functions on the child **Recordset** or a previously shaped **Recordset**; and any columns from the child **Recordset** listed in the optional BY clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="18c57-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18c57-105">Syntax</span></span>

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a><span data-ttu-id="18c57-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="18c57-106">Description</span></span>

<span data-ttu-id="18c57-107">Los elementos de esta cláusula son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="18c57-107">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="18c57-108">*comando secundario*</span><span class="sxs-lookup"><span data-stu-id="18c57-108">*child-command*</span></span>

  - <span data-ttu-id="18c57-109">Consta de uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="18c57-109">Consists of one of the following:</span></span>
    
    - <span data-ttu-id="18c57-p101">Un comando de consulta entre llaves ("{}") que devuelve un objeto **Recordset** secundario. El comando se emite al proveedor de datos subyacente y su sintaxis depende de los requisitos de ese proveedor. Suele ser el lenguaje SQL, si bien ADO no requiere ningún lenguaje de consulta en particular.</span><span class="sxs-lookup"><span data-stu-id="18c57-p101">A query command within curly braces ("{}") that returns a child **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
    - <span data-ttu-id="18c57-113">El nombre de un objeto **Recordset** con forma existente.</span><span class="sxs-lookup"><span data-stu-id="18c57-113">The name of an existing shaped **Recordset**.</span></span>
    
    - <span data-ttu-id="18c57-114">Otro comando Shape.</span><span class="sxs-lookup"><span data-stu-id="18c57-114">Another shape command.</span></span>
    
    - <span data-ttu-id="18c57-115">La palabra clave TABLE, seguida del nombre de una tabla en el proveedor de datos.</span><span class="sxs-lookup"><span data-stu-id="18c57-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="18c57-116">*alias secundario*</span><span class="sxs-lookup"><span data-stu-id="18c57-116">*child-alias*</span></span>

  - <span data-ttu-id="18c57-p102">Un alias utilizado para hacer referencia al objeto **Recordset** devuelto por el *comando secundario*. El *alias secundario* se requiere en la lista de columnas de la cláusula COMPUTE y define la relación entre los objetos **Recordset** primario y secundario.</span><span class="sxs-lookup"><span data-stu-id="18c57-p102">An alias used to refer to the **Recordset** returned by the *child-command.* The *child-alias* is required in the list of columns in the COMPUTE clause and defines the relation between the parent and child **Recordset** objects.</span></span>

- <span data-ttu-id="18c57-119">*lista de columnas adjuntas*</span><span class="sxs-lookup"><span data-stu-id="18c57-119">*appended-column-list*</span></span>

  - <span data-ttu-id="18c57-p103">Una lista donde cada elemento define una columna en el objeto primario generado. Cada elemento contiene una columna de capítulo, una columna nueva, una columna calculada o un valor resultante de una función de agregado en el objeto **Recordset** secundario.</span><span class="sxs-lookup"><span data-stu-id="18c57-p103">A list in which each element defines a column in the generated parent. Each element contains either a chapter column, a new column, a calculated column, or a value resulting from an aggregate function on the child **Recordset**.</span></span>

- <span data-ttu-id="18c57-122">*lista de campos agrupados*</span><span class="sxs-lookup"><span data-stu-id="18c57-122">*grp-field-list*</span></span>

  - <span data-ttu-id="18c57-123">Una lista de columnas en el objeto **Recordset** primario y secundario que especifica cómo deben agruparse las filas en el objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="18c57-123">A list of columns in the parent and child **Recordset** objects that specifies how rows should be grouped in the child.</span></span> <span data-ttu-id="18c57-124">Por cada columna de la *lista de campos agrupados*, hay una columna correspondiente en los objetos **Recordset** primario y secundario.</span><span class="sxs-lookup"><span data-stu-id="18c57-124">For each column in the *grp-field-list,* there is a corresponding column in the child and parent **Recordset** objects.</span></span> <span data-ttu-id="18c57-125">Por cada fila del objeto **Recordset** primario, las columnas de la *lista de campos agrupados* tienen valores únicos, y el objeto **Recordset** secundario al que hace referencia la fila primaria consta sólo de filas secundarias cuyas columnas de la *lista de campos agrupados* tienen los mismos valores que la fila primaria.</span><span class="sxs-lookup"><span data-stu-id="18c57-125">For each row in the parent **Recordset**, the *grp-field-list* columns have unique values, and the child **Recordset** referenced by the parent row consists solely of child rows whose *grp-field-list* columns have the same values as the parent row.</span></span>

<span data-ttu-id="18c57-p105">Si se incluye la cláusula BY, las filas del objeto **Recordset** secundario se agruparán basándose en las columnas de la cláusula COMPUTE. El objeto **Recordset** primario contendrá una fila por cada grupo de filas en el objeto **Recordset** secundario.</span><span class="sxs-lookup"><span data-stu-id="18c57-p105">If the BY clause is included, the child **Recordset**'s rows will be grouped based on the columns in the COMPUTE clause. The parent **Recordset** will contain one row for each group of rows in the child **Recordset**.</span></span>

<span data-ttu-id="18c57-p106">Si se omite la cláusula BY, todo el objeto **Recordset** secundario se trata como un solo grupo y el objeto **Recordset** primario contendrá exactamente una fila. Esa fila hará referencia a todo el objeto **Recordset** secundario. Si se omite la cláusula BY, se podrán calcular agregados de "Total general" en todo el objeto **Recordset** secundario.</span><span class="sxs-lookup"><span data-stu-id="18c57-p106">If the BY clause is omitted, the entire child **Recordset** is treated as a single group and the parent **Recordset** will contain exactly one row. That row will reference the entire child **Recordset**. Omitting the BY clause allows you to compute "grand total" aggregates over the entire child **Recordset**.</span></span>

<span data-ttu-id="18c57-131">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="18c57-131">For example:</span></span>

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

<span data-ttu-id="18c57-p107">Independientemente de cómo se forme el objeto **Recordset** primario (mediante COMPUTE o APPEND), contendrá una columna de capítulo que se usa para relacionarlo con un objeto **Recordset** secundario. Si lo desea, el objeto **Recordset** primario también puede contener columnas con agregados (SUMA, MIN, MAX, etc.) de las filas secundarias. Tanto el objeto **Recordset** primario como el secundario pueden incluir columnas que contienen una expresión en la fila del objeto **Recordset**, así como columnas nuevas e inicialmente vacías.</span><span class="sxs-lookup"><span data-stu-id="18c57-p107">Regardless of which way the parent **Recordset** is formed (using COMPUTE or using APPEND), it will contain a chapter column that is used to relate it to a child **Recordset**. If you wish, the parent **Recordset** may also contain columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows. Both the parent and the child **Recordset** may contain columns that contain an expression on the row in the **Recordset**, as well as columns that are new and initially empty.</span></span>

## <a name="operation"></a><span data-ttu-id="18c57-135">Operación</span><span class="sxs-lookup"><span data-stu-id="18c57-135">Operation</span></span>

<span data-ttu-id="18c57-136">El *comando secundario* se emite al proveedor, que devuelve un objeto **Recordset** secundario.</span><span class="sxs-lookup"><span data-stu-id="18c57-136">The *child-command* is issued to the provider, which returns a child **Recordset**.</span></span>

<span data-ttu-id="18c57-p108">La cláusula COMPUTE especifica las columnas del objeto **Recordset** primario, que pueden ser una referencia al objeto **Recordset** secundario, uno o varios agregados, una expresión calculada o columnas nuevas. Si hay una cláusula BY, las columnas que define también se anexan al objeto **Recordset** primario. La cláusula BY especifica cómo se agrupan las filas del objeto **Recordset** secundario.</span><span class="sxs-lookup"><span data-stu-id="18c57-p108">The COMPUTE clause specifies the columns of the parent **Recordset**, which may be a reference to the child **Recordset**, one or more aggregates, a calculated expression, or new columns. If there is a BY clause, the columns it defines are also appended to the parent **Recordset**. The BY clause specifies how the rows of the child **Recordset** are grouped.</span></span>

<span data-ttu-id="18c57-140">Por ejemplo, supongamos que tenemos una tabla denominada  Demographics  (Datos demográficos) que consta de los campos Estado, Ciudad y Población (los datos de población son a título ilustrativo).</span><span class="sxs-lookup"><span data-stu-id="18c57-140">For example, assume you have a table — Demographics — consisting of State, City, and Population fields (the population figures are solely for illustration).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18c57-141">Estado</span><span class="sxs-lookup"><span data-stu-id="18c57-141">State</span></span></p></th>
<th><p><span data-ttu-id="18c57-142">Ciudad</span><span class="sxs-lookup"><span data-stu-id="18c57-142">City</span></span></p></th>
<th><p><span data-ttu-id="18c57-143">Población</span><span class="sxs-lookup"><span data-stu-id="18c57-143">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18c57-144">WA</span><span class="sxs-lookup"><span data-stu-id="18c57-144">WA</span></span></p></td>
<td><p><span data-ttu-id="18c57-145">Seattle</span><span class="sxs-lookup"><span data-stu-id="18c57-145">Seattle</span></span></p></td>
<td><p><span data-ttu-id="18c57-146">700,000</span><span class="sxs-lookup"><span data-stu-id="18c57-146">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18c57-147">O</span><span class="sxs-lookup"><span data-stu-id="18c57-147">OR</span></span></p></td>
<td><p><span data-ttu-id="18c57-148">Medford</span><span class="sxs-lookup"><span data-stu-id="18c57-148">Medford</span></span></p></td>
<td><p><span data-ttu-id="18c57-149">200.000</span><span class="sxs-lookup"><span data-stu-id="18c57-149">200,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18c57-150">O</span><span class="sxs-lookup"><span data-stu-id="18c57-150">OR</span></span></p></td>
<td><p><span data-ttu-id="18c57-151">Portland</span><span class="sxs-lookup"><span data-stu-id="18c57-151">Portland</span></span></p></td>
<td><p><span data-ttu-id="18c57-152">400,000</span><span class="sxs-lookup"><span data-stu-id="18c57-152">400,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18c57-153">CA</span><span class="sxs-lookup"><span data-stu-id="18c57-153">CA</span></span></p></td>
<td><p><span data-ttu-id="18c57-154">Los Ángeles</span><span class="sxs-lookup"><span data-stu-id="18c57-154">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="18c57-155">800,000</span><span class="sxs-lookup"><span data-stu-id="18c57-155">800,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18c57-156">CA</span><span class="sxs-lookup"><span data-stu-id="18c57-156">CA</span></span></p></td>
<td><p><span data-ttu-id="18c57-157">San Diego</span><span class="sxs-lookup"><span data-stu-id="18c57-157">San Diego</span></span></p></td>
<td><p><span data-ttu-id="18c57-158">600.000</span><span class="sxs-lookup"><span data-stu-id="18c57-158">600,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18c57-159">WA</span><span class="sxs-lookup"><span data-stu-id="18c57-159">WA</span></span></p></td>
<td><p><span data-ttu-id="18c57-160">Ann</span><span class="sxs-lookup"><span data-stu-id="18c57-160">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="18c57-161">500 000</span><span class="sxs-lookup"><span data-stu-id="18c57-161">500,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18c57-162">O</span><span class="sxs-lookup"><span data-stu-id="18c57-162">OR</span></span></p></td>
<td><p><span data-ttu-id="18c57-163">Corvallis</span><span class="sxs-lookup"><span data-stu-id="18c57-163">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="18c57-164">300,000</span><span class="sxs-lookup"><span data-stu-id="18c57-164">300,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18c57-165">Emita ahora este comando Shape:</span><span class="sxs-lookup"><span data-stu-id="18c57-165">Now, issue this shape command:</span></span>

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

<span data-ttu-id="18c57-166">Este comando abre un objeto **Recordset** con forma que consta de dos niveles.</span><span class="sxs-lookup"><span data-stu-id="18c57-166">This command opens a shaped **Recordset** with two levels.</span></span> <span data-ttu-id="18c57-167">El nivel primario  es un conjunto de registros generado con una columna de agregado (SUM(rs.population) ), una columna que hace referencia al objeto **Recordset** secundario (rs) y una columna para agrupar el objeto **Recordset** secundario (estado).</span><span class="sxs-lookup"><span data-stu-id="18c57-167">The parent level is a generated **Recordset** with an aggregate column (SUM(rs.population) ), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="18c57-168">El nivel secundario es el **conjunto** de registros devuelto por el comando de consulta (), una columna que hace referencia al objeto **Recordset** secundario (rs) y una columna para agrupar el objeto **Recordset** secundario (estado).</span><span class="sxs-lookup"><span data-stu-id="18c57-168">The child level is the **Recordset** returned by the query command (), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="18c57-169">El nivel secundario es el **conjunto de registros** devuelto por el comando de consulta (selección de datos \* demográficos).</span><span class="sxs-lookup"><span data-stu-id="18c57-169">The child level is the **Recordset** returned by the query command (select \* from demographics ).</span></span>

<span data-ttu-id="18c57-p110">Las filas de detalle del objeto **Recordset** secundario se agruparán por estado, pero por lo demás en ningún orden particular. Es decir, los grupos no estarán en orden alfabético ni numérico. Si desea ordenar el objeto **Recordset** primario, podrá utilizar el método **Sort** del objeto **Recordset** para ordenar el objeto **Recordset** primario.</span><span class="sxs-lookup"><span data-stu-id="18c57-p110">The child **Recordset** detail rows will be grouped by state, but otherwise in no particular order. That is, the groups will not be in alphabetical or numerical order. If you want the parent **Recordset** to be ordered, you can use the **Recordset** **Sort** method to order the parent **Recordset**.</span></span>

<span data-ttu-id="18c57-p111">Ahora, puede navegar por el objeto **Recordset** primario abierto y obtener acceso a los objetos **Recordset** secundarios de detalle. Para obtener más información, vea [ Obtener acceso a las filas de un objeto Recordset jerárquico](accessing-rows-in-a-hierarchical-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="18c57-p111">You can now navigate the opened parent **Recordset** and access the child detail **Recordset** objects. For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="18c57-175">**Objetos Recordset primarios y secundarios de detalle resultantes**</span><span class="sxs-lookup"><span data-stu-id="18c57-175">**Resultant Parent and Child Detail Recordsets**</span></span>

<span data-ttu-id="18c57-176">**Primario**</span><span class="sxs-lookup"><span data-stu-id="18c57-176">**Parent**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18c57-177">SUM (rs.Population)</span><span class="sxs-lookup"><span data-stu-id="18c57-177">SUM (rs.Population)</span></span></p></th>
<th><p><span data-ttu-id="18c57-178">rs</span><span class="sxs-lookup"><span data-stu-id="18c57-178">rs</span></span></p></th>
<th><p><span data-ttu-id="18c57-179">Estado</span><span class="sxs-lookup"><span data-stu-id="18c57-179">State</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18c57-180">1,300,000</span><span class="sxs-lookup"><span data-stu-id="18c57-180">1,300,000</span></span></p></td>
<td><p><span data-ttu-id="18c57-181">Referencia a secundario1</span><span class="sxs-lookup"><span data-stu-id="18c57-181">Reference to child1</span></span></p></td>
<td><p><span data-ttu-id="18c57-182">CA</span><span class="sxs-lookup"><span data-stu-id="18c57-182">CA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18c57-183">1,200,000</span><span class="sxs-lookup"><span data-stu-id="18c57-183">1,200,000</span></span></p></td>
<td><p><span data-ttu-id="18c57-184">Referencia a secundario2</span><span class="sxs-lookup"><span data-stu-id="18c57-184">Reference to child2</span></span></p></td>
<td><p><span data-ttu-id="18c57-185">WA</span><span class="sxs-lookup"><span data-stu-id="18c57-185">WA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18c57-186">1,100,000</span><span class="sxs-lookup"><span data-stu-id="18c57-186">1,100,000</span></span></p></td>
<td><p><span data-ttu-id="18c57-187">Referencia a secundario3</span><span class="sxs-lookup"><span data-stu-id="18c57-187">Reference to child3</span></span></p></td>
<td><p><span data-ttu-id="18c57-188">O</span><span class="sxs-lookup"><span data-stu-id="18c57-188">OR</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18c57-189">**Child1**</span><span class="sxs-lookup"><span data-stu-id="18c57-189">**Child1**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18c57-190">Estado</span><span class="sxs-lookup"><span data-stu-id="18c57-190">State</span></span></p></th>
<th><p><span data-ttu-id="18c57-191">Ciudad</span><span class="sxs-lookup"><span data-stu-id="18c57-191">City</span></span></p></th>
<th><p><span data-ttu-id="18c57-192">Población</span><span class="sxs-lookup"><span data-stu-id="18c57-192">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18c57-193">CA</span><span class="sxs-lookup"><span data-stu-id="18c57-193">CA</span></span></p></td>
<td><p><span data-ttu-id="18c57-194">Los Ángeles</span><span class="sxs-lookup"><span data-stu-id="18c57-194">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="18c57-195">800,000</span><span class="sxs-lookup"><span data-stu-id="18c57-195">800,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18c57-196">CA</span><span class="sxs-lookup"><span data-stu-id="18c57-196">CA</span></span></p></td>
<td><p><span data-ttu-id="18c57-197">San Diego</span><span class="sxs-lookup"><span data-stu-id="18c57-197">San Diego</span></span></p></td>
<td><p><span data-ttu-id="18c57-198">600.000</span><span class="sxs-lookup"><span data-stu-id="18c57-198">600,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18c57-199">**Child2**</span><span class="sxs-lookup"><span data-stu-id="18c57-199">**Child2**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18c57-200">Estado</span><span class="sxs-lookup"><span data-stu-id="18c57-200">State</span></span></p></th>
<th><p><span data-ttu-id="18c57-201">Ciudad</span><span class="sxs-lookup"><span data-stu-id="18c57-201">City</span></span></p></th>
<th><p><span data-ttu-id="18c57-202">Población</span><span class="sxs-lookup"><span data-stu-id="18c57-202">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18c57-203">WA</span><span class="sxs-lookup"><span data-stu-id="18c57-203">WA</span></span></p></td>
<td><p><span data-ttu-id="18c57-204">Seattle</span><span class="sxs-lookup"><span data-stu-id="18c57-204">Seattle</span></span></p></td>
<td><p><span data-ttu-id="18c57-205">700,000</span><span class="sxs-lookup"><span data-stu-id="18c57-205">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18c57-206">WA</span><span class="sxs-lookup"><span data-stu-id="18c57-206">WA</span></span></p></td>
<td><p><span data-ttu-id="18c57-207">Ann</span><span class="sxs-lookup"><span data-stu-id="18c57-207">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="18c57-208">500 000</span><span class="sxs-lookup"><span data-stu-id="18c57-208">500,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18c57-209">**Child3**</span><span class="sxs-lookup"><span data-stu-id="18c57-209">**Child3**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18c57-210">Estado</span><span class="sxs-lookup"><span data-stu-id="18c57-210">State</span></span></p></th>
<th><p><span data-ttu-id="18c57-211">Ciudad</span><span class="sxs-lookup"><span data-stu-id="18c57-211">City</span></span></p></th>
<th><p><span data-ttu-id="18c57-212">Población</span><span class="sxs-lookup"><span data-stu-id="18c57-212">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18c57-213">O</span><span class="sxs-lookup"><span data-stu-id="18c57-213">OR</span></span></p></td>
<td><p><span data-ttu-id="18c57-214">Medford</span><span class="sxs-lookup"><span data-stu-id="18c57-214">Medford</span></span></p></td>
<td><p><span data-ttu-id="18c57-215">200.000</span><span class="sxs-lookup"><span data-stu-id="18c57-215">200,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18c57-216">O</span><span class="sxs-lookup"><span data-stu-id="18c57-216">OR</span></span></p></td>
<td><p><span data-ttu-id="18c57-217">Portland</span><span class="sxs-lookup"><span data-stu-id="18c57-217">Portland</span></span></p></td>
<td><p><span data-ttu-id="18c57-218">400,000</span><span class="sxs-lookup"><span data-stu-id="18c57-218">400,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18c57-219">O</span><span class="sxs-lookup"><span data-stu-id="18c57-219">OR</span></span></p></td>
<td><p><span data-ttu-id="18c57-220">Corvallis</span><span class="sxs-lookup"><span data-stu-id="18c57-220">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="18c57-221">300,000</span><span class="sxs-lookup"><span data-stu-id="18c57-221">300,000</span></span></p></td>
</tr>
</tbody>
</table>

