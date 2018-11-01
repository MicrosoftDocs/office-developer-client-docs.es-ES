---
title: Workspace.BeginTrans Method (DAO)
TOCTitle: BeginTrans Method
ms:assetid: aa7c3bf8-fb08-9360-5998-4bf3f721ecbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821457(v=office.15)
ms:contentKeyID: 48546948
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 850868a3a5d9dd0cfda2b2f365e05004fc4b2ffd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872629"
---
# <a name="workspacebegintrans-method-dao"></a><span data-ttu-id="76470-102">Workspace.BeginTrans Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="76470-102">Workspace.BeginTrans Method (DAO)</span></span>

<span data-ttu-id="76470-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="76470-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="76470-p101">Comienza una nueva transacción **Database** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="76470-p101">Begins a new transaction. Read/write **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="76470-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76470-106">Syntax</span></span>

<span data-ttu-id="76470-107">*expresión* . BeginTrans</span><span class="sxs-lookup"><span data-stu-id="76470-107">*expression* .BeginTrans</span></span>

<span data-ttu-id="76470-108">*expresión* Variable que representa un objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="76470-108">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="76470-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76470-109">Remarks</span></span>

<span data-ttu-id="76470-p102">Los métodos de transacción **BeginTrans**, **CommitTrans** y **Rollback** dirigen el procesamiento de las transacciones durante una sesión definida por un objeto **Workspace**. Utiliza estos métodos con un objeto **Workspace** cuando desea tratar una serie de cambios realizados en las bases de datos en una sesión como una sola unidad.</span><span class="sxs-lookup"><span data-stu-id="76470-p102">The transaction methods **BeginTrans**, **CommitTrans**, and **Rollback** manage transaction processing during a session defined by a **Workspace** object. You use these methods with a **Workspace** object when you want to treat a series of changes made to the databases in a session as one unit.</span></span>

<span data-ttu-id="76470-p103">En general, las transacciones se utilizan para mantener la integridad de los datos cuando debe actualizar registros en dos o más tablas y asegurarse de que se han completado los cambios (se han aplicado) en todas las tablas o en ninguna (se han deshecho). Por ejemplo, si ha transferido dinero de una cuenta a otra, debe restar una cantidad de otra y sumar la cantidad a otra. Si alguna de las actualizaciones no se realiza correctamente, las cuentas ya no están equilibradas. Utilice el método **BeginTrans** antes de actualizar el primer registro y, luego, si no se realiza correctamente cualquier actualización posterior, puede utilizar el método **Rollback** para deshacer todas las actualizaciones. Utilice el método **CommitTrans** después de actualizar correctamente el último registro.</span><span class="sxs-lookup"><span data-stu-id="76470-p103">Typically, you use transactions to maintain the integrity of your data when you must both update records in two or more tables and ensure changes are completed (committed) in all tables or none at all (rolled back). For example, if you transfer money from one account to another, you might subtract an amount from one and add the amount to another. If either update fails, the accounts no longer balance. Use the **BeginTrans** method before updating the first record, and then, if any subsequent update fails, you can use the **Rollback** method to undo all of the updates. Use the **CommitTrans** method after you successfully update the last record.</span></span>

> [!NOTE]
> <span data-ttu-id="76470-p104">[!NOTA] Dentro de un objeto **Workspace**, las transacciones son siempre globales para **Workspace** y no están limitadas a un único objeto **Connection** o **Database**. Si realiza operaciones en varias conexiones o bases de datos dentro de una transacción de **Workspace**, la resolución de la transacción (es decir, el uso del método **CommitTrans** o **Rollback**) afecta a todas las operaciones de todas las conexiones y bases de datos incluidos en esta área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="76470-p104">Within one **Workspace** object, transactions are always global to the **Workspace** and aren't limited to only one **Connection** or **Database** object. If you perform operations on more than one connection or database within a **Workspace** transaction, resolving the transaction (that is, using the **CommitTrans** or **Rollback** method) affects all operations on all connections and databases within that workspace.</span></span>

<span data-ttu-id="76470-p105">Tras utilizar **CommitTrans**, no puede deshacer los cambios realizados durante esta transacción a menos que la transacción esté anidada dentro de otra transacción que, a su vez, se haya deshecho. Si anida transacciones, debe resolver la transacción activa antes de poder resolver una transacción en un nivel de anidamiento superior.</span><span class="sxs-lookup"><span data-stu-id="76470-p105">After you use **CommitTrans**, you can't undo changes made during that transaction unless the transaction is nested within another transaction that is itself rolled back. If you nest transactions, you must resolve the current transaction before you can resolve a transaction at a higher level of nesting.</span></span>

<span data-ttu-id="76470-121">Si desea tener transacciones simultáneas con ámbitos superpuestos y no anidados, debe crear objetos **Workspace** adicionales para contener las transacciones simultáneas.</span><span class="sxs-lookup"><span data-stu-id="76470-121">If you want to have simultaneous transactions with overlapping, non-nested scopes, you can create additional **Workspace** objects to contain the concurrent transactions.</span></span>

<span data-ttu-id="76470-122">Si cierra un objeto **Workspace** sin resolver las transacciones pendientes, las transacciones se deshacen automáticamente.</span><span class="sxs-lookup"><span data-stu-id="76470-122">If you close a **Workspace** object without resolving any pending transactions, the transactions are automatically rolled back.</span></span>

<span data-ttu-id="76470-123">Si utiliza el método **CommitTrans** o **Rollback** sin utilizar primero el método **BeginTrans**, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="76470-123">If you use the **CommitTrans** or **Rollback** method without first using the **BeginTrans** method, an error occurs.</span></span>

