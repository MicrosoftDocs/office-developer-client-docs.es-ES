---
title: EjecutarSQL (acción de macro)
TOCTitle: RunSQL Macro Action
ms:assetid: 3692142d-f8a8-e194-0b38-051167f46319
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192476(v=office.15)
ms:contentKeyID: 48544174
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12983
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c5fd5bea659b3df368f6e352d0ae233b5e066113
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875598"
---
# <a name="runsql-macro-action"></a><span data-ttu-id="e67f2-102">EjecutarSQL (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="e67f2-102">RunSQL Macro Action</span></span>


<span data-ttu-id="e67f2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e67f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e67f2-p101">La acción **EjecutarSQL** se usa para ejecutar una consulta de acción de Access mediante la correspondiente instrucción SQL. También puede ejecutar una consulta de definición de datos.</span><span class="sxs-lookup"><span data-stu-id="e67f2-p101">You can use the **RunSQL** action to run a Access action query by using the corresponding SQL statement. You can also run a data-definition query.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e67f2-p102">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.</span><span class="sxs-lookup"><span data-stu-id="e67f2-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="e67f2-108">Configuración</span><span class="sxs-lookup"><span data-stu-id="e67f2-108">Setting</span></span>

<span data-ttu-id="e67f2-109">La acción **EjecutarSQL** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="e67f2-109">The **RunSQL** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e67f2-110">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="e67f2-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e67f2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e67f2-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e67f2-112"><strong>Instrucción SQL</strong></span><span class="sxs-lookup"><span data-stu-id="e67f2-112"><strong>SQL Statement</strong></span></span></p></td>
<td><p><span data-ttu-id="e67f2-p103">La instrucción SQL para la consulta de acción o consulta de definición de datos que desea ejecutar. Esta instrucción puede tener como máximo 255 caracteres. Este argumento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e67f2-p103">The SQL statement for the action query or data-definition query you want to run. The maximum length of this statement is 255 characters. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e67f2-116"><strong>Usar transacción</strong></span><span class="sxs-lookup"><span data-stu-id="e67f2-116"><strong>Use Transaction</strong></span></span></p></td>
<td><p><span data-ttu-id="e67f2-p104">Seleccione <strong>Sí</strong> para incluir esta consulta en una transacción. Seleccione <strong>No</strong> si no desea usar una transacción. El valor predeterminado es <strong>Sí</strong>. Si selecciona <strong>No</strong> para este argumento, la consulta se podría ejecutar más rápidamente.  </span><span class="sxs-lookup"><span data-stu-id="e67f2-p104">Select <strong>Yes</strong> to include this query in a transaction. Select <strong>No</strong> if you don't want to use a transaction. The default is <strong>Yes</strong>. If you select <strong>No</strong> for this argument, the query might run faster.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e67f2-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e67f2-121">Remarks</span></span>

<span data-ttu-id="e67f2-p105">Las consultas de acción se utilizan para anexar, eliminar y actualizar registros y para guardar el conjunto de resultados de una consulta como una nueva tabla. Las consultas de definición de datos se utilizan para crear, modificar y eliminar tablas, y para crear y eliminar índices. Puede usar la acción **EjecutarSQL** para realizar estas operaciones directamente desde una macro sin tener que usar consultas almacenadas.</span><span class="sxs-lookup"><span data-stu-id="e67f2-p105">You can use action queries to append, delete, and update records and to save a query's result set as a new table. You can use data-definition queries to create, alter, and delete tables, and to create and delete indexes. You can use the **RunSQL** action to perform these operations directly from a macro without having to use stored queries.</span></span>

<span data-ttu-id="e67f2-p106">Si necesita escribir una instrucción SQL que sea mayor de 255 caracteres, use en su lugar el método **RunSQL** del objeto **DoCmd** en un módulo de Visual Basic para Aplicaciones (VBA). En VBA, puede escribir instrucciones SQL de hasta 32.768 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e67f2-p106">If you need to type an SQL statement longer than 255 characters, use the **RunSQL** method of the **DoCmd** object in a Visual Basic for Applications (VBA) module instead. You can type SQL statements of up to 32,768 characters in VBA.</span></span>

