---
title: Connection.Database Property (DAO)
TOCTitle: Database Property
ms:assetid: cf871353-0ea4-f995-6e0e-812af443daf9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834675(v=office.15)
ms:contentKeyID: 48547809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053581
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9627e5413e362baad505bfdf98092044499986c4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484739"
---
# <a name="connectiondatabase-property-dao"></a><span data-ttu-id="cc0e8-102">Connection.Database Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="cc0e8-102">Connection.Database Property (DAO)</span></span>


<span data-ttu-id="cc0e8-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc0e8-103">**Applies to**: Access 2013 | Office 2013</span></span>



## <a name="syntax"></a><span data-ttu-id="cc0e8-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc0e8-104">Syntax</span></span>

<span data-ttu-id="cc0e8-105">*expresión* . Base de datos</span><span class="sxs-lookup"><span data-stu-id="cc0e8-105">*expression* .Database</span></span>

<span data-ttu-id="cc0e8-106">*expresión* Variable que representa un objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="cc0e8-106">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc0e8-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc0e8-107">Remarks</span></span>

<span data-ttu-id="cc0e8-p101">En un objeto **[Connection](connection-object-dao.md)**, use la propiedad **Database** para obtener una referencia a un objeto **Database** correspondiente al objeto **Connection**. En DAO, un objeto **Connection** y su objeto **Database** correspondiente son simplemente dos referencias diferentes de variable de objeto al mismo objeto. La propiedad **Database** de un objeto **Connection** y la propiedad **[Connection](database-connection-property-dao.md)** de un objeto **Database** facilitan el cambio de conexión a un origen de datos ODBC mediante el motor de base de datos de Microsoft Access para utilizar ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="cc0e8-p101">On a **[Connection](connection-object-dao.md)** object, use the **Database** property to obtain a reference to a **Database** object that corresponds to the **Connection**. In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object. The **Database** property of a **Connection** object and the **[Connection](database-connection-property-dao.md)** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

## <a name="example"></a><span data-ttu-id="cc0e8-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cc0e8-111">Example</span></span>

<span data-ttu-id="cc0e8-112">En este ejemplo, se usa la propiedad **Database** para mostrar cómo se puede convertir código que solía tener acceso a datos ODBC mediante el motor de base de datos de Microsoft Access para que utilice objetos Connection de ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="cc0e8-112">This example uses the **Database** property to show how code that used to access ODBC data through the Microsoft Access database engine can be converted to use ODBCDirect Connection objects.</span></span>

<span data-ttu-id="cc0e8-113">El procedimiento OldDatabaseCode utiliza un origen de datos conectado al motor de base de datos de Microsoft Access para tener acceso a una base de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="cc0e8-113">The OldDatabaseCode procedure uses a Microsoft Access database engine-connected data source to access an ODBC database.</span></span>

```vb
    Sub OldDatabaseCode() 
     
     Dim wrkMain As Workspace 
     Dim dbsPubs As Database 
     Dim prpLoop As Property 
     
     ' Create a Workspace object. 
     Set wrkMain = CreateWorkspace("", "admin", "", dbUseJet) 
     
     ' Open a Database object based on information in 
     ' the connect string. 
     
     'Note: The DSN referenced below must be configured to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set dbsPubs = wrkMain.OpenDatabase("Publishers", _ 
     dbDriverNoPrompt, False, _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     ' Enumerate the Properties collection of the Database 
     ' object. 
     With dbsPubs 
     Debug.Print "Database properties for " & _ 
     .Name & ":" 
     
     On Error Resume Next 
     For Each prpLoop In .Properties 
     If prpLoop.Name = "Connection" Then 
     ' Property actually returns a Connection object. 
     Debug.Print " Connection[.Name] = " & _ 
     .Connection.Name 
     Else 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop 
     End If 
     Next prpLoop 
     On Error GoTo 0 
     
     End With 
     
     dbsPubs.Close 
     wrkMain.Close 
     
    End Sub 
```

<span data-ttu-id="cc0e8-p102">En el ejemplo NewDatabaseCode, se abre un objeto **Connection** en un área de trabajo de ODBCDirect. Después, se asigna la propiedad **Database** del objeto **Connection** a una variable de objeto con el mismo nombre que el origen de datos del procedimiento antiguo. No hay que cambiar el código posterior si no se utilizan características específicas de las áreas de trabajo de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="cc0e8-p102">The NewDatabaseCode example opens a **Connection** object in an ODBCDirect workspace. It then assigns the **Database** property of the **Connection** object to an object variable with the same name as the data source in the old procedure. None of the subsequent code has to be changed as long as it doesn't use any features specific to Microsoft Access workspaces.</span></span>

```vb 
Sub NewDatabaseCode() 
 
 Dim wrkMain As Workspace 
 Dim conPubs As Connection 
 Dim dbsPubs As Database 
 Dim prpLoop As Property 
 
 ' Create ODBCDirect Workspace object instead of Microsoft 
 ' Access Workspace object. 
 Set wrkMain = CreateWorkspace("", "admin", "", dbUseODBC) 
 
 ' Open Connection object based on information in 
 ' the connect string. 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 ' Assign the Database property to the same object 
 ' variable as in the old code. 
 Set dbsPubs = conPubs.Database 
 
 ' Enumerate the Properties collection of the Database 
 ' object. From this point on, the code is the same as the 
 ' old example. 
 With dbsPubs 
 Debug.Print "Database properties for " & _ 
 .Name & ":" 
 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 If prpLoop.Name = "Connection" Then 
 ' Property actually returns a Connection object. 
 Debug.Print " Connection[.Name] = " & _ 
 .Connection.Name 
 Else 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 End If 
 Next prpLoop 
 On Error GoTo 0 
 
 End With 
 
 dbsPubs.Close 
 wrkMain.Close 
 
End Sub 
 
```

