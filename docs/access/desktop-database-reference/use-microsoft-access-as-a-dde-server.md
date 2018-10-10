---
title: Uso de Microsoft Access como servidor DDE
TOCTitle: Use Microsoft Access as a DDE Server
ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15)
ms:contentKeyID: 48546801
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5186349
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 84b4e30877488d84e03839764c1996053e76a2e7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485867"
---
# <a name="use-microsoft-access-as-a-dde-server"></a><span data-ttu-id="eb1c4-102">Uso de Microsoft Access como servidor DDE</span><span class="sxs-lookup"><span data-stu-id="eb1c4-102">Use Microsoft Access as a DDE server</span></span>

<span data-ttu-id="eb1c4-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb1c4-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="eb1c4-p101">Microsoft Access admite el intercambio dinámico de datos (DDE) como aplicación de destino (cliente) o aplicación de origen (servidor). Por ejemplo, una aplicación como Microsoft Word, que actúa como cliente, puede solicitar datos a través de DDE de una base de datos de Microsoft Access que actúa como servidor.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-p101">Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application. For example, an application such as Microsoft Word, acting as a client, can request data through DDE from a Microsoft Access database that's acting as a server.</span></span>

> [!TIP]
> <span data-ttu-id="eb1c4-106">[!SUGERENCIA] Si necesita manipular objetos de Microsoft Access desde otra aplicación, considere la posibilidad de usar Automatización.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-106">If you need to manipulate Microsoft Access objects from another application, you may want to consider using Automation.</span></span>

<span data-ttu-id="eb1c4-p102">Una conversación DDE entre un cliente y un servidor se establece sobre un tema determinado. Un tema puede ser un archivo de datos en el formato admitido por la aplicación servidor o puede ser el tema System, que proporciona información sobre la propia aplicación servidor. Una vez iniciada una conversación sobre un tema determinado, sólo se puede transferir un elemento de datos asociado con dicho tema.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-p102">A DDE conversation between a client and server is established on a particular topic. A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself. Once a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>

<span data-ttu-id="eb1c4-p103">Por ejemplo, suponga que está ejecutando Microsoft Word y desea insertar en un documento datos de una determinada base de datos de Microsoft Access. Para iniciar una conversación DDE con Microsoft Access, abra un canal DDE mediante la función **DDEInitiate** y especifique el nombre del archivo de la base de datos como tema. A continuación, podrá transferir los datos de esa base de datos a Microsoft Word a través de dicho canal.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-p103">For example, suppose you are running Microsoft Word and want to insert data from a particular Microsoft Access database into a document. You begin a DDE conversation with Microsoft Access by opening a DDE channel with the **DDEInitiate** function and specifying the database file name as the topic. You can then transfer data from that database to Microsoft Word through that channel.</span></span>

<span data-ttu-id="eb1c4-113">Como servidor DDE, Microsoft Access admite los siguiente temas:</span><span class="sxs-lookup"><span data-stu-id="eb1c4-113">As a DDE server, Microsoft Access supports the following topics:</span></span>

  - <span data-ttu-id="eb1c4-114">El tema System (Sistema)</span><span class="sxs-lookup"><span data-stu-id="eb1c4-114">The System topic</span></span>

  - <span data-ttu-id="eb1c4-115">El nombre de una base de datos (tema *database (base de datos)*)</span><span class="sxs-lookup"><span data-stu-id="eb1c4-115">The name of a database (*database* topic)</span></span>

  - <span data-ttu-id="eb1c4-116">El nombre de una tabla (tema *tablename (nombretabla)*)</span><span class="sxs-lookup"><span data-stu-id="eb1c4-116">The name of a table (*tablename* topic)</span></span>

  - <span data-ttu-id="eb1c4-117">El nombre de una consulta (tema *queryname (nombreconsulta)*)</span><span class="sxs-lookup"><span data-stu-id="eb1c4-117">The name of a query (*queryname* topic)</span></span>

  - <span data-ttu-id="eb1c4-118">Una cadena SQL de Microsoft Access (tema *sqlstring (cadenasql)*)</span><span class="sxs-lookup"><span data-stu-id="eb1c4-118">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="eb1c4-p104">Sólo después de establecer una conversación DDE, podrá utilizar la instrucción **DDEExecute** para enviar un comando de la aplicación cliente a la aplicación servidor. Cuando se utiliza como servidor DDE, Microsoft Access reconoce los siguientes elementos como un comando válido:</span><span class="sxs-lookup"><span data-stu-id="eb1c4-p104">Once you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application. When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

  - <span data-ttu-id="eb1c4-121">El nombre de una macro en la actual base de datos.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-121">The name of a macro in the current database.</span></span>

  - <span data-ttu-id="eb1c4-122">Cualquier acción que se pueda realizar en Visual Basic mediante uno de los métodos del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-122">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

  - <span data-ttu-id="eb1c4-p105">Las acciones AbrirBaseDeDatos (OpenDatabase) y CerrarBaseDeDatos (CloseDatabase), que se utilizan sólo para las operaciones DDE. (Para ver cómo se utilizan estas funciones, vea el ejemplo que aparece a continuación en este tema.)</span><span class="sxs-lookup"><span data-stu-id="eb1c4-p105">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations. (For an example of how to use these actions, see the example later in this topic.)</span></span>


