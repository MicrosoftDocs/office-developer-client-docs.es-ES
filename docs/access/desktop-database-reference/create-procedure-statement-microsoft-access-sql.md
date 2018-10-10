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
# <a name="create-procedure-statement-microsoft-access-sql"></a>CREATE PROCEDURE (instrucción de Microsoft Access SQL)

**Se aplica a**: Access 2013 | Office 2013 

Crea un procedimiento almacenado.

> [!NOTE]
> [!NOTA] El motor de base de datos de Microsoft Access no admite el uso de CREATE PROCEDURE, ni las instrucciones DDL, con bases de datos que no sean del motor de bases de datos Microsoft Jet.

## <a name="syntax"></a>Sintaxis

CREATE PROCEDURE *procedimiento* \[ *parámetro1 tipoDeDatos*\[, *parámetro2 tipoDeDatos*\[,... \] \] AS instrucciónsql

La instrucción CREATE PROCEDURE consta de los siguientes elementos:

|Elemento|Descripción|
|:---|:----------|
|*procedimiento*|Nombre del procedimiento. Debe seguir las convenciones de nomenclatura estándar.|
|*parámetro1*, *parámetro2*|Entre uno y 255 nombres de campo o parámetros. Por ejemplo:
<br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>Para obtener más información acerca de los parámetros, vea [parámetros](parameters-declaration-microsoft-access-sql.md).|
|*tipoDeDatos*|Uno de los principales [tipos de datos de Microsoft Access SQL](sql-data-types.md) o sus sinónimos.|
|*instrucciónSQL*|Instrucción SQL, como SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE, etc.|


## <a name="remarks"></a>Comentarios

Un procedimiento SQL consta de una cláusula PROCEDURE que especifica el nombre del procedimiento, una lista opcional de definiciones de parámetros y una única instrucción SQL.

Un nombre de procedimiento no puede ser igual que el nombre de una tabla existente.

## <a name="example"></a>Ejemplo

En este ejemplo se nombra la consulta CategoryList y llama al procedimiento EnumFields, que puede encontrar en el ejemplo de la instrucción SELECT.

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
