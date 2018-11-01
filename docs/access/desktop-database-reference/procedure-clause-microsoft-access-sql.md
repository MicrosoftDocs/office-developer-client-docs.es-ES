---
title: Cláusula PROCEDURE (Microsoft Access SQL)
TOCTitle: PROCEDURE Clause (Microsoft Access SQL)
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
ms.openlocfilehash: 63b38a469c5de60588783381c24c61296b177bdd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877992"
---
# <a name="procedure-clause-microsoft-access-sql"></a>Cláusula PROCEDURE (Microsoft Access SQL)

**Se aplica a**: Access 2013, Office 2013

Define un nombre y parámetros opcionales para una consulta.

> [!NOTE]
> [!NOTA] La cláusula PROCEDURE ha sido sustituida por la instrucción PROCEDURE. Aunque la cláusula PROCEDURE todavía se admite, la instrucción PROCEDURE proporciona un superconjunto de la capacidad de la cláusula PROCEDURE y es la sintaxis recomendada.

## <a name="syntax"></a>Sintaxis

*Nombre* del procedimiento \[ *parámetro1 tipoDeDatos*\[, *parámetro2 tipoDeDatos*\[,...\]\]

La cláusula PROCEDURE consta de los siguientes elementos:

|Elemento |Descripción |
|:----|:-----------|
|*name* |Nombre del procedimiento. Debe seguir las convenciones de nomenclatura estándar.|
|*parámetro1*, *parámetro2* |Uno o varios nombres de campo o parámetros. Por ejemplo:
<br/><br/>`PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>Para obtener más información acerca de los parámetros, vea [parámetros](parameters-declaration-microsoft-access-sql.md).|
|*tipoDeDatos* | Uno de los principales [tipos de datos de Microsoft Access SQL](sql-data-types.md) o sus sinónimos. |


## <a name="remarks"></a>Comentarios

Un procedimiento SQL consta de una cláusula PROCEDURE (que especifica el nombre del procedimiento), una lista opcional de definiciones de parámetros y una única instrucción SQL. Por ejemplo, el procedimiento Get\_parte\_número podría ejecutar una consulta que recupera un número de pieza especificado.

> [!NOTE]
> - Si la cláusula incluye más de una definición de campo (es decir, pares *parámetro-tipoDeDatos* ), sepárelas con comas.
> - La cláusula PROCEDURE debe ir seguida de una instrucción SQL (por ejemplo, una instrucción [SELECT](select-statement-microsoft-access-sql.md) o [UPDATE](update-statement-microsoft-access-sql.md)).

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
