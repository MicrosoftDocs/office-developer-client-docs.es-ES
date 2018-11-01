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
# <a name="persisting-data"></a>Persistencia de datos


**Se aplica a**: Access 2013, Office 2013

El uso de equipos informáticos portátiles ha generado la necesidad de aplicaciones que se puedan ejecutar tanto si se está conectado como si no se está. ADO ha agregado esta funcionalidad ofreciendo al programador la posibilidad de guardar un **conjunto de registros** de cursor de cliente en disco y de volverlo a cargar posteriormente.

Existen varios escenarios en los que se podría utilizar este tipo de característica, como por ejemplo:

- **Viajes**: Si sale de viaje con la aplicación, es fundamental tener la posibilidad de efectuar cambios y agregar nuevos registros que posteriormente se puedan volver a conectar a la base de datos y confirmar.

- **Búsquedas poco frecuentes de actualizaciones**: En una aplicación, se suelen utilizar tablas como búsquedas (por ejemplo, tablas de impuestos estatales). Estas tablas se actualizan con poca frecuencia y son de sólo lectura. En vez de volver a leer estos datos del servidor cada vez que se inicia la aplicación, simplemente la aplicación puede cargar los datos desde un **conjunto de registros** persistente localmente.

En ADO, para guardar y cargar **conjuntos de registros**, use los métodos **Recordset.Save** y **Recordset.Open(,,,,adCmdFile)** en el objeto **Recordset** de ADO.

Se puede usar el método **Save** de un **conjunto de registros** para conservar el **conjunto de registros** de ADO en un archivo en el disco (también se puede guardar un **conjunto de registros** en un objeto **Stream** de ADO; los objetos **Stream** se tratan más adelante en la guía). Posteriormente, se puede usar el método **Open** para volver a abrir el **conjunto de registros** cuando se esté listo para usarlo. De forma predeterminada, ADO guarda el **conjunto de registros** en el formato de propietario de Microsoft Advanced Data TableGram (ADTG). Este formato binario se especifica mediante el valor **adPersistADTG** de **PersistFormatEnum**. Otra posibilidad es guardar el **conjunto de registros** como XML utilizando **adPersistXML**. Para obtener más información acerca de guardar conjuntos de registros como XML, vea [Almacenar registros en formato XML](persisting-records-in-xml-format.md).

La sintaxis del método **Save** es la siguiente:

`recordset.Save Destination, PersistFormat`

La primera vez que se guarda el **conjunto de registros**, la especificación de *Destination* es opcional. Si se omite *Destination*, se creará un nuevo archivo con un nombre establecido en el valor de la propiedad [Origen](source-property-ado-recordset.md) del **conjunto de registros**.

Si no se omite *Destination* cuando se vuelve a llamar a **Save** después de la primera vez, se producirá un error en tiempo de ejecución. Si se vuelve a llamar a **Save** con un nuevo valor de *Destination*, el **conjunto de registros** se guardará en el nuevo destino. Sin embargo, tanto el nuevo destino como el original estarán abiertos.

**Save** no cierra el **conjunto de registros** ni el *destino*, por lo que se puede continuar trabajando con el **conjunto de registros** y guardando los cambios más recientes. El *destino* permanece abierto mientras no se cierre el **conjunto de registros**; durante este tiempo, otras aplicaciones pueden leer pero no escribir en el *destino*.

Por motivos de seguridad, el método **Save** sólo permite el uso de configuraciones de seguridad baja y personalizada desde un script ejecutado por Microsoft Internet Explorer. Para obtener una explicación más detallada de los problemas de seguridad, vea el tema sobre los problemas de seguridad de ADO y RDS en Microsoft Internet Explorer, que se encuentra en los artículos técnicos de ActiveX Data Objects (ADO), en la sección de artículos técnicos de Microsoft Data Access.

Si se llama al método **Save** mientras está en curso una operación asincrónica de recuperación, ejecución o actualización de un **conjunto de registros**, **Save** espera a que se complete la operación asincrónica.

Los registros se guardan empezando por la primera fila del **conjunto de registros**. Cuando el método **Save** finaliza, la posición de la fila activa se mueve a la primera fila del **conjunto de registros**.

Para obtener mejores resultados, establezca la propiedad [CursorLocation](cursorlocation-property-ado.md) en **adUseClient** con **Save**. Si su proveedor no admite toda la funcionalidad necesaria para guardar objetos **Recordset**, el Servicio de cursores proporcionará la funcionalidad.

Cuando un **conjunto de registros** persiste con la propiedad **CursorLocation** establecida en **adUseServer**, la capacidad de actualización para el **conjunto de registros** es limitada. Normalmente, solo se permiten actualizaciones, inserciones y eliminaciones con una tabla (dependiendo de la funcionalidad del proveedor). El método [Resync](resync-method-ado.md) tampoco está disponible en esta configuración.

Debido a que el parámetro *Destination* puede aceptar cualquier objeto que admita la interfaz **IStream** de OLE DB, puede guardar un **objeto Recordset** directamente en el objeto de **respuesta** de ASP.

En el ejemplo siguiente, se utilizan los métodos **Save** y **Open** para conservar un **conjunto de registros** y volver a abrirlo posteriormente:

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

Esta sección incluye los temas siguientes:

- [Más información sobre la persistencia del conjunto de registros](more-about-recordset-persistence.md)

- [Persistencia de los conjuntos de registros filtrados y jerárquicos](persisting-filtered-and-hierarchical-recordsets.md)

- [Persisting Records in XML Format (ADO)](persisting-records-in-xml-format.md)