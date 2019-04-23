---
title: Open (método, Recordset de ADO)
TOCTitle: Open method (ADO Recordset)
ms:assetid: 87ef19a4-28e1-dec7-ed33-4ae500b9c460
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249591(v=office.15)
ms:contentKeyID: 48546119
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5f8dbdfa61a671e2efb9aac2596cfda5cd1727b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288409"
---
# <a name="open-method-ado-recordset"></a>Open (método, Recordset de ADO)

**Se aplica a:** Access 2013, Office 2013

Abre un cursor.

## <a name="syntax"></a>Sintaxis

*objeto Recordset*. Open*source*, *ActiveConnection*, *CursorType*, *LockType*, *Options*

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*Source* |Es opcional. Valor de tipo **Variant** que da como resultado un objeto [Command](command-object-ado.md) válido, una instrucción SQL, un nombre de tabla, una llamada a un procedimiento almacenado, una dirección URL, o bien el nombre de un archivo u objeto [Stream](stream-object-ado.md) que contiene un objeto [Recordset](recordset-object-ado.md) almacenado de manera persistente.|
|*ActiveConnection* |Es opcional. Valor de tipo **Variant** que da como resultado una variable de objeto [Connection](connection-object-ado.md) válida o valor de tipo **String** que contiene los parámetros [ConnectionString](connectionstring-property-ado.md).|
|*CursorType* |Es opcional. Valor de [CursorTypeEnum](cursortypeenum.md) que determina el tipo de cursor que el proveedor debe usar cuando se abre el objeto **Recordset**. El valor predeterminado es **adOpenForwardOnly**.|
|*LockType* |Es opcional. Valor de [LockTypeEnum](locktypeenum.md) que determina el tipo de bloqueo (concurrencia) que el proveedor debe utilizar cuando se abre el objeto **Recordset**. El valor predeterminado es **adLockReadOnly**.|
|*Options* |Es opcional. Valor de tipo **Long** que indica cómo el proveedor debe evaluar el argumento de *Source* si representa algo que no sea un objeto **Command**, o que indica que el objeto **Recordset** debe restaurarse desde un archivo en el que se guardó anteriormente. Puede ser uno o varios valores de [CommandTypeEnum](commandtypeenum.md) o [ExecuteOptionEnum](executeoptionenum.md), que se pueden combinar con un operador AND bit a bit.|

> [!NOTE]
> [!NOTA] Si abre un objeto **Recordset** de un objeto **Stream** que contiene un objeto **Recordset** almacenado, el uso del valor **adAsyncFetchNonBlocking** de **ExecuteOptionEnum** no tendrá ningún efecto; la recuperación será sincrónica y de bloqueo.

Los valores **adExecuteNoRecords** y **adExecuteStream** de **ExecuteOpenEnum** no deben utilizarse con **Open**.

## <a name="remarks"></a>Comentarios

El cursor predeterminado de un objeto **Recordset** de ADO es un cursor de sólo avance y de sólo lectura ubicado en el servidor.

Si se utiliza el método **Open** en un objeto **Recordset**, se abre un cursor que representa los registros de una tabla base, los resultados de una consulta o un objeto **Recordset** anteriormente guardado.

Utilice el argumento *Source* opcional para especificar un origen de datos de una de las siguientes maneras: mediante una variable del objeto **Command**, una instrucción SQL, un procedimiento almacenado, un nombre de tabla, una dirección URL o una ruta de acceso completa. Si *source* es un nombre de ruta de acceso de archivo, puede ser una ruta de acceso\\completa\\("c: dir File. RST"), una ruta de acceso relativa (".. \\File. RST ") o una dirección URL ("https://files/file.rst").

No se recomienda usar el argumento *Source* del método **Open** para realizar una consulta de acción que no devuelve registros porque no es fácil determinar si la llamada se ha realizado correctamente. El objeto **Recordset** devuelto por esa consulta se cerrará. Llame al método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) de un objeto **Command** o al método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) de un objeto **Connection** para realizar una consulta que no devuelve registros, como una instrucción SQL INSERT.

