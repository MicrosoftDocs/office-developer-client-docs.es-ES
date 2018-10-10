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
# <a name="step-4-receive-and-display-the-data"></a>Paso 4: Recibir y mostrar los datos


**Se aplica a**: Access 2013 | Office 2013

## <a name="step-4-receive-and-display-the-data"></a>Paso 4: Recibir y mostrar los datos

En este paso, creará un archivo HTML con un objeto [ RDS.DataControl ](datacontrol-object-rds.md) incrustado que apunta al archivo XMLResponse.asp para obtener el objeto **Recordset**. Abra default.htm con un editor de texto (como el Bloc de notas de Windows) y agregue el código siguiente. Sustituya "sqlserver" en la dirección URL por el nombre de su equipo servidor.

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

Cierre el archivo default.htm y guárdelo en la misma carpeta donde guardó XMLResponse.asp. Uso de Internet Explorer 4.0 o posterior, abra la dirección URL https://*sqlserver*/XMLPersist/default.htm y observe los resultados. Los datos se muestran en una tabla DHTML enlazada. Ahora, abra la dirección URL https://*sqlserver*/XMLPersist/XMLResponse.asp y observe los resultados. Aparecerá el XML.

