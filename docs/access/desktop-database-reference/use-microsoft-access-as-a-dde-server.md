---
<span data-ttu-id="ea7da-101">título: uso de Microsoft Access como servidor DDE TOCTitle: uso de Microsoft Access como servidor DDE <<<<<<< HEAD ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: ms.date 48546801: 18/09/2015 === Descripción: Microsoft Access admite el intercambio dinámico de datos (DDE) como una aplicación de destino (cliente) o una aplicación de origen (servidor).</span><span class="sxs-lookup"><span data-stu-id="ea7da-101">title: Use Microsoft Access as a DDE server TOCTitle: Use Microsoft Access as a DDE Server <<<<<<< HEAD ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: 48546801 ms.date: 09/18/2015 ======= description: Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application.</span></span>  
<span data-ttu-id="ea7da-102">MS:AssetId: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: ms.date 48546801: 16/10/2018</span><span class="sxs-lookup"><span data-stu-id="ea7da-102">ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: 48546801 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="ea7da-103">maestro mtps_version: Office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="ea7da-103">master mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="ea7da-104">vbaac10.chm5186349 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="ea7da-104">vbaac10.chm5186349 f1_categories:</span></span>
- <span data-ttu-id="ea7da-105">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="ea7da-105">Office.Version=v15</span></span>
---

# <a name="use-microsoft-access-as-a-dde-server"></a><span data-ttu-id="ea7da-106">Uso de Microsoft Access como servidor DDE</span><span class="sxs-lookup"><span data-stu-id="ea7da-106">Use Microsoft Access as a DDE server</span></span>

<span data-ttu-id="ea7da-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ea7da-107">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="ea7da-p101">Microsoft Access admite el intercambio dinámico de datos (DDE) como aplicación de destino (cliente) o aplicación de origen (servidor). Por ejemplo, una aplicación como Microsoft Word, que actúa como cliente, puede solicitar datos a través de DDE de una base de datos de Microsoft Access que actúa como servidor.</span><span class="sxs-lookup"><span data-stu-id="ea7da-p101">Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application. For example, an application such as Microsoft Word, acting as a client, can request data through DDE from a Microsoft Access database that's acting as a server.</span></span>

> [!TIP]
> <span data-ttu-id="ea7da-110">[!SUGERENCIA] Si necesita manipular objetos de Microsoft Access desde otra aplicación, considere la posibilidad de usar Automatización.</span><span class="sxs-lookup"><span data-stu-id="ea7da-110">If you need to manipulate Microsoft Access objects from another application, you may want to consider using Automation.</span></span>

<span data-ttu-id="ea7da-111"><<<<<<< Conversación de cabeza A DDE entre un cliente y el servidor se establece sobre un tema concreto.</span><span class="sxs-lookup"><span data-stu-id="ea7da-111"><<<<<<< HEAD A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="ea7da-112">Un tema puede ser un archivo de datos en el formato admitido por la aplicación servidor o puede ser el tema System, que proporciona información sobre la propia aplicación servidor.</span><span class="sxs-lookup"><span data-stu-id="ea7da-112">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="ea7da-113">Una vez iniciada una conversación sobre un tema determinado, sólo se puede transferir un elemento de datos asociado con dicho tema.</span><span class="sxs-lookup"><span data-stu-id="ea7da-113">Once a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>
<span data-ttu-id="ea7da-114">=== Una conversación DDE entre un cliente y un servidor se establece sobre un tema concreto.</span><span class="sxs-lookup"><span data-stu-id="ea7da-114">======= A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="ea7da-115">Un tema puede ser un archivo de datos en el formato admitido por la aplicación servidor o puede ser el tema System, que proporciona información sobre la propia aplicación servidor.</span><span class="sxs-lookup"><span data-stu-id="ea7da-115">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="ea7da-116">Una vez iniciada una conversación sobre un tema determinado, sólo un elemento de datos asociado con dicho tema puede transferirse.</span><span class="sxs-lookup"><span data-stu-id="ea7da-116">After a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>
>>>>>>> <span data-ttu-id="ea7da-117">master</span><span class="sxs-lookup"><span data-stu-id="ea7da-117">master</span></span>

<span data-ttu-id="ea7da-p103">Por ejemplo, suponga que está ejecutando Microsoft Word y desea insertar en un documento datos de una determinada base de datos de Microsoft Access. Para iniciar una conversación DDE con Microsoft Access, abra un canal DDE mediante la función **DDEInitiate** y especifique el nombre del archivo de la base de datos como tema. A continuación, podrá transferir los datos de esa base de datos a Microsoft Word a través de dicho canal.</span><span class="sxs-lookup"><span data-stu-id="ea7da-p103">For example, suppose you are running Microsoft Word and want to insert data from a particular Microsoft Access database into a document. You begin a DDE conversation with Microsoft Access by opening a DDE channel with the **DDEInitiate** function and specifying the database file name as the topic. You can then transfer data from that database to Microsoft Word through that channel.</span></span>

<span data-ttu-id="ea7da-121">Como servidor DDE, Microsoft Access admite los siguiente temas:</span><span class="sxs-lookup"><span data-stu-id="ea7da-121">As a DDE server, Microsoft Access supports the following topics:</span></span>

