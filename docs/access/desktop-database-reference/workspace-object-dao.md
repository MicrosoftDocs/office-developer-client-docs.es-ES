---
title: Objeto Workspace (DAO)
TOCTitle: Workspace Object
ms:assetid: bf3ab863-5e9a-4842-1f82-2ccf958d9779
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822782(v=office.15)
ms:contentKeyID: 48547481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 2c734d5e0f022faec4ebb9efe2dfc2f7dd7b7979
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711584"
---
# <a name="workspace-object-dao"></a><span data-ttu-id="6a68b-102">Objeto Workspace (DAO)</span><span class="sxs-lookup"><span data-stu-id="6a68b-102">Workspace object (DAO)</span></span>

<span data-ttu-id="6a68b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a68b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6a68b-p101">Un objeto **Workspace** define una sesión con nombre para un usuario. Contiene bases de datos abiertas y proporciona mecanismos para transacciones simultáneas y, en áreas de trabajo de Microsoft Access, compatibilidad con grupos de trabajo seguros.</span><span class="sxs-lookup"><span data-stu-id="6a68b-p101">A **Workspace** object defines a named session for a user. It contains open databases and provides mechanisms for simultaneous transactions and, in Microsoft Access workspaces, secure workgroup support.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a68b-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a68b-106">Remarks</span></span>

<span data-ttu-id="6a68b-p102">Un **Workspace** es un objeto no persistente que define cómo interactúa la aplicación con los datos usando el motor de base de datos de Microsoft Access. Use el objeto **Workspace** para administrar la sesión actual o iniciar una sesión adicional. En una sesión, puede abrir varias bases de datos o conexiones y administrar transacciones. Por ejemplo, puede:</span><span class="sxs-lookup"><span data-stu-id="6a68b-p102">A **Workspace** is a non-persistent object that defines how your application interacts with data by using the Microsoft Access database engine. Use the **Workspace** object to manage the current session or to start an additional session. In a session, you can open multiple databases or connections, and manage transactions. For example, you can:</span></span>

- <span data-ttu-id="6a68b-p103">Usar las propiedades **Name**, **UserName** y **Type** para establecer una sesión con nombre. La sesión crea un ámbito en el que se pueden abrir varias bases de datos y realizar una instancia de transacciones anidadas.</span><span class="sxs-lookup"><span data-stu-id="6a68b-p103">Use the **Name**, **UserName**, and **Type** properties to establish a named session. The session creates a scope in which you can open multiple databases and conduct one instance of nested transactions.</span></span>

- <span data-ttu-id="6a68b-113">Usar el método **Close** para finalizar la sesión.</span><span class="sxs-lookup"><span data-stu-id="6a68b-113">Use the **Close** method to terminate a session.</span></span>

- <span data-ttu-id="6a68b-114">Usar el método **OpenDatabase** para abrir una o más bases de datos existentes en un **área de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="6a68b-114">Use the **OpenDatabase** method to open one or more existing databases on a **Workspace**.</span></span>

- <span data-ttu-id="6a68b-115">Usar los métodos **BeginTrans**, **CommitTrans** y **Rollback** para administrar el procesamiento de transacciones anidadas dentro de un **área de trabajo** y usar varios objetos **Workspace** para llevar a cabo varias transacciones simultáneas y superpuestas.</span><span class="sxs-lookup"><span data-stu-id="6a68b-115">Use the **BeginTrans**, **CommitTrans**, and **Rollback** methods to manage nested transaction processing within a **Workspace** and use several **Workspace** objects to conduct multiple, simultaneous, and overlapping transactions.</span></span>

