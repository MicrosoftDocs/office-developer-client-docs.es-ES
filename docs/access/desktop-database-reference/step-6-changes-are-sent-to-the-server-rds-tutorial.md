---
title: 'Paso 6: Los cambios se envían al servidor (Tutorial de RDS)'
TOCTitle: 'Step 6: Changes are Sent to the Server (RDS Tutorial)'
ms:assetid: c5915d89-77b6-bb3f-a962-49378160751f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249965(v=office.15)
ms:contentKeyID: 48547611
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d26ca621ba7102dc0f9c6219ba3a16b28138770f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484807"
---
# <a name="step-6-changes-are-sent-to-the-server-rds-tutorial"></a>Paso 6: Los cambios se envían al servidor (Tutorial de RDS)


**Se aplica a**: Access 2013 | Office 2013

Si se modifica el objeto **Recordset**, cualquier cambio (es decir, filas que se agregan, modifican o eliminan) se puede enviar de nuevo al servidor.


> [!NOTE]
> <P>El comportamiento predeterminado de RDS se puede invocar implícitamente con objetos ADO y con el Proveedor de acceso remoto de OLE DB de Microsoft. Las consultas pueden devolver objetos <STRONG>Recordset</STRONG>, y los <STRONG> conjuntos de registros</STRONG> modificados pueden actualizar el origen de datos. Este tutorial no usa RDS con objetos ADO, pero, en caso de hacerlo, sería del siguiente modo:</P>



```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

**Parte A** 

Suponga para este caso que sólo ha utilizado el [RDS. DataControl](datacontrol-object-rds.md) y que un objeto **Recordset** está ahora asociado con el **RDS. DataControl**. El método [SubmitChanges](submitchanges-method-rds.md) actualiza el origen de datos con los cambios del objeto **Recordset** si las propiedades [Server](server-property-rds.md) y [Connect](connect-property-rds.md) están establecidas.

```vb 
 
Sub RDSTutorial6A() 
Dim DC as New RDS.DataControl 
Dim RS as ADODB.Recordset 
DC.Server = "https://yourServer" 
DC.Connect = "DSN=Pubs" 
DC.SQL = "SELECT * FROM Authors" 
DC.Refresh 
... 
Set RS = DC.Recordset 
 ' Edit the Recordset. 
... 
DC.SubmitChanges 
... 
```

**Parte B** 

Como alternativa, podría actualizar el servidor con el objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md) , especificando una conexión y un objeto **Recordset** .

```vb 
 
Sub RDSTutorial6B() 
Dim DS As New RDS.DataSpace 
Dim RS As ADODB.Recordset 
Dim DC As New RDS.DataControl 
Dim DF As Object 
Dim blnStatus As Boolean 
Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
 ' Edit the Recordset. 
blnStatus = DF.SubmitChanges "DSN=Pubs", RS 
End Sub 
```

**Éste es el final del tutorial.**