<span data-ttu-id="ea7da-122"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="ea7da-122"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="ea7da-123">El tema System (Sistema)</span><span class="sxs-lookup"><span data-stu-id="ea7da-123">The System topic</span></span>

  - <span data-ttu-id="ea7da-124">El nombre de una base de datos (tema *database (base de datos)*)</span><span class="sxs-lookup"><span data-stu-id="ea7da-124">The name of a database (*database* topic)</span></span>

  - <span data-ttu-id="ea7da-125">El nombre de una tabla (tema *tablename (nombretabla)*)</span><span class="sxs-lookup"><span data-stu-id="ea7da-125">The name of a table (*tablename* topic)</span></span>

  - <span data-ttu-id="ea7da-126">El nombre de una consulta (tema *queryname (nombreconsulta)*)</span><span class="sxs-lookup"><span data-stu-id="ea7da-126">The name of a query (*queryname* topic)</span></span>

  - <span data-ttu-id="ea7da-127">Una cadena SQL de Microsoft Access (tema *sqlstring (cadenasql)*)</span><span class="sxs-lookup"><span data-stu-id="ea7da-127">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="ea7da-p104">Sólo después de establecer una conversación DDE, podrá utilizar la instrucción **DDEExecute** para enviar un comando de la aplicación cliente a la aplicación servidor. Cuando se utiliza como servidor DDE, Microsoft Access reconoce los siguientes elementos como un comando válido:</span><span class="sxs-lookup"><span data-stu-id="ea7da-p104">Once you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application. When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

  - <span data-ttu-id="ea7da-130">El nombre de una macro en la actual base de datos.</span><span class="sxs-lookup"><span data-stu-id="ea7da-130">The name of a macro in the current database.</span></span>

  - <span data-ttu-id="ea7da-131">Cualquier acción que se pueda realizar en Visual Basic mediante uno de los métodos del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="ea7da-131">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

  - <span data-ttu-id="ea7da-p105">Las acciones AbrirBaseDeDatos (OpenDatabase) y CerrarBaseDeDatos (CloseDatabase), que se utilizan sólo para las operaciones DDE. (Para ver cómo se utilizan estas funciones, vea el ejemplo que aparece a continuación en este tema.)</span><span class="sxs-lookup"><span data-stu-id="ea7da-p105">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations. (For an example of how to use these actions, see the example later in this topic.)</span></span>


> [!NOTE]
> <P><span data-ttu-id="ea7da-p106">[!NOTA] Al especificar una acción de macro como instrucción <STRONG>DDEExecute</STRONG>, la acción y los argumentos siguen la sintaxis del objeto <STRONG>DoCmd</STRONG> y deben ir entre corchetes ([ ]). Sin embargo, las aplicaciones que admiten DDE no reconocen las constantes intrínsecas en las operaciones DDE. Asimismo, los argumentos de cadena deben ir entre comillas (" ") si la cadena contiene una coma. En caso contrario, no son necesarias las comillas.</span><span class="sxs-lookup"><span data-stu-id="ea7da-p106">When you specify a macro action as a <STRONG>DDEExecute</STRONG> statement, the action and any arguments follow the <STRONG>DoCmd</STRONG> object syntax and must be enclosed in brackets ([ ]). However, applications that support DDE don't recognize intrinsic constants in DDE operations. Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma. Otherwise, quotation marks aren't required.</span></span></P>



<span data-ttu-id="ea7da-p107">La aplicación cliente puede utilizar la función **DDERequest** para solicitar datos de texto de la aplicación servidor a través de un canal DDE abierto. O bien, el cliente puede utilizar la instrucción **DDEPoke** para enviar datos a la aplicación servidor. Tras finalizar la transferencia de datos, el cliente puede utilizar la instrucción **DDETerminate** para cerrar el canal DDE o la instrucción **DDETerminateAll** para cerrar todos los canales abiertos.</span><span class="sxs-lookup"><span data-stu-id="ea7da-p107">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel. Or the client can use the **DDEPoke** statement to send data to the server application. Once the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ea7da-141">[!NOTA] Cuando la aplicación cliente termine de recibir datos a través de un canal DDE, deberá cerrar dicho canal para conservar los recursos de la memoria.</span><span class="sxs-lookup"><span data-stu-id="ea7da-141">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span></P>


=======
- <span data-ttu-id="ea7da-142">El tema System (Sistema)</span><span class="sxs-lookup"><span data-stu-id="ea7da-142">The System topic</span></span>

- <span data-ttu-id="ea7da-143">El nombre de una base de datos (tema *database (base de datos)*)</span><span class="sxs-lookup"><span data-stu-id="ea7da-143">The name of a database (*database* topic)</span></span>

- <span data-ttu-id="ea7da-144">El nombre de una tabla (tema *tablename (nombretabla)*)</span><span class="sxs-lookup"><span data-stu-id="ea7da-144">The name of a table (*tablename* topic)</span></span>

- <span data-ttu-id="ea7da-145">El nombre de una consulta (tema *queryname (nombreconsulta)*)</span><span class="sxs-lookup"><span data-stu-id="ea7da-145">The name of a query (*queryname* topic)</span></span>

- <span data-ttu-id="ea7da-146">Una cadena SQL de Microsoft Access (tema *sqlstring (cadenasql)*)</span><span class="sxs-lookup"><span data-stu-id="ea7da-146">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="ea7da-147">Después de establecer una conversación DDE, puede usar la instrucción **DDEExecute** para enviar un comando desde el cliente a la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="ea7da-147">After you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application.</span></span> <span data-ttu-id="ea7da-148">Cuando se utiliza como servidor DDE, Microsoft Access reconoce los siguientes elementos como un comando válido:</span><span class="sxs-lookup"><span data-stu-id="ea7da-148">When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

- <span data-ttu-id="ea7da-149">El nombre de una macro en la actual base de datos.</span><span class="sxs-lookup"><span data-stu-id="ea7da-149">The name of a macro in the current database.</span></span>

