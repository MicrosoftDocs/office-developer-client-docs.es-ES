---
title: Comparación de Microsoft Access SQL y ANSI SQL
TOCTitle: Comparison of Microsoft Access SQL and ANSI SQL
ms:assetid: 0686f98f-10fe-0e02-e9d1-84ff3e755b57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844937(v=office.15)
ms:contentKeyID: 48543052
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 195d9f5d882fd252b1b10e937fe851c4830c52d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296055"
---
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a><span data-ttu-id="a1596-102">Comparación de Microsoft Access SQL y ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="a1596-102">Comparison of Microsoft Access SQL and ANSI SQL</span></span>

<span data-ttu-id="a1596-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1596-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1596-104">En términos generales, SQL en el motor de base de datos de Microsoft Access es compatible con ANSI-89 nivel 1.</span><span class="sxs-lookup"><span data-stu-id="a1596-104">Microsoft Access database engine SQL is generally ANSI-89 Level 1 compliant.</span></span> <span data-ttu-id="a1596-105">Sin embargo, algunas características de ANSI SQL no se implementan en Microsoft Access SQL.</span><span class="sxs-lookup"><span data-stu-id="a1596-105">However, certain ANSI SQL features are not implemented in Microsoft Access SQL.</span></span> <span data-ttu-id="a1596-106">Por su parte, Microsoft Access SQL incluye palabras reservadas y características no admitidas en ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="a1596-106">Conversely, Microsoft Access SQL includes reserved words and features not supported in ANSI SQL.</span></span>

## <a name="major-differences"></a><span data-ttu-id="a1596-107">Diferencias principales</span><span class="sxs-lookup"><span data-stu-id="a1596-107">Major differences</span></span>

- <span data-ttu-id="a1596-p102">Microsoft Access SQL y ANSI SQL tienen palabras reservadas y tipos de datos diferentes. Para obtener más información, vea [Palabras reservadas SQL del motor de base de datos de Microsoft Access](sql-reserved-words.md) y [Tipos de datos equivalentes de ANSI SQL](equivalent-ansi-sql-data-types.md). Si se usa el proveedor OLE DB del motor de base de datos de Microsoft Access, hay palabras reservadas adicionales.</span><span class="sxs-lookup"><span data-stu-id="a1596-p102">Microsoft Access SQL and ANSI SQL each have different reserved words and data types. For more information, see [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md) and [Equivalent ANSI SQL Data Types](equivalent-ansi-sql-data-types.md). Using the Microsoft Access Database Engine OLE DB Provider there are additional reserved words.</span></span>