El argumento *ActiveConnection* corresponde a la propiedad [ActiveConnection](activeconnection-property-ado.md) y especifica la conexión en la que se va a abrir el objeto **Recordset**. Si pasa una definición de conexión para este argumento, ADO abre una conexión nueva con los parámetros especificados. Después de abrir el **objeto Recordset** con un cursor de cliente (**CursorLocation** = **adUseClient**), puede cambiar el valor de esta propiedad para enviar actualizaciones a otro proveedor. O bien, puede establecer el valor de esta propiedad en **Nothing** (en Microsoft Visual Basic) o en NULL para desconectar el objeto **Recordset** de todos los proveedores. Sin embargo, si se cambia el valor de **ActiveConnection** en el caso de un cursor de servidor, se generará un error.

Para los demás argumentos que se corresponden directamente con las propiedades de un objeto **Recordset** (*Source*, *CursorType* y *LockType*), la relación entre los argumentos y las propiedades es la siguiente:

- La propiedad es de lectura y de escritura antes de abrirse el objeto **Recordset**.

- Se utilizan los valores de configuración de las propiedades, a menos que se pasen los argumentos correspondientes cuando se ejecute el método **Open**. Si se pasa un argumento, éste invalida el valor de la propiedad correspondiente y el valor de la propiedad se actualiza con el valor del argumento.

- Una vez abierto el objeto **Recordset**, estas propiedades son de solo lectura.

> [!NOTE]
> La propiedad **ActiveConnection** es de sólo lectura para los objetos **Recordset** cuya propiedad [Source](source-property-ado-recordset.md) esté establecida en un objeto **Command** válido, incluso si no está abierto el objeto **Recordset**.

Si se pasa un objeto **Command** en el argumento *Source* y se pasa asimismo un argumento *ActiveConnection*, se produce un error. La propiedad **ActiveConnection** del objeto **Command** ya debe estar establecida en un objeto **Connection** válido o en una cadena de conexión válida.

Si en el argumento *Source* se pasa algo que no sea un objeto **Command**, se puede utilizar el argumento *Options* para optimizar la evaluación del argumento *Source*. Si no se define el argumento *Options*, puede que disminuya el rendimiento porque ADO debe realizar llamadas al proveedor para determinar si el argumento es una instrucción SQL, un procedimiento almacenado, una dirección URL o un nombre de tabla. Si se conoce el tipo de *Source*, la configuración del argumento *Options* indica a ADO que salte directamente al código pertinente. Si el argumento *Options* no coincide con el tipo de *Source*, se produce un error.

Si se pasa un objeto **Stream** en el argumento *Source*, no debe pasarse información en los demás argumentos. En caso contrario, se generará un error. La información de **ActiveConnection** no se conserva cuando se abre un objeto **Recordset** de un objeto **Stream**.

**adCmdFile** es el valor predeterminado del argumento *Options* si no hay ninguna conexión asociada al objeto **Recordset**. Este suele ser el caso para los objetos **Recordset** almacenados de manera persistente.

Si el origen de datos no devuelve ningún registro, el proveedor establece las propiedades [BOF](bof-eof-properties-ado.md) y [EOF](bof-eof-properties-ado.md) en **True**, y la posición de registro actual está sin definir. Se pueden agregar datos nuevos a este objeto **Recordset** vacío si el tipo de cursor lo permite.

Una vez finalizadas las operaciones en un objeto **Recordset** abierto, use el método [Close](close-method-ado.md) para liberar los recursos del sistema asociados. Cerrar un objeto no lo quita de la memoria; puede cambiar los valores de sus propiedades y volver a abrirlo más adelante mediante el método **Open**. Para eliminar completamente un objeto de la memoria, establezca el valor de la variable del objeto en *Nothing*.

Antes de establecer la propiedad **ActiveConnection** , llame a **Open** sin operandos para crear una instancia de un **objeto Recordset** creado al anexar campos a la colección [Fields](fields-collection-ado.md) del **objeto Recordset** .

Si el valor de la propiedad [CursorLocation](cursorlocation-property-ado.md) es **adUseClient**, se pueden recuperar las filas asincrónicamente de una sola manera. El método recomendado es establecer el valor de *Options* en **adAsyncFetch**. Asimismo, se puede utilizar la propiedad dinámica "Asynchronous Rowset Processing" de la colección [Properties](properties-collection-ado.md), pero se pueden perder los eventos recuperados relacionados si no se establece el valor del parámetro **Options** en **adAsyncFetch**.

> [!NOTE]
> La recuperación en segundo plano en el proveedor MS Remote se admite sólo a través del parámetro *Options* del método **Open**.

> [!NOTE]
> [!NOTA] Las direcciones URL que utilizan el esquema http llamarán automáticamente a [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).


