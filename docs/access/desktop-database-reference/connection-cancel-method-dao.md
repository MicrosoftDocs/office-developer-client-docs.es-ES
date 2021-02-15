---
title: Método Connection.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 43ad7b64-823d-3fac-e4d4-5e9514f60011
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192953(v=office.15)
ms:contentKeyID: 48544509
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a0826a30f22cc46eb6ff9a114dbf02cab1d9f76a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295971"
---
# <a name="connectioncancel-method-dao"></a>Método Connection.Cancel (DAO)

**Se aplica a:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . Cancelar

*expression* Variable que representa un objeto **Connection**.

## <a name="remarks"></a>Comentarios

Use el **método Cancel** para finalizar la ejecución de una llamada asincrónica al método **Execute** o **OpenConnection** (es decir, el método se invocó con la opción dbRunAsync). **Cancel** devolverá un error en tiempo de ejecución si dbRunAsync no se usó en el método que está intentando finalizar.

Se producirá un error si, después de una llamada al método **Cancel**, intenta hacer referencia al objeto que debería haber sido creado por una llamada a **OpenConnection** asincrónica (es decir, el objeto **Connection** desde el que llamó al método **Cancel**).

## <a name="example"></a>Ejemplo

En este ejemplo se utilizan la propiedad **StillExecuting** y el método **Cancel** para abrir de forma asincrónica un objeto **Connection**.

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
