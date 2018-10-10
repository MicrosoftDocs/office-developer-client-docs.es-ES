---
title: 'Paso 4: Recibir y mostrar los datos'
TOCTitle: 'Step 4: Receive and Display the Data'
ms:assetid: a27cc1d8-0ee0-95a5-ad70-88c454c10485
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249749(v=office.15)
ms:contentKeyID: 48546764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2a447b68b8c0eeb18d18050ba8dbbb6f09786ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486027"
---
# <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="58e28-102">Paso 4: Recibir y mostrar los datos</span><span class="sxs-lookup"><span data-stu-id="58e28-102">Step 4: Receive and Display the Data</span></span>


<span data-ttu-id="58e28-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="58e28-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="58e28-104">Paso 4: Recibir y mostrar los datos</span><span class="sxs-lookup"><span data-stu-id="58e28-104">Step 4: Receive and Display the Data</span></span>

<span data-ttu-id="58e28-p101">En este paso, creará un archivo HTML con un objeto [ RDS.DataControl ](datacontrol-object-rds.md) incrustado que apunta al archivo XMLResponse.asp para obtener el objeto **Recordset**. Abra default.htm con un editor de texto (como el Bloc de notas de Windows) y agregue el código siguiente. Sustituya "sqlserver" en la dirección URL por el nombre de su equipo servidor.</span><span class="sxs-lookup"><span data-stu-id="58e28-p101">In this step you will create an HTML file with an embedded [RDS.DataControl](datacontrol-object-rds.md) object that points at the XMLResponse.asp file to get the **Recordset**. Open default.htm with a text editor, such as Windows Notepad, and add the code below. Replace "sqlserver" in the URL with the name of your server computer.</span></span>

```html 
 
<HTML> 
<HEAD><TITLE>ADO Recordset Persistence Sample</TITLE></HEAD> 
<BODY> 
 
<TABLE DATASRC="#RDC1" border="1"> 
  <TR> 
<TD><SPAN DATAFLD="title"></SPAN></TD> 
<TD><SPAN DATAFLD="price"></SPAN></TD> 
  </TR> 
</TABLE> 

<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="RDC1"> 
   <PARAM NAME="URL" VALUE="XMLResponse.asp"> 
</OBJECT> 
 
</BODY> 
</HTML> 
```

<span data-ttu-id="58e28-108">Cierre el archivo default.htm y guárdelo en la misma carpeta donde guardó XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="58e28-108">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</span></span> <span data-ttu-id="58e28-109">Uso de Internet Explorer 4.0 o posterior, abra la dirección URL https://*sqlserver*/XMLPersist/default.htm y observe los resultados.</span><span class="sxs-lookup"><span data-stu-id="58e28-109">Using Internet Explorer 4.0 or later, open the URL https://*sqlserver*/XMLPersist/default.htm and observe the results.</span></span> <span data-ttu-id="58e28-110">Los datos se muestran en una tabla DHTML enlazada.</span><span class="sxs-lookup"><span data-stu-id="58e28-110">The data is displayed in a bound DHTML table.</span></span> <span data-ttu-id="58e28-111">Ahora, abra la dirección URL https://*sqlserver*/XMLPersist/XMLResponse.asp y observe los resultados.</span><span class="sxs-lookup"><span data-stu-id="58e28-111">Now open the URL https://*sqlserver*/XMLPersist/XMLResponse.asp and observe the results.</span></span> <span data-ttu-id="58e28-112">Aparecerá el XML.</span><span class="sxs-lookup"><span data-stu-id="58e28-112">The XML is displayed.</span></span>

