---
title: 'Capítulo 9: Crear formas de datos'
TOCTitle: 'Chapter 9: Data shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ad9d5e989bc1c6f4a54fb4882cfe3c3e357fd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296426"
---
# <a name="chapter-9-data-shaping"></a><span data-ttu-id="bae96-102">Capítulo 9: Crear formas de datos</span><span class="sxs-lookup"><span data-stu-id="bae96-102">Chapter 9: Data shaping</span></span>

<span data-ttu-id="bae96-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bae96-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bae96-104">La *Forma de datos* permite consultar un origen de datos y devolver un objeto [Recordset](recordset-object-ado.md) que representa una relación de objeto primario-objeto secundario entre dos o más entidades lógicas (una jerarquía).</span><span class="sxs-lookup"><span data-stu-id="bae96-104">*Data shaping* provides a way to query a data source and return a [Recordset](recordset-object-ado.md) that represents a parent-child relationship between two or more logical entities (a hierarchy).</span></span> 

<span data-ttu-id="bae96-105">Un ejemplo clásico de una relación jerárquica es la de clientes y pedidos.</span><span class="sxs-lookup"><span data-stu-id="bae96-105">A classic example of a hierarchical relationship is customers and orders.</span></span> <span data-ttu-id="bae96-106">For every customer in a database, there can be zero or more orders.</span><span class="sxs-lookup"><span data-stu-id="bae96-106">For every customer in a database, there can be zero or more orders.</span></span> <span data-ttu-id="bae96-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span><span class="sxs-lookup"><span data-stu-id="bae96-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span></span> <span data-ttu-id="bae96-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span><span class="sxs-lookup"><span data-stu-id="bae96-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span></span> <span data-ttu-id="bae96-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span><span class="sxs-lookup"><span data-stu-id="bae96-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span></span>

<span data-ttu-id="bae96-p102">La sintaxis de la forma de datos también proporciona otras funciones. Los programadores pueden crear nuevos objetos **Recordset** sin origen de datos subyacente mediante la palabra clave NEW para describir los campos de los objetos **Recordset** primarios y secundarios. El nuevo objeto **Recordset** se puede rellenar con datos y almacenar de manera permanente. Los programadores también pueden realizar varios cálculos o agregaciones (por ejemplo, SUMA, MEDIA y MAX) en los campos secundarios. Además, la forma de datos puede crear un objeto **Recordset** primario a partir de un objeto **Recordset** secundario agrupando los registros en el objeto secundario y colocando una fila en el objeto primario por cada grupo en el objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="bae96-p102">The data shaping syntax also provides other capabilities. Developers can create new **Recordset** objects without an underlying data source by using the NEW keyword to describe the fields of the parent and child **Recordsets**. The new **Recordset** object can be populated with data and persistently stored. Developers can also perform various calculations or aggregations (for example, SUM, AVG, and MAX) on child fields. Data shaping can also create a parent **Recordset** from a child **Recordset** by grouping records in the child and placing one row in the parent for each group in the child.</span></span>

<span data-ttu-id="bae96-115">Vea los temas siguientes para obtener más información sobre la forma de datos:</span><span class="sxs-lookup"><span data-stu-id="bae96-115">See the following topics to learn more about data shaping:</span></span>

- [<span data-ttu-id="bae96-116">Proveedores necesarios para la creación de formas de datos</span><span class="sxs-lookup"><span data-stu-id="bae96-116">Required providers for data shaping</span></span>](required-providers-for-data-shaping.md)
- [<span data-ttu-id="bae96-117">Cláusula de forma Compute</span><span class="sxs-lookup"><span data-stu-id="bae96-117">Shape Compute clause</span></span>](shape-compute-clause.md)
- [<span data-ttu-id="bae96-118">Fabricación de conjuntos de registros jerárquicos</span><span class="sxs-lookup"><span data-stu-id="bae96-118">Fabricating hierarchical Recordsets</span></span>](fabricating-hierarchical-recordsets.md)
- [<span data-ttu-id="bae96-119">Acceso a las filas en conjuntos de registros jerárquicos</span><span class="sxs-lookup"><span data-stu-id="bae96-119">Accessing rows in a hierarchical Recordset</span></span>](accessing-rows-in-a-hierarchical-recordset.md)
- [<span data-ttu-id="bae96-120">Gramática de las formas formales</span><span class="sxs-lookup"><span data-stu-id="bae96-120">Formal shape grammar</span></span>](formal-shape-grammar.md)
- [<span data-ttu-id="bae96-121">Funciones de Visual Basic para Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="bae96-121">Visual Basic for Applications functions</span></span>](visual-basic-for-applications-functions.md)
- [<span data-ttu-id="bae96-122">Cláusula Shape Append (ADO)</span><span class="sxs-lookup"><span data-stu-id="bae96-122">Shape Append clause (ADO)</span></span>](shape-append-clause.md)
- [<span data-ttu-id="bae96-123">Forma de datos (ADO)</span><span class="sxs-lookup"><span data-stu-id="bae96-123">Data shaping (ADO)</span></span>](data-shaping.md)
- [<span data-ttu-id="bae96-124">Comandos Shape en general (ADO)</span><span class="sxs-lookup"><span data-stu-id="bae96-124">Shape commands in general (ADO)</span></span>](shape-commands-in-general.md)

