---
title: Secuencias y persistencia
TOCTitle: Streams and Persistence
ms:assetid: 564fc098-52bf-77d7-9d48-75186483e3fe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249289(v=office.15)
ms:contentKeyID: 48544949
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d47d7bb4d8e9243d48daf4ad7947cef2416d4004
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485774"
---
# <a name="streams-and-persistence"></a>Secuencias y persistencia


**Se aplica a**: Access 2013 | Office 2013

El método [Save](save-method-ado.md) del objeto [Recordset](recordset-object-ado.md) guarda o *persiste* un objeto **Recordset** en un archivo, y el método [Open](open-method-ado-recordset.md) restaura el objeto **Recordset** de ese archivo.

Con ADO 2.5, los métodos **Save** y **Open** también pueden persistir un objeto **Recordset** en un objeto [Stream](stream-object-ado.md). Esta característica es especialmente útil al trabajar con el Servicio de datos remoto (RDS) y páginas Active Server (ASP).

Para obtener más información sobre cómo utilizar la persistencia en páginas ASP, vea la documentación de ASP.

A continuación se describen algunos escenarios que muestran cómo se pueden utilizar los objetos **Stream** y la persistencia.

## <a name="scenario-1"></a>Escenario 1

En este escenario se guarda simplemente un objeto **Recordset** en un archivo y, a continuación, en un objeto **Stream**. A continuación, se abre la secuencia guardada en otro objeto **Recordset**.

```vb 
 
Dim rs1 As ADODB.Recordset 
Dim rs2 As ADODB.Recordset 
Dim stm As ADODB.Stream 
 
Set rs1 = New ADODB.Recordset 
Set rs2 = New ADODB.Recordset 
Set stm = New ADODB.Stream 
 
rs1.Open "SELECT * FROM Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""", adopenStatic, adLockReadOnly, adCmdText 
rs1.Save "c:\myfolder\mysubfolder\myrs.xml", adPersistXML 
rs1.Save stm, adPersistXML 
rs2.Open stm 
```

## <a name="scenario-2"></a>Escenario 2

En este escenario se persiste un objeto **Recordset** en un objeto **Stream** con formato XML. A continuación, se lee el objeto **Stream** en una cadena que se puede examinar, manipular o mostrar.

```vb 
 
Dim rs As ADODB.Recordset 
Dim stm As ADODB.Stream 
Dim strRst As String 
 
Set rs = New ADODB.Recordset 
Set stm = New ADODB.Stream 
 
' Open, save, and close the recordset. 
rs.Open "SELECT * FROM Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""" 
rs.Save stm, adPersistXML 
rs.Close 
Set rs = nothing 
 
' Put saved Recordset into a string variable. 
strRst = stm.ReadText(adReadAll) 
 
' Examine, manipulate, or display the XML data. 
... 
```

## <a name="scenario-3"></a>Escenario 3

En este código de ejemplo se muestra cómo código ASP almacena un objeto **Recordset** como XML directamente en el objeto **Response**:

```vb 
 
... 
<% 
response.ContentType = "text/xml" 
 
' Create and open a Recordset. 
Set rs = Server.CreateObject("ADODB.Recordset") 
rs.Open "select * from Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""" 
 
' Save Recordset directly into output stream. 
rs.Save Response, adPersistXML 
 
' Close Recordset. 
rs.Close 
Set rs = nothing 
%> 
... 
```

## <a name="scenario-4"></a>Escenario 4

En este escenario, código ASP escribe el contenido del objeto **Recordset** con formato ADTG en el cliente. El [Servicio de cursores de Microsoft para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) puede utilizar estos datos para crear un objeto **Recordset** desconectado.

Una nueva propiedad en el objeto [DataControl](datacontrol-object-rds.md) de RDS, [URL](url-property-rds.md), señala la página .asp que genera el objeto **Recordset**. Esto significa que se puede obtener un objeto **Recordset** sin que RDS use el objeto [DataFactory](datafactory-object-rdsserver.md) del servidor o sin que el usuario escriba un objeto de negocio. De este modo, se simplifica considerablemente el modelo de programación de RDS.

Código de servidor, que se denomina https://server/directory/recordset.asp:

```vb 
 
<% 
Dim rs 
Set rs = Server.CreateObject("ADODB.Recordset") 
rs.Open "select au_fname, au_lname, phone from Authors", ""& _ 
 "Provider=sqloledb;Data Source=MyServer;" & _ 
 "Initial Catalog=Pubs;Integrated Security=SSPI;" 
response.ContentType = "multipart/mixed" 
rs.Save response, adPersistADTG 
%> 
```

Código de cliente:

```html 
 
<HTML> 
<HEAD> 
<TITLE>RDS Query Page</TITLE> 
</HEAD> 
<body> 
<CENTER> 
<H1>Remote Data Service 2.5</H1> 
<TABLE DATASRC="#DC1"> 
 <TR> 
 <TD><SPAN DATAFLD="au_fname"></SPAN></TD> 
 <TD><SPAN DATAFLD="au_lname"></SPAN></TD> 
 <TD><SPAN DATAFLD="phone"></SPAN></TD> 
 </TR> 
</TABLE> 

<BR> 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
 ID=DC1 HEIGHT=1 WIDTH = 1> 
 <PARAM NAME="URL" VALUE="https://server/directory/recordset.asp"> 
</OBJECT> 
 
</SCRIPT> 
</BODY> 
</HTML> 
```

Los programadores también pueden usar un objeto **Recordset** en el cliente:

```vb
... 
function GetRs() 
 { 
 rs = CreateObject("ADODB.Recordset"); 
 rs.Open "https://server/directory/recordset.asp" 
 DC1.SourceRecordset = rs; 
 } 
... 
```