- <span data-ttu-id="a1596-111">**[Between…And](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**</span><span class="sxs-lookup"><span data-stu-id="a1596-111">**[Between…And](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**</span></span>
    
  <span data-ttu-id="a1596-112">*expr1* \[No\] **entre** *valor1* **y** *valor2*</span><span class="sxs-lookup"><span data-stu-id="a1596-112">*expr1* \[NOT\] **Between** *value1* **And** *value2*</span></span>
    
  <span data-ttu-id="a1596-113">En Microsoft Access SQL, *valor1* puede ser mayor que *valor2*; en ANSI SQL, *valor1* debe ser igual o menor que *valor2.*</span><span class="sxs-lookup"><span data-stu-id="a1596-113">In Microsoft Access SQL, *value1* can be greater than *value2*; in ANSI SQL, *value1* must be equal to or less than *value2.*</span></span>

- <span data-ttu-id="a1596-p103">Microsoft Access SQL admite los caracteres comodín de ANSI SQL y los [caracteres comodín](using-wildcard-characters-in-string-comparisons.md) que son específicos del motor de base de datos de Microsoft Access para su uso con el operador **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**. El uso de los caracteres comodín de ANSI y el motor de base de datos de Microsoft Access es mutuamente excluyente. Debe usar uno de los dos conjuntos y no se pueden mezclar. Los caracteres comodín de ANSI SQL sólo están disponibles cuando se usa el motor de base de datos de Microsoft Access y el proveedor OLE DB del motor de base de datos de Microsoft Access. Si intenta usar los caracteres comodín de ANSI SQL con Microsoft Access o DAO, se interpretarán como caracteres literales. Y también sucede lo contrario cuando se utiliza el proveedor OLE DB del motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a1596-p103">Microsoft Access SQL supports both ANSI SQL wildcard characters and [wildcard characters](using-wildcard-characters-in-string-comparisons.md) that are specific to the Microsoft Access database engine to use with the **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** operator. The use of the ANSI and Microsoft Access database engine wildcard characters is mutually exclusive. You must use one set or the other and cannot mix them. The ANSI SQL wildcards are only available when using the Microsoft Access database engine and the Microsoft Access Database Engine OLE DB Provider. If you try to use the ANSI SQL wildcards through Microsoft Access or DAO, then they will be interpreted as literals. The opposite is true when using the Microsoft Access Database Engine OLE DB Provider.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="a1596-120">Carácter correspondiente</span><span class="sxs-lookup"><span data-stu-id="a1596-120">Matching character</span></span></p></th>
    <th><p><span data-ttu-id="a1596-121">Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="a1596-121">Microsoft Access SQL</span></span></p></th>
    <th><p><span data-ttu-id="a1596-122">ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="a1596-122">ANSI SQL</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="a1596-123">Cualquier carácter</span><span class="sxs-lookup"><span data-stu-id="a1596-123">Any single character</span></span></p></td>
    <td><p><span data-ttu-id="a1596-124">?</span><span class="sxs-lookup"><span data-stu-id="a1596-124"></span></span></p></td>
    <td><p><span data-ttu-id="a1596-125">_ (subrayado)</span><span class="sxs-lookup"><span data-stu-id="a1596-125">_ (underscore)</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="a1596-126">Cero o más caracteres</span><span class="sxs-lookup"><span data-stu-id="a1596-126">Zero or more characters</span></span></p></td>
    <td><p>*</p></td>
    <td><p>%</p></td>
    </tr>
    </tbody>
    </table>


- <span data-ttu-id="a1596-p104">En general, Microsoft Access SQL es menos restrictivo. Por ejemplo, permite agrupar y ordenar por expresiones.</span><span class="sxs-lookup"><span data-stu-id="a1596-p104">Microsoft Access SQL is generally less restrictive. For example, it permits grouping and ordering on expressions.</span></span>

- <span data-ttu-id="a1596-129">Microsoft Access SQL admite expresiones más eficaces.</span><span class="sxs-lookup"><span data-stu-id="a1596-129">Microsoft Access SQL supports more powerful expressions.</span></span>

## <a name="enhanced-features-of-microsoft-access-sql"></a><span data-ttu-id="a1596-130">Características mejoradas de Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="a1596-130">Enhanced features of Microsoft Access SQL</span></span>

<span data-ttu-id="a1596-131">Microsoft Access SQL ofrece las siguientes características mejoradas:</span><span class="sxs-lookup"><span data-stu-id="a1596-131">Microsoft Access SQL provides the following enhanced features:</span></span>

- <span data-ttu-id="a1596-132">Instrucción [TRANSFORM](transform-statement-microsoft-access-sql.md), que proporciona compatibilidad con las consultas de tabla de referencias cruzadas.</span><span class="sxs-lookup"><span data-stu-id="a1596-132">The [TRANSFORM](transform-statement-microsoft-access-sql.md) statement, which provides support for crosstab queries.</span></span>

- <span data-ttu-id="a1596-133">[Funciones de agregado](sql-aggregate-functions-sql.md) adicionales, como **StDev** y **VarP**.</span><span class="sxs-lookup"><span data-stu-id="a1596-133">Additional [aggregate functions](sql-aggregate-functions-sql.md), such as **StDev** and **VarP**.</span></span>

- <span data-ttu-id="a1596-134">Declaración [PARAMETERS](parameters-declaration-microsoft-access-sql.md) para definir consultas de parámetros.</span><span class="sxs-lookup"><span data-stu-id="a1596-134">The [PARAMETERS](parameters-declaration-microsoft-access-sql.md) declaration for defining parameter queries.</span></span>

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a><span data-ttu-id="a1596-135">Características de ANSI SQL no admitidas en Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="a1596-135">ANSI SQL features not supported in Microsoft Access SQL</span></span>

<span data-ttu-id="a1596-136">Microsoft Access SQL no admite las siguientes características de ANSI SQL:</span><span class="sxs-lookup"><span data-stu-id="a1596-136">Microsoft Access SQL does not support the following ANSI SQL features:</span></span>

- <span data-ttu-id="a1596-p105">Referencias de la función de agregado DISTINCT. Por ejemplo, Microsoft Access SQL no permite SUM(DISTINCT *nombreDeColumna*).</span><span class="sxs-lookup"><span data-stu-id="a1596-p105">DISTINCT aggregate function references. For example, Microsoft Access SQL does not allow SUM(DISTINCT *columnname*).</span></span>

- <span data-ttu-id="a1596-p106">Cláusula LIMIT TO *nn* ROWS usada para limitar el número de filas devueltas por una consulta. Sólo se puede usar la [cláusula WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) para limitar el ámbito de una consulta.</span><span class="sxs-lookup"><span data-stu-id="a1596-p106">The LIMIT TO *nn* ROWS clause used to limit the number of rows returned by a query. You can use only the [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) to limit the scope of a query.</span></span>

