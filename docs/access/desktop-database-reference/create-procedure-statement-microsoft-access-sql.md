---
title: Instrucción CREATE PROCEDURE (Microsoft Access SQL)
TOCTitle: CREATE PROCEDURE statement (Microsoft Access SQL)
ms:assetid: 1fbb5267-9862-bfb4-6436-176152d7a6cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845861(v=office.15)
ms:contentKeyID: 48543649
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: f223e164bd36a6a1a76140a28dd57cd2005e4a20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295410"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a><span data-ttu-id="6b26a-102">Instrucción CREATE PROCEDURE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="6b26a-102">CREATE PROCEDURE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="6b26a-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b26a-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="6b26a-104">Crea un procedimiento almacenado.</span><span class="sxs-lookup"><span data-stu-id="6b26a-104">Creates a stored procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="6b26a-105">El motor de base de datos de Microsoft Access no admite el uso de CREATE PROCEDURE, ni las instrucciones DDL, con bases de datos que no sean del motor de bases de datos Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="6b26a-105">The Microsoft Access database engine does not support the use of CREATE PROCEDURE, or any of the DDL statements, with non-Microsoft Jet database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b26a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b26a-106">Syntax</span></span>

<span data-ttu-id="6b26a-107">CREATE PROCEDURE *procedimiento* \[*párametro1 tipo_datos*\[, *párametro2 tipo_datos*\[, …\]\] AS sqlstatement</span><span class="sxs-lookup"><span data-stu-id="6b26a-107">CREATE PROCEDURE procedure
    [param1 datatype[, param2 datatype[, …]] AS sqlstatement</span></span>

<span data-ttu-id="6b26a-108">La instrucción CREATE PROCEDURE consta de las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="6b26a-108">The CREATE PROCEDURE statement has these parts:</span></span>

|<span data-ttu-id="6b26a-109">Part</span><span class="sxs-lookup"><span data-stu-id="6b26a-109">Part</span></span>|<span data-ttu-id="6b26a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b26a-110">Description</span></span>|
|:---|:----------|
|<span data-ttu-id="6b26a-111">*procedimiento*</span><span class="sxs-lookup"><span data-stu-id="6b26a-111">*procedure*</span></span>|<span data-ttu-id="6b26a-112">Un nombre para el procedimiento.</span><span class="sxs-lookup"><span data-stu-id="6b26a-112">A name for the procedure.</span></span> <span data-ttu-id="6b26a-113">Debe seguir las convenciones de nomenclatura estándar.</span><span class="sxs-lookup"><span data-stu-id="6b26a-113">It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="6b26a-114">*párametro1*, *párametro2*</span><span class="sxs-lookup"><span data-stu-id="6b26a-114">*param1*, *param2*</span></span>|<span data-ttu-id="6b26a-115">De uno a 255 nombres de campo o parámetros.</span><span class="sxs-lookup"><span data-stu-id="6b26a-115">From one to 255 field names or parameters.</span></span> <span data-ttu-id="6b26a-116">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6b26a-116">For example:</span></span><br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="6b26a-117">Para obtener más información acerca de los parámetros, vea [parámetros](parameters-declaration-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="6b26a-117">For more information on parameters, see [PARAMETERS](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="6b26a-118">*tipo_datos*</span><span class="sxs-lookup"><span data-stu-id="6b26a-118">*datatype*</span></span>|<span data-ttu-id="6b26a-119">Uno de los principales [tipos de datos de Microsoft Access SQL](sql-data-types.md) o sus sinónimos.</span><span class="sxs-lookup"><span data-stu-id="6b26a-119">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span>|
|<span data-ttu-id="6b26a-120">*sqlstatement*</span><span class="sxs-lookup"><span data-stu-id="6b26a-120">*SQLStatement*</span></span>|<span data-ttu-id="6b26a-121">Una instrucción SQL como SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="6b26a-121">An SQL statement such as SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE, and so on.</span></span>|


## <a name="remarks"></a><span data-ttu-id="6b26a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b26a-122">Remarks</span></span>

<span data-ttu-id="6b26a-123">Un procedimiento SQL consiste en una cláusula PROCEDURE que especifica el nombre del procedimiento, una lista opcional de definiciones de parámetros y una única instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="6b26a-123">An SQL procedure consists of a PROCEDURE clause that specifies the name of the procedure, an optional list of parameter definitions, and a single SQL statement.</span></span>

<span data-ttu-id="6b26a-124">El nombre de un procedimiento no puede ser el mismo que el nombre de una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="6b26a-124">A procedure name cannot be the same as the name of an existing table.</span></span>

## <a name="example"></a><span data-ttu-id="6b26a-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6b26a-125">Example</span></span>

<span data-ttu-id="6b26a-126">En este ejemplo se nombra la consulta CategoryList y llama al procedimiento EnumFields, que puede encontrar en el ejemplo de instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="6b26a-126">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
