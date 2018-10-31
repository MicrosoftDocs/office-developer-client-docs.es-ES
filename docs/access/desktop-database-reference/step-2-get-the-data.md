---
title: 'Paso 2: Obtener los datos'
TOCTitle: 'Step 2: Get the Data'
ms:assetid: e6be8801-6e57-d287-e8d2-348963706edc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250171(v=office.15)
ms:contentKeyID: 48548387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 80dae05dc691343b3c89ce8fd3ccfe72b776984c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860332"
---
# <a name="step-2-get-the-data"></a>Paso 2: Obtener los datos


**Se aplica a**: Access 2013 | Office 2013

## <a name="step-2-get-the-data"></a>Paso 2: Obtener los datos

En este paso, escribirá el código para abrir un objeto **Recordset** de ADO y prepararlo para su envío al cliente. Abra el archivo XMLResponse.asp con un editor de texto, tal como el Bloc de notas de Windows, e inserte el código siguiente:

```vb 
 
<%@ language="VBScript" %> 
 
<!-- #include file='adovbs.inc' --> 
 
<% 
  Dim strSQL, strCon 
  Dim adoRec  
  Dim adoCon  
  Dim xmlDoc  
 
  ' You will need to change "slqServer" below to the name of the SQL  
  ' server machine to which you want to connect. 
  strCon = "Provider=sqloledb;Data Source=sqlServer;Initial Catalog=Pubs;Integrated Security=SSPI;" 
  Set adoCon = server.createObject("ADODB.Connection") 
  adoCon.Open strCon 
 
  strSQL = "SELECT Title, Price FROM Titles ORDER BY Price" 
  Set adoRec = Server.CreateObject("ADODB.Recordset") 
  adoRec.Open strSQL, adoCon, adOpenStatic, adLockOptimistic, adCmdText 
```

Asegúrese de cambiar el valor del parámetro origen de datos en el parámetro en strCon en el nombre de su equipo con Microsoft SQL Server.

Mantenga el archivo abierto y vaya al paso siguiente.

### <a name="next-step"></a>Paso siguiente

[Paso 3: Enviar los datos](step-3-send-the-data.md)