> [!NOTE]
> <P><span data-ttu-id="eb1c4-p106">[!NOTA] Al especificar una acción de macro como instrucción <STRONG>DDEExecute</STRONG>, la acción y los argumentos siguen la sintaxis del objeto <STRONG>DoCmd</STRONG> y deben ir entre corchetes ([ ]). Sin embargo, las aplicaciones que admiten DDE no reconocen las constantes intrínsecas en las operaciones DDE. Asimismo, los argumentos de cadena deben ir entre comillas (" ") si la cadena contiene una coma. En caso contrario, no son necesarias las comillas.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-p106">When you specify a macro action as a <STRONG>DDEExecute</STRONG> statement, the action and any arguments follow the <STRONG>DoCmd</STRONG> object syntax and must be enclosed in brackets ([ ]). However, applications that support DDE don't recognize intrinsic constants in DDE operations. Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma. Otherwise, quotation marks aren't required.</span></span></P>



<span data-ttu-id="eb1c4-p107">La aplicación cliente puede utilizar la función **DDERequest** para solicitar datos de texto de la aplicación servidor a través de un canal DDE abierto. O bien, el cliente puede utilizar la instrucción **DDEPoke** para enviar datos a la aplicación servidor. Tras finalizar la transferencia de datos, el cliente puede utilizar la instrucción **DDETerminate** para cerrar el canal DDE o la instrucción **DDETerminateAll** para cerrar todos los canales abiertos.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-p107">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel. Or the client can use the **DDEPoke** statement to send data to the server application. Once the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>


> [!NOTE]
> <P><span data-ttu-id="eb1c4-132">[!NOTA] Cuando la aplicación cliente termine de recibir datos a través de un canal DDE, deberá cerrar dicho canal para conservar los recursos de la memoria.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-132">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span></P>



<span data-ttu-id="eb1c4-p108">El siguiente ejemplo muestra cómo se crea un procedimiento de Microsoft Word mediante Visual Basic que utiliza Microsoft Access como servidor DDE. (Para que funcione este ejemplo, Microsoft Access debe estar ejecutándose.)</span><span class="sxs-lookup"><span data-stu-id="eb1c4-p108">The following example demonstrates how to create a Microsoft Word procedure with Visual Basic that uses Microsoft Access as a DDE server. (For this example to work, Microsoft Access must be running.)</span></span>

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

<span data-ttu-id="eb1c4-135">La siguiente sección facilita información sobre los temas DDE válidos que admite Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-135">The following sections provide information about the valid DDE topics supported by Microsoft Access.</span></span>

## <a name="the-system-topic"></a><span data-ttu-id="eb1c4-136">El tema System (Sistema)</span><span class="sxs-lookup"><span data-stu-id="eb1c4-136">The System topic</span></span>