- <span data-ttu-id="ea7da-150">Cualquier acción que se pueda realizar en Visual Basic mediante uno de los métodos del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="ea7da-150">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

- <span data-ttu-id="ea7da-p109">Las acciones AbrirBaseDeDatos (OpenDatabase) y CerrarBaseDeDatos (CloseDatabase), que se utilizan sólo para las operaciones DDE. (Para ver cómo se utilizan estas funciones, vea el ejemplo que aparece a continuación en este tema.)</span><span class="sxs-lookup"><span data-stu-id="ea7da-p109">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations. (For an example of how to use these actions, see the example later in this topic.)</span></span>

> [!NOTE]
> <span data-ttu-id="ea7da-p110">[!NOTA] Al especificar una acción de macro como instrucción **DDEExecute**, la acción y los argumentos siguen la sintaxis del objeto **DoCmd** y deben ir entre corchetes ([ ]). Sin embargo, las aplicaciones que admiten DDE no reconocen las constantes intrínsecas en las operaciones DDE. Asimismo, los argumentos de cadena deben ir entre comillas (" ") si la cadena contiene una coma. En caso contrario, no son necesarias las comillas.</span><span class="sxs-lookup"><span data-stu-id="ea7da-p110">When you specify a macro action as a **DDEExecute** statement, the action and any arguments follow the **DoCmd** object syntax and must be enclosed in brackets ([ ]). However, applications that support DDE don't recognize intrinsic constants in DDE operations. Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma. Otherwise, quotation marks aren't required.</span></span>

<span data-ttu-id="ea7da-157">La aplicación cliente puede utilizar la función **DDERequest** para solicitar datos de texto de la aplicación servidor a través de un canal DDE abierto.</span><span class="sxs-lookup"><span data-stu-id="ea7da-157">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel.</span></span> <span data-ttu-id="ea7da-158">O bien, el cliente puede utilizar la instrucción **DDEPoke** para enviar datos a la aplicación servidor.</span><span class="sxs-lookup"><span data-stu-id="ea7da-158">Or the client can use the **DDEPoke** statement to send data to the server application.</span></span> <span data-ttu-id="ea7da-159">Una vez completada la transferencia de datos, el cliente puede usar la instrucción **DDETerminate** para cerrar el canal DDE o la instrucción **DDETerminateAll** para cerrar todos los canales abiertos.</span><span class="sxs-lookup"><span data-stu-id="ea7da-159">After the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>

> [!NOTE]
> <span data-ttu-id="ea7da-160">[!NOTA] Cuando la aplicación cliente termine de recibir datos a través de un canal DDE, deberá cerrar dicho canal para conservar los recursos de la memoria.</span><span class="sxs-lookup"><span data-stu-id="ea7da-160">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span>
>>>>>>> <span data-ttu-id="ea7da-161">master</span><span class="sxs-lookup"><span data-stu-id="ea7da-161">master</span></span>

<span data-ttu-id="ea7da-p112">El siguiente ejemplo muestra cómo se crea un procedimiento de Microsoft Word mediante Visual Basic que utiliza Microsoft Access como servidor DDE. (Para que funcione este ejemplo, Microsoft Access debe estar ejecutándose.)</span><span class="sxs-lookup"><span data-stu-id="ea7da-p112">The following example demonstrates how to create a Microsoft Word procedure with Visual Basic that uses Microsoft Access as a DDE server. (For this example to work, Microsoft Access must be running.)</span></span>

```vb
    Sub AccessDDE() 
        Dim intChan1 As Integer, intChan2 As Integer 
        Dim strQueryData As String 
     
        ' Use System topic to open Northwind sample database. 
        ' Database must be open before using other DDE topics. 
        intChan1 = DDEInitiate("MSAccess", "System") 
        ' You may need to change this path to point to actual location 
        ' of Northwind sample database. 
        DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]" 
     
        ' Get all data from Ten Most Expensive Products query. 
        intChan2 = DDEInitiate("MSAccess", "Northwind.mdb;" _ 
            & "QUERY Ten Most Expensive Products") 
        strQueryData = DDERequest(intChan2, "All") 
        DDETerminate intChan2 
     
        ' Close database. 
        DDEExecute intChan1, "[CloseDatabase]" 
        DDETerminate intChan1 
     
        ' Print retrieved data to Debug Window. 
        Debug.Print strQueryData 
    End Sub
```

<a name="-head"></a><span data-ttu-id="ea7da-164"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="ea7da-164"><<<<<<< HEAD</span></span>
=======
<br/>

>>>>>>> <span data-ttu-id="ea7da-165">patrón de que las secciones siguientes proporcionan información acerca de los temas DDE válidos que admite Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ea7da-165">master The following sections provide information about the valid DDE topics supported by Microsoft Access.</span></span>

## <a name="the-system-topic"></a><span data-ttu-id="ea7da-166">El tema System (Sistema)</span><span class="sxs-lookup"><span data-stu-id="ea7da-166">The System topic</span></span>

