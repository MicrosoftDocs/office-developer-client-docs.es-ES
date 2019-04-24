---
title: PROCEDURE (cláusula de Microsoft Access SQL)
TOCTitle: PROCEDURE clause (Microsoft Access SQL)
ms:assetid: a718802c-9260-88d5-ec29-d5e5594927b0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821342(v=office.15)
ms:contentKeyID: 48546872
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277578
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 72f31c71e710cca79695a7221f0e033d18d2f420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301382"
---
# <a name="procedure-clause-microsoft-access-sql"></a><span data-ttu-id="37695-102">PROCEDURE (cláusula de Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="37695-102">PROCEDURE clause (Microsoft Access SQL)</span></span>

<span data-ttu-id="37695-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="37695-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37695-104">Define un nombre y parámetros opcionales para una consulta.</span><span class="sxs-lookup"><span data-stu-id="37695-104">Defines a name and optional parameters for a query.</span></span>

> [!NOTE]
> <span data-ttu-id="37695-p101">[!NOTA] La cláusula PROCEDURE ha sido sustituida por la instrucción PROCEDURE. Aunque la cláusula PROCEDURE todavía se admite, la instrucción PROCEDURE proporciona un superconjunto de la capacidad de la cláusula PROCEDURE y es la sintaxis recomendada.</span><span class="sxs-lookup"><span data-stu-id="37695-p101">The PROCEDURE clause has been superseded by the PROCEDURE statement. Although the PROCEDURE clause is still supported, the PROCEDURE statement provides a superset of the capability of the PROCEDURE clause and is the recommended syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="37695-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37695-107">Syntax</span></span>

<span data-ttu-id="37695-108">PROCEDURE *nombre* \[ *parámetro1 tipodedatos*\[, *parám2 tipodedatos*\[,...\]\]</span><span class="sxs-lookup"><span data-stu-id="37695-108">PROCEDURE *name* \[*param1 datatype*\[, *param2 datatype*\[, …\]\]</span></span>

<span data-ttu-id="37695-109">La cláusula PROCEDURE consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="37695-109">The PROCEDURE clause has these parts:</span></span>

|<span data-ttu-id="37695-110">Parte</span><span class="sxs-lookup"><span data-stu-id="37695-110">Part</span></span> |<span data-ttu-id="37695-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="37695-111">Description</span></span> |
|:----|:-----------|
|<span data-ttu-id="37695-112">*name*</span><span class="sxs-lookup"><span data-stu-id="37695-112">*name*</span></span> |<span data-ttu-id="37695-113">Nombre del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="37695-113">A name for the procedure.</span></span> <span data-ttu-id="37695-114">Debe seguir las convenciones de nomenclatura estándar.</span><span class="sxs-lookup"><span data-stu-id="37695-114">It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="37695-115">*param1*, *parám2*</span><span class="sxs-lookup"><span data-stu-id="37695-115">*param1*, *param2*</span></span> |<span data-ttu-id="37695-116">Uno o varios nombres de campo o parámetros.</span><span class="sxs-lookup"><span data-stu-id="37695-116">One or more field names or parameters.</span></span> <span data-ttu-id="37695-117">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="37695-117">For example:</span></span><br/><br/>`PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="37695-118">Para obtener más información acerca de los [](parameters-declaration-microsoft-access-sql.md)parámetros, consulte Parameters.</span><span class="sxs-lookup"><span data-stu-id="37695-118">For more information about parameters, see [parameters](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="37695-119">*tipoDeDatos*</span><span class="sxs-lookup"><span data-stu-id="37695-119">*datatype*</span></span> | <span data-ttu-id="37695-120">Uno de los principales [tipos de datos de Microsoft Access SQL](sql-data-types.md) o sus sinónimos.</span><span class="sxs-lookup"><span data-stu-id="37695-120">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span> |


## <a name="remarks"></a><span data-ttu-id="37695-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37695-121">Remarks</span></span>

<span data-ttu-id="37695-122">Un procedimiento SQL consta de una cláusula PROCEDURE (que especifica el nombre del procedimiento), una lista opcional de definiciones de parámetros y una única instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="37695-122">An SQL procedure consists of a PROCEDURE clause (which specifies the name of the procedure), an optional list of parameter definitions, and a single SQL statement.</span></span> <span data-ttu-id="37695-123">Por ejemplo, el procedimiento obtener\_número\_de pieza podría ejecutar una consulta que recupera un número de pieza especificado.</span><span class="sxs-lookup"><span data-stu-id="37695-123">For example, the procedure Get\_Part\_Number might run a query that retrieves a specified part number.</span></span>

> [!NOTE]
> - <span data-ttu-id="37695-124">Si la cláusula incluye varias definiciones de campo (pares *parámetro-tipoDeDatos*), sepárelas mediante comas.</span><span class="sxs-lookup"><span data-stu-id="37695-124">If the clause includes more than one field definition (that is, *param-datatype* pairs), separate them with commas.</span></span>
> - <span data-ttu-id="37695-125">La cláusula PROCEDURE debe ir seguida de una instrucción SQL (por ejemplo, una instrucción [SELECT](select-statement-microsoft-access-sql.md) o [UPDATE](update-statement-microsoft-access-sql.md)).</span><span class="sxs-lookup"><span data-stu-id="37695-125">The PROCEDURE clause must be followed by an SQL statement (for example, a [SELECT](select-statement-microsoft-access-sql.md) or [UPDATE](update-statement-microsoft-access-sql.md) statement).</span></span>

## <a name="example"></a><span data-ttu-id="37695-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="37695-126">Example</span></span>

<span data-ttu-id="37695-127">En este ejemplo se asigna un nombre a la consulta CategoryList y se llama al procedimiento EnumFields, que encontrará en el ejemplo de la instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="37695-127">This example names the query CategoryList, and calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub ProcedureX() 
     
        Dim dbs As Database, rst As Recordset 
        Dim qdf As QueryDef, strSql As String 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        strSql = "PROCEDURE CategoryList; " _ 
            & "SELECT DISTINCTROW CategoryName, " _ 
            & "CategoryID FROM Categories " _ 
            & "ORDER BY CategoryName;" 
         
        ' Create a named QueryDef based on the SQL 
        ' statement. 
        Set qdf = dbs.CreateQueryDef("NewQry", strSql) 
     
        ' Create a temporary snapshot-type Recordset. 
        Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
        ' Populate the Recordset. 
        rst.MoveLast 
                 
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
