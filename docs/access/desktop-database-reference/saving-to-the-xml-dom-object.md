---
title: Guardar en el objeto XML DOM
TOCTitle: Saving to the XML DOM Object
ms:assetid: 3c61fc30-9862-347b-c215-08597eccfead
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249160(v=office.15)
ms:contentKeyID: 48544318
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bb85d34da052dda3e2bea5cead7ee4113ac2c12
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483322"
---
# <a name="saving-to-the-xml-dom-object"></a>Guardar en el objeto XML DOM


**Se aplica a**: Access 2013 | Office 2013

## <a name="saving-to-the-xml-dom-object"></a>Guardar en el objeto XML DOM

Un **conjunto de registros** se puede guardar en formato XML en una instancia de un objeto DOM de MSXML, como se muestra en el código siguiente de Visual Basic:

```vb 
 
Dim xDOM As New MSXML.DOMDocument 
Dim rsXML As New ADODB.Recordset 
Dim sSQL As String, sConn As String 
     
sSQL = "SELECT customerid, companyname, contactname FROM customers" 
sConn="Provider=Microsoft.Jet.OLEDB.4.0;Data Source=D:\Program Files" & _ 
        "\Common Files\System\msadc\samples\NWind.mdb" 
rsXML.Open sSQL, sConn 
rsXML.Save xDOM, adPersistADO   'Save Recordset directly into a DOM tree. 
... 
```