<span data-ttu-id="6a68b-116">Cuando en primer lugar, consulte o usar un objeto **Workspace** , se crea automáticamente el área de trabajo de forma predeterminada, DBEngine.Workspaces(0).</span><span class="sxs-lookup"><span data-stu-id="6a68b-116">When you first refer to or use a **Workspace** object, you automatically create the default workspace, DBEngine.Workspaces(0).</span></span> <span data-ttu-id="6a68b-117">Los valores de las propiedades **Name** y **UserName** del área de trabajo predeterminada son "\#área de trabajo predeterminada\#" y "Admin", respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6a68b-117">The settings of the **Name** and **UserName** properties of the default workspace are "\#Default Workspace\#" and "Admin," respectively.</span></span> <span data-ttu-id="6a68b-118">Si está habilitada la seguridad, la configuración de la propiedad **UserName** es el nombre del usuario que ha iniciado la sesión.</span><span class="sxs-lookup"><span data-stu-id="6a68b-118">If security is enabled, the **UserName** property setting is the name of the user who logged on.</span></span>

<span data-ttu-id="6a68b-p105">Cuando se usan transacciones, se ven afectadas todas las bases de datos del **área de trabajo** especificada aunque se abran varios objetos **Database** en el **área de trabajo**. Por ejemplo, si usa un método **BeginTrans**, actualiza varios registros de una base de datos y luego elimina registros de otra base de datos, pero después usa el método **Rollback**, tanto las operaciones de actualización como de eliminación se cancelan y se deshacen. Puede crear más objetos **Workspace** para administrar las transacciones de forma independiente entre los objetos **Database**.</span><span class="sxs-lookup"><span data-stu-id="6a68b-p105">When you use transactions, all databases in the specified **Workspace** are affected— even if multiple **Database** objects are opened in the **Workspace**. For example, you use a **BeginTrans** method, update several records in a database, and then delete records in another database. If you then use the **Rollback** method, both the update and delete operations are canceled and rolled back. You can create additional **Workspace** objects to manage transactions independently across **Database** objects.</span></span>

<span data-ttu-id="6a68b-p106">Puede crear objetos **Workspace** con el método **CreateWorkspace**. Después de crear un nuevo objeto **Workspace**, debe anexarlo a la colección **Workspaces** si necesita hacer referencia a él desde la colección **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="6a68b-p106">You can create **Workspace** objects with the **CreateWorkspace** method. After you create a new **Workspace** object, you must append it to the **Workspaces** collection if you need to refer to it from the **Workspaces** collection.</span></span>

<span data-ttu-id="6a68b-p107">Puede usar un objeto **Workspace** recién creado sin anexarlo a la colección **Workspaces**. Sin embargo, debe hacer referencia a él por la variable de objeto que le asignó.</span><span class="sxs-lookup"><span data-stu-id="6a68b-p107">You can use a newly created **Workspace** object without appending it to the **Workspaces** collection. However, you must refer to it by the object variable to which you have assigned it.</span></span>

<span data-ttu-id="6a68b-127">Para hacer referencia a un objeto **Workspace** de una colección por su número ordinal o por su propiedad **Name**, use cualquiera de las formas sintácticas siguientes:</span><span class="sxs-lookup"><span data-stu-id="6a68b-127">To refer to a **Workspace** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="6a68b-128">**DBEngine**. **Áreas de trabajo** (0)</span><span class="sxs-lookup"><span data-stu-id="6a68b-128">**DBEngine**.**Workspaces**(0)</span></span>

<span data-ttu-id="6a68b-129">**DBEngine**. **Áreas de trabajo** ("nombre")</span><span class="sxs-lookup"><span data-stu-id="6a68b-129">**DBEngine**.**Workspaces**("name")</span></span>

<span data-ttu-id="6a68b-130">**DBEngine**. **Áreas de trabajo** \! \[nombre\]</span><span class="sxs-lookup"><span data-stu-id="6a68b-130">**DBEngine**.**Workspaces**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="6a68b-p108">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6a68b-p108">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


## <a name="example"></a><span data-ttu-id="6a68b-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6a68b-133">Example</span></span>

