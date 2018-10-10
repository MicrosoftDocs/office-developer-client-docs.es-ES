---
title: Recordset.UpdateOptions Property (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 14ab955d-1c5a-dc76-8dbf-dbca49816bc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845468(v=office.15)
ms:contentKeyID: 48543391
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101185
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 065ca41d46f50911835d79989e39636b62b30b97
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485294"
---
# <a name="recordsetupdateoptions-property-dao"></a><span data-ttu-id="9b0ae-102">Recordset.UpdateOptions Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="9b0ae-102">Recordset.UpdateOptions Property (DAO)</span></span>


<span data-ttu-id="9b0ae-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b0ae-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="9b0ae-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b0ae-104">Syntax</span></span>

<span data-ttu-id="9b0ae-105">*expresión* . UpdateOptions</span><span class="sxs-lookup"><span data-stu-id="9b0ae-105">*expression* .UpdateOptions</span></span>

<span data-ttu-id="9b0ae-106">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="9b0ae-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b0ae-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b0ae-107">Remarks</span></span>

<span data-ttu-id="9b0ae-108">Cuando se ejecuta **[Update](recordset-update-method-dao.md)** en modo por lotes, DAO y la biblioteca de cursores por lotes cliente crean una serie de instrucciones SQL UPDATE para realizar los cambios necesarios.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-108">When a batch-mode **[Update](recordset-update-method-dao.md)** is executed, DAO and the client batch cursor library create a series of SQL UPDATE statements to make the needed changes.</span></span> <span data-ttu-id="9b0ae-109">Se crea una cláusula SQL WHERE para cada actualización para aislar los registros marcados como modificados por la propiedad **[RecordStatus](recordset-recordstatus-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-109">An SQL WHERE clause is created for each update to isolate the records that are marked as changed by the **[RecordStatus](recordset-recordstatus-property-dao.md)** property.</span></span> <span data-ttu-id="9b0ae-110">Como algunos servidores remotos usan desencadenadores u otras formas para aplicar la integridad referencial, con frecuencia es importante limitar la actualización de los campos solo a los afectados por el cambio.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-110">Because some remote servers use triggers or other ways to enforce referential integrity, is it often important to limit the fields being updated to just those affected by the change.</span></span> 

<span data-ttu-id="9b0ae-111">Para ello, establezca la propiedad **UpdateOptions** en una de las siguientes constantes **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** o **dbCriteriaTimeStamp**.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-111">To do this, set the **UpdateOptions** property to one of the constants **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols**, or **dbCriteriaTimeStamp**.</span></span> <span data-ttu-id="9b0ae-112">De esta forma, solo se ejecuta la cantidad mínima total de código desencadenador.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-112">This way, only the absolute minimum amount of trigger code is executed.</span></span> <span data-ttu-id="9b0ae-113">Como resultado, la operación de actualización se ejecuta con más rapidez y con menos errores potenciales.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-113">As a result, the update operation is executed more quickly, and with fewer potential errors.</span></span>

<span data-ttu-id="9b0ae-p103">También puede concatenar cualquiera de las constantes **dbCriteriaDeleteInsert** o **dbCriteriaUpdate** para determinar si debe utilizar un conjunto de instrucciones SQL DELETE e INSERT o una instrucción SQL UPDATE para cada actualización cuando se devuelven modificaciones por lotes al servidor. En el primer caso, se requieren dos operaciones distintas para actualizar el registro. En algunos casos, sobre todo cuando el sistema remoto implementa los desencadenadores DELETE, INSERT y UPDATE, al elegir el valor correcto de la propiedad **UpdateOptions** se puede afectar significativamente en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-p103">You can also concatenate either of the constants **dbCriteriaDeleteInsert** or **dbCriteriaUpdate** to determine whether to use a set of SQL DELETE and INSERT statements or an SQL UPDATE statement for each update when sending batched modifications back to the server. In the former case, two separate operations are required to update the record. In some cases, especially where the remote system implements DELETE, INSERT, and UPDATE triggers, choosing the correct **UpdateOptions** property setting can significantly impact performance.</span></span>

<span data-ttu-id="9b0ae-117">Si no especifica ninguna de las constantes, se utilizarán **dbCriteriaUpdate** y **dbCriteriaKey**.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-117">If you don't specify any constants, **dbCriteriaUpdate** and **dbCriteriaKey** will be used.</span></span>

<span data-ttu-id="9b0ae-118">Los registros nuevos agregados generarán siempre instrucciones INSERT y los registros eliminados generarán siempre instrucciones DELETE, por lo que esta propiedad sólo se aplica a la forma en que la biblioteca de cursores actualiza los registros modificados.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-118">Newly added records will always generate INSERT statements and deleted records will always generate DELETE statements, so this property only applies to how the cursor library updates modified records.</span></span>

## <a name="example"></a><span data-ttu-id="9b0ae-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b0ae-119">Example</span></span>

<span data-ttu-id="9b0ae-120">En este ejemplo se usan las propiedades **BatchSize** y **UpdateOptions** para controlar aspectos de una actualización por lotes para el objeto **Recordset** especificado.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-120">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified **Recordset** object.</span></span>

```vb 
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Increase the number of statements sent to the server 
 ' during a single batch update, thereby reducing the 
 ' number of times an update would have to access the 
 ' server. 
 .BatchSize = 25 
 
 ' Change the UpdateOptions property so that the WHERE 
 ' clause of any batched statements going to the server 
 ' will include any updated columns in addition to the 
 ' key column(s). Also, any modifications to records 
 ' will be made by deleting the original record 
 ' and adding a modified version rather than just 
 ' modifying the original record. 
 .UpdateOptions = dbCriteriaModValues + _ 
 dbCriteriaDeleteInsert 
 
 ' Engage in batch updating using the new settings 
 ' above. 
 ' ... 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

