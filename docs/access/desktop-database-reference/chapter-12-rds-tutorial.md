---
title: 'Capítulo 12: Tutorial de servicio de datos remotos (RDS)'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fb29fd070a693b608cede1d21329b3749c18e852
ms.sourcegitcommit: 007141520d6479860f452371532f9267f33eb260
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999504"
---
# <a name="chapter-12-remote-data-service-rds-tutorial"></a><span data-ttu-id="df27e-102">Capítulo 12: Tutorial de servicio de datos remotos (RDS)</span><span class="sxs-lookup"><span data-stu-id="df27e-102">Chapter 12: Remote Data Service (RDS) tutorial</span></span>

<span data-ttu-id="df27e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df27e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df27e-104">Este tutorial muestra el uso del modelo de programación RDS para consultar y actualizar un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="df27e-104">This tutorial illustrates using the RDS programming model to query and update a data source.</span></span> <span data-ttu-id="df27e-105">Primero, describe los pasos necesarios para realizar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="df27e-105">First, it describes the steps necessary to accomplish this task.</span></span> <span data-ttu-id="df27e-106">A continuación, se repite el tutorial en Microsoft Visual Basic Scripting Edition y Microsoft Visual J ++, que cuenta con ADO para Windows Foundation Classes (ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="df27e-106">Then the tutorial is repeated in Microsoft Visual Basic Scripting Edition and Microsoft Visual J++, featuring ADO for Windows Foundation Classes (ADO/WFC).</span></span>

<span data-ttu-id="df27e-107">Este tutorial se codifica en diferentes lenguajes por dos motivos:</span><span class="sxs-lookup"><span data-stu-id="df27e-107">This tutorial is coded in different languages for two reasons:</span></span>

- <span data-ttu-id="df27e-p102">La documentación para RDS supone que el lector codifica en Visual Basic. Esto hace que la documentación sea más apropiada para programadores de Visual Basic, pero menos útil para los que utilizan otros lenguajes.</span><span class="sxs-lookup"><span data-stu-id="df27e-p102">The documentation for RDS assumes the reader codes in Visual Basic. This makes the documentation convenient for Visual Basic programmers, but less useful for programmers who use other languages.</span></span>

- <span data-ttu-id="df27e-110">Si no está seguro de una determinada función de RDS y conoce algo de otro lenguaje, podría resolver sus dudas buscando la misma característica expresada en el otro lenguaje.</span><span class="sxs-lookup"><span data-stu-id="df27e-110">If you are uncertain about a particular RDS feature and you know a little of another language, you might be able to resolve your question by looking for the same feature expressed in another language.</span></span>

<span data-ttu-id="df27e-p103">Este tutorial se basa en el modelo de programación RDS. Analiza individualmente cada paso del modelo de programación. Además, ilustra cada paso con un fragmento de código de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="df27e-p103">This tutorial is based on the RDS programming model. It discusses each step of the programming model individually. In addition, it illustrates each step with a fragment of Visual Basic code.</span></span>

<span data-ttu-id="df27e-p104">El ejemplo de código se repite en otros lenguajes con una mínima descripción. Cada paso de un tutorial de un lenguaje de programación dado está marcado con el paso correspondiente del tutorial descriptivo y del modelo de programación. Utilice el número del paso como referencia a la explicación del tutorial descriptivo.</span><span class="sxs-lookup"><span data-stu-id="df27e-p104">The code example is repeated in other languages with minimal discussion. Each step in a given programming language tutorial is marked with the corresponding step in the programming model and descriptive tutorial. Use the number of the step to refer to the discussion in the descriptive tutorial.</span></span>

<span data-ttu-id="df27e-p105">El modelo de programación RDS se especifica a continuación. Úselo como una guía mientras avanza en el tutorial.</span><span class="sxs-lookup"><span data-stu-id="df27e-p105">The RDS programming model is stated below. Use it as a roadmap as you proceed through the tutorial.</span></span>

### <a name="rds-programming-model-with-objects"></a><span data-ttu-id="df27e-119">Modelo de programación de RDS con objetos</span><span class="sxs-lookup"><span data-stu-id="df27e-119">RDS programming model with objects</span></span>

- <span data-ttu-id="df27e-120">Especifique el programa que se va a invocar en el servidor y obtenga una forma (proxy) de hacer referencia al mismo desde el cliente.</span><span class="sxs-lookup"><span data-stu-id="df27e-120">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client.</span></span>

- <span data-ttu-id="df27e-p106">Llame al programa de servidor. Pásele los parámetros que identifican el origen de datos y el comando que se desea emitir.</span><span class="sxs-lookup"><span data-stu-id="df27e-p106">Invoke the server program. Pass parameters to the server program that identifies the data source and the command to issue.</span></span>

- <span data-ttu-id="df27e-p107">Normalmente, el programa de servidor obtiene un objeto [Recordset](recordset-object-ado.md) desde el origen de datos utilizando ADO. Opcionalmente, el objeto **Recordset** se procesa en el servidor.</span><span class="sxs-lookup"><span data-stu-id="df27e-p107">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO. Optionally, the **Recordset** object is processed on the server.</span></span>

- <span data-ttu-id="df27e-125">El programa de servidor devuelve el objeto **Recordset** final a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="df27e-125">The server program returns the final **Recordset** object to the client application.</span></span>

- <span data-ttu-id="df27e-126">En el cliente, el objeto **Recordset** se coloca opcionalmente en un formulario que se puede usar fácilmente mediante controles visuales.</span><span class="sxs-lookup"><span data-stu-id="df27e-126">On the client, the **Recordset** object is optionally put into a form that can be easily used by visual controls.</span></span>

- <span data-ttu-id="df27e-127">Los cambios realizados en el objeto **Recordset** se envían al servidor y se usan para actualizar el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="df27e-127">Changes to the **Recordset** object are sent back to the server and used to update the data source.</span></span>

## <a name="step-1-specify-a-server-program"></a><span data-ttu-id="df27e-128">Paso 1: Especificar un programa de servidor</span><span class="sxs-lookup"><span data-stu-id="df27e-128">Step 1: Specify a server program</span></span>

<span data-ttu-id="df27e-p108">En el caso más general, use el método [CreateObject](createobject-method-rds.md) del objeto [RDS.DataSpace](dataspace-object-rds.md) para especificar el programa predeterminado de servidor, [RDSServer.DataFactory](datafactory-object-rdsserver.md), o su propio programa de servidor personalizado (objeto de negocio). Se crea entonces una instancia del programa de servidor en el servidor y se devuelve una referencia (o *proxy*) al programa de servidor.</span><span class="sxs-lookup"><span data-stu-id="df27e-p108">In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object). A server program is instantiated on the server, and a reference to the server program, or *proxy*, is returned.</span></span>

