---
title: Connection.StillExecuting Property (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 0121f98a-cc23-5b5e-9a75-28307404a9a3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844743(v=office.15)
ms:contentKeyID: 48542927
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7dfb5dc1abee81e24de7e6cfcd23bd298e684c10
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484061"
---
# <a name="connectionstillexecuting-property-dao"></a><span data-ttu-id="8bcee-102">Connection.StillExecuting Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="8bcee-102">Connection.StillExecuting Property (DAO)</span></span>

<span data-ttu-id="8bcee-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8bcee-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="8bcee-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bcee-104">Syntax</span></span>

<span data-ttu-id="8bcee-105">*expresión* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="8bcee-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="8bcee-106">*expresión* Variable que representa un objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="8bcee-106">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bcee-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8bcee-107">Remarks</span></span>

<span data-ttu-id="8bcee-p101">Utilice la propiedad **StillExecuting** para determinar si el método asincrónico **Execute** o **OpenConnection** invocado más recientemente (es decir, un método ejecutado con la opción **dbRunAsync**) se ha completado. Mientras la propiedad **StillExecuting** esté establecida en **True**, no se puede tener acceso a ningún objeto devuelto.</span><span class="sxs-lookup"><span data-stu-id="8bcee-p101">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete. While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="8bcee-p102">Una vez que la propiedad **StillExecuting** devuelva **False**, seguido de la llamada **OpenConnection** que devuelve el objeto asociado **Connection**, se puede hacer referencia al objeto. Mientras que **StillExecuting** permanezca establecida en **True**, no se puede hacer referencia al objeto, aparte de leer la propiedad **StillExecuting**.</span><span class="sxs-lookup"><span data-stu-id="8bcee-p102">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced. So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="8bcee-112">Use el método **[Cancel](connection-cancel-method-dao.md)** para finalizar la ejecución de una tarea en curso.</span><span class="sxs-lookup"><span data-stu-id="8bcee-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

## <a name="example"></a><span data-ttu-id="8bcee-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8bcee-113">Example</span></span>

<span data-ttu-id="8bcee-114">En este ejemplo se utilizan la propiedad **StillExecuting** y el método **Cancel** para abrir de forma asincrónica un objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="8bcee-114">This example uses the **StillExecuting** property and the **Cancel** method to asynchronously open a **Connection** object.</span></span>

```vb
    Sub CancelConnectionX() 
     
     Dim wrkMain As Workspace 
     Dim conMain As Connection 
     Dim sngTime As Single 
     
     Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
     "admin", "", dbUseODBC) 
     ' Open the connection asynchronously. 
     
     ' Note: The DSN referenced below must be configured to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set conMain = wrkMain.OpenConnection("Publishers", _ 
     dbDriverNoPrompt + dbRunAsync, False, _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     sngTime = Timer 
     
     ' Wait five seconds. 
     Do While Timer - sngTime < 5 
     Loop 
     
     ' If the connection has not been made, ask the user 
     ' if she wants to keep waiting. If she does not, cancel 
     ' the connection and exit the procedure. 
     Do While conMain.StillExecuting 
     
     If MsgBox("No connection yet--keep waiting?", _ 
     vbYesNo) = vbNo Then 
     conMain.Cancel 
     MsgBox "Connection cancelled!" 
     wrkMain.Close 
     Exit Sub 
     End If 
     
     Loop 
     
     With conMain 
     ' Use the Connection object conMain. 
     .Close 
     End With 
     
     wrkMain.Close 
     
    End Sub
```