<span data-ttu-id="eb1c4-137">El tema System es un tema estándar para todas las aplicaciones basadas en Windows de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-137">The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="eb1c4-138">Facilita información sobre los demás temas que admite la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-138">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="eb1c4-139">Para obtener acceso a esta información, el código debe llamar primero a la función **DDEInitiate** con como el argumento *tema* y, a continuación, ejecutar la instrucción **DDERequest** con uno de los siguientes para el argumento de *elemento* .</span><span class="sxs-lookup"><span data-stu-id="eb1c4-139">To access this information, your code must first call the **DDEInitiate** function with as the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb1c4-140">Elemento</span><span class="sxs-lookup"><span data-stu-id="eb1c4-140">Item</span></span></p></th>
<th><p><span data-ttu-id="eb1c4-141">Devuelve</span><span class="sxs-lookup"><span data-stu-id="eb1c4-141">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb1c4-142">SysItems</span><span class="sxs-lookup"><span data-stu-id="eb1c4-142">SysItems</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-143">Una lista de elementos que admite el tema System en Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-143">A list of items supported by the System topic in Microsoft Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1c4-144">Formats</span><span class="sxs-lookup"><span data-stu-id="eb1c4-144">Formats</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-145">Una lista de formatos que Microsoft Access puede copiar al Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-145">A list of the formats Microsoft Access can copy onto the Clipboard.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb1c4-146">Status</span><span class="sxs-lookup"><span data-stu-id="eb1c4-146">Status</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-147">&quot;Ocupado&quot; o &quot;listo&quot;.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-147">&quot;Busy&quot; or &quot;Ready&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1c4-148">Topics</span><span class="sxs-lookup"><span data-stu-id="eb1c4-148">Topics</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-149">Una lista de todas las bases de datos abiertas.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-149">A list of all open databases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eb1c4-150">El siguiente ejemplo muestra cómo se utilizan las funciones **DDEIniciar (DDEInitiate)** y **DDEPedido (DDERequest)** con el tema System:</span><span class="sxs-lookup"><span data-stu-id="eb1c4-150">The following example demonstrates the use of the **DDEInitiate** and **DDERequest** functions with the System topic:</span></span>

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

## <a name="the-database-topic"></a><span data-ttu-id="eb1c4-151">El tema de la base de datos</span><span class="sxs-lookup"><span data-stu-id="eb1c4-151">The database topic</span></span>

<span data-ttu-id="eb1c4-152">El tema de la *base de datos* es el nombre de archivo de base de datos existente.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-152">The *database* topic is the file name of an existing database.</span></span> <span data-ttu-id="eb1c4-153">Puede escribir simplemente el nombre (Northwind) o su ruta de acceso y la extensión .mdb (C:\\Access\\ejemplos\\Neptuno.mdb).</span><span class="sxs-lookup"><span data-stu-id="eb1c4-153">You can type either just the base name (Northwind), or its path and .mdb extension (C:\\Access\\Samples\\Northwind.mdb).</span></span> <span data-ttu-id="eb1c4-154">Tras iniciar una conversación DDE con la base de datos, puede solicitar una lista de los objetos incluidos en dicha base de datos.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-154">After you start a DDE conversation with the database, you can request a list of the objects in that database.</span></span>


> [!NOTE]
> <P><span data-ttu-id="eb1c4-155">[!NOTA] No se puede utilizar DDE para consultar el archivo de información de grupo de trabajo de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-155">You can't use DDE to query the Microsoft Access workgroup information file.</span></span></P>