<span data-ttu-id="df27e-131">Este tutorial utiliza el programa de servidor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="df27e-131">This tutorial uses the default server program:</span></span>

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
``` 

## <a name="step-2-invoke-the-server-program"></a><span data-ttu-id="df27e-132">Paso 2: Llamar al programa de servidor</span><span class="sxs-lookup"><span data-stu-id="df27e-132">Step 2: Invoke the server program</span></span> 

<span data-ttu-id="df27e-p109">Cuando se llama a un método en el *proxy* cliente, el programa real en el servidor ejecuta el método. En este paso, se ejecutará una consulta en el servidor.</span><span class="sxs-lookup"><span data-stu-id="df27e-p109">When you invoke a method on the client *proxy*, the actual program on the server executes the method. In this step, you'll execute a query on the server.</span></span>

### <a name="part-a"></a><span data-ttu-id="df27e-135">Parte A</span><span class="sxs-lookup"><span data-stu-id="df27e-135">Part A</span></span>

<span data-ttu-id="df27e-136">Si no utilizo [RDSServer.DataFactory](datafactory-object-rdsserver.md) en este tutorial, la forma más conveniente para realizar este paso sería utilizar el [RDS. DataControl](datacontrol-object-rds.md) objeto.</span><span class="sxs-lookup"><span data-stu-id="df27e-136">If you weren't using [RDSServer.DataFactory](datafactory-object-rdsserver.md) in this tutorial, the most convenient way to perform this step would be to use the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="df27e-137">El objeto **RDS.DataControl** combina el paso anterior de crear un proxy con este paso que emite la consulta.</span><span class="sxs-lookup"><span data-stu-id="df27e-137">The **RDS.DataControl** combines the previous step of creating a proxy, with this step, issuing the query.</span></span>

1. <span data-ttu-id="df27e-138">Establecer el **RDS. DataControl** propiedad [Server](server-property-rds.md) para identificar donde se debe crear una instancia del programa de servidor de objetos.</span><span class="sxs-lookup"><span data-stu-id="df27e-138">Set the **RDS.DataControl** object [Server](server-property-rds.md) property to identify where the server program should be instantiated.</span></span>

2. <span data-ttu-id="df27e-139">Establecer la propiedad [Connect](connect-property-rds.md) para especificar la cadena de conexión para obtener acceso al origen de datos.</span><span class="sxs-lookup"><span data-stu-id="df27e-139">Set the [Connect](connect-property-rds.md) property to specify the connect string to access the data source.</span></span>

3. <span data-ttu-id="df27e-140">Establezca la propiedad [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) para especificar el texto de comando de la consulta.</span><span class="sxs-lookup"><span data-stu-id="df27e-140">Set the [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) property to specify the query command text.</span></span> 

4. <span data-ttu-id="df27e-141">Emita el método [Refresh](refresh-method-rds.md) para hacer que el programa de servidor para conectarse al origen de datos, recupere las filas especificadas por la consulta y devolver un objeto **Recordset** al cliente.</span><span class="sxs-lookup"><span data-stu-id="df27e-141">Issue the [Refresh](refresh-method-rds.md) method to cause the server program to connect to the data source, retrieve rows specified by the query, and return a **Recordset** object to the client.</span></span>

<span data-ttu-id="df27e-142">Este tutorial no utiliza el objeto **RDS.DataControl**, pero, en caso de utilizarlo, sería del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="df27e-142">This tutorial does not use the **RDS.DataControl**, but this is how it would look if it did:</span></span>

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<br/>

<span data-ttu-id="df27e-143">El tutorial tampoco llama a RDS con objetos de ADO, pero, en caso de hacerlo, sería del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="df27e-143">Nor does the tutorial invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

### <a name="part-b"></a><span data-ttu-id="df27e-144">Parte B</span><span class="sxs-lookup"><span data-stu-id="df27e-144">Part B</span></span>

<span data-ttu-id="df27e-145">El método general de realizar este paso consiste en invocar el método [Query](query-method-rds.md) del objeto **RDSServer.DataFactory** .</span><span class="sxs-lookup"><span data-stu-id="df27e-145">The general method of performing this step is to invoke the **RDSServer.DataFactory** object [Query](query-method-rds.md) method.</span></span> <span data-ttu-id="df27e-146">Ese método toma una cadena de conexión, que se utiliza para conectar con un origen de datos, y un texto de comando, utilizado para especificar las filas devueltas desde el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="df27e-146">That method takes a connect string, which is used to connect to a data source, and a command text, which is used to specify the rows to be returned from the data source.</span></span>

<span data-ttu-id="df27e-147">Este tutorial utiliza el método **Query** del objeto **DataFactory**:</span><span class="sxs-lookup"><span data-stu-id="df27e-147">This tutorial uses the **DataFactory** object **Query** method:</span></span>

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-3-server-obtains-a-recordset"></a><span data-ttu-id="df27e-148">Paso 3: El servidor obtiene un objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="df27e-148">Step 3: Server obtains a Recordset</span></span> 

<span data-ttu-id="df27e-p112">El programa servidor usa el texto del comando y la cadena de conexión para solicitar al origen de datos las filas deseadas. Normalmente, se utiliza ADO para recuperar este objeto **Recordset**, aunque también se podrían usar otras interfaces de acceso a datos de Microsoft, tales como OLE DB.</span><span class="sxs-lookup"><span data-stu-id="df27e-p112">The server program uses the connect string and command text to query the data source for the desired rows. ADO is typically used to retrieve this **Recordset**, although other Microsoft data access interfaces, such as OLE DB, could be used.</span></span>

<span data-ttu-id="df27e-151">El aspecto de un programa servidor personalizado puede ser el siguiente:</span><span class="sxs-lookup"><span data-stu-id="df27e-151">A custom server program might look like this:</span></span>

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

## <a name="step-4-server-returns-the-recordset"></a><span data-ttu-id="df27e-152">Paso 4: El servidor devuelve el objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="df27e-152">Step 4: Server returns the Recordset</span></span> 

<span data-ttu-id="df27e-p113">RDS convierte el objeto **Recordset** recuperado en un formulario que se puede devolver al cliente (es decir, *reorganiza* el objeto **Recordset**). La forma exacta de la conversión y de cómo se envía depende de si el servidor está en Internet o en una intranet, en una red de área local, o de si se trata de una biblioteca de vínculos dinámicos (dll). No obstante, este detalle no es crítico: lo que importa es que RDS devuelva el objeto **Recordset** al cliente.</span><span class="sxs-lookup"><span data-stu-id="df27e-p113">RDS converts the retrieved **Recordset** object to a form that can be sent back to the client (that is, it *marshals* the **Recordset**). The exact form of the conversion and how it is sent depends on whether the server is on the Internet or an intranet, a local area network, or is a dynamic-link library. However, this detail is not critical; all that matters is that RDS sends the **Recordset** back to the client.</span></span>

<span data-ttu-id="df27e-156">En el cliente, se recibe un objeto **Recordset** y se asigna a una variable local.</span><span class="sxs-lookup"><span data-stu-id="df27e-156">On the client side, a **Recordset** object is returned and assigned to a local variable.</span></span>

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-5-datacontrol-is-made-usable"></a><span data-ttu-id="df27e-157">Paso 5: DataControl se facilita</span><span class="sxs-lookup"><span data-stu-id="df27e-157">Step 5: DataControl is made usable</span></span> 

<span data-ttu-id="df27e-p114">El objeto **Recordset** devuelto está disponible para su uso. Puede examinarlo, navegar por él o editarlo como lo haría con cualquier otro objeto **Recordset**. Las operaciones que se pueden realizar con **Recordset** dependen del entorno disponible. Visual Basic y Visual C++ poseen controles visuales que pueden usar un objeto **Recordset** directa o indirectamente con la ayuda de un control de datos.</span><span class="sxs-lookup"><span data-stu-id="df27e-p114">The returned **Recordset** object is available for use. You can examine, navigate, or edit it as you would any other **Recordset**. What you can do with the **Recordset** depends on your environment. Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="df27e-162">Por ejemplo, si va a mostrar una página Web en Internet Explorer, es posible que desea mostrar los datos del objeto **Recordset** en un control visual.</span><span class="sxs-lookup"><span data-stu-id="df27e-162">For example, if you are displaying a webpage in Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="df27e-163">Los controles visuales de una página Web no pueden tener acceso a un objeto **Recordset** directamente.</span><span class="sxs-lookup"><span data-stu-id="df27e-163">Visual controls on a webpage cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="df27e-164">Sin embargo, pueden obtener acceso al objeto **Recordset** por medio del objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="df27e-164">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="df27e-165">El **RDS.DataControl** puede ser utilizado por un control visual cuando su propiedad [SourceRecordset](recordset-sourcerecordset-properties-rds.md) se establece en el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="df27e-165">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>

<span data-ttu-id="df27e-166">El objeto control visual debe tener su parámetro **DATASRC** establecido con el valor del **RDS.DataControl**, y su propiedad **DATAFLD** con el valor de un campo (columna) del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="df27e-166">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="df27e-167">En este tutorial, establezca la propiedad **SourceRecordset**:</span><span class="sxs-lookup"><span data-stu-id="df27e-167">In this tutorial, set the **SourceRecordset** property:</span></span>

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

## <a name="step-6-changes-are-sent-to-the-server"></a><span data-ttu-id="df27e-168">Paso 6: Los cambios se envían al servidor</span><span class="sxs-lookup"><span data-stu-id="df27e-168">Step 6: Changes are sent to the server</span></span>

<span data-ttu-id="df27e-169">Si se modifica el objeto **Recordset**, cualquier cambio (es decir, filas que se agregan, modifican o eliminan) se puede enviar de nuevo al servidor.</span><span class="sxs-lookup"><span data-stu-id="df27e-169">If the **Recordset** object is edited, any changes (that is, rows that are added, changed, or deleted) can be sent back to the server.</span></span>

<span data-ttu-id="df27e-170">El comportamiento predeterminado de RDS se puede invocar implícitamente con objetos ADO y el proveedor de servicios remotos de Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="df27e-170">The default behavior of RDS can be invoked implicitly with ADO objects and the Microsoft OLE DB Remoting Provider.</span></span> <span data-ttu-id="df27e-171">Las consultas pueden devolver **conjuntos de registros**y editado **los conjuntos de registros** pueden actualizar el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="df27e-171">Queries can return **Recordsets**, and edited **Recordsets** can update the data source.</span></span> <span data-ttu-id="df27e-172">En este tutorial no utiliza RDS con objetos ADO, pero este es el aspecto que tendría si lo hiciera:</span><span class="sxs-lookup"><span data-stu-id="df27e-172">This tutorial does not invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

### <a name="part-a"></a><span data-ttu-id="df27e-173">Parte A</span><span class="sxs-lookup"><span data-stu-id="df27e-173">Part A</span></span>

<span data-ttu-id="df27e-174">Suponga para este caso que sólo ha utilizado el [RDS. DataControl](datacontrol-object-rds.md) y que un objeto **Recordset** está ahora asociado con el **RDS. DataControl**.</span><span class="sxs-lookup"><span data-stu-id="df27e-174">Assume for this case that you have only used the [RDS.DataControl](datacontrol-object-rds.md) and that a **Recordset** object is now associated with the **RDS.DataControl**.</span></span> <span data-ttu-id="df27e-175">El método [SubmitChanges](submitchanges-method-rds.md) actualiza el origen de datos con los cambios del objeto **Recordset** si las propiedades [Server](server-property-rds.md) y [Connect](connect-property-rds.md) están establecidas.</span><span class="sxs-lookup"><span data-stu-id="df27e-175">The [SubmitChanges](submitchanges-method-rds.md) method updates the data source with any changes to the **Recordset** object if the [Server](server-property-rds.md) and [Connect](connect-property-rds.md) properties are still set.</span></span>

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

### <a name="part-b"></a><span data-ttu-id="df27e-176">Parte B</span><span class="sxs-lookup"><span data-stu-id="df27e-176">Part B</span></span>

<span data-ttu-id="df27e-177">Como alternativa, podría actualizar el servidor con el objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md) , especificando una conexión y un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="df27e-177">Alternatively, you could update the server with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, specifying a connection and a **Recordset** object.</span></span>

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


## <a name="appendix-a-rds-tutorial-vbscript"></a><span data-ttu-id="df27e-178">Apéndice A: tutorial de RDS (VBScript)</span><span class="sxs-lookup"><span data-stu-id="df27e-178">Appendix A: RDS tutorial (VBScript)</span></span>

<span data-ttu-id="df27e-179">Este es el tutorial de RDS, escrito en Microsoft Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="df27e-179">This is the RDS tutorial, written in Microsoft Visual Basic Scripting Edition.</span></span> <span data-ttu-id="df27e-180">Para obtener una descripción del propósito de este tutorial, vea la introducción a este tema.</span><span class="sxs-lookup"><span data-stu-id="df27e-180">For a description of the purpose of this tutorial, see the introduction to this topic.</span></span>

<span data-ttu-id="df27e-181">En este tutorial, [RDS. DataControl](datacontrol-object-rds.md) y [RDS. DataSpace](dataspace-object-rds.md) se crean en tiempo de diseño; es decir, se definen con etiquetas de objeto.</span><span class="sxs-lookup"><span data-stu-id="df27e-181">In this tutorial, [RDS.DataControl](datacontrol-object-rds.md) and [RDS.DataSpace](dataspace-object-rds.md) are created at design time; that is, they are defined with object tags.</span></span> <span data-ttu-id="df27e-182">De forma alternativa, se podrían crear en tiempo de ejecución con el método **Server.CreateObject**.</span><span class="sxs-lookup"><span data-stu-id="df27e-182">Alternatively, they could be created at run time with the **Server.CreateObject** method.</span></span> 

<span data-ttu-id="df27e-183">Por ejemplo, el objeto **RDS.DataControl** se crearía del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="df27e-183">For example, the **RDS.DataControl** object could be created like this:</span></span>

```vb
    Set DC = Server.CreateObject("RDS.DataControl") 
     <!-- RDS.DataControl --> 
     <OBJECT 
     ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"> 
     </OBJECT> 
     
     <!-- RDS.DataSpace --> 
     <OBJECT 
     ID="DS1" WIDTH=1 HEIGHT=1 
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"> 
     </OBJECT> 
     
     <SCRIPT LANGUAGE="VBScript"> 
     
     Sub RDSTutorial() 
     Dim DF1 
