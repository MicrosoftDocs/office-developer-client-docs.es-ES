---
title: Método Recordset.Seek (DAO)
TOCTitle: Seek Method
ms:assetid: ef83d909-c962-b016-7d33-36eacdc25c2c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836416(v=office.15)
ms:contentKeyID: 48548585
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053061
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: db2c90d42feacee58af9eea30a2d99439cb4ddaf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307605"
---
# <a name="recordsetseek-method-dao"></a>Método Recordset.Seek (DAO)

**Se aplica a:** Access 2013, Office 2013

Busca el registro en un objeto **Recordset** indexado de tipo tabla que satisface los criterios especificados para el índice actual y convierte a ese registro en el registro actual (espacios de trabajo de Microsoft Access solamente).

## <a name="syntax"></a>Sintaxis

*expression* .Seek(***Comparison***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)

*expression* Variable que representa un objeto **Recordset**.

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
<td><p><em>Comparación</em></p></td>
<td><p>Necesario</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Una de las siguientes expresiones de cadena: &lt;, &lt;=, =, &gt;=, o &gt;.</p></td>
</tr>
<tr class="even">
<td><p><em>Key1, Key2...Key13</em></p></td>
<td><p>Necesario</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uno o más valores correspondientes a campos en el índice actual del objeto <strong>Recordset</strong>, según lo especificado por su configuración de propiedad <strong>Index</strong>. Puede usar hasta 13 argumentos clave.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Debe establecer el índice actual con la propiedad **Index** para poder usar **Seek**. Si el índice identifica un campo de clave que no es único, **Seek** busca el primer registro que satisface los criterios.

El método **Seek** busca en los campos clave especificados y localiza el primer registro que satisface los criterios indicados por comparison y key1. Una vez encontrado, hace del registro el registro activo y establece la propiedad **NoMatch** en **False**. Si el método **Seek** no consigue encontrar coincidencias, la propiedad **NoMatch** se establece en **True** y el registro activo es indefinido.

Si comparison es igual que (=), mayor o igual que (\>=), o mayor que (\>), **Seek** comienza por el principio del índice y busca hacia delante.

Si comparison es menor que (\<) o menor o igual que (\<=), **Seek** comienza por el final del índice y busca hacia atrás. No obstante, si hay entradas de índice duplicadas al final del éste, **Seek** comienza en una entrada arbitraria entre las duplicadas y busca hacia atrás.

Debe especificar valores para todos los campos definidos en el índice. Si utiliza **Seek** con un índice de varias columnas y no especifica un valor de comparación para cada campo del índice, no puede utilizar el operador igual (=) en la comparación. Esto sucede porque algunos de los campos de criterios (key2, key3, etc.) tendrán el valor Null de forma predeterminada, lo que probablemente no coincidirá. Por lo tanto, el operador igual funcionará correctamente solo si tiene un registro que es todo **null** excepto la clave que está buscando. Se recomienda utilizar el operador mayor o igual que (\>=) en su lugar.

El argumento key1 debe ser del mismo tipo de datos de campo que el campo correspondiente en el índice activo. Por ejemplo, si el índice activo se refiere a un número de campo (como ID de empleado), key1 debe ser numérico. De igual forma, si el índice activo se refiere a un campo de texto (como Apellido), key1 debe ser una cadena.

No es necesario que exista un registro actual cuando usa **Seek**.

Puede usar la colección **[Indexes](indexes-collection-dao.md)** para enumerar los índices existentes.

Para encontrar un registro en un **Recordset** de tipo dynaset o snapshot que satisface una condición específica que no está cubierta por índices existentes, use los métodos **[Find](recordset-findfirst-method-dao.md)**. Para incluir todos los registros, no solo aquellos que satisfacen una condición específica, use los métodos **[Move](recordset-movefirst-method-dao.md)** para mover de registro a registro.

No puede usar el método **Seek** en una tabla vinculada porque no puede abrir tablas vinculadas como objetos **Recordset** de tipo tabla. No obstante, si usa el método **[OpenDatabase](dbengine-opendatabase-method-dao.md)** para abrir directamente una base de datos ISAM (no ODBC) que es instalable, puede usar **Seek** en tablas de esa base de datos.

## <a name="example"></a>Ejemplo

