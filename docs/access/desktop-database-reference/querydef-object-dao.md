---
title: Objeto QueryDef (DAO)
TOCTitle: QueryDef Object
ms:assetid: 0b3d901c-345d-42a2-f5f1-fb09cc562e27
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845129(v=office.15)
ms:contentKeyID: 48543169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a94d34a2dbe8043e6db637b649f59047cf3f1dda
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713558"
---
# <a name="querydef-object-dao"></a>Objeto QueryDef (DAO)

**Se aplica a:** Access 2013 | Office 2013 

Un objeto **QueryDef** es una definición de una consulta almacenada en una base de datos del motor de base de datos de Microsoft Access.

## <a name="remarks"></a>Observaciones

Puede usar el objeto **QueryDef** para definir una consulta. Por ejemplo, puede:

- Usar la propiedad **SQL** para configurar o devolver la definición de la consulta.

- Usar la colección **Parameters** del objeto **QueryDef** para configurar o devolver parámetros de consulta.

- Usar la propiedad **Type** para devolver un valor que indique si la consulta selecciona registros de una tabla existente, crea una tabla nueva, inserta registros de una tabla en otra, elimina registros o los actualiza.

- Usar la propiedad **MaxRecords** para limitar el número de registros que devuelve una consulta.

- Usar la propiedad **ODBCTimeout** para indicar cuánto tiempo se debe esperar a que la consulta devuelva registros. La propiedad **ODBCTimeout** se aplica a cualquier consulta que tenga acceso a datos ODBC.

- Usar la propiedad **ReturnsRecords** para indicar que la consulta devuelve registros. La propiedad **ReturnsRecords** solo es válida en consultas SQL de paso a través.

- Usar la propiedad **Connect** para crear una consulta SQL de paso a través en una base de datos ODBC.

También se pueden crear objetos **QueryDef** temporales. A diferencia de los objetos **QueryDef** permanentes, los objetos **QueryDef** temporales no se guardan en el disco ni se anexan a la colección **QueryDefs**. Los objetos **QueryDef** temporales son útiles para las consultas que se deben ejecutar de forma repetida en tiempo de ejecución pero que no es necesario guardar en el disco, especialmente si se crean las instrucciones SQL en tiempo de ejecución.

Puede considerar un objeto **QueryDef** permanente de un área de trabajo de Microsoft Access como una instrucción SQL compilada. Si ejecuta una consulta desde un objeto **QueryDef** permanente, la consulta se ejecutará más rápidamente que si ejecuta la instrucción SQL equivalente desde el método **OpenRecordset**. Esto se debe a que el motor de base de datos de Microsoft Access no necesita compilar la consulta antes de ejecutarla.

La forma preferida de usar el dialecto SQL nativo de un motor de base de datos externo al que se accede a través del motor de base de datos de Microsoft Access es mediante objetos **QueryDef**. Por ejemplo, puede crear una consulta de Microsoft SQL Server y almacenarla en un objeto **QueryDef**. Cuando necesite usar una consulta SQL de un motor de base de datos que no sea de Microsoft Access, deberá proporcionar una cadena de propiedad **Connect** que apunte al origen de datos externo. Las consultas con propiedades **Connect** válidas omiten el motor de base de datos de Microsoft Access y pasan la consulta directamente al servidor de base de datos externo para procesarla.

Para crear un objeto **QueryDef** nuevo, use el método **CreateQueryDef**. En un área de trabajo de Microsoft Access, si proporciona una cadena para el argumento name o si establece explícitamente la propiedad **Name** del nuevo objeto **QueryDef** en una cadena de longitud – cero, va a crear un **objeto QueryDef** permanente que se va a automáticamente se anexa a la colección **QueryDefs** y se guardan en el disco. Proporciona una cadena de longitud cero como el argumento de nombre o establecer explícitamente la propiedad **Name** en una cadena de longitud cero se producirá en un objeto **QueryDef** temporal.

Para hacer referencia a un objeto **QueryDef** en una colección por su número ordinal o por la configuración de la propiedad **Nombre**, use cualquiera de las siguientes formas de sintaxis:

QueryDefs(0)

QueryDefs("name")

QueryDefs\! \[ nombre\]

Puede hacer referencia a objetos **QueryDef** temporales solo por las variables de objeto que les haya asignado.

**Vínculo proporcionado por** la Comunidad [UtterAccess](https://www.utteraccess.com) . UtterAccess es el principal foro de ayuda y wiki de Microsoft Access.

- [Consultas: documentar SQL en Word](https://www.utteraccess.com/wiki/index.php/queries:_document_sql_to_word)

## <a name="example"></a>Ejemplo

En este ejemplo se crea un nuevo objeto **QueryDef** y se anexa a la colección **QueryDefs** del objeto **Base de datos** de Northwind. Luego se enumera la colección **QueryDefs** y la colección **Propiedades** del nuevo **QueryDef**.

```vb
    Sub QueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfNew As QueryDef 
       Dim qdfLoop As QueryDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new QueryDef object. Because it has a  
       ' name, it is automatically appended to the  
       ' QueryDefs collection. 
       Set qdfNew = dbsNorthwind.CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
     
       With dbsNorthwind 
          Debug.Print .QueryDefs.Count & _ 
             " QueryDefs in " & .Name 
     
          ' Enumerate QueryDefs collection. 
          For Each qdfLoop In .QueryDefs 
             Debug.Print "  " & qdfLoop.Name 
          Next qdfLoop 
     
          With qdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new  
             ' QueryDef object. 
             For Each prpLoop In .Properties 
                On Error Resume Next 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
                On Error Goto 0 
             Next prpLoop 
          End With 
     
          ' Delete new QueryDef because this is a  
          ' demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

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

En el siguiente ejemplo se muestra cómo reemplazar la instrucción de Lenguaje de consulta estructurado (SQL) en una consulta guardada.

**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    ‘To change the Where clause in a saved query  
    Dim qdf as QueryDef
    Dim db as Database
    Set db = CurrentDB
    Set qdf = db.QueryDefs("YourQueryName")
    qdf.SQL = ReplaceWhereClause(qdf.SQL, strYourNewWhereClause)
    set qdf = Nothing
    set db = Nothing
    
    Public Function ReplaceWhereClause(strSQL As Variant, strNewWHERE As Variant)
    On Error GoTo Error_Handler
    
    ‘This subroutine accepts a valid SQL string and Where clause, and
    ‘returns the same SQL statement with the original Where clause (if any)
    ‘replaced by the passed in Where clause.
    ‘
    ‘INPUT:
    ‘ strSQL valid SQL string to change
    ‘OUTPUT:
    ‘ strNewWHERE New WHERE clause to insert into SQL statement
    ‘
        Dim strSELECT As String, strWhere As String
        Dim strOrderBy As String, strGROUPBY As String, strHAVING As String
    
        Call ParseSQL(strSQL, strSELECT, strWhere, strOrderBy, _
            strGROUPBY, strHAVING)
    
        ReplaceWhereClause = strSELECT &""& strNewWHERE &""_
            & strGROUPBY &""& strHAVING &""& strOrderBy
    
        Exit_Procedure:
            Exit Function
    
        Error_Handler:
            MsgBox (Err.Number & ": " & Err.Description)
            Resume Exit_Procedure
    
    End Function
```