<span data-ttu-id="ea7da-167"><<<<<<< HEAD del sistema es un tema estándar para todas las aplicaciones basadas en Windows de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ea7da-167"><<<<<<< HEAD The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="ea7da-168">Facilita información sobre los demás temas que admite la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ea7da-168">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="ea7da-169">Para obtener acceso a esta información, el código debe llamar primero a la función **DDEInitiate** con como el argumento *tema* y, a continuación, ejecutar la instrucción **DDERequest** con uno de los siguientes para el argumento de *elemento* .</span><span class="sxs-lookup"><span data-stu-id="ea7da-169">To access this information, your code must first call the **DDEInitiate** function with as the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>
<span data-ttu-id="ea7da-170">=== El tema System es un tema estándar para todas las aplicaciones basadas en Windows de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ea7da-170">======= The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="ea7da-171">Facilita información sobre los demás temas que admite la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ea7da-171">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="ea7da-172">Para obtener acceso a esta información, el código debe llamar primero a la función **DDEIniciar (DDEInitiate)** con el argumento *tema* y, a continuación, ejecutar la instrucción **DDERequest** con uno de los siguientes argumentos *elemento* .</span><span class="sxs-lookup"><span data-stu-id="ea7da-172">To access this information, your code must first call the **DDEInitiate** function with the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>
>>>>>>> <span data-ttu-id="ea7da-173">master</span><span class="sxs-lookup"><span data-stu-id="ea7da-173">master</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea7da-174">Elemento</span><span class="sxs-lookup"><span data-stu-id="ea7da-174">Item</span></span></p></th>
<th><p><span data-ttu-id="ea7da-175">Devuelve</span><span class="sxs-lookup"><span data-stu-id="ea7da-175">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea7da-176">SysItems</span><span class="sxs-lookup"><span data-stu-id="ea7da-176">SysItems</span></span></p></td>
<td><p><span data-ttu-id="ea7da-177">Una lista de elementos que admite el tema System en Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ea7da-177">A list of items supported by the System topic in Microsoft Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-178">Formats</span><span class="sxs-lookup"><span data-stu-id="ea7da-178">Formats</span></span></p></td>
<td><p><span data-ttu-id="ea7da-179">Una lista de formatos que Microsoft Access puede copiar al Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="ea7da-179">A list of the formats Microsoft Access can copy onto the Clipboard.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea7da-180">Status</span><span class="sxs-lookup"><span data-stu-id="ea7da-180">Status</span></span></p></td>
<td><p><span data-ttu-id="ea7da-181">&quot;Ocupado&quot; o &quot;listo&quot;.</span><span class="sxs-lookup"><span data-stu-id="ea7da-181">&quot;Busy&quot; or &quot;Ready&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-182">Topics</span><span class="sxs-lookup"><span data-stu-id="ea7da-182">Topics</span></span></p></td>
<td><p><span data-ttu-id="ea7da-183">Una lista de todas las bases de datos abiertas.</span><span class="sxs-lookup"><span data-stu-id="ea7da-183">A list of all open databases.</span></span></p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><span data-ttu-id="ea7da-184"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="ea7da-184"><<<<<<< HEAD</span></span>
=======
<br/>
>>>>>>> <span data-ttu-id="ea7da-185">master</span><span class="sxs-lookup"><span data-stu-id="ea7da-185">master</span></span>

<span data-ttu-id="ea7da-186">El siguiente ejemplo muestra cómo se utilizan las funciones **DDEIniciar (DDEInitiate)** y **DDEPedido (DDERequest)** con el tema System:</span><span class="sxs-lookup"><span data-stu-id="ea7da-186">The following example demonstrates the use of the **DDEInitiate** and **DDERequest** functions with the System topic:</span></span>

```vb
    ' In Visual Basic, initiate DDE conversation with Microsoft Access. 
    Dim intChan1 As Integer, strResults As String 
    intChan1 = DDEInitiate("MSAccess", "System") 
    ' Request list of topics supported by System topic. 
    strResults = DDERequest(intChan1, "SysItems") 
    ' Run OpenDatabase action to open Northwind.mdb. 
    ' You may need to change this path to point to actual location 
    ' of Northwind sample database. 
    DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]"
```

## <a name="the-database-topic"></a><span data-ttu-id="ea7da-187">El tema de la base de datos</span><span class="sxs-lookup"><span data-stu-id="ea7da-187">The database topic</span></span>

<span data-ttu-id="ea7da-188">El tema de la *base de datos* es el nombre de archivo de base de datos existente.</span><span class="sxs-lookup"><span data-stu-id="ea7da-188">The *database* topic is the file name of an existing database.</span></span> <span data-ttu-id="ea7da-189">Puede escribir simplemente el nombre (Northwind) o su ruta de acceso y la extensión .mdb (C:\\Access\\ejemplos\\Neptuno.mdb).</span><span class="sxs-lookup"><span data-stu-id="ea7da-189">You can type either just the base name (Northwind), or its path and .mdb extension (C:\\Access\\Samples\\Northwind.mdb).</span></span> <span data-ttu-id="ea7da-190">Tras iniciar una conversación DDE con la base de datos, puede solicitar una lista de los objetos incluidos en dicha base de datos.</span><span class="sxs-lookup"><span data-stu-id="ea7da-190">After you start a DDE conversation with the database, you can request a list of the objects in that database.</span></span>

<span data-ttu-id="ea7da-191"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="ea7da-191"><<<<<<< HEAD</span></span>

> [!NOTE]
> <P><span data-ttu-id="ea7da-192">[!NOTA] No se puede utilizar DDE para consultar el archivo de información de grupo de trabajo de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ea7da-192">You can't use DDE to query the Microsoft Access workgroup information file.</span></span></P>


=======
> [!NOTE]
> <span data-ttu-id="ea7da-193">[!NOTA] No se puede utilizar DDE para consultar el archivo de información de grupo de trabajo de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ea7da-193">You can't use DDE to query the Microsoft Access workgroup information file.</span></span>
>>>>>>> <span data-ttu-id="ea7da-194">master</span><span class="sxs-lookup"><span data-stu-id="ea7da-194">master</span></span>