<span data-ttu-id="eb1c4-156">El tema *database* admite los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-156">The *database* topic supports the following items.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb1c4-157">Elemento</span><span class="sxs-lookup"><span data-stu-id="eb1c4-157">Item</span></span></p></th>
<th><p><span data-ttu-id="eb1c4-158">Devuelve</span><span class="sxs-lookup"><span data-stu-id="eb1c4-158">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb1c4-159">ListaDeTablas</span><span class="sxs-lookup"><span data-stu-id="eb1c4-159">TableList</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-160">Una lista de tablas.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-160">A list of tables.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1c4-161">QueryList</span><span class="sxs-lookup"><span data-stu-id="eb1c4-161">QueryList</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-162">Una lista de consultas.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-162">A list of queries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb1c4-163">FormList</span><span class="sxs-lookup"><span data-stu-id="eb1c4-163">FormList</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-164">Una lista de formularios.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-164">A list of forms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1c4-165">ReportList</span><span class="sxs-lookup"><span data-stu-id="eb1c4-165">ReportList</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-166">Una lista de informes.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-166">A list of reports.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb1c4-167">MacroList</span><span class="sxs-lookup"><span data-stu-id="eb1c4-167">MacroList</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-168">Una lista de macros.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-168">A list of macros.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1c4-169">ModuleList</span><span class="sxs-lookup"><span data-stu-id="eb1c4-169">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-170">Una lista de módulos.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-170">A list of modules.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb1c4-171">ViewList</span><span class="sxs-lookup"><span data-stu-id="eb1c4-171">ViewList</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-172">Una lista de vistas</span><span class="sxs-lookup"><span data-stu-id="eb1c4-172">A list of views</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1c4-173">StoredProcedureList</span><span class="sxs-lookup"><span data-stu-id="eb1c4-173">StoredProcedureList</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-174">Una lista de procedimientos almacenados</span><span class="sxs-lookup"><span data-stu-id="eb1c4-174">A list of stored procedures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb1c4-175">DatabaseDiagramList</span><span class="sxs-lookup"><span data-stu-id="eb1c4-175">DatabaseDiagramList</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-176">Una lista de diagramas de base de datos</span><span class="sxs-lookup"><span data-stu-id="eb1c4-176">A list of database diagrams</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eb1c4-177">El siguiente ejemplo muestra cómo se puede abrir el formulario Empleados en la base de datos de ejemplo Northwind desde un procedimiento de Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="eb1c4-177">The following example shows how you can open the Employees form in the Northwind sample database from a Visual Basic procedure:</span></span>

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

## <a name="the-table-topic"></a><span data-ttu-id="eb1c4-178">El tema de la tabla</span><span class="sxs-lookup"><span data-stu-id="eb1c4-178">The TABLE topic</span></span>

<span data-ttu-id="eb1c4-179">Estos temas utilizan la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="eb1c4-179">These topics use the following syntax:</span></span>

<span data-ttu-id="eb1c4-180">_databasename_ ; **Tabla** _TableName_</span><span class="sxs-lookup"><span data-stu-id="eb1c4-180">_databasename_ ; **TABLE** _tablename_</span></span>

<span data-ttu-id="eb1c4-181">_databasename_ ; **Consulta** _nombreconsulta_</span><span class="sxs-lookup"><span data-stu-id="eb1c4-181">_databasename_ ; **QUERY** _queryname_</span></span>

