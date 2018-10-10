---
title: 'Paso 2: Obtener los datos'
TOCTitle: 'Step 2: Get the Data'
ms:assetid: e6be8801-6e57-d287-e8d2-348963706edc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250171(v=office.15)
ms:contentKeyID: 48548387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e4b93eb3e3679fdbc235f4406b0480ad2597d25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483591"
---
# <a name="step-2-get-the-data"></a><span data-ttu-id="772fd-102">Paso 2: Obtener los datos</span><span class="sxs-lookup"><span data-stu-id="772fd-102">Step 2: Get the Data</span></span>


<span data-ttu-id="772fd-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="772fd-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-2-get-the-data"></a><span data-ttu-id="772fd-104">Paso 2: Obtener los datos</span><span class="sxs-lookup"><span data-stu-id="772fd-104">Step 2: Get the Data</span></span>

<span data-ttu-id="772fd-p101">En este paso, escribirá el código para abrir un objeto **Recordset** de ADO y prepararlo para su envío al cliente. Abra el archivo XMLResponse.asp con un editor de texto, tal como el Bloc de notas de Windows, e inserte el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="772fd-p101">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client. Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

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

<span data-ttu-id="772fd-107">Asegúrese de cambiar el valor del parámetro origen de datos en el parámetro en strCon en el nombre de su equipo con Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="772fd-107">Be sure to change the value of the Data Source parameter in parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

<span data-ttu-id="772fd-108">Mantenga el archivo abierto y vaya al paso siguiente.</span><span class="sxs-lookup"><span data-stu-id="772fd-108">Keep the file open and go on to the next step.</span></span>

<span data-ttu-id="772fd-109">**Siguiente** [Paso 3: enviar los datos](step-3-send-the-data.md)</span><span class="sxs-lookup"><span data-stu-id="772fd-109">**Next** [Step 3: Send the Data](step-3-send-the-data.md)</span></span>

