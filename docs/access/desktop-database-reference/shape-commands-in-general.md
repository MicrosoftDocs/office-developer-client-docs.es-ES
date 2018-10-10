---
title: Comandos Shape en general
TOCTitle: Shape Commands in General
ms:assetid: ad555aa7-bc64-b495-a98d-e927061a5809
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249814(v=office.15)
ms:contentKeyID: 48547039
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 33570bec65de4ff88667ad90b591c4f288c86d96
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485190"
---
# <a name="shape-commands-in-general"></a><span data-ttu-id="da47c-102">Comandos Shape en general</span><span class="sxs-lookup"><span data-stu-id="da47c-102">Shape Commands in General</span></span>


<span data-ttu-id="da47c-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="da47c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="da47c-104">La aplicación de forma a los datos define las columnas de un objeto **Recordset** con forma, las relaciones entre las entidades representadas por las columnas y la forma en que se rellena el objeto **Recordset** con datos.</span><span class="sxs-lookup"><span data-stu-id="da47c-104">Data shaping defines the columns of a shaped **Recordset**, the relationships between the entities represented by the columns, and the manner in which the **Recordset** is populated with data.</span></span>

<span data-ttu-id="da47c-105">Un objeto **Recordset** con forma puede constar de los siguientes tipos de columna.</span><span class="sxs-lookup"><span data-stu-id="da47c-105">A shaped **Recordset** may consist of the following types of columns.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da47c-106">Tipo de columna</span><span class="sxs-lookup"><span data-stu-id="da47c-106">Column type</span></span></p></th>
<th><p><span data-ttu-id="da47c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="da47c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da47c-108">data</span><span class="sxs-lookup"><span data-stu-id="da47c-108">data</span></span></p></td>
<td><p><span data-ttu-id="da47c-109">Campos de un objeto <strong>Recordset</strong> devueltos por un comando de consulta a un proveedor de datos, una tabla o un objeto <strong>Recordset</strong> al que se ha aplicado forma anteriormente.</span><span class="sxs-lookup"><span data-stu-id="da47c-109">Fields from a <strong>Recordset</strong> returned by a query command to a data provider, table, or previously shaped <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da47c-110">capítulo</span><span class="sxs-lookup"><span data-stu-id="da47c-110">chapter</span></span></p></td>
<td><p><span data-ttu-id="da47c-p101">Referencia a otro objeto <strong>Recordset</strong>, que se denomina <em>capítulo</em>. Las columnas de capítulo permiten definir una relación de <em>objeto primario-objeto secundario</em> donde el <em>objeto primario</em> es el objeto <strong>Recordset</strong> que contiene la columna de capítulo y el <em>objeto secundario</em> es el objeto <strong>Recordset</strong> representado por el capítulo.</span><span class="sxs-lookup"><span data-stu-id="da47c-p101">A reference to another <strong>Recordset</strong>, called a <em>chapter</em>. Chapter columns make it possible to define a <em>parent-child</em> relationship where the <em>parent</em> is the <strong>Recordset</strong> containing the chapter column and the <em>child</em> is the <strong>Recordset</strong> represented by the chapter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da47c-113">agregado</span><span class="sxs-lookup"><span data-stu-id="da47c-113">aggregate</span></span></p></td>
<td><p><span data-ttu-id="da47c-p102">El valor de la columna se deriva ejecutando una <em>función de agregado</em> en todas las filas o una columna de todos las filas de un objeto <strong>Recordset</strong> secundario. (Vea Funciones de agregado en el tema siguiente, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Funciones de agregado, función CALC y palabra clave NEW</a>.)</span><span class="sxs-lookup"><span data-stu-id="da47c-p102">The value of the column is derived by executing an <em>aggregate function</em> on all the rows or a column of all the rows of a child <strong>Recordset</strong>. (See Aggregate Functions in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a>.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da47c-116">expresión calculada</span><span class="sxs-lookup"><span data-stu-id="da47c-116">calculated expression</span></span></p></td>
<td><p><span data-ttu-id="da47c-p103">El valor de la columna se deriva calculando una expresión de Visual Basic para Aplicaciones en las columnas de la misma fila del objeto <strong>Recordset</strong>. La expresión es el argumento de la función CALC. (Vea Expresión calculada en el siguiente tema, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Funciones de agregado, función CALC y palabra clave NEW</a>, y en <a href="visual-basic-for-applications-functions.md">Funciones de Visual Basic para Aplicaciones</a>.)</span><span class="sxs-lookup"><span data-stu-id="da47c-p103">The value of the column is derived by calculating a Visual Basic for Applications expression on columns in the same row of the <strong>Recordset</strong>. The expression is the argument to the CALC function. (See Calculated Expression in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a> and in <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications Functions</a>.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da47c-120">nuevo</span><span class="sxs-lookup"><span data-stu-id="da47c-120">new</span></span></p></td>
<td><p><span data-ttu-id="da47c-p104">Campos creados vacíos, que se pueden rellenar con datos más adelante. La columna se define con la palabra clave NEW. (Vea la palabra clave NEW en el tema siguiente, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Funciones de agregado, función CALC y palabra clave NEW</a>.)</span><span class="sxs-lookup"><span data-stu-id="da47c-p104">Empty, fabricated fields, which may be populated with data at a later time. The column is defined with the NEW keyword. (See NEW keyword in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a>.)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="da47c-p105">Un comando Shape puede contener una cláusula que especifica un comando de consulta a un proveedor de datos subyacente que va a devolver un objeto **Recordset**. La sintaxis de la consulta depende de los requisitos del proveedor de datos subyacente. Normalmente será el Lenguaje de consulta estructurado (SQL), si bien ADO no requiere el uso de ningún lenguaje de consulta en particular.</span><span class="sxs-lookup"><span data-stu-id="da47c-p105">A shape command may contain a clause specifying a query command to an underlying data provider that will return a **Recordset** object. The query's syntax depends on the requirements of the underlying data provider. This will usually be Structured Query Language (SQL), although ADO does not require the use of any particular query language.</span></span>

<span data-ttu-id="da47c-p106">Se puede usar una cláusula SQL JOIN para relacionar dos tablas; sin embargo, un objeto **Recordset** jerárquico puede representar la información más eficazmente. Cada fila de un objeto **Recordset** que se ha creado mediante JOIN repite de manera redundante la información de una de las tablas. Un objeto **Recordset** jerárquico tiene solo un objeto **Recordset** primario por cada uno de los múltiples objetos **Recordset** secundarios.</span><span class="sxs-lookup"><span data-stu-id="da47c-p106">You could use a SQL JOIN clause to relate two tables; however, a hierarchical **Recordset** may represent the information more efficiently. Each row of a **Recordset** created by a JOIN repeats information redundantly from one of the tables. A hierarchical **Recordset** has only one parent **Recordset** for each of multiple child **Recordset** objects.</span></span>

<span data-ttu-id="da47c-130">Los comandos Shape los pueden emitir los objetos **Recordset** o se pueden emitir estableciendo la propiedad [CommandText](commandtext-property-ado.md) del objeto [Command](command-object-ado.md) y, a continuación, llamando al método [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="da47c-130">Shape commands can be issued by **Recordset** objects or by setting the [CommandText](commandtext-property-ado.md) property of the [Command](command-object-ado.md) object and then calling the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method.</span></span>

<span data-ttu-id="da47c-131">Los comandos Shape se pueden anidar.</span><span class="sxs-lookup"><span data-stu-id="da47c-131">Shape commands can be nested.</span></span> <span data-ttu-id="da47c-132">Es decir, el *comando a primario* o el *comando a secundario* puede ser otro comando shape.</span><span class="sxs-lookup"><span data-stu-id="da47c-132">That is, the *parent-command* or *child-command* may itself be another shape command.</span></span>

<span data-ttu-id="da47c-133">El proveedor de formas siempre devuelve un cursor de cliente, incluso si el usuario especifica una ubicación de cursor de \*\* adUseServer\*\*.</span><span class="sxs-lookup"><span data-stu-id="da47c-133">The shape provider always returns a client cursor, even when the user specifies a cursor location of **adUseServer**.</span></span>

<span data-ttu-id="da47c-134">Para obtener información sobre cómo desplazarse por un objeto **Recordset** jerárquico, vea [ Obtener acceso a las filas de un objeto Recordset jerárquico ](accessing-rows-in-a-hierarchical-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="da47c-134">For information about navigating a hierarchical **Recordset**, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="da47c-135">Para obtener información precisa sobre los comandos Shape sintácticamente correctos, vea [Gramática formal del comando Shape](formal-shape-grammar.md).</span><span class="sxs-lookup"><span data-stu-id="da47c-135">For precise information about syntactically correct shape commands, see [Formal Shape Grammar](formal-shape-grammar.md).</span></span>

