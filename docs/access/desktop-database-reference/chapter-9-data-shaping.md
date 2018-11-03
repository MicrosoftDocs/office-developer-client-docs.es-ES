---
title: 'Capítulo 9: Forma de datos'
TOCTitle: 'Chapter 9: Data shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 53a74a53b8c741921ad51ae79ca18e95cda2923d
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936556"
---
# <a name="chapter-9-data-shaping"></a><span data-ttu-id="c5649-102">Capítulo 9: Forma de datos</span><span class="sxs-lookup"><span data-stu-id="c5649-102">Chapter 9: Data shaping</span></span>

<span data-ttu-id="c5649-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5649-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5649-104">*Forma de datos* proporciona una forma de consultar un origen de datos y devolver un [objeto Recordset](recordset-object-ado.md) que representa una relación de elementos primarios y secundarios entre dos o más entidades lógicas (una jerarquía).</span><span class="sxs-lookup"><span data-stu-id="c5649-104">*Data shaping* provides a way to query a data source and return a [Recordset](recordset-object-ado.md) that represents a parent-child relationship between two or more logical entities (a hierarchy).</span></span> 

<span data-ttu-id="c5649-105">Un ejemplo clásico de una relación jerárquica es customers y orders.</span><span class="sxs-lookup"><span data-stu-id="c5649-105">A classic example of a hierarchical relationship is customers and orders.</span></span> <span data-ttu-id="c5649-106">Para cada cliente en una base de datos, puede ser cero o más pedidos.</span><span class="sxs-lookup"><span data-stu-id="c5649-106">For every customer in a database, there can be zero or more orders.</span></span> <span data-ttu-id="c5649-107">Regular SQL proporciona un medio de recuperar los datos mediante la sintaxis JOIN, pero esto puede ser ineficaz y poco flexible porque los datos primarios redundantes se repiten en cada registro devuelto para una relación de elementos primarios y secundarios determinado.</span><span class="sxs-lookup"><span data-stu-id="c5649-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span></span> <span data-ttu-id="c5649-108">Forma de datos puede estar relacionado con un solo registro primario del **objeto Recordset** primario con varios registros secundarios en el **conjunto de registros**, evitando la redundancia de una combinación secundario.</span><span class="sxs-lookup"><span data-stu-id="c5649-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span></span> <span data-ttu-id="c5649-109">La mayoría de las personas encontrar a los elementos primarios y secundarios modelo de programación de **Recordset** más natural y más sencillo trabajar con que el modelo de **conjunto de registros de** combinación solo.</span><span class="sxs-lookup"><span data-stu-id="c5649-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span></span>

<span data-ttu-id="c5649-p102">La sintaxis de la forma de datos también proporciona otras funciones. Los programadores pueden crear nuevos objetos **Recordset** sin origen de datos subyacente mediante la palabra clave NEW para describir los campos de los objetos **Recordset** primarios y secundarios. El nuevo objeto **Recordset** se puede rellenar con datos y almacenar de manera permanente. Los programadores también pueden realizar varios cálculos o agregaciones (por ejemplo, SUMA, MEDIA y MAX) en los campos secundarios. Además, la forma de datos puede crear un objeto **Recordset** primario a partir de un objeto **Recordset** secundario agrupando los registros en el objeto secundario y colocando una fila en el objeto primario por cada grupo en el objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="c5649-p102">The data shaping syntax also provides other capabilities. Developers can create new **Recordset** objects without an underlying data source by using the NEW keyword to describe the fields of the parent and child **Recordsets**. The new **Recordset** object can be populated with data and persistently stored. Developers can also perform various calculations or aggregations (for example, SUM, AVG, and MAX) on child fields. Data shaping can also create a parent **Recordset** from a child **Recordset** by grouping records in the child and placing one row in the parent for each group in the child.</span></span>

<span data-ttu-id="c5649-115">Vea los temas siguientes para obtener más información sobre la forma de datos:</span><span class="sxs-lookup"><span data-stu-id="c5649-115">See the following topics to learn more about data shaping:</span></span>

- [<span data-ttu-id="c5649-116">Proveedores necesarios para la forma de datos</span><span class="sxs-lookup"><span data-stu-id="c5649-116">Required providers for data shaping</span></span>](required-providers-for-data-shaping.md)
- [<span data-ttu-id="c5649-117">Cláusula Compute de Shape</span><span class="sxs-lookup"><span data-stu-id="c5649-117">Shape Compute clause</span></span>](shape-compute-clause.md)
- [<span data-ttu-id="c5649-118">Crear conjuntos de registros jerárquicos</span><span class="sxs-lookup"><span data-stu-id="c5649-118">Fabricating hierarchical Recordsets</span></span>](fabricating-hierarchical-recordsets.md)
- [<span data-ttu-id="c5649-119">Acceso a las filas de un Recordset jerárquico</span><span class="sxs-lookup"><span data-stu-id="c5649-119">Accessing rows in a hierarchical Recordset</span></span>](accessing-rows-in-a-hierarchical-recordset.md)
- [<span data-ttu-id="c5649-120">Gramática formal de forma</span><span class="sxs-lookup"><span data-stu-id="c5649-120">Formal shape grammar</span></span>](formal-shape-grammar.md)
- [<span data-ttu-id="c5649-121">Funciones de Visual Basic para Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c5649-121">Visual Basic for Applications functions</span></span>](visual-basic-for-applications-functions.md)
- [<span data-ttu-id="c5649-122">Cláusula Append de forma (ADO)</span><span class="sxs-lookup"><span data-stu-id="c5649-122">Shape Append clause (ADO)</span></span>](shape-append-clause.md)
- [<span data-ttu-id="c5649-123">Forma (ADO) de datos</span><span class="sxs-lookup"><span data-stu-id="c5649-123">Data shaping (ADO)</span></span>](data-shaping.md)
- [<span data-ttu-id="c5649-124">En general de forma comandos (ADO)</span><span class="sxs-lookup"><span data-stu-id="c5649-124">Shape commands in general (ADO)</span></span>](shape-commands-in-general.md)

