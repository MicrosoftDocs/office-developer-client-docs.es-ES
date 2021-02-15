---
title: Método Workspace.BeginTrans (DAO)
TOCTitle: BeginTrans Method
ms:assetid: aa7c3bf8-fb08-9360-5998-4bf3f721ecbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821457(v=office.15)
ms:contentKeyID: 48546948
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c143d91c3dfe786c3245c2b67768c57379869e75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302551"
---
# <a name="workspacebegintrans-method-dao"></a><span data-ttu-id="2a2cb-102">Método Workspace.BeginTrans (DAO)</span><span class="sxs-lookup"><span data-stu-id="2a2cb-102">Workspace.BeginTrans method (DAO)</span></span>

<span data-ttu-id="2a2cb-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a2cb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2a2cb-104">Inicia una nueva transacción.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-104">Begins a new transaction.</span></span> <span data-ttu-id="2a2cb-105">**Database** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-105">Read/write **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a2cb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a2cb-106">Syntax</span></span>

<span data-ttu-id="2a2cb-107">*expresión* . BeginTrans</span><span class="sxs-lookup"><span data-stu-id="2a2cb-107">*expression* .BeginTrans</span></span>

<span data-ttu-id="2a2cb-108">*expression* Variable que representa un objeto **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-108">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a2cb-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2a2cb-109">Remarks</span></span>

<span data-ttu-id="2a2cb-p102">Los métodos de transacción **BeginTrans**, **CommitTrans** y **Rollback** administran el procesamiento de transacciones durante una sesión definida por un objeto **Workspace**. Estos métodos se utilizan con un objeto **Workspace** cuando se desea tratar un conjunto de cambios realizados en las bases de datos en una sesión como una sola unidad.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-p102">The transaction methods **BeginTrans**, **CommitTrans**, and **Rollback** manage transaction processing during a session defined by a **Workspace** object. You use these methods with a **Workspace** object when you want to treat a series of changes made to the databases in a session as one unit.</span></span>

<span data-ttu-id="2a2cb-p103">Normalmente, se utilizan transacciones para mantener la integridad de los datos cuando es necesario actualizar registros en dos o más tablas y, al mismo tiempo, asegurarse de que los cambios se realizan (se validan) en todas las tablas o en ninguna (se revierten). Por ejemplo, si transfiere dinero de una cuenta a otra, podría restar una cantidad de una cuenta y agregar dicha cantidad a la otra cuenta. Si alguna de las actualizaciones no se realiza correctamente, las cuentas no cuadrarán. Utilice el método **BeginTrans** antes de actualizar el primer registro y, a continuación, si la siguiente actualización produce un error, puede utilizar el método **Rollback** para deshacer todas las actualizaciones. Use el método **CommitTrans** una vez actualizado correctamente el último registro.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-p103">Typically, you use transactions to maintain the integrity of your data when you must both update records in two or more tables and ensure changes are completed (committed) in all tables or none at all (rolled back). For example, if you transfer money from one account to another, you might subtract an amount from one and add the amount to another. If either update fails, the accounts no longer balance. Use the **BeginTrans** method before updating the first record, and then, if any subsequent update fails, you can use the **Rollback** method to undo all of the updates. Use the **CommitTrans** method after you successfully update the last record.</span></span>

> [!NOTE]
> <span data-ttu-id="2a2cb-p104">[!NOTA] Dentro de un objeto **Workspace**, las transacciones son siempre globales con respecto al **Workspace** y no se limitan a un único objeto **Connection** o **Database**. Si realiza operaciones en varias conexiones o bases de datos dentro de una transacción de **Workspace**, la resolución de las transacciones (por ejemplo, mediante el método **CommitTrans** o **Rollback**) afecta a todas las operaciones en todas las conexiones y bases de datos dentro de esa área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-p104">Within one **Workspace** object, transactions are always global to the **Workspace** and aren't limited to only one **Connection** or **Database** object. If you perform operations on more than one connection or database within a **Workspace** transaction, resolving the transaction (that is, using the **CommitTrans** or **Rollback** method) affects all operations on all connections and databases within that workspace.</span></span>

<span data-ttu-id="2a2cb-p105">Después de utilizar **CommitTrans**, no se pueden deshacer los cambios realizados a no ser que la transacción esté anidada dentro de otra transacción que haya sido revertida. Si anida transacciones, debe resolver la transacción actual antes de resolver una transacción situada en un nivel de anidamiento superior.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-p105">After you use **CommitTrans**, you can't undo changes made during that transaction unless the transaction is nested within another transaction that is itself rolled back. If you nest transactions, you must resolve the current transaction before you can resolve a transaction at a higher level of nesting.</span></span>

<span data-ttu-id="2a2cb-121">Si desea realizar transacciones simultáneas con ámbitos superpuestos no anidados, puede crear objetos **Workspace** adicionales que contengan las transacciones simultáneas.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-121">If you want to have simultaneous transactions with overlapping, non-nested scopes, you can create additional **Workspace** objects to contain the concurrent transactions.</span></span>

<span data-ttu-id="2a2cb-122">Si cierra un objeto **Workspace** sin resolver las transacciones pendientes, las transacciones se revierten automáticamente.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-122">If you close a **Workspace** object without resolving any pending transactions, the transactions are automatically rolled back.</span></span>

