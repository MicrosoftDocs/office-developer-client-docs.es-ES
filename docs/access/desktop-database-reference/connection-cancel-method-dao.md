---
title: Connection.Cancel Method (DAO)
TOCTitle: Cancel Method
ms:assetid: 43ad7b64-823d-3fac-e4d4-5e9514f60011
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192953(v=office.15)
ms:contentKeyID: 48544509
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 565dff4e1592ef431aad0c7cb1daa581520f73ec
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486648"
---
# <a name="connectioncancel-method-dao"></a><span data-ttu-id="76c33-102">Connection.Cancel Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="76c33-102">Connection.Cancel Method (DAO)</span></span>

<span data-ttu-id="76c33-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="76c33-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="76c33-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76c33-104">Syntax</span></span>

<span data-ttu-id="76c33-105">*expresión* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="76c33-105">*expression* .Cancel</span></span>

<span data-ttu-id="76c33-106">*expresión* Variable que representa un objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="76c33-106">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="76c33-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="76c33-107">Remarks</span></span>

<span data-ttu-id="76c33-108">Utilice el método **Cancel** para finalizar la ejecución de una llamada al método **Execute** u **OpenConnection** asincrónica (es decir, el método se abrió con la opción dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="76c33-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="76c33-109">**Cancel** devolverá un error en tiempo de ejecución si no se utilizó dbRunAsync en el método que está intentando terminar.</span><span class="sxs-lookup"><span data-stu-id="76c33-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

<span data-ttu-id="76c33-110">Se producirá un error si, después de una llamada al método **Cancel**, intenta hacer referencia al objeto que debería haber sido creado por una llamada a **OpenConnection** asincrónica (es decir, el objeto **Connection** desde el que llamó al método **Cancel**).</span><span class="sxs-lookup"><span data-stu-id="76c33-110">An error will occur if, following a **Cancel** method call, you try to reference the object that would have been created by an asynchronous **OpenConnection** call (that is, the **Connection** object from which you called the **Cancel** method).</span></span>

## <a name="example"></a><span data-ttu-id="76c33-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="76c33-111">Example</span></span>

<span data-ttu-id="76c33-112">En este ejemplo se utilizan la propiedad **StillExecuting** y el método **Cancel** para abrir de forma asincrónica un objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="76c33-112">This example uses the **StillExecuting** property and the **Cancel** method to asynchronously open a **Connection** object.</span></span>

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
