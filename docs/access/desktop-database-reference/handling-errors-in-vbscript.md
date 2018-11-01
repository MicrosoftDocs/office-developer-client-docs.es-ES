---
title: Tratar errores en VBScript
TOCTitle: Handling Errors in VBScript
ms:assetid: df8f96d5-b917-ddac-d274-6345b2499bf1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250135(v=office.15)
ms:contentKeyID: 48548222
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc7f915b32c9a6bec79afe5de554bf7863030c03
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869802"
---
# <a name="handling-errors-in-vbscript"></a><span data-ttu-id="589c6-102">Tratar errores en VBScript</span><span class="sxs-lookup"><span data-stu-id="589c6-102">Handling Errors in VBScript</span></span>


<span data-ttu-id="589c6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="589c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="589c6-104">Hay poca diferencia entre los métodos utilizados en Visual Basic y los usados con VBScript.</span><span class="sxs-lookup"><span data-stu-id="589c6-104">There is little difference between the methods used in Visual Basic and those used with VBScript.</span></span> <span data-ttu-id="589c6-105">La principal diferencia es que VBScript no admite el concepto de tratamiento de errores por continuación de la ejecución en una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="589c6-105">The primary difference is that VBScript does not support the concept of error handling by continuing execution at a label.</span></span> <span data-ttu-id="589c6-106">En otras palabras, no puede utilizar On Error GoTo en VBScript.</span><span class="sxs-lookup"><span data-stu-id="589c6-106">In other words, you cannot use On Error GoTo in VBScript.</span></span> <span data-ttu-id="589c6-107">En su lugar, use en VBScript.</span><span class="sxs-lookup"><span data-stu-id="589c6-107">Instead, use in VBScript.</span></span> <span data-ttu-id="589c6-108">En su lugar, use On Error Resume Next y, a continuación, revise **Err.Number** y la propiedad **Count** de la colección **Errors** , tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="589c6-108">Instead, use On Error Resume Next and then check both **Err.Number** and the **Count** property of the **Errors** collection, as shown in the following example:</span></span>

```vb 
 
<!-- BeginErrorExampleVBS --> 
<HTML> 
<HEAD> 
<META NAME="GENERATOR" Content="Microsoft Visual Studio 6.0"> 
<TITLE>Error Handling example (VBScript)</TITLE> 
</HEAD> 
<BODY> 
 
<h1>Error Handling example (VBScript)</h1> 
 
<% 
 Dim errLoop 
 Dim strError 
 
 On Error Resume Next 
 
 ' Intentionally trigger an error. 
 Set cnn1 = Server.CreateObject("ADODB.Connection") 
 cnn1.Open "nothing" 
 
 If cnn1.Errors.Count > 0 Then 
 ' Enumerate Errors collection and display 
 ' properties of each Error object. 
 For Each errLoop In cnn1.Errors 
 strError = "Error #" & errLoop.Number & "<br>" & _ 
 " " & errLoop.Description & "<br>" & _ 
 " (Source: " & errLoop.Source & ")" & "<br>" & _ 
 " (SQL State: " & errLoop.SQLState & ")" & "<br>" & _ 
 " (NativeError: " & errLoop.NativeError & ")" & "<br>" 
 If errLoop.HelpFile = "" Then 
 strError = strError & _ 
 " No Help file available" & _ 
 "<br><br>" 
 Else 
 strError = strError & _ 
 " (HelpFile: " & errLoop.HelpFile & ")" & "<br>" & _ 
 " (HelpContext: " & errLoop.HelpContext & ")" & _ 
 "<br><br>" 
 End If 
 Response.Write ("<p>" & strError & "</p>") 
 Next 
 End If 
%> 
 
</BODY> 
</HTML> 
<!-- EndErrorExampleVBS --> 
```