<span data-ttu-id="2a2cb-123">Si utiliza el método **CommitTrans** o **Rollback** sin usar primero el método **BeginTrans**, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-123">If you use the **CommitTrans** or **Rollback** method without first using the **BeginTrans** method, an error occurs.</span></span>

<span data-ttu-id="2a2cb-124">Es posible que algunas bases de datos ISAM usadas en un área de trabajo de Microsoft Access no admitan transacciones, en cuyo caso la propiedad **Transactions** del objeto **Database** o del objeto **Recordset** es **False**.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-124">Some ISAM databases used in a Microsoft Access workspace may not support transactions, in which case the **Transactions** property of the **Database** object or **Recordset** object is **False**.</span></span> <span data-ttu-id="2a2cb-125">Para asegurarse de que la base de datos admite transacciones, compruebe el valor de la propiedad **Transactions** del objeto **Database** antes de usar el método **BeginTrans**.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-125">To make sure the database supports transactions, check the value of the **Transactions** property of the **Database** object before using the **BeginTrans** method.</span></span> <span data-ttu-id="2a2cb-126">Si usa un objeto **Recordset** basado en varias bases de datos, compruebe la propiedad **Transactions** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-126">If you are using a **Recordset** object based on more than one database, check the **Transactions** property of the **Recordset** object.</span></span> 

<span data-ttu-id="2a2cb-127">Si un objeto **Recordset** se basa íntegramente en tablas del motor de base de datos de Microsoft Access, siempre puede usar transacciones.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-127">If a **Recordset** is based entirely on Microsoft Access database engine tables, you can always use transactions.</span></span> <span data-ttu-id="2a2cb-128">No obstante, es posible que los objetos **Recordset** basados en tablas creadas por otros productos de base de datos no admitan transacciones.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-128">**Recordset** objects based on tables created by other database products, however, may not support transactions.</span></span> <span data-ttu-id="2a2cb-129">Por ejemplo, no puede usar transacciones en un objeto **Recordset** basado en una tabla de Paradox.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-129">For example, you can't use transactions in a **Recordset** based on a Paradox table.</span></span> <span data-ttu-id="2a2cb-130">En este caso, la propiedad **Transactions** es **False**.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-130">In this case, the **Transactions** property is **False**.</span></span> <span data-ttu-id="2a2cb-131">Si los objetos **Database** o **Recordset** no admiten transacciones, los métodos se omiten y no se produce ningún error.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-131">If the **Database** or **Recordset** doesn't support transactions, the methods are ignored and no error occurs.</span></span>

<span data-ttu-id="2a2cb-132">No puede anidar transacciones si tiene acceso a orígenes de datos de ODBC a través del motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-132">You can't nest transactions if you are accessing ODBC data sources through the Microsoft Access database engine.</span></span>

<span data-ttu-id="2a2cb-p108">En áreas de trabajo de ODBC, cuando usa **CommitTrans**, es posible que el cursor ya no sea válido. Use el método **Requery** para ver los cambios en **Recordset**, o bien cierre y vuelva a abrir **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-p108">In ODBC workspaces, when you use **CommitTrans** your cursor may no longer be valid. Use the **Requery** method to view the changes in the **Recordset**, or close and re-open the **Recordset**.</span></span>

> [!NOTE]
> - <span data-ttu-id="2a2cb-p109">A menudo, es posible aumentar el rendimiento de la aplicación dividiendo las transacciones que requieren acceso al disco en bloques de transacciones. De esta forma, las operaciones se almacenan en un búfer y se reduce considerablemente el número de operaciones de acceso al disco.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-p109">You can often improve the performance of your application by breaking operations that require disk access into transaction blocks. This buffers your operations and may significantly reduce the number of times a disk is accessed.</span></span>
> - <span data-ttu-id="2a2cb-p110">En un área de trabajo de Microsoft Access, las transacciones se registran en un archivo almacenado en el directorio especificado por la variable de entorno TEMP en la estación de trabajo. Si el archivo de registro de transacciones utiliza todo el espacio de almacenamiento disponible en la unidad TEMP, el motor de base de datos genera un error en tiempo de ejecución. En este punto, si utiliza **CommitTrans**, se validan un número indeterminado de transacciones, pero las operaciones incompletas restantes se pierden y es necesario reiniciar la operación. Al utilizar el método **Rollback**, se libera el registro de transacciones y se revierten todas las operaciones de la transacción.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-p110">In a Microsoft Access workspace, transactions are logged in a file kept in the directory specified by the TEMP environment variable on the workstation. If the transaction log file exhausts the available storage on your TEMP drive, the database engine triggers a run-time error. At this point, if you use **CommitTrans**, an indeterminate number of operations are committed, but the remaining uncompleted operations are lost, and the operation has to be restarted. Using a **Rollback** method releases the transaction log and rolls back all operations in the transaction.</span></span>
> - <span data-ttu-id="2a2cb-141">Al cerrar una copia del objeto **Recordset** en una transacción pendiente, se genera una operación **Rollback** implícita.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-141">Closing a clone **Recordset** within a pending transaction will cause an implicit **Rollback** operation.</span></span>

## <a name="example"></a><span data-ttu-id="2a2cb-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2a2cb-142">Example</span></span>

<span data-ttu-id="2a2cb-143">En el ejemplo siguiente, se muestra cómo usar una transacción en un área de trabajo de objetos de acceso a datos (DAO).</span><span class="sxs-lookup"><span data-stu-id="2a2cb-143">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="2a2cb-144">**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="2a2cb-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
