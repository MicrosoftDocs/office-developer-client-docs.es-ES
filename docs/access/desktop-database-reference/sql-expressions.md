---
title: Expresiones SQL (referencia de escritorio de la base de datos de Access)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a8d340f008fd198068d6dacc1b2bf847838ede1
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025738"
---
# <a name="sql-expressions"></a><span data-ttu-id="490b1-102">Expresiones SQL</span><span class="sxs-lookup"><span data-stu-id="490b1-102">SQL expressions</span></span>

<span data-ttu-id="490b1-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="490b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="490b1-p101">Una expresión SQL es una cadena que forma total o parcialmente una instrucción SQL. Por ejemplo, el método **FindFirst** de un objeto **Recordset** usa una expresión SQL que consta de los criterios de selección incluidos en una [cláusula WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) de SQL.</span><span class="sxs-lookup"><span data-stu-id="490b1-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the **FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span></span>

<span data-ttu-id="490b1-106">El motor de base de datos de Microsoft Access utiliza el servicio de expresiones de Microsoft Visual Basic para aplicaciones (o VBA) para realizar sencillas evaluaciones de aritmética y función.</span><span class="sxs-lookup"><span data-stu-id="490b1-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="490b1-107">El servicio de expresión VBA define todos los operadores utilizados en las expresiones de SQL del motor de base de datos de Microsoft Access (excepto **[entre](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** y **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**).</span><span class="sxs-lookup"><span data-stu-id="490b1-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)**, and **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) are defined by the VBA expression service.</span></span> <span data-ttu-id="490b1-108">Además, el servicio de expresiones VBA ofrece más de 100 funciones VBA que se pueden usar en expresiones SQL.</span><span class="sxs-lookup"><span data-stu-id="490b1-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="490b1-109">Por ejemplo, puede usar estas funciones VBA para componer una consulta SQL en la vista de diseño de la consulta de Microsoft Access, y también puede usar estas funciones en una consulta SQL en el método **OpenRecordset** DAO en Microsoft Visual C++, Microsoft Visual Basic y Microsoft Código de Excel.</span><span class="sxs-lookup"><span data-stu-id="490b1-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

## <a name="see-also"></a><span data-ttu-id="490b1-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="490b1-110">See also</span></span>

- [<span data-ttu-id="490b1-111">Conceptos VBA de Access</span><span class="sxs-lookup"><span data-stu-id="490b1-111">Access VBA Concepts</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)