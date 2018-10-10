---
title: CREATE PROCEDURE (instrucción de Microsoft Access SQL)
TOCTitle: CREATE PROCEDURE Statement (Microsoft Access SQL)
ms:assetid: 1fbb5267-9862-bfb4-6436-176152d7a6cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845861(v=office.15)
ms:contentKeyID: 48543649
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: adad7d052e7efbece90f626a50eb50b7bb5b834e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485696"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a><span data-ttu-id="c2aa5-102">CREATE PROCEDURE (instrucción de Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="c2aa5-102">CREATE PROCEDURE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="c2aa5-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2aa5-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="c2aa5-104">Crea un procedimiento almacenado.</span><span class="sxs-lookup"><span data-stu-id="c2aa5-104">Creates a stored procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="c2aa5-105">[!NOTA] El motor de base de datos de Microsoft Access no admite el uso de CREATE PROCEDURE, ni las instrucciones DDL, con bases de datos que no sean del motor de bases de datos Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="c2aa5-105">The Microsoft Access database engine does not support the use of CREATE PROCEDURE, or any of the DDL statements, with non-Microsoft Jet database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2aa5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2aa5-106">Syntax</span></span>

<span data-ttu-id="c2aa5-107">CREATE PROCEDURE *procedimiento* \[ *parámetro1 tipoDeDatos*\[, *parámetro2 tipoDeDatos*\[,... \] \] AS instrucciónsql</span><span class="sxs-lookup"><span data-stu-id="c2aa5-107">CREATE PROCEDURE *procedure* \[*param1 datatype*\[, *param2 datatype*\[, …\]\] AS sqlstatement</span></span>

<span data-ttu-id="c2aa5-108">La instrucción CREATE PROCEDURE consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="c2aa5-108">The CREATE PROCEDURE statement has these parts:</span></span>

|<span data-ttu-id="c2aa5-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="c2aa5-109">Part</span></span>|<span data-ttu-id="c2aa5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2aa5-110">Description</span></span>|
|:---|:----------|
|<span data-ttu-id="c2aa5-111">*procedimiento*</span><span class="sxs-lookup"><span data-stu-id="c2aa5-111">*procedure*</span></span>|<span data-ttu-id="c2aa5-p101">Nombre del procedimiento. Debe seguir las convenciones de nomenclatura estándar.</span><span class="sxs-lookup"><span data-stu-id="c2aa5-p101">A name for the procedure. It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="c2aa5-114">*parámetro1*, *parámetro2*</span><span class="sxs-lookup"><span data-stu-id="c2aa5-114">*param1*, *param2*</span></span>|<span data-ttu-id="c2aa5-p102">Entre uno y 255 nombres de campo o parámetros. Por ejemplo:
</span><span class="sxs-lookup"><span data-stu-id="c2aa5-p102">From one to 255 field names or parameters. For example:</span></span><br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="c2aa5-117">Para obtener más información acerca de los parámetros, vea [parámetros](parameters-declaration-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="c2aa5-117">For more information about parameters, see [PARAMETERS](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="c2aa5-118">*tipoDeDatos*</span><span class="sxs-lookup"><span data-stu-id="c2aa5-118">*datatype*</span></span>|<span data-ttu-id="c2aa5-119">Uno de los principales [tipos de datos de Microsoft Access SQL](sql-data-types.md) o sus sinónimos.</span><span class="sxs-lookup"><span data-stu-id="c2aa5-119">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span>|
|<span data-ttu-id="c2aa5-120">*instrucciónSQL*</span><span class="sxs-lookup"><span data-stu-id="c2aa5-120">*sqlstatement*</span></span>|<span data-ttu-id="c2aa5-121">Instrucción SQL, como SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE, etc.</span><span class="sxs-lookup"><span data-stu-id="c2aa5-121">An SQL statement such as SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE, and so on.</span></span>|


## <a name="remarks"></a><span data-ttu-id="c2aa5-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2aa5-122">Remarks</span></span>

<span data-ttu-id="c2aa5-123">Un procedimiento SQL consta de una cláusula PROCEDURE que especifica el nombre del procedimiento, una lista opcional de definiciones de parámetros y una única instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="c2aa5-123">An SQL procedure consists of a PROCEDURE clause that specifies the name of the procedure, an optional list of parameter definitions, and a single SQL statement.</span></span>

<span data-ttu-id="c2aa5-124">Un nombre de procedimiento no puede ser igual que el nombre de una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="c2aa5-124">A procedure name cannot be the same as the name of an existing table.</span></span>

## <a name="example"></a><span data-ttu-id="c2aa5-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2aa5-125">Example</span></span>

<span data-ttu-id="c2aa5-126">En este ejemplo se nombra la consulta CategoryList y llama al procedimiento EnumFields, que puede encontrar en el ejemplo de la instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="c2aa5-126">This example names the query CategoryList, and calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