<span data-ttu-id="e67f2-p107">Las consultas de Access son en realidad instrucciones SQL que se crean cuando se diseña una consulta con la cuadrícula de diseño en la ventana Consulta. La siguiente tabla muestra las consultas de acción y las consultas de definición de datos de Access y sus correspondientes instrucciones SQL.</span><span class="sxs-lookup"><span data-stu-id="e67f2-p107">Access queries are actually SQL statements that are created when you design a query by using the design grid in the Query window. The following table shows the Access action queries and data-definition queries and their corresponding SQL statements.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e67f2-129">Tipo de consulta</span><span class="sxs-lookup"><span data-stu-id="e67f2-129">Query type</span></span></p></th>
<th><p><span data-ttu-id="e67f2-130">Instrucción SQL</span><span class="sxs-lookup"><span data-stu-id="e67f2-130">SQL statement</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e67f2-131"><strong>Acción</strong></span><span class="sxs-lookup"><span data-stu-id="e67f2-131"><strong>Action</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e67f2-132">Anexar</span><span class="sxs-lookup"><span data-stu-id="e67f2-132">Append</span></span></p></td>
<td><p><span data-ttu-id="e67f2-133">INSERT INTO</span><span class="sxs-lookup"><span data-stu-id="e67f2-133">INSERT INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e67f2-134">Eliminar</span><span class="sxs-lookup"><span data-stu-id="e67f2-134">Delete</span></span></p></td>
<td><p><span data-ttu-id="e67f2-135">DELETE</span><span class="sxs-lookup"><span data-stu-id="e67f2-135">DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e67f2-136">Creación de tabla</span><span class="sxs-lookup"><span data-stu-id="e67f2-136">Make-table</span></span></p></td>
<td><p><span data-ttu-id="e67f2-137">SELECCIONE... EN</span><span class="sxs-lookup"><span data-stu-id="e67f2-137">SELECT...INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e67f2-138">Actualizar</span><span class="sxs-lookup"><span data-stu-id="e67f2-138">Update</span></span></p></td>
<td><p><span data-ttu-id="e67f2-139">UPDATE</span><span class="sxs-lookup"><span data-stu-id="e67f2-139">UPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e67f2-140"><strong>Definición de datos (específico de SQL)</strong></span><span class="sxs-lookup"><span data-stu-id="e67f2-140"><strong>Data-definition (SQL-specific)</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e67f2-141">Crear una tabla</span><span class="sxs-lookup"><span data-stu-id="e67f2-141">Create a table</span></span></p></td>
<td><p><span data-ttu-id="e67f2-142">CREATE TABLE</span><span class="sxs-lookup"><span data-stu-id="e67f2-142">CREATE TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e67f2-143">Modificar una tabla</span><span class="sxs-lookup"><span data-stu-id="e67f2-143">Alter a table</span></span></p></td>
<td><p><span data-ttu-id="e67f2-144">ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="e67f2-144">ALTER TABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e67f2-145">Eliminar una tabla</span><span class="sxs-lookup"><span data-stu-id="e67f2-145">Delete a table</span></span></p></td>
<td><p><span data-ttu-id="e67f2-146">DROP TABLE</span><span class="sxs-lookup"><span data-stu-id="e67f2-146">DROP TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e67f2-147">Crear un índice</span><span class="sxs-lookup"><span data-stu-id="e67f2-147">Create an index</span></span></p></td>
<td><p><span data-ttu-id="e67f2-148">CREATE INDEX</span><span class="sxs-lookup"><span data-stu-id="e67f2-148">CREATE INDEX</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e67f2-149">Eliminar un índice</span><span class="sxs-lookup"><span data-stu-id="e67f2-149">Delete an index</span></span></p></td>
<td><p><span data-ttu-id="e67f2-150">DROP INDEX</span><span class="sxs-lookup"><span data-stu-id="e67f2-150">DROP INDEX</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e67f2-151">También puede usar una cláusula IN con estas instrucciones para modificar datos de otra base de datos.</span><span class="sxs-lookup"><span data-stu-id="e67f2-151">You can also use an IN clause with these statements to modify data in another database.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e67f2-p108">[!NOTA] Para ejecutar una consulta de selección o una consulta de tabla de referencias cruzadas desde una macro, use el argumento Vista de la acción <STRONG>AbrirConsulta</STRONG> para abrir una consulta de selección o una consulta de tabla de referencias cruzadas existente en la vista Hoja de datos. También puede ejecutar consultas de acción y consultas específicas de SQL existentes de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="e67f2-p108">To run a select query or crosstab query from a macro, use the View argument of the <STRONG>OpenQuery</STRONG> action to open an existing select query or crosstab query in Datasheet view. You can also run existing action queries and SQL-specific queries in the same way.</span></span></P>


