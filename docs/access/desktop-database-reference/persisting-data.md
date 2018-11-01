---
title: Datos persistentes (referencia de escritorio de la base de datos de Access)
TOCTitle: Persisting Data
ms:assetid: cb8a32f7-2cdc-26ed-c6d4-dd93c1ac37ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250010(v=office.15)
ms:contentKeyID: 48547715
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4db6e157ff5999dbf8892029840529c2306ef4e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869935"
---
# <a name="persisting-data"></a><span data-ttu-id="a46df-102">Persistencia de datos</span><span class="sxs-lookup"><span data-stu-id="a46df-102">Persisting Data</span></span>


<span data-ttu-id="a46df-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a46df-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a46df-p101">El uso de equipos informáticos portátiles ha generado la necesidad de aplicaciones que se puedan ejecutar tanto si se está conectado como si no se está. ADO ha agregado esta funcionalidad ofreciendo al programador la posibilidad de guardar un **conjunto de registros** de cursor de cliente en disco y de volverlo a cargar posteriormente.</span><span class="sxs-lookup"><span data-stu-id="a46df-p101">Portable computing (for example, using laptops) has generated the need for applications that can run in both a connected and disconnected state. ADO has added support for this by giving the developer the ability to save a client cursor **Recordset** to disk and reload it later.</span></span>

<span data-ttu-id="a46df-106">Existen varios escenarios en los que se podría utilizar este tipo de característica, como por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a46df-106">There are several scenarios in which you could use this type of feature, including the following:</span></span>

- <span data-ttu-id="a46df-107">**Viajes**: Si sale de viaje con la aplicación, es fundamental tener la posibilidad de efectuar cambios y agregar nuevos registros que posteriormente se puedan volver a conectar a la base de datos y confirmar.</span><span class="sxs-lookup"><span data-stu-id="a46df-107">**Traveling:** When taking the application on the road, it is vital to supply the ability to make changes and add new records that can then be reconnected to the database later and committed.</span></span>

- <span data-ttu-id="a46df-p102">**Búsquedas poco frecuentes de actualizaciones**: En una aplicación, se suelen utilizar tablas como búsquedas (por ejemplo, tablas de impuestos estatales). Estas tablas se actualizan con poca frecuencia y son de sólo lectura. En vez de volver a leer estos datos del servidor cada vez que se inicia la aplicación, simplemente la aplicación puede cargar los datos desde un **conjunto de registros** persistente localmente.</span><span class="sxs-lookup"><span data-stu-id="a46df-p102">**Infrequently updated lookups:** Often in an application, tables are used as lookups — for example, state tax tables. They are infrequently updated and are read-only. Instead of rereading this data from the server each time the application is started, the application can simply load the data from a locally persisted **Recordset**.</span></span>

<span data-ttu-id="a46df-111">En ADO, para guardar y cargar **conjuntos de registros**, use los métodos **Recordset.Save** y **Recordset.Open(,,,,adCmdFile)** en el objeto **Recordset** de ADO.</span><span class="sxs-lookup"><span data-stu-id="a46df-111">In ADO, to save and load **Recordsets**, use the **Recordset.Save** and **Recordset.Open(,,,,adCmdFile)** methods on the ADO **Recordset** object.</span></span>

<span data-ttu-id="a46df-p103">Se puede usar el método **Save** de un **conjunto de registros** para conservar el **conjunto de registros** de ADO en un archivo en el disco (también se puede guardar un **conjunto de registros** en un objeto **Stream** de ADO; los objetos **Stream** se tratan más adelante en la guía). Posteriormente, se puede usar el método **Open** para volver a abrir el **conjunto de registros** cuando se esté listo para usarlo. De forma predeterminada, ADO guarda el **conjunto de registros** en el formato de propietario de Microsoft Advanced Data TableGram (ADTG). Este formato binario se especifica mediante el valor **adPersistADTG** de **PersistFormatEnum**. Otra posibilidad es guardar el **conjunto de registros** como XML utilizando **adPersistXML**. Para obtener más información acerca de guardar conjuntos de registros como XML, vea [Almacenar registros en formato XML](persisting-records-in-xml-format.md).</span><span class="sxs-lookup"><span data-stu-id="a46df-p103">You can use the **Recordset** **Save** method to persist your ADO **Recordset** to a file on a disk. (You can also save a **Recordset** to an ADO **Stream** object. **Stream** objects are discussed later in the guide.) Later, you can use the **Open** method to reopen the **Recordset** when you are ready to use it. By default, ADO saves the **Recordset** into the proprietary Microsoft Advanced Data TableGram (ADTG) format. This binary format is specified using the **adPersistADTG** **PersistFormatEnum** value. Alternatively, you may choose to save your **Recordset** out as XML instead using **adPersistXML**. For more information about saving Recordsets as XML, see [Persisting Records in XML Format](persisting-records-in-xml-format.md).</span></span>

