---
title: Funcionamiento de los comandos sin parámetros
TOCTitle: Operation of non-parameterized commands
ms:assetid: 934740b1-07d0-140e-7c83-00feb34c01d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249651(v=office.15)
ms:contentKeyID: 48546395
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 720cbaf346b64d4d23b1e3314b06ba941e78b700
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288269"
---
# <a name="operation-of-non-parameterized-commands"></a><span data-ttu-id="940bd-102">Funcionamiento de los comandos sin parámetros</span><span class="sxs-lookup"><span data-stu-id="940bd-102">Operation of non-parameterized commands</span></span>


<span data-ttu-id="940bd-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="940bd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="940bd-p101">Para comandos no parametrizados, durante la ejecución del comando, se ejecutan todos los comandos de proveedor y se crean los **conjuntos de registros**. Si el comando se ejecuta sincrónicamente, todos los **conjuntos de registros** se llenarán completamente. Si se seleccionó un modo de llenado asincrónico, el estado relleno de los **conjuntos de registros** dependerá del modo de llenado y del tamaño de los **conjuntos de registros**.</span><span class="sxs-lookup"><span data-stu-id="940bd-p101">For non-parameterized commands, all of the provider commands are executed and the **Recordsets** are created during command execution. If the command is executed synchronously, all of the **Recordsets** will be fully populated. If an asynchronous population mode was selected, the populated state of the **Recordsets** will depend on the population mode and the size of the **Recordsets**.</span></span>

<span data-ttu-id="940bd-107">Por ejemplo, el *comando principal* podría devolver un **conjunto de registros** de clientes para una compañía desde una tabla Customers y el *comando secundario* podría devolver un **conjunto de registros** de pedidos correspondientes a todos los clientes desde una tabla Orders.</span><span class="sxs-lookup"><span data-stu-id="940bd-107">For example, the *parent-command* could return a **Recordset** of customers for a company from a Customers table, and the *child-command* could return a **Recordset** of orders for all customers from an Orders table.</span></span>

```vb 
 
SHAPE {SELECT * FROM Customers} 
 APPEND ({SELECT * FROM Orders} AS chapOrders 
 RELATE customerID TO customerID) 
```

<span data-ttu-id="940bd-108">Para relaciones principal-secundario no parametrizados, cada objeto **Recordset** principal y secundario debe tener una columna en común para poder asociarlos.</span><span class="sxs-lookup"><span data-stu-id="940bd-108">For non-parameterized parent-child relationships, each parent and child **Recordset** object must have a column in common to associate them.</span></span> <span data-ttu-id="940bd-109">Las columnas se mencionan en la cláusula RELATE, primero la *columna principal* y luego la *columna secundaria*.</span><span class="sxs-lookup"><span data-stu-id="940bd-109">The columns are named in the RELATE clause, *parent-column* first and then *child-column*.</span></span> <span data-ttu-id="940bd-110">Las columnas pueden tener nombres distintos en sus objetos **Recordset** respectivos, pero deben hacer referencia a la misma información para poder especificar una relación significativa.</span><span class="sxs-lookup"><span data-stu-id="940bd-110">The columns may have different names in their respective **Recordset** objects but must refer to the same information in order to specify a meaningful relation.</span></span> <span data-ttu-id="940bd-111">Por ejemplo, los objetos **Recordset** de **Customers** y **Orders** podrían tener en común un campo customerID de identificación del cliente.</span><span class="sxs-lookup"><span data-stu-id="940bd-111">For example, the **Customers** and **Orders** **Recordset** objects could both have a customerID field.</span></span> <span data-ttu-id="940bd-112">Dado que la pertenencia del **conjunto de registros** secundario se determina mediante el comando del proveedor, el **conjunto de registros** secundario puede contener filas huérfanas.</span><span class="sxs-lookup"><span data-stu-id="940bd-112">Because the membership of the child **Recordset** is determined by the provider command, it is possible for the child **Recordset** to contain orphaned rows.</span></span> <span data-ttu-id="940bd-113">No se puede tener acceso a estas filas huérfanas sin cambiar de forma.</span><span class="sxs-lookup"><span data-stu-id="940bd-113">These orphaned rows are inaccessible without further reshaping.</span></span>

<span data-ttu-id="940bd-p103">El proceso de forma de datos anexa una columna de capítulo al **conjunto de registros** principal. Los valores de la columna de capítulo son referencias a filas del **conjunto de registros** secundario, que cumplen la cláusula RELATE. Es decir, el mismo valor está en la *columna principal* de una fila principal determinada y en la *columna secundaria* de todas las filas del secundario del capítulo. Cuando se utilizan varias cláusulas TO en la misma cláusula RELATE, éstas se combinan implícitamente utilizando un operador AND. Si las columnas principales de la cláusula RELATE no constituyen una clave para el **conjunto de registros** principal, una fila secundaria única podría tener varias filas principales.</span><span class="sxs-lookup"><span data-stu-id="940bd-p103">Data shaping appends a chapter column to the parent **Recordset**. The values in the chapter column are references to rows in the child **Recordset**, which satisfy the RELATE clause. That is, the same value is in the *parent-column* of a given parent row as is in the *child-column* of all the rows of the chapter child. When multiple TO clauses are used in the same RELATE clause, they are implicitly combined using an AND operator. If the parent columns in the relate clause do not constitute a key to the parent **Recordset**, a single child row may have multiple parent rows.</span></span>

<span data-ttu-id="940bd-p104">Cuando se obtiene acceso a la referencia de la columna de capítulo, ADO recupera automáticamente el **conjunto de registros** representado por la referencia. Tenga en cuenta que, en un comando no parametrizado, aunque se haya recuperado el **conjunto de registros** secundario completo, el capítulo sólo presenta un subconjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="940bd-p104">When you access the reference in the chapter column, ADO automatically retrieves the **Recordset** represented by the reference. Note that in a non-parameterized command, although the entire child **Recordset** has been retrieved, the chapter only presents a subset of rows.</span></span>

<span data-ttu-id="940bd-p105">Si la columna anexada no tiene ningún *alias de capítulo*, se generará un nombre para ella automáticamente. Un objeto [Field](field-object-ado.md) para la columna se anexará en la colección [Fields](fields-collection-ado.md) del objeto **Recordset**, y su tipo de datos será **adChapter**.</span><span class="sxs-lookup"><span data-stu-id="940bd-p105">If the appended column has no *chapter-alias*, a name will be generated for it automatically. A [Field](field-object-ado.md) object for the column will be appended to the **Recordset** object's [Fields](fields-collection-ado.md) collection, and its data type will be **adChapter**.</span></span>

<span data-ttu-id="940bd-123">Para obtener información acerca de la navegación por un **Recordset** jerárquico, vea [Obtener acceso a filas en un Recordset jerárquico](accessing-rows-in-a-hierarchical-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="940bd-123">For information about navigating a hierarchical **Recordset**, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

