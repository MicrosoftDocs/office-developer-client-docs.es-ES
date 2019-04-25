---
title: Método Database.CreateQueryDef (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 75ee7cac-dcd0-b4c5-b55b-9cbaaae2cbf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195966(v=office.15)
ms:contentKeyID: 48545686
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c19ef8ab8ef2e937ba7467b3695f9aa5780c21c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294984"
---
# <a name="databasecreatequerydef-method-dao"></a>Método Database.CreateQueryDef (DAO)

**Se aplica a:** Access 2013, Office 2013

Crea un nuevo objeto **[QueryDef](querydef-object-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expression* .CreateQueryDef(***Name***, ***SQLText***)

*expression* Variable que representa un objeto **Database**.

## <a name="parameters"></a>Parameters

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (subtipo <strong>String</strong>) que designa inequívocamente el nuevo objeto <strong>QueryDef</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>SQLText</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (subtipo <strong>String</strong>) que es una instrucción SQL que define el objeto <strong>QueryDef</strong>. Si omite este argumento, puede definir el objeto <strong>QueryDef</strong> estableciendo su propiedad <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> antes o después de agregarlo a una colección.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor devuelto

QueryDef

## <a name="remarks"></a>Comentarios

En un área de trabajo de Microsoft Access, si proporciona cualquier otro elemento que no sea una cadena de longitud cero para el nombre al crear un objeto **QueryDef**, el objeto **QueryDef** resultante se agrega automáticamente a la colección **[QueryDefs](querydefs-collection-dao.md)**.

Si el objeto especificado por el nombre ya es un miembro de la colección **QueryDefs**, se produce un error en tiempo de ejecución. Puede crear un archivo **QueryDef** temporal utilizando una cadena de longitud cero para el argumento de nombre cuando ejecuta el método **CreateQueryDef**. También puede realizar esto estableciendo la propiedad **[nombre](querydef-name-property-dao.md)** de un **QueryDef** recién creado en una cadena de longitud cero (""). 

Los objetos **QueryDef** temporales son útiles si quiere utilizar instrucciones SQL repetidamente sin tener que crear nuevos objetos permanentes en la colección **QueryDefs**. No puede anexar un **QueryDef** temporal a cualquier colección ya que una cadena de longitud cero no es un nombre válido para un objeto **QueryDef** permanente. Siempre puede establecer las propiedades **Name** y **SQL** del objeto **QueryDef** recién creado y posteriormente anexar **QueryDef** a la colección **QueryDefs**.

Para ejecutar una instrucción SQL en un objeto **QueryDef**, use el método **[Execute](querydef-execute-method-dao.md)** u **[OpenRecordset](database-openrecordset-method-dao.md)**.

El uso de un objeto **QueryDef** es el método recomendado para realizar consultas de paso a través SQL con bases de datos ODBC.

Para quitar un objeto **QueryDef** de una colección **QueryDefs** de una base de datos del motor de base de datos de Microsoft Access, use el método **[Delete](querydefs-delete-method-dao.md)** en la colección.

## <a name="example"></a>Ejemplo

En este ejemplo se usa el método **CreateQueryDef** para crear y ejecutar un **QueryDef** temporal y otro permanente. La función GetrstTemp es necesaria para que se ejecute este procedimiento.

```vb
    Sub CreateQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim qdfNew As QueryDef 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
          ' Create temporary QueryDef. 
          Set qdfTemp = .CreateQueryDef("", _ 
             "SELECT * FROM Employees") 
          ' Open Recordset and print report. 
          GetrstTemp qdfTemp 
          ' Create permanent QueryDef. 
          Set qdfNew = .CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
          ' Open Recordset and print report. 
          GetrstTemp qdfNew 
          ' Delete new QueryDef because this is a demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
     
    Function GetrstTemp(qdfTemp As QueryDef) 
     
       Dim rstTemp As Recordset 
     
       With qdfTemp 
          Debug.Print .Name 
          Debug.Print "  " & .SQL 
          ' Open Recordset from QueryDef. 
          Set rstTemp = .OpenRecordset(dbOpenSnapshot) 
     
          With rstTemp 
             ' Populate Recordset and print number of records. 
             .MoveLast 
             Debug.Print "  Number of records = " & _ 
                .RecordCount 
             Debug.Print 
             .Close 
          End With 
     
       End With 
     
    End Function 
```

<br/>

En este ejemplo se usan los métodos **CreateQueryDef** y **OpenRecordset** y la propiedad **SQL** para realizar una consulta en la tabla de títulos de la base de datos de ejemplo Pubs de Microsoft SQL Server, y devolver el título y el identificador de título del libro más vendido. A continuación, se realiza una consulta en la tabla de autores y se indica al usuario que envíe una prima a cada autor en función de su porcentaje de derechos de autor (la prima total es de 1.000 dólares y cada autor debe recibir un porcentaje de ese importe).

```vb 
Sub ClientServerX2() 
 
   Dim dbsCurrent As Database 
   Dim qdfBestSellers As QueryDef 
   Dim qdfBonusEarners As QueryDef 
   Dim rstTopSeller As Recordset 
   Dim rstBonusRecipients As Recordset 
   Dim strAuthorList As String 
 
   ' Open a database from which QueryDef objects can be  
   ' created. 
   Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
   ' Create a temporary QueryDef object to retrieve 
   ' data from a Microsoft SQL Server database. 
   Set qdfBestSellers = dbsCurrent.CreateQueryDef("") 
   With qdfBestSellers 
      ' Note: The DSN referenced below must be configured to  
      '       use Microsoft Windows NT Authentication Mode to  
      '       authorize user access to the Microsoft SQL Server. 
      .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
      .SQL = "SELECT title, title_id FROM titles " & _ 
         "ORDER BY ytd_sales DESC" 
      Set rstTopSeller = .OpenRecordset() 
      rstTopSeller.MoveFirst 
   End With 
 
   ' Create a temporary QueryDef to retrieve data from 
   ' a Microsoft SQL Server database based on the results from 
   ' the first query. 
   Set qdfBonusEarners = dbsCurrent.CreateQueryDef("") 
   With qdfBonusEarners 
      ' Note: The DSN referenced below must be configured to  
      '       use Microsoft Windows NT Authentication Mode to  
      '       authorize user access to the Microsoft SQL Server. 
      .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
      .SQL = "SELECT * FROM titleauthor " & _ 
         "WHERE title_id = '" & _ 
         rstTopSeller!title_id & "'" 
      Set rstBonusRecipients = .OpenRecordset() 
   End With 
 
   ' Build the output string. 
   With rstBonusRecipients 
      Do While Not .EOF 
         strAuthorList = strAuthorList & "  " & _ 
            !au_id & ":  $" & (10 * !royaltyper) & vbCr 
         .MoveNext 
      Loop 
   End With 
 
   ' Display results. 
   MsgBox "Please send a check to the following " & _ 
      "authors in the amounts shown:" & vbCr & _ 
      strAuthorList & "for outstanding sales of " & _ 
      rstTopSeller!Title & "." 
 
   rstTopSeller.Close 
   dbsCurrent.Close 
 
End Sub 
```

<br/>

El siguiente ejemplo muestra cómo crear una consulta de parámetros. Una consulta denominada **myQuery** se crea con dos parámetros, denominados Param1 y Param2. Para ello, la propiedad SQL de la consulta está configurada en una instrucción de Lenguaje de consulta estructurado (SQL) que define los parámetros.

**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateQueryWithParameters()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
        Dim strSQL As String
    
        Set dbs = CurrentDb
        Set qdf = dbs.CreateQueryDef("myQuery")
        Application.RefreshDatabaseWindow
    
        strSQL = "PARAMETERS Param1 TEXT, Param2 INT; "
        strSQL = strSQL & "SELECT * FROM [Table1] "
        strSQL = strSQL & "WHERE [Field1] = [Param1] AND [Field2] = [Param2];"
        qdf.SQL = strSQL
    
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```
