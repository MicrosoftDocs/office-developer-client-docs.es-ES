---
<<<<<<< Título HEAD: proveedor (propiedad) (ADO) TOCTitle: proveedor (propiedad) (ADO) === título: proveedor (propiedad, ADO) TOCTitle: proveedor (propiedad, ADO)
>>>>>>> Master ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15) ms:contentKeyID: ms.date 48543543: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="provider-property-ado"></a>Provider (propiedad, ADO)
=======
# <a name="provider-property-ado"></a>Proveedor (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica el nombre del proveedor para un objeto [Connection](connection-object-ado.md).

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo **String** que indica el nombre del proveedor.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Provider** para establecer o devolver el nombre del proveedor de una conexión. Esta propiedad también puede establecerse mediante el contenido de la propiedad [ConnectionString](connectionstring-property-ado.md) o el argumento *ConnectionString* del método [Open](open-method-ado-connection.md); sin embargo, la especificación de un proveedor en más de un lugar mientras se llama al método **Open** pueda dar lugar a resultados impredecibles. Si no se especifica ningún proveedor, el valor predeterminado de la propiedad será MSDASQL ([Proveedor de Microsoft OLE DB para ODBC](microsoft-ole-db-provider-for-odbc.md)).

La propiedad **Provider** es de lectura y escritura cuando la conexión está cerrada y de sólo lectura cuando está abierta. El valor no tiene ningún efecto hasta que se abre el objeto **Connection** o se obtiene acceso a la colección [Properties](properties-collection-ado.md) del objeto **Connection**. Si el valor no es válido, se produce un error.