<span data-ttu-id="ea7da-195">El tema *database* admite los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="ea7da-195">The *database* topic supports the following items.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea7da-196">Elemento</span><span class="sxs-lookup"><span data-stu-id="ea7da-196">Item</span></span></p></th>
<th><p><span data-ttu-id="ea7da-197">Devuelve</span><span class="sxs-lookup"><span data-stu-id="ea7da-197">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea7da-198">ListaDeTablas</span><span class="sxs-lookup"><span data-stu-id="ea7da-198">TableList</span></span></p></td>
<span data-ttu-id="ea7da-199"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="ea7da-199"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="ea7da-200">Una lista de tablas.</span><span class="sxs-lookup"><span data-stu-id="ea7da-200">A list of tables.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-201">QueryList</span><span class="sxs-lookup"><span data-stu-id="ea7da-201">QueryList</span></span></p></td>
<td><p><span data-ttu-id="ea7da-202">Una lista de consultas.</span><span class="sxs-lookup"><span data-stu-id="ea7da-202">A list of queries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea7da-203">FormList</span><span class="sxs-lookup"><span data-stu-id="ea7da-203">FormList</span></span></p></td>
<td><p><span data-ttu-id="ea7da-204">Una lista de formularios.</span><span class="sxs-lookup"><span data-stu-id="ea7da-204">A list of forms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-205">ReportList</span><span class="sxs-lookup"><span data-stu-id="ea7da-205">ReportList</span></span></p></td>
<td><p><span data-ttu-id="ea7da-206">Una lista de informes.</span><span class="sxs-lookup"><span data-stu-id="ea7da-206">A list of reports.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea7da-207">MacroList</span><span class="sxs-lookup"><span data-stu-id="ea7da-207">MacroList</span></span></p></td>
<td><p><span data-ttu-id="ea7da-208">Una lista de macros.</span><span class="sxs-lookup"><span data-stu-id="ea7da-208">A list of macros.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-209">ModuleList</span><span class="sxs-lookup"><span data-stu-id="ea7da-209">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="ea7da-210">Una lista de módulos.</span><span class="sxs-lookup"><span data-stu-id="ea7da-210">A list of modules.</span></span></p></td>
=======
<td><p><span data-ttu-id="ea7da-211">Una lista de tablas</span><span class="sxs-lookup"><span data-stu-id="ea7da-211">A list of tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-212">QueryList</span><span class="sxs-lookup"><span data-stu-id="ea7da-212">QueryList</span></span></p></td>
<td><p><span data-ttu-id="ea7da-213">Una lista de consultas</span><span class="sxs-lookup"><span data-stu-id="ea7da-213">A list of queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea7da-214">FormList</span><span class="sxs-lookup"><span data-stu-id="ea7da-214">FormList</span></span></p></td>
<td><p><span data-ttu-id="ea7da-215">Una lista de formularios</span><span class="sxs-lookup"><span data-stu-id="ea7da-215">A list of forms</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-216">ReportList</span><span class="sxs-lookup"><span data-stu-id="ea7da-216">ReportList</span></span></p></td>
<td><p><span data-ttu-id="ea7da-217">Una lista de informes</span><span class="sxs-lookup"><span data-stu-id="ea7da-217">A list of reports</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea7da-218">MacroList</span><span class="sxs-lookup"><span data-stu-id="ea7da-218">MacroList</span></span></p></td>
<td><p><span data-ttu-id="ea7da-219">Una lista de macros</span><span class="sxs-lookup"><span data-stu-id="ea7da-219">A list of macros</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-220">ModuleList</span><span class="sxs-lookup"><span data-stu-id="ea7da-220">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="ea7da-221">Una lista de módulos</span><span class="sxs-lookup"><span data-stu-id="ea7da-221">A list of modules</span></span></p></td><span data-ttu-id="ea7da-222">
>>>>>>>patrón</span><span class="sxs-lookup"><span data-stu-id="ea7da-222">
>>>>>>> master</span></span>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea7da-223">ViewList</span><span class="sxs-lookup"><span data-stu-id="ea7da-223">ViewList</span></span></p></td>
<td><p><span data-ttu-id="ea7da-224">Una lista de vistas</span><span class="sxs-lookup"><span data-stu-id="ea7da-224">A list of views</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-225">StoredProcedureList</span><span class="sxs-lookup"><span data-stu-id="ea7da-225">StoredProcedureList</span></span></p></td>
<td><p><span data-ttu-id="ea7da-226">Una lista de procedimientos almacenados</span><span class="sxs-lookup"><span data-stu-id="ea7da-226">A list of stored procedures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea7da-227">DatabaseDiagramList</span><span class="sxs-lookup"><span data-stu-id="ea7da-227">DatabaseDiagramList</span></span></p></td>
<td><p><span data-ttu-id="ea7da-228">Una lista de diagramas de base de datos</span><span class="sxs-lookup"><span data-stu-id="ea7da-228">A list of database diagrams</span></span></p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><span data-ttu-id="ea7da-229"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="ea7da-229"><<<<<<< HEAD</span></span>
=======
<br/>
>>>>>>> <span data-ttu-id="ea7da-230">master</span><span class="sxs-lookup"><span data-stu-id="ea7da-230">master</span></span>

<span data-ttu-id="ea7da-231">El siguiente ejemplo muestra cómo se puede abrir el formulario Empleados en la base de datos de ejemplo Northwind desde un procedimiento de Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ea7da-231">The following example shows how you can open the Employees form in the Northwind sample database from a Visual Basic procedure:</span></span>