<span data-ttu-id="a46df-119">La sintaxis del método **Save** es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="a46df-119">The syntax of the **Save** method is as follows:</span></span>

`recordset.Save Destination, PersistFormat`

<span data-ttu-id="a46df-p104">La primera vez que se guarda el **conjunto de registros**, la especificación de *Destination* es opcional. Si se omite *Destination*, se creará un nuevo archivo con un nombre establecido en el valor de la propiedad [Origen](source-property-ado-recordset.md) del **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="a46df-p104">The first time you save the **Recordset**, it is optional to specify *Destination*. If you omit *Destination*, a new file will be created with a name set to the value of the [Source](source-property-ado-recordset.md) property of the **Recordset**.</span></span>

<span data-ttu-id="a46df-p105">Si no se omite *Destination* cuando se vuelve a llamar a **Save** después de la primera vez, se producirá un error en tiempo de ejecución. Si se vuelve a llamar a **Save** con un nuevo valor de *Destination*, el **conjunto de registros** se guardará en el nuevo destino. Sin embargo, tanto el nuevo destino como el original estarán abiertos.</span><span class="sxs-lookup"><span data-stu-id="a46df-p105">Omit *Destination* when you subsequently call **Save** after the first save or a run-time error will occur. If you subsequently call **Save** with a new *Destination*, the **Recordset** is saved to the new destination. However, the new destination and the original destination will both be open.</span></span>

<span data-ttu-id="a46df-p106">**Save** no cierra el **conjunto de registros** ni el *destino*, por lo que se puede continuar trabajando con el **conjunto de registros** y guardando los cambios más recientes. El *destino* permanece abierto mientras no se cierre el **conjunto de registros**; durante este tiempo, otras aplicaciones pueden leer pero no escribir en el *destino*.</span><span class="sxs-lookup"><span data-stu-id="a46df-p106">**Save** does not close the **Recordset** or *Destination*, so you can continue to work with the **Recordset** and save your most recent changes. *Destination* remains open until the **Recordset** is closed, during which time other applications can read but not write to *Destination*.</span></span>

<span data-ttu-id="a46df-p107">Por motivos de seguridad, el método **Save** sólo permite el uso de configuraciones de seguridad baja y personalizada desde un script ejecutado por Microsoft Internet Explorer. Para obtener una explicación más detallada de los problemas de seguridad, vea el tema sobre los problemas de seguridad de ADO y RDS en Microsoft Internet Explorer, que se encuentra en los artículos técnicos de ActiveX Data Objects (ADO), en la sección de artículos técnicos de Microsoft Data Access.</span><span class="sxs-lookup"><span data-stu-id="a46df-p107">For reasons of security, the **Save** method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer. For a more detailed explanation of security issues, see "ADO and RDS Security Issues in Microsoft Internet Explorer" under ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.</span></span>

<span data-ttu-id="a46df-129">Si se llama al método **Save** mientras está en curso una operación asincrónica de recuperación, ejecución o actualización de un **conjunto de registros**, **Save** espera a que se complete la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="a46df-129">If the **Save** method is called while an asynchronous **Recordset** fetch, execute, or update operation is in progress, **Save** waits until the asynchronous operation is complete.</span></span>

<span data-ttu-id="a46df-p108">Los registros se guardan empezando por la primera fila del **conjunto de registros**. Cuando el método **Save** finaliza, la posición de la fila activa se mueve a la primera fila del **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="a46df-p108">Records are saved beginning with the first row of the **Recordset**. When the **Save** method is finished, the current row position is moved to the first row of the **Recordset**.</span></span>

<span data-ttu-id="a46df-p109">Para obtener mejores resultados, establezca la propiedad [CursorLocation](cursorlocation-property-ado.md) en **adUseClient** con **Save**. Si su proveedor no admite toda la funcionalidad necesaria para guardar objetos **Recordset**, el Servicio de cursores proporcionará la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="a46df-p109">For best results, set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** with **Save**. If your provider does not support all of the functionality necessary to save **Recordset** objects, the Cursor Service will provide that functionality.</span></span>

