---
title: Escenario de persistencia de Recordset XML
TOCTitle: XML Recordset persistence scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4840b59f8f145b17b45a9732443d3f844b336868
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945491"
---
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="384d4-102">Escenario de persistencia de Recordset XML</span><span class="sxs-lookup"><span data-stu-id="384d4-102">XML Recordset persistence scenario</span></span>

<span data-ttu-id="384d4-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="384d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="384d4-104">En este escenario, creará una aplicación de páginas ASP que guarda el contenido de un objeto **Recordset** directamente en el objeto **Response** de ASP.</span><span class="sxs-lookup"><span data-stu-id="384d4-104">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>

> [!NOTE]
> <span data-ttu-id="384d4-105">[!NOTA] Este escenario requiere que el servidor tenga instalado Internet Information Server 5.0 (IIS) o una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="384d4-105">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span>

<span data-ttu-id="384d4-106">El objeto **Recordset** devuelto se muestra en Internet Explorer mediante un [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="384d4-106">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="384d4-107">Para crear el escenario, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="384d4-107">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="384d4-108">Configurar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="384d4-108">Set up the application.</span></span>
2.  <span data-ttu-id="384d4-109">Obtener los datos.</span><span class="sxs-lookup"><span data-stu-id="384d4-109">Get the data.</span></span>
3.  <span data-ttu-id="384d4-110">Enviar los datos.</span><span class="sxs-lookup"><span data-stu-id="384d4-110">Send the data.</span></span>
4.  <span data-ttu-id="384d4-111">Recibir y mostrar los datos.</span><span class="sxs-lookup"><span data-stu-id="384d4-111">Receive and display the data.</span></span>

## <a name="step-1-set-up-the-application"></a><span data-ttu-id="384d4-112">Paso 1: Configurar la aplicación</span><span class="sxs-lookup"><span data-stu-id="384d4-112">Step 1: Set up the application</span></span>

1. <span data-ttu-id="384d4-113">Crear un directorio virtual de IIS denominado **XMLPersist** con permisos de secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="384d4-113">Create an IIS virtual directory named **XMLPersist** with script permissions.</span></span> 

2. <span data-ttu-id="384d4-114">Crear dos nuevos archivos de texto en la carpeta a la que apunta el directorio virtual, uno con nombre **XMLResponse.asp**, y la otra denominada **Default.htm**.</span><span class="sxs-lookup"><span data-stu-id="384d4-114">Create two new text files in the folder to which the virtual directory points, one named **XMLResponse.asp**, and the other named **Default.htm**.</span></span>


## <a name="step-2-get-the-data"></a><span data-ttu-id="384d4-115">Paso 2: Obtener los datos</span><span class="sxs-lookup"><span data-stu-id="384d4-115">Step 2: Get the data</span></span>

<span data-ttu-id="384d4-116">En este paso, escribirá el código para abrir un objeto **Recordset** de ADO y prepararlo para su envío al cliente.</span><span class="sxs-lookup"><span data-stu-id="384d4-116">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client.</span></span> 

1. <span data-ttu-id="384d4-117">Abra el archivo XMLResponse.asp con un editor de texto, tal como el Bloc de notas de Windows, e inserte el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="384d4-117">Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

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

2. <span data-ttu-id="384d4-118">Asegúrese de cambiar el valor del parámetro origen de datos en strCon en el nombre de su equipo con Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="384d4-118">Be sure to change the value of the Data Source parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

3. <span data-ttu-id="384d4-119">Mantenga el archivo abierto y vaya al paso siguiente.</span><span class="sxs-lookup"><span data-stu-id="384d4-119">Keep the file open and go on to the next step.</span></span>

## <a name="step-3-send-the-data"></a><span data-ttu-id="384d4-120">Paso 3: Enviar los datos</span><span class="sxs-lookup"><span data-stu-id="384d4-120">Step 3: Send the data</span></span>

<span data-ttu-id="384d4-121">Ahora que ya tiene un **Recordset**, deberá enviarlo al cliente guardándolo como XML en el objeto **Response**.</span><span class="sxs-lookup"><span data-stu-id="384d4-121">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object.</span></span> 

1. <span data-ttu-id="384d4-122">Agregue el código siguiente al final de XMLResponse.asp:</span><span class="sxs-lookup"><span data-stu-id="384d4-122">Add the following code to the bottom of XMLResponse.asp:</span></span>

   ```vb 
    
    Response.ContentType = "text/xml" 
    Response.Expires = 0 
    Response.Buffer = False 
    
    
    Response.Write "<?xml version='1.0'?>" & vbNewLine 
    adoRec.save Response, adPersistXML 
    adoRec.Close 
    Set adoRec=Nothing 
    %> 
   ```

   <span data-ttu-id="384d4-123">Tenga en cuenta que el objeto de **respuesta** de ASP se especifica como el destino para el método **Recordset** [Guardar](save-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="384d4-123">Notice that the ASP **Response** object is specified as the destination for the **Recordset** [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="384d4-124">El destino del método **Save** puede ser cualquier objeto que admita la interfaz **IStream**, tal como un objeto ADO [Stream](stream-object-ado.md) o un nombre de archivo que incluya la ruta de acceso completa donde se va a guardar el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="384d4-124">The destination of the **Save** method can be any object that supports the **IStream** interface, such as an ADO [Stream](stream-object-ado.md) object, or a file name that includes the complete path to which the **Recordset** is to be saved.</span></span>

2. <span data-ttu-id="384d4-125">Antes de ir al paso siguiente, guarde y cierre XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="384d4-125">Save and close XMLResponse.asp before going to the next step.</span></span> <span data-ttu-id="384d4-126">Copie también el archivo adovbs.inc desde C:\\archivos de programa\\archivos comunes\\System\\carpeta de Ado en la misma carpeta donde se encuentra el archivo XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="384d4-126">Also copy the adovbs.inc file from C:\\Program Files\\Common Files\\System\\Ado folder to the same folder where you have the XMLResponse.asp file.</span></span>

## <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="384d4-127">Paso 4: Recibir y mostrar los datos</span><span class="sxs-lookup"><span data-stu-id="384d4-127">Step 4: Receive and display the data</span></span>

<span data-ttu-id="384d4-128">En este paso, creará un archivo HTML con un [incrustado RDS. DataControl](datacontrol-object-rds.md) objeto que apunta al archivo XMLResponse.asp para obtener el **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="384d4-128">In this step, you will create an HTML file with an embedded [RDS.DataControl](datacontrol-object-rds.md) object that points at the XMLResponse.asp file to get the **Recordset**.</span></span> 

1. <span data-ttu-id="384d4-129">Abra default.htm con un editor de texto, como el Bloc de notas de Windows y agregue el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="384d4-129">Open default.htm with a text editor, such as Windows Notepad, and add the following code.</span></span> <span data-ttu-id="384d4-130">Sustituya "sqlserver" en la dirección URL por el nombre de su equipo servidor.</span><span class="sxs-lookup"><span data-stu-id="384d4-130">Replace "sqlserver" in the URL with the name of your server computer.</span></span>

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

2. <span data-ttu-id="384d4-131">Cierre el archivo default.htm y guárdelo en la misma carpeta donde guardó XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="384d4-131">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</span></span> 

3. <span data-ttu-id="384d4-132">Uso de Internet Explorer 4.0 o posterior, abra la dirección URL `https://<sqlserver>/XMLPersist/default.htm` y observe los resultados.</span><span class="sxs-lookup"><span data-stu-id="384d4-132">Using Internet Explorer 4.0 or later, open the URL `https://<sqlserver>/XMLPersist/default.htm` and observe the results.</span></span> <span data-ttu-id="384d4-133">Los datos se muestran en una tabla DHTML enlazada.</span><span class="sxs-lookup"><span data-stu-id="384d4-133">The data is displayed in a bound DHTML table.</span></span> 

4. <span data-ttu-id="384d4-134">Ahora, abra la dirección URL `https://<sqlserver>/XMLPersist/XMLResponse.asp` y observe los resultados.</span><span class="sxs-lookup"><span data-stu-id="384d4-134">Now open the URL `https://<sqlserver>/XMLPersist/XMLResponse.asp` and observe the results.</span></span> <span data-ttu-id="384d4-135">Aparecerá el XML.</span><span class="sxs-lookup"><span data-stu-id="384d4-135">The XML is displayed.</span></span>




