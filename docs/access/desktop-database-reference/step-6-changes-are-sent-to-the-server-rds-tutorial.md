---
title: 'Paso 6: Los cambios se envían al servidor (Tutorial de RDS)'
TOCTitle: 'Step 6: Changes are Sent to the Server (RDS Tutorial)'
ms:assetid: c5915d89-77b6-bb3f-a962-49378160751f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249965(v=office.15)
ms:contentKeyID: 48547611
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9f75e5215e3e3d79363ab7110f7c16bcacf3cbb
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998997"
---
# <a name="step-6-changes-are-sent-to-the-server-rds-tutorial"></a><span data-ttu-id="11a72-102">Paso 6: Los cambios se envían al servidor (Tutorial de RDS)</span><span class="sxs-lookup"><span data-stu-id="11a72-102">Step 6: Changes are sent to the server (RDS Tutorial)</span></span>

<span data-ttu-id="11a72-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="11a72-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="11a72-104">Si se modifica el objeto **Recordset**, cualquier cambio (es decir, filas que se agregan, modifican o eliminan) se puede enviar de nuevo al servidor.</span><span class="sxs-lookup"><span data-stu-id="11a72-104">If the **Recordset** object is edited, any changes (that is, rows that are added, changed, or deleted) can be sent back to the server.</span></span>

<span data-ttu-id="11a72-105">El comportamiento predeterminado de RDS se puede invocar implícitamente con objetos ADO y el proveedor de servicios remotos de Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="11a72-105">The default behavior of RDS can be invoked implicitly with ADO objects and the Microsoft OLE DB Remoting Provider.</span></span> <span data-ttu-id="11a72-106">Las consultas pueden devolver **conjuntos de registros**y editado **los conjuntos de registros** pueden actualizar el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="11a72-106">Queries can return **Recordsets**, and edited **Recordsets** can update the data source.</span></span> <span data-ttu-id="11a72-107">En este tutorial no utiliza RDS con objetos ADO, pero este es el aspecto que tendría si lo hiciera:</span><span class="sxs-lookup"><span data-stu-id="11a72-107">This tutorial does not invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

<span data-ttu-id="11a72-108">**Parte A**</span><span class="sxs-lookup"><span data-stu-id="11a72-108">**Part A**</span></span> 

<span data-ttu-id="11a72-109">Suponga para este caso que sólo ha utilizado el [RDS. DataControl](datacontrol-object-rds.md) y que un objeto **Recordset** está ahora asociado con el **RDS. DataControl**.</span><span class="sxs-lookup"><span data-stu-id="11a72-109">Assume for this case that you have only used the [RDS.DataControl](datacontrol-object-rds.md) and that a **Recordset** object is now associated with the **RDS.DataControl**.</span></span> <span data-ttu-id="11a72-110">El método [SubmitChanges](submitchanges-method-rds.md) actualiza el origen de datos con los cambios del objeto **Recordset** si las propiedades [Server](server-property-rds.md) y [Connect](connect-property-rds.md) están establecidas.</span><span class="sxs-lookup"><span data-stu-id="11a72-110">The [SubmitChanges](submitchanges-method-rds.md) method updates the data source with any changes to the **Recordset** object if the [Server](server-property-rds.md) and [Connect](connect-property-rds.md) properties are still set.</span></span>

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

<span data-ttu-id="11a72-111">**Parte B**</span><span class="sxs-lookup"><span data-stu-id="11a72-111">**Part B**</span></span> 

<span data-ttu-id="11a72-112">Como alternativa, podría actualizar el servidor con el objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md) , especificando una conexión y un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="11a72-112">Alternatively, you could update the server with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, specifying a connection and a **Recordset** object.</span></span>

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

<span data-ttu-id="11a72-113">**Éste es el final del tutorial.**</span><span class="sxs-lookup"><span data-stu-id="11a72-113">**This is the end of the tutorial.**</span></span>

