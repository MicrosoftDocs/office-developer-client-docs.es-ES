---
title: Objeto Workspace (DAO)
TOCTitle: Workspace Object
ms:assetid: bf3ab863-5e9a-4842-1f82-2ccf958d9779
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822782(v=office.15)
ms:contentKeyID: 48547481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 17e8bd561858c8cb1eeb9bf84f6fc636a37f812b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875066"
---
# <a name="workspace-object-dao"></a>Objeto Workspace (DAO)

**Se aplica a**: Access 2013, Office 2013

Un objeto **Workspace** define una sesión con nombre para un usuario. Contiene bases de datos abiertas y proporciona mecanismos para transacciones simultáneas y, en áreas de trabajo de Microsoft Access, compatibilidad con grupos de trabajo seguros.

## <a name="remarks"></a>Observaciones

Un **Workspace** es un objeto no persistente que define cómo interactúa la aplicación con los datos usando el motor de base de datos de Microsoft Access. Use el objeto **Workspace** para administrar la sesión actual o iniciar una sesión adicional. En una sesión, puede abrir varias bases de datos o conexiones y administrar transacciones. Por ejemplo, puede:

- Usar las propiedades **Name**, **UserName** y **Type** para establecer una sesión con nombre. La sesión crea un ámbito en el que se pueden abrir varias bases de datos y realizar una instancia de transacciones anidadas.

- Usar el método **Close** para finalizar la sesión.

- Usar el método **OpenDatabase** para abrir una o más bases de datos existentes en un **área de trabajo**.

- Usar los métodos **BeginTrans**, **CommitTrans** y **Rollback** para administrar el procesamiento de transacciones anidadas dentro de un **área de trabajo** y usar varios objetos **Workspace** para llevar a cabo varias transacciones simultáneas y superpuestas.

Cuando en primer lugar, consulte o usar un objeto **Workspace** , se crea automáticamente el área de trabajo de forma predeterminada, DBEngine.Workspaces(0). Los valores de las propiedades **Name** y **UserName** del área de trabajo predeterminada son "\#área de trabajo predeterminada\#" y "Admin", respectivamente. Si está habilitada la seguridad, la configuración de la propiedad **UserName** es el nombre del usuario que ha iniciado la sesión.

Cuando se usan transacciones, se ven afectadas todas las bases de datos del **área de trabajo** especificada aunque se abran varios objetos **Database** en el **área de trabajo**. Por ejemplo, si usa un método **BeginTrans**, actualiza varios registros de una base de datos y luego elimina registros de otra base de datos, pero después usa el método **Rollback**, tanto las operaciones de actualización como de eliminación se cancelan y se deshacen. Puede crear más objetos **Workspace** para administrar las transacciones de forma independiente entre los objetos **Database**.

Puede crear objetos **Workspace** con el método **CreateWorkspace**. Después de crear un nuevo objeto **Workspace**, debe anexarlo a la colección **Workspaces** si necesita hacer referencia a él desde la colección **Workspaces**.

Puede usar un objeto **Workspace** recién creado sin anexarlo a la colección **Workspaces**. Sin embargo, debe hacer referencia a él por la variable de objeto que le asignó.

Para hacer referencia a un objeto **Workspace** de una colección por su número ordinal o por su propiedad **Name**, use cualquiera de las formas sintácticas siguientes:

**DBEngine**. **Áreas de trabajo** (0)

**DBEngine**. **Áreas de trabajo** ("nombre")

**DBEngine**. **Áreas de trabajo** \! \[nombre\]

> [!NOTE]
> [!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.


## <a name="example"></a>Ejemplo

En este ejemplo, se crea un nuevo objeto Workspace de Microsoft Access y se lo anexa a la colección **Workspaces**. Luego se enumeran las colecciones **Workspaces** y la colección **Properties** del objeto **Workspace**.

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

En este ejemplo, se usa el método **CreateWorkspace** para crear un área de trabajo de Microsoft Access. A continuación, se enumeran las propiedades del área de trabajo.

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

En el ejemplo siguiente, se muestra cómo usar una transacción en un área de trabajo de objetos de acceso a datos (DAO).

**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).


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
