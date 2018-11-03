---
title: Expresiones SQL (referencia de escritorio de la base de datos de Access)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25b7d11430b730b6cedd1d8a084acd4984c5f292
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944154"
---
# <a name="sql-expressions"></a><span data-ttu-id="bd86b-102">Expresiones SQL</span><span class="sxs-lookup"><span data-stu-id="bd86b-102">SQL expressions</span></span>


<span data-ttu-id="bd86b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd86b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bd86b-p101">Una expresión SQL es una cadena que forma total o parcialmente una instrucción SQL. Por ejemplo, el método **FindFirst** de un objeto **Recordset** usa una expresión SQL que consta de los criterios de selección incluidos en una [cláusula WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) de SQL.</span><span class="sxs-lookup"><span data-stu-id="bd86b-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the**FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://msdn.microsoft.com/library/ff195245\(v=office.15\)).</span></span>

<span data-ttu-id="bd86b-106">El motor de base de datos de Microsoft Access utiliza el servicio de expresiones de Microsoft Visual Basic para aplicaciones (o VBA) para realizar sencillas evaluaciones de aritmética y función.</span><span class="sxs-lookup"><span data-stu-id="bd86b-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="bd86b-107">El servicio de expresión VBA define todos los operadores utilizados en las expresiones de SQL del motor de base de datos de Microsoft Access (excepto **[entre](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, **[In](https://msdn.microsoft.com/library/ff836369\(v=office.15\))** y **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**).</span><span class="sxs-lookup"><span data-stu-id="bd86b-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, **[In](https://msdn.microsoft.com/library/ff836369\(v=office.15\))**, and **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**) are defined by the VBA expression service.</span></span> <span data-ttu-id="bd86b-108">Además, el servicio de expresiones VBA ofrece más de 100 funciones VBA que se pueden usar en expresiones SQL.</span><span class="sxs-lookup"><span data-stu-id="bd86b-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="bd86b-109">Por ejemplo, puede usar estas funciones VBA para componer una consulta SQL en la vista de diseño de la consulta de Microsoft Access, y también puede usar estas funciones en una consulta SQL en el método **OpenRecordset** DAO en Microsoft Visual C++, Microsoft Visual Basic y Microsoft Código de Excel.</span><span class="sxs-lookup"><span data-stu-id="bd86b-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

