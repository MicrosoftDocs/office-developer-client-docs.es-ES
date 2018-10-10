---
title: Tratar errores en JScript
TOCTitle: Handling Errors in JScript
ms:assetid: 2197b4b9-819f-43ff-3ac6-3823c62b40c6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248993(v=office.15)
ms:contentKeyID: 48543684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f2a2fadb9f7f377782ce7cc7d45820769927b4f0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485456"
---
# <a name="handling-errors-in-jscript"></a>Tratar errores en JScript


**Se aplica a**: Access 2013 | Office 2013

Un código de Microsoft JScript debe comprobar la propiedad **Contar** de la colección **Errors** del objeto **Connection**. Si el valor es mayor que 0, recorra la colección en iteración e imprima los valores como lo haría en cualquier otro lenguaje.

```javascript 
 
<!-- BeginErrorExampleJS --> 
<%@ Language=JScript %> 
<HTML> 
<HEAD> 
<title>Error Handling Example (JScript)</title> 
</HEAD> 
<BODY> 
<h1>Error Handling Example (JScript)</h1> 
<% 
 var cnn1 = Server.CreateObject("ADODB.Connection"); 
 var errLoop = Server.CreateObject("ADODB.Error"); 
 var strError = new String; 
 
 try 
 { 
 // Intentionally trigger an error. 
 cnn1.Open("nothing"); 
 } 
 catch(e) 
 { 
 Response.Write(e.message); 
 } 
%> 
 
</BODY> 
</HTML> 
<!-- EndErrorExampleJS --> 
```

