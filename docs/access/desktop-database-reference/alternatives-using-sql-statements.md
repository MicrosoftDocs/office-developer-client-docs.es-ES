---
title: 'Alternativas: Utilizar instrucciones SQL'
TOCTitle: 'Alternatives: Using SQL Statements'
ms:assetid: 9ed787da-7099-2ef5-b2c6-c4f6bce5ddfe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249727(v=office.15)
ms:contentKeyID: 48546668
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 853dfaab43d6d4c831b7ec9288bc8e9477fe2683
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888100"
---
# <a name="alternatives-using-sql-statements"></a><span data-ttu-id="da1d1-102">Alternativas: Uso de instrucciones SQL</span><span class="sxs-lookup"><span data-stu-id="da1d1-102">Alternatives: Using SQL Statements</span></span>


<span data-ttu-id="da1d1-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="da1d1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="da1d1-p101">ADO también permite utilizar comandos como alternativa a sus propiedades y métodos integrados para modificar datos. Dependiendo de su proveedor, todas las operaciones mencionadas en este capítulo también se podrían realizar pasando comandos a su origen de datos. Por ejemplo, se pueden utilizar instrucciones SQL UPDATE para modificar datos sin usar la propiedad **Valor** de un **campo**. Se pueden utilizar instrucciones INSERT para agregar nuevos registros a un origen de datos, en lugar del método **AddNew** de ADO. Para obtener más información acerca de SQL o el lenguaje de manipulación de datos de su proveedor, vea la documentación de su origen de datos.</span><span class="sxs-lookup"><span data-stu-id="da1d1-p101">ADO also allows using commands as alternatives to its built-in properties and methods for editing data. Depending upon your provider, all operations mentioned in this chapter could also be accomplished by passing commands to your data source. For example, SQL UPDATE statements can be used to modify data without using the **Value** property of a **Field**. SQL INSERT statements can be used to add new records to a data source, rather than the ADO method **AddNew**. For more information about SQL or the data-manipulation language of your provider, see the documentation of your data source.</span></span>

<span data-ttu-id="da1d1-109">Por ejemplo, puede pasar una cadena SQL que contiene una instrucción DELETE a una base de datos, como se muestra en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="da1d1-109">For example, you can pass a SQL string containing a DELETE statement to a database, as shown in the following code:</span></span>

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