Este ejemplo demuestra el método **Seek** al permitir al usuario buscar un producto según un número de ID.

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim intFirst As Integer 
       Dim intLast As Integer 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' You must open a table-type Recordset to use an index,  
       ' and hence the Seek method. 
       Set rstProducts = _ 
          dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
       With rstProducts 
          ' Set the index. 
          .Index = "PrimaryKey" 
     
          ' Get the lowest and highest product IDs. 
          .MoveLast 
          intLast = !ProductID 
          .MoveFirst 
          intFirst = !ProductID 
     
          Do While True 
             ' Display current record information and ask user  
             ' for ID number. 
             strMessage = "Product ID: " & !ProductID & vbCr & _ 
                "Name: " & !ProductName & vbCr & vbCr & _ 
                "Enter a product ID between " & intFirst & _ 
                " and " & intLast & "." 
             strSeek = InputBox(strMessage) 
     
             If strSeek = "" Then Exit Do 
     
             ' Store current bookmark in case the Seek fails. 
             varBookmark = .Bookmark 
     
             .Seek "=", Val(strSeek) 
     
             ' Return to the current record if the Seek fails. 
             If .NoMatch Then 
                MsgBox "ID not found!" 
                .Bookmark = varBookmark 
             End If 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

En este ejemplo se utiliza la propiedad **NoMatch** para determinar si **Seek** y **FindFirst** han tenido un resultado correcto y, en caso contrario, proporcionar información adecuada. Se necesitan los procedimientos SeekMatch y FindMatch para que pueda ejecutarse este procedimiento.

```vb
    Sub NoMatchX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim rstCustomers As Recordset 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim strCountry As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' Default is dbOpenTable; required if Index property will  
       ' be used. 
       Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
       With rstProducts 
          .Index = "PrimaryKey" 
     
          Do While True 
             ' Show current record information; ask user for  
             ' input. 
             strMessage = "NoMatch with Seek method" & vbCr & _ 
                "Product ID: " & !ProductID & vbCr & _ 
                "Product Name: " & !ProductName & vbCr & _ 
                "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
                "Enter a product ID." 
             strSeek = InputBox(strMessage) 
             If strSeek = "" Then Exit Do 
     
             ' Call procedure that seeks for a record based on  
             ' the ID number supplied by the user. 
             SeekMatch rstProducts, Val(strSeek) 
          Loop 
     
          .Close 
       End With 
     
       Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
          "SELECT CompanyName, Country FROM Customers " & _ 
          "ORDER BY CompanyName", dbOpenSnapshot) 
     
       With rstCustomers 
     
          Do While True 
             ' Show current record information; ask user for  
             ' input. 
             strMessage = "NoMatch with FindFirst method" & _ 
                vbCr & "Customer Name: " & !CompanyName & _ 
                vbCr & "Country: " & !Country & vbCr & _ 
                "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
                "Enter country on which to search." 
             strCountry = Trim(InputBox(strMessage)) 
             If strCountry = "" Then Exit Do 
     
             ' Call procedure that finds a record based on  
             ' the country name supplied by the user. 
             FindMatch rstCustomers, _ 
                "Country = '" & strCountry & "'" 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset, _ 
       intSeek As Integer) 
     
       Dim varBookmark As Variant 
       Dim strMessage As String 
     
       With rstTemp 
          ' Store current record location. 
          varBookmark = .Bookmark 
          .Seek "=", intSeek 
     
          ' If Seek method fails, notify user and return to the  
          ' last current record. 
          If .NoMatch Then 
             strMessage = _ 
                "Not found! Returning to current record." & _ 
                vbCr & vbCr & "NoMatch = " & .NoMatch 
             MsgBox strMessage 
             .Bookmark = varBookmark 
          End If 
     
       End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
       strFind As String) 
     
       Dim varBookmark As Variant 
       Dim strMessage As String 
     
       With rstTemp 
          ' Store current record location. 
          varBookmark = .Bookmark 
          .FindFirst strFind 
     
          ' If Find method fails, notify user and return to the  
          ' last current record. 
          If .NoMatch Then 
             strMessage = _ 
                "Not found! Returning to current record." & _ 
                vbCr & vbCr & "NoMatch = " & .NoMatch 
             MsgBox strMessage 
             .Bookmark = varBookmark 
          End If 
     
       End With 
     
    End Sub 
```

<br/>

El siguiente ejemplo muestra cómo usar el método Seek para encontrar un registro en una tabla vinculada.

**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```