```

### <a name="step-1-specify-a-server-program"></a><span data-ttu-id="df27e-184">Paso 1: Especificar un programa de servidor</span><span class="sxs-lookup"><span data-stu-id="df27e-184">Step 1: Specify a server program</span></span>

<span data-ttu-id="df27e-185">VBScript puede descubrir el nombre del servidor web IIS que se está ejecutando mediante el método **Request.ServerVariables** de VBScript disponible para páginas Active Server:</span><span class="sxs-lookup"><span data-stu-id="df27e-185">VBScript can discover the name of the IIS web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages:</span></span>

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

<span data-ttu-id="df27e-186">Sin embargo, para este tutorial, utilice el servidor imaginario "yourServer".</span><span class="sxs-lookup"><span data-stu-id="df27e-186">However, for this tutorial, use the imaginary server, "yourServer."</span></span>

> [!NOTE]
> <span data-ttu-id="df27e-p120">[!NOTA] Preste atención a los tipos de datos de argumentos **ByRef**. VBScript no permite especificar el tipo de variable, por lo que siempre se debe pasar un tipo Variant. Cuando se usa HTTP, RDS permitirá pasar un valor Variant a un método que espera un valor no Variant si lo llama con el método **CreateObject** del objeto [RDS.DataSpace](createobject-method-rds.md). Cuando se usa DCOM o un servidor en proceso, use los mismos tipos de parámetro en el cliente y en el servidor o recibirá un error de no coincidencia de tipos.</span><span class="sxs-lookup"><span data-stu-id="df27e-p120">Pay attention to the data type of **ByRef** arguments. VBScript does not let you specify the variable type, so you must always pass a Variant. When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the **RDS.DataSpace** object [CreateObject](createobject-method-rds.md) method. When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span></span>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

### <a name="step-2-part-a-invoke-the-server-program-with-rdsdatacontrol"></a><span data-ttu-id="df27e-191">Paso 2: parte A: invocar el programa de servidor con RDS. DataControl</span><span class="sxs-lookup"><span data-stu-id="df27e-191">Step 2, Part A: Invoke the server program with RDS.DataControl</span></span>

<span data-ttu-id="df27e-192">Este ejemplo es simplemente un comentario que muestra que el comportamiento predeterminado del objeto **RDS.DataControl** consiste en realizar la consulta especificada.</span><span class="sxs-lookup"><span data-stu-id="df27e-192">This example is merely a comment demonstrating that the default behavior of the **RDS.DataControl** is to perform the specified query.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial2A() 
 Dim RS 
 DC1.Refresh 
 Set RS = DC1.Recordset 
... 
```