<span data-ttu-id="76470-124">Es posible que algunas bases de datos ISAM usadas en un área de trabajo de Microsoft Access no admitan transacciones, en este caso la propiedad **Transactions** del objeto **Database** o **Recordset** es **False**.</span><span class="sxs-lookup"><span data-stu-id="76470-124">Some ISAM databases used in a Microsoft Access workspace may not support transactions, in which case the **Transactions** property of the **Database** object or **Recordset** object is **False**.</span></span> <span data-ttu-id="76470-125">Para asegurarse de que la base de datos admite transacciones, compruebe el valor de la propiedad **Transactions** del objeto **Database** antes de usar el método **BeginTrans**.</span><span class="sxs-lookup"><span data-stu-id="76470-125">To make sure the database supports transactions, check the value of the **Transactions** property of the **Database** object before using the **BeginTrans** method.</span></span> <span data-ttu-id="76470-126">Si usa un objeto **Recordset** basado en varias bases de datos, compruebe la propiedad **Transactions** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="76470-126">If you are using a **Recordset** object based on more than one database, check the **Transactions** property of the **Recordset** object.</span></span> 

<span data-ttu-id="76470-127">Si un objeto **Recordset** está totalmente basado en tablas del motor de base de datos de Microsoft Access, siempre puede usar transacciones.</span><span class="sxs-lookup"><span data-stu-id="76470-127">If a **Recordset** is based entirely on Microsoft Access database engine tables, you can always use transactions.</span></span> <span data-ttu-id="76470-128">Es posible, no obstante, que los objetos **Recordset** basados en tablas creadas por otros productos de bases de datos no admitan transacciones.</span><span class="sxs-lookup"><span data-stu-id="76470-128">**Recordset** objects based on tables created by other database products, however, may not support transactions.</span></span> <span data-ttu-id="76470-129">Por ejemplo, no puede utilizar transacciones en un objeto **Recordset** basado en una tabla Parados.</span><span class="sxs-lookup"><span data-stu-id="76470-129">For example, you can't use transactions in a **Recordset** based on a Paradox table.</span></span> <span data-ttu-id="76470-130">En este caso, la propiedad **Transactions** es **False**.</span><span class="sxs-lookup"><span data-stu-id="76470-130">In this case, the **Transactions** property is **False**.</span></span> <span data-ttu-id="76470-131">Si el objeto **Database** o **Recordset** no admite transacciones, los métodos se omiten y no se producen errores.</span><span class="sxs-lookup"><span data-stu-id="76470-131">If the **Database** or **Recordset** doesn't support transactions, the methods are ignored and no error occurs.</span></span>

<span data-ttu-id="76470-132">No puede anidar transacciones si tiene acceso a orígenes de datos ODBC a través del motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="76470-132">You can't nest transactions if you are accessing ODBC data sources through the Microsoft Access database engine.</span></span>

<span data-ttu-id="76470-p108">En áreas de trabajo de ODBC, cuando usa **CommitTrans**, es posible que el cursor ya no sea válido. Use el método **Requery** para ver los cambios en **Recordset** o cierre y vuelva a abrir **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="76470-p108">In ODBC workspaces, when you use **CommitTrans** your cursor may no longer be valid. Use the **Requery** method to view the changes in the **Recordset**, or close and re-open the **Recordset**.</span></span>

> [!NOTE]
> - <span data-ttu-id="76470-p109">A menudo, puede mejorar el rendimiento de su aplicación segmentando las operaciones que requieren acceso al disco en bloques de transacciones. Esto guarda en el búfer las operaciones y puede reducir significativamente el número de veces que se tiene acceso a un disco.</span><span class="sxs-lookup"><span data-stu-id="76470-p109">You can often improve the performance of your application by breaking operations that require disk access into transaction blocks. This buffers your operations and may significantly reduce the number of times a disk is accessed.</span></span>
> - <span data-ttu-id="76470-p110">En un área de trabajo de Microsoft Access, las transacciones se registran en un archivo que se guarda en el directorio especificado por la variable de entorno TEMP en la estación de trabajo. Si el archivo de registro de transacciones agota el almacenamiento disponible en la unidad TEMP, el motor de base de datos activa un error en tiempo de ejecución. En ese momento, si utiliza **CommitTrans**, se aplica un número indeterminado de operaciones pero se pierden las operaciones restantes que no se hayan completado y es necesario reiniciar la operación. El uso del método **Rollback** libera el registro de transacciones y deshace todas las operaciones de la transacción.</span><span class="sxs-lookup"><span data-stu-id="76470-p110">In a Microsoft Access workspace, transactions are logged in a file kept in the directory specified by the TEMP environment variable on the workstation. If the transaction log file exhausts the available storage on your TEMP drive, the database engine triggers a run-time error. At this point, if you use **CommitTrans**, an indeterminate number of operations are committed, but the remaining uncompleted operations are lost, and the operation has to be restarted. Using a **Rollback** method releases the transaction log and rolls back all operations in the transaction.</span></span>
> - <span data-ttu-id="76470-141">Cerrar un objeto **Recordset** clon con una transacción pendiente provoca una operación **Rollback** implícita.</span><span class="sxs-lookup"><span data-stu-id="76470-141">Closing a clone **Recordset** within a pending transaction will cause an implicit **Rollback** operation.</span></span>

## <a name="example"></a><span data-ttu-id="76470-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="76470-142">Example</span></span>

<span data-ttu-id="76470-143">En el ejemplo siguiente, se muestra cómo usar una transacción en un área de trabajo de objetos de acceso a datos (DAO).</span><span class="sxs-lookup"><span data-stu-id="76470-143">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="76470-144">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="76470-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