<span data-ttu-id="a46df-p110">Cuando un **conjunto de registros** persiste con la propiedad **CursorLocation** establecida en **adUseServer**, la capacidad de actualización para el **conjunto de registros** es limitada. Normalmente, solo se permiten actualizaciones, inserciones y eliminaciones con una tabla (dependiendo de la funcionalidad del proveedor). El método [Resync](resync-method-ado.md) tampoco está disponible en esta configuración.</span><span class="sxs-lookup"><span data-stu-id="a46df-p110">When a **Recordset** is persisted with the **CursorLocation** property set to **adUseServer**, the update capability for the **Recordset** is limited. Typically, only single-table updates, insertions, and deletions are allowed (dependent on provider functionality). The [Resync](resync-method-ado.md) method is also unavailable in this configuration.</span></span>

<span data-ttu-id="a46df-137">Debido a que el parámetro *Destination* puede aceptar cualquier objeto que admita la interfaz **IStream** de OLE DB, puede guardar un **objeto Recordset** directamente en el objeto de **respuesta** de ASP.</span><span class="sxs-lookup"><span data-stu-id="a46df-137">Because the *Destination* parameter can accept any object that supports the OLE DB **IStream** interface, you can save a **Recordset** directly to the ASP **Response** object.</span></span>

<span data-ttu-id="a46df-138">En el ejemplo siguiente, se utilizan los métodos **Save** y **Open** para conservar un **conjunto de registros** y volver a abrirlo posteriormente:</span><span class="sxs-lookup"><span data-stu-id="a46df-138">In the following example, the **Save** and **Open** methods are used to persist a **Recordset** and later reopen it:</span></span>

```vb 
 
'BeginPersist 
 conn.ConnectionString = _ 
 "Provider='SQLOLEDB';Data Source='MySqlServer';" _ 
 & "Integrated Security='SSPI';Initial Catalog='pubs'" 
 conn.Open 
 
 conn.Execute "create table testtable (dbkey int " & _ 
 "primary key, field1 char(10))" 
 conn.Execute "insert into testtable values (1, 'string1')" 
 
 Set rst.ActiveConnection = conn 
 rst.CursorLocation = adUseClient 
 
 rst.Open "select * from testtable", conn, adOpenStatic, _ 
 adLockBatchOptimistic 
 
 'Change the row on the client 
 rst!field1 = "NewValue" 
 
 'Save to a file--the .dat extension is an example; choose 
 'your own extension. The changes will be saved in the file 
 'as well as the original data. 
 MyFile = Dir("c:\temp\temptbl.dat") 
 If MyFile <> "" Then 
 Kill "c:\temp\temptbl.dat" 
 End If 
 
 rst.Save "c:\temp\temptbl.dat", adPersistADTG 
 rst.Close 
 Set rst = Nothing 
 
 'Now reload the data from the file 
 Set rst = New ADODB.Recordset 
 rst.Open "c:\temp\temptbl.dat", , adOpenStatic, _ 
 adLockBatchOptimistic, adCmdFile 
 
 Debug.Print "After Loading the file from disk" 
 Debug.Print " Current Edited Value: " & rst!field1.Value 
 Debug.Print " Value Before Editing: " & rst!field1.OriginalValue 
 
 'Note that you can reconnect to a connection and 
 'submit the changes to the data source 
 Set rst.ActiveConnection = conn 
 rst.UpdateBatch 
'EndPersist 
```

<span data-ttu-id="a46df-139">Esta sección incluye los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a46df-139">This section includes the following topics:</span></span>

- [<span data-ttu-id="a46df-140">Más información sobre la persistencia del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="a46df-140">More About Recordset Persistence</span></span>](more-about-recordset-persistence.md)

- [<span data-ttu-id="a46df-141">Persistencia de los conjuntos de registros filtrados y jerárquicos</span><span class="sxs-lookup"><span data-stu-id="a46df-141">Persisting Filtered and Hierarchical Recordsets</span></span>](persisting-filtered-and-hierarchical-recordsets.md)

- [<span data-ttu-id="a46df-142">Persisting Records in XML Format (ADO)</span><span class="sxs-lookup"><span data-stu-id="a46df-142">Persisting Records in XML Format (ADO)</span></span>](persisting-records-in-xml-format.md)