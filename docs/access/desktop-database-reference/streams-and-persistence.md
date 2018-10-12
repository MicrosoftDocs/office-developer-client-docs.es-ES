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
# <a name="streams-and-persistence"></a><span data-ttu-id="6e74a-102">Secuencias y persistencia</span><span class="sxs-lookup"><span data-stu-id="6e74a-102">Streams and Persistence</span></span>


<span data-ttu-id="6e74a-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e74a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6e74a-104">El método [Save](save-method-ado.md) del objeto [Recordset](recordset-object-ado.md) guarda o *persiste* un objeto **Recordset** en un archivo, y el método [Open](open-method-ado-recordset.md) restaura el objeto **Recordset** de ese archivo.</span><span class="sxs-lookup"><span data-stu-id="6e74a-104">The [Recordset](recordset-object-ado.md) object [Save](save-method-ado.md) method stores, or *persists*, a **Recordset** in a file, and the [Open](open-method-ado-recordset.md) method restores the **Recordset** from that file.</span></span>

<span data-ttu-id="6e74a-p101">Con ADO 2.5, los métodos **Save** y **Open** también pueden persistir un objeto **Recordset** en un objeto [Stream](stream-object-ado.md). Esta característica es especialmente útil al trabajar con el Servicio de datos remoto (RDS) y páginas Active Server (ASP).</span><span class="sxs-lookup"><span data-stu-id="6e74a-p101">With ADO 2.5, the **Save** and **Open** methods can persist a **Recordset** to a [Stream](stream-object-ado.md) object as well. This feature is especially useful when working with Remote Data Service (RDS) and Active Server Pages (ASP).</span></span>

<span data-ttu-id="6e74a-107">Para obtener más información sobre cómo utilizar la persistencia en páginas ASP, vea la documentación de ASP.</span><span class="sxs-lookup"><span data-stu-id="6e74a-107">For more information about how persistence can be used by itself on ASP pages, see the current ASP documentation.</span></span>

<span data-ttu-id="6e74a-108">A continuación se describen algunos escenarios que muestran cómo se pueden utilizar los objetos **Stream** y la persistencia.</span><span class="sxs-lookup"><span data-stu-id="6e74a-108">The following are a few scenarios that show how **Stream** objects and persistence can be used.</span></span>

## <a name="scenario-1"></a><span data-ttu-id="6e74a-109">Escenario 1</span><span class="sxs-lookup"><span data-stu-id="6e74a-109">Scenario 1</span></span>

<span data-ttu-id="6e74a-p102">En este escenario se guarda simplemente un objeto **Recordset** en un archivo y, a continuación, en un objeto **Stream**. A continuación, se abre la secuencia guardada en otro objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6e74a-p102">This scenario simply saves a **Recordset** to a file and then to a **Stream**. It then opens the persisted stream into another **Recordset**.</span></span>

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

## <a name="scenario-2"></a><span data-ttu-id="6e74a-112">Escenario 2</span><span class="sxs-lookup"><span data-stu-id="6e74a-112">Scenario 2</span></span>

<span data-ttu-id="6e74a-p103">En este escenario se persiste un objeto **Recordset** en un objeto **Stream** con formato XML. A continuación, se lee el objeto **Stream** en una cadena que se puede examinar, manipular o mostrar.</span><span class="sxs-lookup"><span data-stu-id="6e74a-p103">This scenario persists a **Recordset** into a **Stream** in XML format. It then reads the **Stream** into a string that you can examine, manipulate, or display.</span></span>

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

## <a name="scenario-3"></a><span data-ttu-id="6e74a-115">Escenario 3</span><span class="sxs-lookup"><span data-stu-id="6e74a-115">Scenario 3</span></span>

<span data-ttu-id="6e74a-116">En este código de ejemplo se muestra cómo código ASP almacena un objeto **Recordset** como XML directamente en el objeto **Response**:</span><span class="sxs-lookup"><span data-stu-id="6e74a-116">This example code shows ASP code persisting a **Recordset** as XML directly to the **Response** object:</span></span>

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

## <a name="scenario-4"></a><span data-ttu-id="6e74a-117">Escenario 4</span><span class="sxs-lookup"><span data-stu-id="6e74a-117">Scenario 4</span></span>

<span data-ttu-id="6e74a-p104">En este escenario, código ASP escribe el contenido del objeto **Recordset** con formato ADTG en el cliente. El [Servicio de cursores de Microsoft para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) puede utilizar estos datos para crear un objeto **Recordset** desconectado.</span><span class="sxs-lookup"><span data-stu-id="6e74a-p104">In this scenario, ASP code writes the contents of the **Recordset** in ADTG format to the client. The [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) can use this data to create a disconnected **Recordset**.</span></span>

<span data-ttu-id="6e74a-p105">Una nueva propiedad en el objeto [DataControl](datacontrol-object-rds.md) de RDS, [URL](url-property-rds.md), señala la página .asp que genera el objeto **Recordset**. Esto significa que se puede obtener un objeto **Recordset** sin que RDS use el objeto [DataFactory](datafactory-object-rdsserver.md) del servidor o sin que el usuario escriba un objeto de negocio. De este modo, se simplifica considerablemente el modelo de programación de RDS.</span><span class="sxs-lookup"><span data-stu-id="6e74a-p105">A new property on the RDS [DataControl](datacontrol-object-rds.md), [URL](url-property-rds.md), points to the .asp page that generates the **Recordset**. This means a **Recordset** object can be obtained without RDS using the server-side [DataFactory](datafactory-object-rdsserver.md) object or the user writing a business object. This simplifies the RDS programming model significantly.</span></span>

<span data-ttu-id="6e74a-123">Código de servidor, que se denomina https://server/directory/recordset.asp:</span><span class="sxs-lookup"><span data-stu-id="6e74a-123">Server-side code, named https://server/directory/recordset.asp:</span></span>

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

<span data-ttu-id="6e74a-124">Código de cliente:</span><span class="sxs-lookup"><span data-stu-id="6e74a-124">Client-side code:</span></span>

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

<span data-ttu-id="6e74a-125">Los programadores también pueden usar un objeto **Recordset** en el cliente:</span><span class="sxs-lookup"><span data-stu-id="6e74a-125">Developers also have the option of using a **Recordset** object on the client:</span></span>

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
