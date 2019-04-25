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
# <a name="create-procedure-statement-microsoft-access-sql"></a>Instrucción CREATE PROCEDURE (Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013 

Crea un procedimiento almacenado.

> [!NOTE]
> El motor de base de datos de Microsoft Access no admite el uso de CREATE PROCEDURE, ni las instrucciones DDL, con bases de datos que no sean del motor de bases de datos Microsoft Jet.

## <a name="syntax"></a>Sintaxis

CREATE PROCEDURE *procedimiento* \[*párametro1 tipo_datos*\[, *párametro2 tipo_datos*\[, …\]\] AS sqlstatement

La instrucción CREATE PROCEDURE consta de las siguientes partes:

|Part|Descripción|
|:---|:----------|
|*procedimiento*|Un nombre para el procedimiento. Debe seguir las convenciones de nomenclatura estándar.|
|*párametro1*, *párametro2*|De uno a 255 nombres de campo o parámetros. Por ejemplo:<br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>Para obtener más información acerca de los parámetros, vea [parámetros](parameters-declaration-microsoft-access-sql.md).|
|*tipo_datos*|Uno de los principales [tipos de datos de Microsoft Access SQL](sql-data-types.md) o sus sinónimos.|
|*sqlstatement*|Una instrucción SQL como SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE y así sucesivamente.|


## <a name="remarks"></a>Comentarios

Un procedimiento SQL consiste en una cláusula PROCEDURE que especifica el nombre del procedimiento, una lista opcional de definiciones de parámetros y una única instrucción SQL.

El nombre de un procedimiento no puede ser el mismo que el nombre de una tabla existente.

## <a name="example"></a>Ejemplo

En este ejemplo se nombra la consulta CategoryList y llama al procedimiento EnumFields, que puede encontrar en el ejemplo de instrucción SELECT.

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