```vb
    ' In Visual Basic, initiate DDE conversation with 
    ' Northwind sample database. 
    ' Make sure database is open. 
    intChan2 = DDEInitiate("MSAccess", "Northwind") 
    ' Request list of forms in Northwind sample database. 
    strResponse = DDERequest(intChan2, "FormList") 
    ' Run OpenForm action and arguments to open Employees form. 
    DDEExecute intChan2, "[OpenForm Employees,0,,,1,0]"
```

## <a name="the-table-topic"></a><span data-ttu-id="ea7da-232">El tema de la tabla</span><span class="sxs-lookup"><span data-stu-id="ea7da-232">The TABLE topic</span></span>

<span data-ttu-id="ea7da-233">Estos temas utilizan la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="ea7da-233">These topics use the following syntax:</span></span>

<span data-ttu-id="ea7da-234">_databasename_ ; **Tabla** _TableName_</span><span class="sxs-lookup"><span data-stu-id="ea7da-234">_databasename_ ; **TABLE** _tablename_</span></span>

<span data-ttu-id="ea7da-235">_databasename_ ; **Consulta** _nombreconsulta_</span><span class="sxs-lookup"><span data-stu-id="ea7da-235">_databasename_ ; **QUERY** _queryname_</span></span>

<span data-ttu-id="ea7da-236">_databasename_ ; **SQL** [ _cadenasql_ ]</span><span class="sxs-lookup"><span data-stu-id="ea7da-236">_databasename_ ; **SQL** [ _sqlstring_ ]</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea7da-237">Parte</span><span class="sxs-lookup"><span data-stu-id="ea7da-237">Part</span></span></p></th>
<th><p><span data-ttu-id="ea7da-238">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea7da-238">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea7da-239"><em>nombrebasedatos</em></span><span class="sxs-lookup"><span data-stu-id="ea7da-239"><em>databasename</em></span></span></p></td>
<td><p><span data-ttu-id="ea7da-p115">El nombre de la base de datos donde se encuentra la tabla o consulta o a la que se aplica la instrucción SQL, seguido de un punto y coma (;). El nombre de la base de datos puede ser simplemente el nombre (Northwind) o su ruta de acceso completa y la extensión .mdb (C:\Access\Samples\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="ea7da-p115">The name of the database that the table or query is in or that the SQL statement applies to, followed by a semicolon (;). The database name can be just the base name (Northwind) or its full path and .mdb extension (C:\Access\Samples\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-242"><em>nombretabla</em></span><span class="sxs-lookup"><span data-stu-id="ea7da-242"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="ea7da-243">El nombre de una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="ea7da-243">The name of an existing table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea7da-244"><em>nombreconsulta</em></span><span class="sxs-lookup"><span data-stu-id="ea7da-244"><em>queryname</em></span></span></p></td>
<td><p><span data-ttu-id="ea7da-245">El nombre de una consulta existente.</span><span class="sxs-lookup"><span data-stu-id="ea7da-245">The name of an existing query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-246"><em>sqlstring</em></span><span class="sxs-lookup"><span data-stu-id="ea7da-246"><em>sqlstring</em></span></span></p></td>
<td><p><span data-ttu-id="ea7da-247">Una instrucción SQL válida hasta 256 caracteres de longitud, que terminan con un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="ea7da-247">A valid SQL statement up to 256 characters long, ending with a semicolon.</span></span> <span data-ttu-id="ea7da-248">Para intercambiar más de 256 caracteres, omita este argumento y utilice instrucciones <strong>DDEPoke</strong> sucesivas para generar una instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="ea7da-248">To exchange more than 256 characters, omit this argument and instead use successive <strong>DDEPoke</strong> statements to build an SQL statement.</span></span> <span data-ttu-id="ea7da-249">Por ejemplo, el siguiente código de Visual Basic utiliza la instrucción <strong>DDEPoke</strong> para generar una instrucción SQL y, a continuación, solicita los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="ea7da-249">For example, the following Visual Basic code uses the <strong>DDEPoke</strong> statement to build an SQL statement and then request the results of the query.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="ea7da-250">La siguiente tabla muestra los elementos válidos para los temas TABLA *nombretabla*, CONSULTA *nombreconsulta* y SQL *cadenasql*.</span><span class="sxs-lookup"><span data-stu-id="ea7da-250">The following table lists the valid items for the TABLE *tablename*, QUERY *queryname*, and SQL *sqlstring* topics.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea7da-251">Elemento</span><span class="sxs-lookup"><span data-stu-id="ea7da-251">Item</span></span></p></th>
<th><p><span data-ttu-id="ea7da-252">Devuelve</span><span class="sxs-lookup"><span data-stu-id="ea7da-252">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea7da-253">Todos</span><span class="sxs-lookup"><span data-stu-id="ea7da-253">All</span></span></p></td>
<td><p><span data-ttu-id="ea7da-254">Todos los datos de la tabla, incluidos los nombres de campo.</span><span class="sxs-lookup"><span data-stu-id="ea7da-254">All the data in the table, including field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-255">Datos</span><span class="sxs-lookup"><span data-stu-id="ea7da-255">Data</span></span></p></td>
<td><p><span data-ttu-id="ea7da-256">Todas las filas de datos, sin los nombres de campo.</span><span class="sxs-lookup"><span data-stu-id="ea7da-256">All rows of data, without field names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea7da-257">FieldNames</span><span class="sxs-lookup"><span data-stu-id="ea7da-257">FieldNames</span></span></p></td>
<td><p><span data-ttu-id="ea7da-258">Una lista de una sola fila con los nombres de campo.</span><span class="sxs-lookup"><span data-stu-id="ea7da-258">A single-row list of field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-259">FieldNames; T</span><span class="sxs-lookup"><span data-stu-id="ea7da-259">FieldNames;T</span></span></p></td>
<span data-ttu-id="ea7da-260"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="ea7da-260"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="ea7da-261">Una lista de dos filas con los nombres de campo (primera fila) y los tipos de datos (segunda fila).</span><span class="sxs-lookup"><span data-stu-id="ea7da-261">A two-row list of field names (first row) and their data types (second row).</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ea7da-262">Éstos son los valores devueltos y los tipos de datos que representan.</span><span class="sxs-lookup"><span data-stu-id="ea7da-262">These are the values returned and the data types they represent:</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="ea7da-263"><b>Valor</b></span><span class="sxs-lookup"><span data-stu-id="ea7da-263"><b>Value</b></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ea7da-264">0</span><span class="sxs-lookup"><span data-stu-id="ea7da-264">0</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="ea7da-265">1</span><span class="sxs-lookup"><span data-stu-id="ea7da-265">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ea7da-266">2</span><span class="sxs-lookup"><span data-stu-id="ea7da-266">2</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="ea7da-267">3</span><span class="sxs-lookup"><span data-stu-id="ea7da-267">3</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ea7da-268">4</span><span class="sxs-lookup"><span data-stu-id="ea7da-268">4</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="ea7da-269">5</span><span class="sxs-lookup"><span data-stu-id="ea7da-269">5</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ea7da-270">6</span><span class="sxs-lookup"><span data-stu-id="ea7da-270">6</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="ea7da-271">7</span><span class="sxs-lookup"><span data-stu-id="ea7da-271">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ea7da-272">8</span><span class="sxs-lookup"><span data-stu-id="ea7da-272">8</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="ea7da-273">9</span><span class="sxs-lookup"><span data-stu-id="ea7da-273">9</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ea7da-274">10</span><span class="sxs-lookup"><span data-stu-id="ea7da-274">10</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="ea7da-275">11</span><span class="sxs-lookup"><span data-stu-id="ea7da-275">11</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ea7da-276">12</span><span class="sxs-lookup"><span data-stu-id="ea7da-276">12</span></span></p></td>
=======
<td><p><span data-ttu-id="ea7da-277">Una lista de dos filas con los nombres de campo (primera fila) y los tipos de datos (segunda fila).</span><span class="sxs-lookup"><span data-stu-id="ea7da-277">A two-row list of field names (first row) and their data types (second row).</span></span></p>
<p><span data-ttu-id="ea7da-278">Estos son los valores devueltos:</span><span class="sxs-lookup"><span data-stu-id="ea7da-278">These are the values returned:</span></span></p>
<p><span data-ttu-id="ea7da-279">Valor</span><span class="sxs-lookup"><span data-stu-id="ea7da-279">Value</span></span></p>
<p><ul>
<li><span data-ttu-id="ea7da-280">0</span><span class="sxs-lookup"><span data-stu-id="ea7da-280">0</span></span></li>
<li><span data-ttu-id="ea7da-281">1</span><span class="sxs-lookup"><span data-stu-id="ea7da-281">1</span></span></li>
<li><span data-ttu-id="ea7da-282">2</span><span class="sxs-lookup"><span data-stu-id="ea7da-282">2</span></span></li>
<li><span data-ttu-id="ea7da-283">3</span><span class="sxs-lookup"><span data-stu-id="ea7da-283">3</span></span></li>
<li><span data-ttu-id="ea7da-284">4</span><span class="sxs-lookup"><span data-stu-id="ea7da-284">4</span></span></li>
<li><span data-ttu-id="ea7da-285">5</span><span class="sxs-lookup"><span data-stu-id="ea7da-285">5</span></span></li>
<li><span data-ttu-id="ea7da-286">6</span><span class="sxs-lookup"><span data-stu-id="ea7da-286">6</span></span></li>
<li><span data-ttu-id="ea7da-287">7</span><span class="sxs-lookup"><span data-stu-id="ea7da-287">7</span></span></li>
<li><span data-ttu-id="ea7da-288">8</span><span class="sxs-lookup"><span data-stu-id="ea7da-288">8</span></span></li>
<li><span data-ttu-id="ea7da-289">9</span><span class="sxs-lookup"><span data-stu-id="ea7da-289">9</span></span></li>
<li><span data-ttu-id="ea7da-290">10</span><span class="sxs-lookup"><span data-stu-id="ea7da-290">10</span></span></li>
<li><span data-ttu-id="ea7da-291">11</span><span class="sxs-lookup"><span data-stu-id="ea7da-291">11</span></span></li>
<li><span data-ttu-id="ea7da-292">12</span><span class="sxs-lookup"><span data-stu-id="ea7da-292">12</span></span></li>
</ul>
</p>
</td><span data-ttu-id="ea7da-293">
>>>>>>>patrón</span><span class="sxs-lookup"><span data-stu-id="ea7da-293">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-294">NextRow</span><span class="sxs-lookup"><span data-stu-id="ea7da-294">NextRow</span></span></p></td>
<td><p><span data-ttu-id="ea7da-p117">Los datos en la siguiente fila de la tabla o consulta. Al abrir un canal, NextRow devuelve los datos de la primera fila. Si la fila actual es el último registro y ejecuta NextRow, se produce un error en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea7da-p117">The data in the next row in the table or query. When you open a channel, NextRow returns the data in the first row. If the current row is the last record and you run NextRow, the request fails.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea7da-298">PrevRow</span><span class="sxs-lookup"><span data-stu-id="ea7da-298">PrevRow</span></span></p></td>
<td><p><span data-ttu-id="ea7da-p118">Los datos en la fila anterior de la tabla o consulta. Si PrevRow es la primera solicitud en un nuevo canal, se devolverán los datos en la última fila de la tabla o consulta. Si el primer registro es la fila actual, se produce un error en la solicitud de PrevRow.</span><span class="sxs-lookup"><span data-stu-id="ea7da-p118">The data in the previous row in the table or query. If PrevRow is the first request on a new channel, the data in the last row of the table or query is returned. If the first record is the current row, the request for PrevRow fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-302">FirstRow</span><span class="sxs-lookup"><span data-stu-id="ea7da-302">FirstRow</span></span></p></td>
<td><p><span data-ttu-id="ea7da-303">Los datos en la primera fila de la tabla o consulta.</span><span class="sxs-lookup"><span data-stu-id="ea7da-303">The data in the first row of the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea7da-304">LastRow</span><span class="sxs-lookup"><span data-stu-id="ea7da-304">LastRow</span></span></p></td>
<td><p><span data-ttu-id="ea7da-305">Los datos en la última fila de la tabla o consulta.</span><span class="sxs-lookup"><span data-stu-id="ea7da-305">The data in the last row of the table or query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-306">FieldCount</span><span class="sxs-lookup"><span data-stu-id="ea7da-306">FieldCount</span></span></p></td>
<td><p><span data-ttu-id="ea7da-307">El número de campos de la tabla o consulta.</span><span class="sxs-lookup"><span data-stu-id="ea7da-307">The number of fields in the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ea7da-308">SQLText</span><span class="sxs-lookup"><span data-stu-id="ea7da-308">SQLText</span></span></p></td>
<td><p><span data-ttu-id="ea7da-309">Una instrucción SQL que representa la tabla o consulta.</span><span class="sxs-lookup"><span data-stu-id="ea7da-309">An SQL statement representing the table or query.</span></span> <span data-ttu-id="ea7da-310">Para las tablas, este elemento devuelve una instrucción SQL en el formulario &quot;seleccione `*` de <em>tabla</em>; &quot;.</span><span class="sxs-lookup"><span data-stu-id="ea7da-310">For tables, this item returns an SQL statement in the form &quot;SELECT `*` FROM <em>table</em>;&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea7da-311">SQLText;<em>n</em></span><span class="sxs-lookup"><span data-stu-id="ea7da-311">SQLText;<em>n</em></span></span></p></td>
<td><p><span data-ttu-id="ea7da-312">Una instrucción SQL, en <em>n</em>-carácter fragmentos, que representa la tabla o consulta, donde <em>n</em> es un entero hasta 256.</span><span class="sxs-lookup"><span data-stu-id="ea7da-312">An SQL statement, in <em>n</em>-character chunks, representing the table or query, where <em>n</em> is an integer up to 256.</span></span> <span data-ttu-id="ea7da-313">Por ejemplo, suponga que una consulta está representada por la siguiente instrucción SQL: el elemento &quot;SQLText; 7&quot; devuelve los siguientes fragmentos delimitado por tabulaciones: el elemento &quot;SQLText; 7&quot; devuelve los siguientes fragmentos delimitado por tabulaciones:</span><span class="sxs-lookup"><span data-stu-id="ea7da-313">For example, suppose a query is represented by the following SQL statement: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks:</span></span></p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><span data-ttu-id="ea7da-314"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="ea7da-314"><<<<<<< HEAD</span></span>
=======
<br/>
>>>>>>> <span data-ttu-id="ea7da-315">master</span><span class="sxs-lookup"><span data-stu-id="ea7da-315">master</span></span>

<span data-ttu-id="ea7da-316">El siguiente ejemplo muestra cómo se puede utilizar DDE en un procedimiento de Visual Basic para solicitar datos de una tabla en la base de datos de ejemplo Northwind e insertar dichos datos en un archivo de texto:</span><span class="sxs-lookup"><span data-stu-id="ea7da-316">The following example shows how you can use DDE in a Visual Basic procedure to request data from a table in the Northwind sample database and insert that data into a text file:</span></span>

```vb
    Sub NorthwindDDE 
        Dim intChan1 As Integer, intChan2 As Integer, intChan3 As Integer 
        Dim strResp1 As Variant, strResp2 As Variant, strResp3 As Variant 
     
        ' In a Visual Basic module, get data from Categories table, 
        ' Catalog query, and Orders table in Northwind.mdb. 
        ' Make sure database is open first. 
        intChan1 = DDEInitiate("MSAccess", "Northwind;TABLE Shippers") 
        intChan2 = DDEInitiate("MSAccess", "Northwind;QUERY Catalog") 
        intChan3 = DDEInitiate("MSAccess", "Northwind;SQL SELECT * " _ 
            & "FROM Orders " _ 
            & "WHERE OrderID > 10050;") 
     
        strResp1 = DDERequest(intChan1, "All") 
        strResp2 = DDERequest(intChan2, "FieldNames;T") 
        strResp3 = DDERequest(intChan3, "FieldNames;T") 
        DDETerminate intChan1 
        DDETerminate intChan2 
        DDETerminate intChan3 
     
        ' Insert data into text file. 
        Open "C:\DATA.TXT" For Append As #1 
        Print #1, strResp1 
        Print #1, strResp2 
        Print #1, strResp3 
        Close #1 
    End Sub
```