<span data-ttu-id="df27e-193">Vaya al paso siguiente.</span><span class="sxs-lookup"><span data-stu-id="df27e-193">Skip to the following step.</span></span>

### <a name="step-4-server-returns-the-recordset"></a><span data-ttu-id="df27e-194">Paso 4: El servidor devuelve el objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="df27e-194">Step 4: Server returns the Recordset</span></span>

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

### <a name="step-5-datacontrol-is-made-usable-by-visual-controls"></a><span data-ttu-id="df27e-195">Paso 5: DataControl se facilita mediante controles visuales</span><span class="sxs-lookup"><span data-stu-id="df27e-195">Step 5: DataControl is made usable by visual controls</span></span>

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

### <a name="step-6-part-a-changes-are-sent-to-the-server-with-rdsdatacontrol"></a><span data-ttu-id="df27e-196">Paso 6, parte A: los cambios se envían al servidor con RDS. DataControl</span><span class="sxs-lookup"><span data-stu-id="df27e-196">Step 6, Part A: Changes are sent to the server with RDS.DataControl</span></span>

<span data-ttu-id="df27e-197">Este ejemplo es simplemente un comentario que demuestra cómo el objeto **RDS.DataControl** realiza las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="df27e-197">This example is merely a comment demonstrating how the **RDS.DataControl** performs updates.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial6A() 
Dim RS 
DC1.Refresh 
... 
Set RS = DC1.Recordset 
' Edit the Recordset object... 
' The SERVER and CONNECT properties are already set from Step 2A. 
Set DC1.SourceRecordset = RS 
... 
DC1.SubmitChanges 
```

### <a name="step-6-part-b-changes-are-sent-to-the-server-with-rdsserverdatafactory"></a><span data-ttu-id="df27e-198">Paso 6, parte B: los cambios se envían al servidor con RDSServer.DataFactory</span><span class="sxs-lookup"><span data-stu-id="df27e-198">Step 6, Part B: Changes are sent to the server with RDSServer.DataFactory</span></span>

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

## <a name="appendix-b-rds-tutorial-visual-j"></a><span data-ttu-id="df27e-199">Apéndice B: tutorial de RDS (Visual J ++)</span><span class="sxs-lookup"><span data-stu-id="df27e-199">Appendix B: RDS tutorial (Visual J++)</span></span>

<span data-ttu-id="df27e-p121">ADO/WFC no sigue completamente el modelo de objetos RDS, ya que no implementa el objeto [RDS.DataControl](datacontrol-object-rds.md). ADO/WFC sólo implementa la clase de la parte cliente, [RDS.DataSpace](dataspace-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="df27e-p121">ADO/WFC does not completely follow the RDS object model in that it does not implement the [RDS.DataControl](datacontrol-object-rds.md) object. ADO/WFC only implements the client-side class, [RDS.DataSpace](dataspace-object-rds.md).</span></span>

<span data-ttu-id="df27e-p122">La clase **DataSpace** implementa un método, [CreateObject](createobject-method-rds.md), que devuelve un objeto [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax). La clase **DataSpace** también implementa la propiedad [InternetTimeout](internettimeout-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="df27e-p122">The **DataSpace** class implements one method, [CreateObject](createobject-method-rds.md), which returns an [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax) object. The **DataSpace** class also implements the [InternetTimeout](internettimeout-property-rds.md) property.</span></span>

<span data-ttu-id="df27e-204">La clase **ObjectProxy** implementa un método, call, que puede llamar a cualquier objeto de negocio de servidor.</span><span class="sxs-lookup"><span data-stu-id="df27e-204">The **ObjectProxy** class implements one method, call, which can invoke any server-side business object.</span></span>

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```



