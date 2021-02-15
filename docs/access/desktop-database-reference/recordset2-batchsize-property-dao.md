---
title: Recordset2.BatchSize (DAO)
TOCTitle: BatchSize Property
ms:assetid: fa7f12f6-36c8-5aad-31d2-668cfe46f9f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837054(v=office.15)
ms:contentKeyID: 48548846
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f615823f99e2fdaa50a051d89a90c8f85a6ec841
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307472"
---
# <a name="recordset2batchsize-property-dao"></a><span data-ttu-id="f5058-102">Recordset2.BatchSize (DAO)</span><span class="sxs-lookup"><span data-stu-id="f5058-102">Recordset2.BatchSize property (DAO)</span></span>


<span data-ttu-id="f5058-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5058-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="f5058-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5058-104">Syntax</span></span>

<span data-ttu-id="f5058-105">*expresión* . BatchSize</span><span class="sxs-lookup"><span data-stu-id="f5058-105">*expression* .BatchSize</span></span>

<span data-ttu-id="f5058-106">*expresión* Variable que representa un objeto **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="f5058-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5058-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f5058-107">Remarks</span></span>

<span data-ttu-id="f5058-p101">La propiedad **BatchSize** determina el tamaño del lote utilizado para enviar instrucciones al servidor en una actualización por lotes. El valor de la propiedad determina el número de instrucciones enviadas al servidor en un búfer de comando. De forma predeterminada, se envían al servidor 15 instrucciones en cada lote. Esta propiedad se puede cambiar en cualquier momento. Si un servidor de base de datos no admite lotes de instrucciones, puede establecer esta propiedad en 1, lo que produce que cada instrucción se envíe por separado.</span><span class="sxs-lookup"><span data-stu-id="f5058-p101">The **BatchSize** property determines the batch size used when sending statements to the server in a batch update. The value of the property determines the number of statements sent to the server in one command buffer. By default, 15 statements are sent to the server in each batch. This property can be changed at any time. If a database server doesn't support statement batching, you can set this property to 1, causing each statement to be sent separately.</span></span>

## <a name="example"></a><span data-ttu-id="f5058-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f5058-113">Example</span></span>

<span data-ttu-id="f5058-114">En este ejemplo, se usan las propiedades **BatchSize** y **UpdateOptions** para controlar aspectos de cualquier actualización por lotes para el objeto Recordset especificado.</span><span class="sxs-lookup"><span data-stu-id="f5058-114">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified Recordset object.</span></span>

```vb
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 
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

