---
title: 'Capítulo 9: Creación de formas de datos'
TOCTitle: 'Chapter 9: Data Shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4636c853f58557b30474b78d902131329084a1a2
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863888"
---
# <a name="chapter-9-data-shaping"></a><span data-ttu-id="07cc5-102">Capítulo 9: Creación de formas de datos</span><span class="sxs-lookup"><span data-stu-id="07cc5-102">Chapter 9: Data Shaping</span></span>


<span data-ttu-id="07cc5-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="07cc5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="07cc5-p101">La *Forma de datos* permite consultar un origen de datos y devolver un objeto [Recordset](recordset-object-ado.md) que representa una relación de objeto primario-objeto secundario entre dos o más entidades lógicas (una jerarquía). Un ejemplo clásico de una relación jerárquica es la de clientes y pedidos. Para cada cliente de una base de datos, puede haber cero o más pedidos. SQL permite recuperar los datos mediante la sintaxis de JOIN, pero esto puede resultar ser ineficaz y poco flexible porque los datos primarios redundantes se repiten en cada registro devuelto para una determinada relación de objeto primario-objeto secundario. La Forma de datos puede relacionar un solo registro primario del objeto **Recordset** primario con varios registros secundarios en el objeto **Recordset** secundario, evitando la redundancia de una sintaxis de JOIN. La mayoría de los usuarios opinan que este modelo de programación de \*\* Recordset\*\* es más natural y más sencillo de usar que el modelo de JOIN de un solo objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="07cc5-p101">*Data shaping* provides a way to query a data source and return a [Recordset](recordset-object-ado.md) that represents a parent-child relationship between two or more logical entities (a hierarchy). A classic example of a hierarchical relationship is customers and orders. For every customer in a database, there can be zero or more orders. Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship. Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN. Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span></span>

<span data-ttu-id="07cc5-p102">La sintaxis de la forma de datos también proporciona otras funciones. Los programadores pueden crear nuevos objetos **Recordset** sin origen de datos subyacente mediante la palabra clave NEW para describir los campos de los objetos **Recordset** primarios y secundarios. El nuevo objeto **Recordset** se puede rellenar con datos y almacenar de manera permanente. Los programadores también pueden realizar varios cálculos o agregaciones (por ejemplo, SUMA, MEDIA y MAX) en los campos secundarios. Además, la forma de datos puede crear un objeto **Recordset** primario a partir de un objeto **Recordset** secundario agrupando los registros en el objeto secundario y colocando una fila en el objeto primario por cada grupo en el objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="07cc5-p102">The data shaping syntax also provides other capabilities. Developers can create new **Recordset** objects without an underlying data source by using the NEW keyword to describe the fields of the parent and child **Recordsets**. The new **Recordset** object can be populated with data and persistently stored. Developers can also perform various calculations or aggregations (for example, SUM, AVG, and MAX) on child fields. Data shaping can also create a parent **Recordset** from a child **Recordset** by grouping records in the child and placing one row in the parent for each group in the child.</span></span>

<span data-ttu-id="07cc5-115">Vea los temas siguientes para obtener más información sobre la forma de datos:</span><span class="sxs-lookup"><span data-stu-id="07cc5-115">See the following topics to learn more about data shaping:</span></span>

- [<span data-ttu-id="07cc5-116">Proveedores necesarios para la forma de datos</span><span class="sxs-lookup"><span data-stu-id="07cc5-116">Required Providers for Data Shaping</span></span>](required-providers-for-data-shaping.md)

- [<span data-ttu-id="07cc5-117">Cláusula Compute de Shape</span><span class="sxs-lookup"><span data-stu-id="07cc5-117">Shape Compute Clause</span></span>](shape-compute-clause.md)

- [<span data-ttu-id="07cc5-118">Crear conjuntos de registros jerárquicos</span><span class="sxs-lookup"><span data-stu-id="07cc5-118">Fabricating Hierarchical Recordsets</span></span>](fabricating-hierarchical-recordsets.md)

- [<span data-ttu-id="07cc5-119">Obtener acceso a las filas de un objeto Recordset jerárquico</span><span class="sxs-lookup"><span data-stu-id="07cc5-119">Accessing Rows in a Hierarchical Recordset</span></span>](accessing-rows-in-a-hierarchical-recordset.md)

- [<span data-ttu-id="07cc5-120">Gramática formal del comando Shape</span><span class="sxs-lookup"><span data-stu-id="07cc5-120">Formal Shape Grammar</span></span>](formal-shape-grammar.md)

- [<span data-ttu-id="07cc5-121">Para las funciones de las aplicaciones de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="07cc5-121">Visual Basic for Applications functions</span></span>](visual-basic-for-applications-functions.md)

- [<span data-ttu-id="07cc5-122">Shape Append Clause (ADO)</span><span class="sxs-lookup"><span data-stu-id="07cc5-122">Shape Append Clause (ADO)</span></span>](shape-append-clause.md)

- [<span data-ttu-id="07cc5-123">Forma (ADO) de datos</span><span class="sxs-lookup"><span data-stu-id="07cc5-123">Data Shaping (ADO)</span></span>](data-shaping.md)

- [<span data-ttu-id="07cc5-124">Shape Commands in General (ADO)</span><span class="sxs-lookup"><span data-stu-id="07cc5-124">Shape Commands in General (ADO)</span></span>](shape-commands-in-general.md)

