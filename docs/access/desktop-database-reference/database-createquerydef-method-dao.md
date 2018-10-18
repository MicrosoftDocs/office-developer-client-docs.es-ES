---
title: Método Database.CreateQueryDef (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 75ee7cac-dcd0-b4c5-b55b-9cbaaae2cbf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195966(v=office.15)
ms:contentKeyID: 48545686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 15577750d7c6a2373178bce9fefff16fef512023
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602675"
---
# <a name="databasecreatequerydef-method-dao"></a><span data-ttu-id="1c49c-102">Método Database.CreateQueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="1c49c-102">Database.CreateQueryDef Method (DAO)</span></span>

<span data-ttu-id="1c49c-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c49c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1c49c-104">Crea un nuevo objeto **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="1c49c-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c49c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c49c-105">Syntax</span></span>

<span data-ttu-id="1c49c-106">*expresión* . CreateQueryDef (***nombre***, ***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="1c49c-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="1c49c-107">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="1c49c-107">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="1c49c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c49c-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c49c-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="1c49c-109">Name</span></span></p></th>
<th><p><span data-ttu-id="1c49c-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="1c49c-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="1c49c-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1c49c-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="1c49c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c49c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c49c-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="1c49c-113">Name</span></span></p></td>
<td><p><span data-ttu-id="1c49c-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="1c49c-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="1c49c-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1c49c-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1c49c-116"><strong>Variant</strong> (subtipo <strong>String</strong>) que designa inequívocamente el nuevo objeto <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="1c49c-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c49c-117">SQLText</span><span class="sxs-lookup"><span data-stu-id="1c49c-117">SQLText</span></span></p></td>
<td><p><span data-ttu-id="1c49c-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="1c49c-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="1c49c-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1c49c-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1c49c-p101"><strong>Variant</strong> (subtipo <strong>String</strong>) que es una instrucción SQL que define el objeto <strong>QueryDef</strong>. Si omite este argumento, puede definir el objeto <strong>QueryDef</strong> estableciendo su propiedad <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> antes o después de agregarlo a una colección.</span><span class="sxs-lookup"><span data-stu-id="1c49c-p101">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>. If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1c49c-122"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="1c49c-122"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="1c49c-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c49c-123">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="1c49c-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c49c-124">Return value</span></span>
>>>>>>> <span data-ttu-id="1c49c-125">master</span><span class="sxs-lookup"><span data-stu-id="1c49c-125">master</span></span>

<span data-ttu-id="1c49c-126">Objeto QueryDef</span><span class="sxs-lookup"><span data-stu-id="1c49c-126">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="1c49c-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c49c-127">Remarks</span></span>

<span data-ttu-id="1c49c-128">En un área de trabajo de Microsoft Access, si proporciona cualquier otro elemento que no sea una cadena de longitud cero para el nombre al crear un objeto **QueryDef**, el objeto **QueryDef** resultante se agrega automáticamente a la colección **[QueryDefs](querydefs-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="1c49c-128">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="1c49c-129">Si el objeto especificado por el nombre ya es un miembro de la colección **QueryDefs** , se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="1c49c-129">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="1c49c-130">Puede crear un **objeto QueryDef** de temporal utilizando una cadena de longitud cero para el argumento name cuando ejecute el método **CreateQueryDef** .</span><span class="sxs-lookup"><span data-stu-id="1c49c-130">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="1c49c-131">También puede hacerlo estableciendo la propiedad **[Name](querydef-name-property-dao.md)** de un **objeto QueryDef** de recién creado en una cadena de longitud cero ("").</span><span class="sxs-lookup"><span data-stu-id="1c49c-131">You can also accomplish this by setting the **[Name](querydef-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> 

<span data-ttu-id="1c49c-132">Los objetos **QueryDef** temporales son útiles si desea utilizar repetidamente instrucciones SQL sin tener que crear nuevos objetos permanentes en la colección **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="1c49c-132">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="1c49c-133">No se puede anexar un **objeto QueryDef** de temporal a cualquier colección debido a que una cadena de longitud cero no es un nombre válido para un objeto **QueryDef** permanente.</span><span class="sxs-lookup"><span data-stu-id="1c49c-133">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="1c49c-134">Siempre puede establecer el **nombre** y las propiedades **SQL** del objeto **QueryDef** recién creado y, posteriormente, anexe el **objeto QueryDef** a la colección **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="1c49c-134">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="1c49c-135">Para ejecutar una instrucción SQL en un objeto **QueryDef**, use el método **[Execute](querydef-execute-method-dao.md)** u **[OpenRecordset](database-openrecordset-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="1c49c-135">To run the SQL statement in a **QueryDef** object, use the **[Execute](querydef-execute-method-dao.md)** or **[OpenRecordset](database-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="1c49c-136">El uso de un objeto **QueryDef** es el método recomendado para realizar consultas de paso SQL con bases de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="1c49c-136">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="1c49c-137">Para quitar un objeto **QueryDef** de una colección **QueryDefs** de una base de datos del motor de base de datos de Microsoft Access, use el método **[Delete](querydefs-delete-method-dao.md)** en la colección.</span><span class="sxs-lookup"><span data-stu-id="1c49c-137">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](querydefs-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="1c49c-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1c49c-138">Example</span></span>

<span data-ttu-id="1c49c-p104">En este ejemplo se usa el método **CreateQueryDef** para crear y ejecutar un **QueryDef** temporal y uno permanente. La función GetrstTemp es obligatoria para que este procedimiento se ejecute.</span><span class="sxs-lookup"><span data-stu-id="1c49c-p104">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**. The GetrstTemp function is required for this procedure to run.</span></span>

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

<span data-ttu-id="1c49c-p105">En este ejemplo se usan los métodos **CreateQueryDef** y **OpenRecordset** y la propiedad **SQL** para realizar una consulta en la tabla de títulos de la base de datos de ejemplo Pubs de Microsoft SQL Server y devolver el título y el identificador de título del libro más vendido. A continuación, se realiza una consulta en la tabla de autores y se indica al usuario que envíe una prima a cada autor en función de su porcentaje de derechos de autor (la prima total es de 1.000 dólares y cada autor debe recibir un porcentaje de ese importe).</span><span class="sxs-lookup"><span data-stu-id="1c49c-p105">This example uses the **CreateQueryDef** and **OpenRecordset** methods and the **SQL** property to query the table of titles in the Microsoft SQL Server sample database Pubs and return the title and title identifier of the best-selling book. The example then queries the table of authors and instructs the user to send a bonus check to each author based on his or her royalty share (the total bonus is $1,000 and each author should receive a percentage of that amount).</span></span>

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

<span data-ttu-id="1c49c-143">En el siguiente ejemplo se muestra cómo crear una consulta de parámetro.</span><span class="sxs-lookup"><span data-stu-id="1c49c-143">The following example shows how to create a parameter query.</span></span> <span data-ttu-id="1c49c-144">Se crea una consulta denominada **myQuery** con dos parámetros, denominados Param1 y parámetro2.</span><span class="sxs-lookup"><span data-stu-id="1c49c-144">A query named **myQuery** is created with two parameters, named Param1 and Param2.</span></span> <span data-ttu-id="1c49c-145">Para ello, la propiedad SQL de la consulta está configurada en una instrucción Lenguaje de consulta estructurado (SQL) que define los parámetros.</span><span class="sxs-lookup"><span data-stu-id="1c49c-145">To do this, the SQL property of the query is set to a Structured Query Language (SQL) statement that defines the parameters.</span></span>

<span data-ttu-id="1c49c-146">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="1c49c-146">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
