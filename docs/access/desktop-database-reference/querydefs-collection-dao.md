---
title: Colección QueryDefs (DAO)
TOCTitle: QueryDefs Collection
ms:assetid: 6178c3a6-8301-16bf-4657-0fb113de0a36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194892(v=office.15)
ms:contentKeyID: 48545215
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8e42e11fa2fd9fe3d1b7c09ada65869d609a7df
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484876"
---
# <a name="querydefs-collection-dao"></a><span data-ttu-id="1b0ab-102">Colección QueryDefs (DAO)</span><span class="sxs-lookup"><span data-stu-id="1b0ab-102">QueryDefs Collection (DAO)</span></span>

<span data-ttu-id="1b0ab-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b0ab-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="1b0ab-104">Una colección **QueryDefs** contiene todos los objetos **QueryDef** de un objeto de **Base de datos** que hay en una base de datos de motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1b0ab-104">A **QueryDefs** collection contains all **QueryDef** objects of a **Database** object in a Microsoft Access database engine database.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b0ab-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1b0ab-105">Remarks</span></span>

<span data-ttu-id="1b0ab-106">Para crear un objeto **QueryDef** nuevo, use el método **CreateQueryDef**.</span><span class="sxs-lookup"><span data-stu-id="1b0ab-106">To create a new **QueryDef** object, use the **CreateQueryDef** method.</span></span> <span data-ttu-id="1b0ab-107">En un área de trabajo de Microsoft Access, si proporciona una cadena para el argumento name o si establece explícitamente la propiedad **Name** del nuevo objeto **QueryDef** en una cadena de longitud – cero, va a crear un **objeto QueryDef** permanente que se va a automáticamente se anexa a la colección **QueryDefs** y se guardan en el disco.</span><span class="sxs-lookup"><span data-stu-id="1b0ab-107">In a Microsoft Access workspace, if you supply a string for the name argument or if you explicitly set the **Name** property of the new **QueryDef** object to a non–zero-length string, you will create a permanent **QueryDef** that will automatically be appended to the **QueryDefs** collection and saved to disk.</span></span> <span data-ttu-id="1b0ab-108">Proporciona una cadena de longitud cero como el argumento de nombre o establecer explícitamente la propiedad **Name** en una cadena de longitud cero se producirá en un objeto **QueryDef** temporal.</span><span class="sxs-lookup"><span data-stu-id="1b0ab-108">Supplying a zero-length string as the name argument or explicitly setting the **Name** property to a zero-length string will result in a temporary **QueryDef** object.</span></span>

<span data-ttu-id="1b0ab-109">Para hacer referencia a un objeto **QueryDef** en una colección por su número ordinal o por la configuración de la propiedad **Nombre**, use cualquiera de las siguientes formas de sintaxis:</span><span class="sxs-lookup"><span data-stu-id="1b0ab-109">To refer to a **QueryDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="1b0ab-110">**Definiciones de consulta** (0)</span><span class="sxs-lookup"><span data-stu-id="1b0ab-110">**QueryDefs**(0)</span></span>

<span data-ttu-id="1b0ab-111">**Definiciones de consulta** ("nombre")</span><span class="sxs-lookup"><span data-stu-id="1b0ab-111">**QueryDefs**("name")</span></span>

<span data-ttu-id="1b0ab-112">**QueryDefs**\!\[nombre\]</span><span class="sxs-lookup"><span data-stu-id="1b0ab-112">**QueryDefs**\!\[name\]</span></span>

<span data-ttu-id="1b0ab-113">Puede hacer referencia a objetos **QueryDef** temporales solo por las variables de objeto que les haya asignado.</span><span class="sxs-lookup"><span data-stu-id="1b0ab-113">You can refer to temporary **QueryDef** objects only by the object variables that you have assigned to them.</span></span>

## <a name="example"></a><span data-ttu-id="1b0ab-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1b0ab-114">Example</span></span>

<span data-ttu-id="1b0ab-p102">En este ejemplo se crea un nuevo objeto **QueryDef** y se anexa a la colección **QueryDefs** del objeto **Base de datos** de Northwind. Luego se enumera la colección **QueryDefs** y la colección **Propiedades** del nuevo **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="1b0ab-p102">This example creates a new **QueryDef** object and appends it to the **QueryDefs** collection of the Northwind **Database** object. It then enumerates the **QueryDefs** collection and the **Properties** collection of the new **QueryDef**.</span></span>

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

<span data-ttu-id="1b0ab-p103">En este ejemplo se usa el método **CreateQueryDef** para crear y ejecutar un **QueryDef** temporal y otro permanente. La función GetrstTemp es necesaria para ejecutar este proceso.</span><span class="sxs-lookup"><span data-stu-id="1b0ab-p103">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**. The GetrstTemp function is required for this procedure to run.</span></span>

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

<span data-ttu-id="1b0ab-p104">En el ejemplo siguiente vemos cómo ejecutar una consulta de parámetros. La colección Parameters se usa para establecer el parámetro Organization de la consulta myActionQuery antes de que esta se ejecute.</span><span class="sxs-lookup"><span data-stu-id="1b0ab-p104">The following example shows how to execute a parameter query. The Parameters collection is used to set the Organization parameter of the myActionQuery query before the query is executed.</span></span>

<span data-ttu-id="1b0ab-121">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="1b0ab-121">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Public Sub ExecParameterQuery()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
    
        Set dbs = CurrentDb
        Set qdf = dbs.QueryDefs("myActionQuery")
    
        'Set the value of the QueryDef's parameter
        qdf.Parameters("Organization").Value = "Microsoft"
    
        'Execute the query
        qdf.Execute dbFailOnError
    
        'Clean up
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="1b0ab-122">En el ejemplo siguiente vemos cómo abrir un Recordset basado en una consulta de parámetros.</span><span class="sxs-lookup"><span data-stu-id="1b0ab-122">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