<span data-ttu-id="eb1c4-182">_databasename_ ; **SQL** [ _cadenasql_ ]</span><span class="sxs-lookup"><span data-stu-id="eb1c4-182">_databasename_ ; **SQL** [ _sqlstring_ ]</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb1c4-183">Parte</span><span class="sxs-lookup"><span data-stu-id="eb1c4-183">Part</span></span></p></th>
<th><p><span data-ttu-id="eb1c4-184">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb1c4-184">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb1c4-185"><em>nombrebasedatos</em></span><span class="sxs-lookup"><span data-stu-id="eb1c4-185"><em>databasename</em></span></span></p></td>
<td><p><span data-ttu-id="eb1c4-p111">El nombre de la base de datos donde se encuentra la tabla o consulta o a la que se aplica la instrucción SQL, seguido de un punto y coma (;). El nombre de la base de datos puede ser simplemente el nombre (Northwind) o su ruta de acceso completa y la extensión .mdb (C:\Access\Samples\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="eb1c4-p111">The name of the database that the table or query is in or that the SQL statement applies to, followed by a semicolon (;). The database name can be just the base name (Northwind) or its full path and .mdb extension (C:\Access\Samples\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1c4-188"><em>nombretabla</em></span><span class="sxs-lookup"><span data-stu-id="eb1c4-188"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="eb1c4-189">El nombre de una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-189">The name of an existing table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb1c4-190"><em>nombreconsulta</em></span><span class="sxs-lookup"><span data-stu-id="eb1c4-190"><em>queryname</em></span></span></p></td>
<td><p><span data-ttu-id="eb1c4-191">El nombre de una consulta existente.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-191">The name of an existing query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1c4-192"><em>sqlstring</em></span><span class="sxs-lookup"><span data-stu-id="eb1c4-192"><em>sqlstring</em></span></span></p></td>
<td><p><span data-ttu-id="eb1c4-193">Una instrucción SQL válida hasta 256 caracteres de longitud, que terminan con un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-193">A valid SQL statement up to 256 characters long, ending with a semicolon.</span></span> <span data-ttu-id="eb1c4-194">Para intercambiar más de 256 caracteres, omita este argumento y utilice instrucciones <strong>DDEPoke</strong> sucesivas para generar una instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-194">To exchange more than 256 characters, omit this argument and instead use successive <strong>DDEPoke</strong> statements to build an SQL statement.</span></span> <span data-ttu-id="eb1c4-195">Por ejemplo, el siguiente código de Visual Basic utiliza la instrucción <strong>DDEPoke</strong> para generar una instrucción SQL y, a continuación, solicita los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-195">For example, the following Visual Basic code uses the <strong>DDEPoke</strong> statement to build an SQL statement and then request the results of the query.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="eb1c4-196">La siguiente tabla muestra los elementos válidos para los temas TABLA *nombretabla*, CONSULTA *nombreconsulta* y SQL *cadenasql*.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-196">The following table lists the valid items for the TABLE *tablename*, QUERY *queryname*, and SQL *sqlstring* topics.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb1c4-197">Elemento</span><span class="sxs-lookup"><span data-stu-id="eb1c4-197">Item</span></span></p></th>
<th><p><span data-ttu-id="eb1c4-198">Devuelve</span><span class="sxs-lookup"><span data-stu-id="eb1c4-198">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb1c4-199">Todos</span><span class="sxs-lookup"><span data-stu-id="eb1c4-199">All</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-200">Todos los datos de la tabla, incluidos los nombres de campo.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-200">All the data in the table, including field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1c4-201">Datos</span><span class="sxs-lookup"><span data-stu-id="eb1c4-201">Data</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-202">Todas las filas de datos, sin los nombres de campo.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-202">All rows of data, without field names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb1c4-203">FieldNames</span><span class="sxs-lookup"><span data-stu-id="eb1c4-203">FieldNames</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-204">Una lista de una sola fila con los nombres de campo.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-204">A single-row list of field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1c4-205">FieldNames; T</span><span class="sxs-lookup"><span data-stu-id="eb1c4-205">FieldNames;T</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-206">Una lista de dos filas con los nombres de campo (primera fila) y los tipos de datos (segunda fila).</span><span class="sxs-lookup"><span data-stu-id="eb1c4-206">A two-row list of field names (first row) and their data types (second row).</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="eb1c4-207">Éstos son los valores devueltos y los tipos de datos que representan.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-207">These are the values returned and the data types they represent:</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="eb1c4-208"><b>Valor</b></span><span class="sxs-lookup"><span data-stu-id="eb1c4-208"><b>Value</b></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="eb1c4-209">0</span><span class="sxs-lookup"><span data-stu-id="eb1c4-209">0</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="eb1c4-210">1</span><span class="sxs-lookup"><span data-stu-id="eb1c4-210">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="eb1c4-211">2</span><span class="sxs-lookup"><span data-stu-id="eb1c4-211">2</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="eb1c4-212">3</span><span class="sxs-lookup"><span data-stu-id="eb1c4-212">3</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="eb1c4-213">4</span><span class="sxs-lookup"><span data-stu-id="eb1c4-213">4</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="eb1c4-214">5</span><span class="sxs-lookup"><span data-stu-id="eb1c4-214">5</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="eb1c4-215">6</span><span class="sxs-lookup"><span data-stu-id="eb1c4-215">6</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="eb1c4-216">7</span><span class="sxs-lookup"><span data-stu-id="eb1c4-216">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="eb1c4-217">8</span><span class="sxs-lookup"><span data-stu-id="eb1c4-217">8</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="eb1c4-218">9</span><span class="sxs-lookup"><span data-stu-id="eb1c4-218">9</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="eb1c4-219">10</span><span class="sxs-lookup"><span data-stu-id="eb1c4-219">10</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="eb1c4-220">11</span><span class="sxs-lookup"><span data-stu-id="eb1c4-220">11</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="eb1c4-221">12</span><span class="sxs-lookup"><span data-stu-id="eb1c4-221">12</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1c4-222">NextRow</span><span class="sxs-lookup"><span data-stu-id="eb1c4-222">NextRow</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-p113">Los datos en la siguiente fila de la tabla o consulta. Al abrir un canal, NextRow devuelve los datos de la primera fila. Si la fila actual es el último registro y ejecuta NextRow, se produce un error en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-p113">The data in the next row in the table or query. When you open a channel, NextRow returns the data in the first row. If the current row is the last record and you run NextRow, the request fails.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb1c4-226">PrevRow</span><span class="sxs-lookup"><span data-stu-id="eb1c4-226">PrevRow</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-p114">Los datos en la fila anterior de la tabla o consulta. Si PrevRow es la primera solicitud en un nuevo canal, se devolverán los datos en la última fila de la tabla o consulta. Si el primer registro es la fila actual, se produce un error en la solicitud de PrevRow.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-p114">The data in the previous row in the table or query. If PrevRow is the first request on a new channel, the data in the last row of the table or query is returned. If the first record is the current row, the request for PrevRow fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1c4-230">FirstRow</span><span class="sxs-lookup"><span data-stu-id="eb1c4-230">FirstRow</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-231">Los datos en la primera fila de la tabla o consulta.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-231">The data in the first row of the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb1c4-232">LastRow</span><span class="sxs-lookup"><span data-stu-id="eb1c4-232">LastRow</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-233">Los datos en la última fila de la tabla o consulta.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-233">The data in the last row of the table or query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1c4-234">FieldCount</span><span class="sxs-lookup"><span data-stu-id="eb1c4-234">FieldCount</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-235">El número de campos de la tabla o consulta.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-235">The number of fields in the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb1c4-236">SQLText</span><span class="sxs-lookup"><span data-stu-id="eb1c4-236">SQLText</span></span></p></td>
<td><p><span data-ttu-id="eb1c4-237">Una instrucción SQL que representa la tabla o consulta.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-237">An SQL statement representing the table or query.</span></span> <span data-ttu-id="eb1c4-238">Para las tablas, este elemento devuelve una instrucción SQL en el formulario &quot;seleccione `*` de <em>tabla</em>; &quot;.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-238">For tables, this item returns an SQL statement in the form &quot;SELECT `*` FROM <em>table</em>;&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb1c4-239">SQLText;<em>n</em></span><span class="sxs-lookup"><span data-stu-id="eb1c4-239">SQLText;<em>n</em></span></span></p></td>
<td><p><span data-ttu-id="eb1c4-240">Una instrucción SQL, en <em>n</em>-carácter fragmentos, que representa la tabla o consulta, donde <em>n</em> es un entero hasta 256.</span><span class="sxs-lookup"><span data-stu-id="eb1c4-240">An SQL statement, in <em>n</em>-character chunks, representing the table or query, where <em>n</em> is an integer up to 256.</span></span> <span data-ttu-id="eb1c4-241">Por ejemplo, suponga que una consulta está representada por la siguiente instrucción SQL: el elemento &quot;SQLText; 7&quot; devuelve los siguientes fragmentos delimitado por tabulaciones: el elemento &quot;SQLText; 7&quot; devuelve los siguientes fragmentos delimitado por tabulaciones:</span><span class="sxs-lookup"><span data-stu-id="eb1c4-241">For example, suppose a query is represented by the following SQL statement: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks:</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eb1c4-242">El siguiente ejemplo muestra cómo se puede utilizar DDE en un procedimiento de Visual Basic para solicitar datos de una tabla en la base de datos de ejemplo Northwind e insertar dichos datos en un archivo de texto:</span><span class="sxs-lookup"><span data-stu-id="eb1c4-242">The following example shows how you can use DDE in a Visual Basic procedure to request data from a table in the Northwind sample database and insert that data into a text file:</span></span>

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