<span data-ttu-id="6a68b-p109">En este ejemplo, se crea un nuevo objeto Workspace de Microsoft Access y se lo anexa a la colección **Workspaces**. Luego se enumeran las colecciones **Workspaces** y la colección **Properties** del objeto **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="6a68b-p109">This example creates a new Microsoft Access Workspace object and appends it to the **Workspaces** collection. It then enumerates the **Workspaces** collections and the **Properties** collection of the **Workspace** object.</span></span>

```vb 
Sub WorkspaceX() 
 
   Dim wrkNewAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
   ' Create a new Microsoft Access workspace. 
   Set wrkNewAcc = CreateWorkspace("NewAccessWorkspace", _ 
      "admin", "", dbUseJet) 
   Workspaces.Append wrkNewAcc 
 
   ' Enumerate the Workspaces collection. 
   For Each wrkLoop In Workspaces 
      With wrkLoop 
         Debug.Print "Properties of " & .Name 
         ' Enumerate the Properties collection of the new 
         ' Workspace object. 
         For Each prpLoop In .Properties 
            On Error Resume Next 
            If prpLoop <> "" Then Debug.Print "  " & _ 
               prpLoop.Name & " = " & prpLoop 
            On Error GoTo 0 
         Next prpLoop 
      End With 
   Next wrkLoop 
 
   wrkNewAcc.Close 
End Sub 
```

<br/>

<span data-ttu-id="6a68b-p110">En este ejemplo, se usa el método **CreateWorkspace** para crear un área de trabajo de Microsoft Access. A continuación, se enumeran las propiedades del área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6a68b-p110">This example uses the **CreateWorkspace** method to create a Microsoft Access workspace. It then lists the properties of theworkspace.</span></span>

```vb 
Sub CreateWorkspaceX() 
 
   Dim wrkAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
 
   DefaultType = dbUseJet 
   ' Create an unnamed Workspace object of the type  
   ' specified by the DefaultType property of DBEngine  
   ' (dbUseJet). 
   Set wrkAcc = CreateWorkspace("", "admin", "") 
 
   ' Enumerate Workspaces collection. 
   Debug.Print "Workspace objects in Workspaces collection:" 
   For Each wrkLoop In Workspaces 
      Debug.Print "  " & wrkLoop.Name 
   Next wrkLoop 
 
   With wrkAcc 
      ' Enumerate Properties collection of Microsoft Access  
      ' workspace. 
      Debug.Print _ 
         "Properties of unnamed Microsoft Access workspace" 
      On Error Resume Next 
      For Each prpLoop In .Properties 
         Debug.Print "  " & prpLoop.Name & " = " & prpLoop 
      Next prpLoop 
      On Error GoTo 0 
   End With 
 
   wrkAcc.Close 
 
End Sub 
```

<br/>

<span data-ttu-id="6a68b-138">En el ejemplo siguiente, se muestra cómo usar una transacción en un área de trabajo de objetos de acceso a datos (DAO).</span><span class="sxs-lookup"><span data-stu-id="6a68b-138">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="6a68b-139">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="6a68b-139">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


```vb
    Public Sub TransferFunds()
        Dim wrk As DAO.Workspace
        Dim dbC As DAO.Database
        Dim dbX As DAO.Database
        
        Set wrk = DBEngine(0)
        Set dbC = CurrentDb
        Set dbX = wrk.OpenDatabase("e:\books\acc2007vba\myDB.accdb")
        
        On Error GoTo trans_Err
        
        'Begin the transaction
        
        wrk.BeginTrans
        
        'Withdraw funds from one account table
        dbC.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT -20, 'DEBIT', Date()", dbFailOnError
    
        'Deposit funds into another account table
        dbX.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT 20, 'CREDIT', Date()", dbFailOnError
        
        'Commit the transaction
        wrk.CommitTrans dbForceOSFlush
        
    trans_Exit:
        'Clean up
        wrk.Close
        Set dbC = Nothing
        Set dbX = Nothing
        Set wrk = Nothing
        Exit Sub
        
    trans_Err:
        'Roll back the transaction
        wrk.Rollback
        Resume trans_Exit
        
    End Sub
```
