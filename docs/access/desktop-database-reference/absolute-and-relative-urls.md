---
<<<<<<< Título HEAD: absolutas y relativas TOCTitle de direcciones URL: ms:assetid absolutas y direcciones URL relativas: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15) ms:contentKeyID: ms.date 48545774: 18/09/2015 mtps_version: v = Office.15
---

# <a name="absolute-and-relative-urls"></a>Direcciones URL absolutas y relativas

**Se aplica a**: Access 2013 | Office 2013 

Una dirección URL especifica la ubicación de un destino almacenado en un equipo local o conectado en red, como un archivo, un directorio, una página HTML, una imagen, un programa, etc.** En este tema, una *dirección URL absoluta* tiene el siguiente formato:
=======
título: TOCTitle las direcciones URL absolutas y relativas: ms:assetid las direcciones URL absolutas y relativas: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15) ms:contentKeyID: ms.date 48545774: 17/10/2018 mtps_version: Office.15
---

# <a name="absolute-and-relative-urls"></a>Direcciones URL absolutas y relativas

**Se aplica a**: Access 2013 | Office 2013 

Una dirección URL especifica la ubicación de un destino almacenado en un equipo local o de red, como un archivo, directorio, HTML página, imagen, programa y así sucesivamente. En esta descripción, una *dirección URL absoluta* es del formulario:
>>>>>>> master

*esquema://servidor/ruta de acceso/recurso*

donde:

<<<<<<< HEAD
  - *esquema*

  - Especifica cómo se puede tener acceso a los *recursos* .

  - *servidor*

  - Especifica el nombre del equipo donde está ubicado el *recurso* .

  - *ruta de acceso*

  - Especifica la secuencia de directorios que llevan al destino. Si se omite el *recurso*, el destino es el último directorio de la *ruta de acceso*.

  - *recurso*

  - Si se incluye, *recurso* es el destino y normalmente es el nombre de un archivo. Puede ser un *archivo simple,* que contiene una única secuencia binaria de bytes o un *documento estructurado,* que contiene uno o varios almacenamientos y secuencias binarias de bytes.
=======
|Nombre |Descripción|
|:----|:----------|
|*esquema*|Especifica cómo se puede tener acceso a los *recursos* .|
|*servidor*|Especifica el nombre del equipo donde está ubicado el *recurso* .|
|*ruta de acceso*|Especifica la secuencia de directorios que llevan al destino. Si se omite el *recurso*, el destino es el último directorio de la *ruta de acceso*.|
|*recurso*|Si se incluye, *recurso* es el destino y normalmente es el nombre de un archivo. Puede ser un *archivo simple*, que contiene una secuencia binaria única de bytes, o un *documento estructurado*, que contiene uno o varios almacenamientos y secuencias binarias de bytes.|
>>>>>>> master

Una *dirección URL absoluta* contiene toda la información necesaria para localizar un recurso.

Una *dirección URL relativa* localiza un recurso mediante una dirección URL absoluta como punto de partida. En efecto, la "dirección URL completa" del destino se especifica concatenando las direcciones URL absoluta y relativa. Una dirección URL relativa normalmente se compone sólo de la *ruta de acceso* y, de manera opcional, del *recurso*, pero no del *esquema* ni del *servidor*.

<<<<<<< HEAD
## <a name="url-scheme-registration"></a>Registro de esquemas URL

Si un proveedor admite direcciones URL, se registrará para uno o varios esquemas URL. Esto significa que las direcciones URL que utilicen este esquema invocarán automáticamente el proveedor registrado. Por ejemplo, el esquema *http* se registra para el [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). ADO da por supuesto que todas las direcciones URL precedidas del prefijo "http" representan carpetas o archivos Web que deben utilizarse con el proveedor de publicaciones en Internet. Para obtener información sobre los esquemas registrados por su proveedor, vea la documentación del proveedor.

## <a name="defining-context-with-a-url"></a>Definir contexto con una dirección URL
=======
## <a name="url-scheme-registration"></a>Registro de esquemas URL

Si un proveedor admite direcciones URL, se registrará para uno o varios esquemas URL. Esto significa que las direcciones URL que utilicen este esquema invocarán automáticamente el proveedor registrado. Por ejemplo, el esquema *http* se registra para el [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). ADO se da por supuesto que todas las direcciones URL van precedidas de "http" representan carpetas web o los archivos que se usará con el proveedor de publicación en Internet. Para obtener información sobre los esquemas registrados por su proveedor, vea la documentación del proveedor.

## <a name="defining-context-with-a-url"></a>Definir contexto con una dirección URL
>>>>>>> master

Una de las funciones de una conexión abierta, representada por un objeto [Connection](connection-object-ado.md), es restringir las operaciones subsiguientes en el origen de datos representado por esa conexión. Es decir, la conexión define el contexto de las operaciones subsiguientes.

Con ADO 2.5, una dirección URL absoluta también puede definir un contexto. Por ejemplo, al abrirse un objeto [Record](record-object-ado.md) con una dirección URL absoluta, se crea implícitamente un objeto **Connection** para representar el recurso especificado por la dirección URL.

<<<<<<< Método [Open](open-method-ado-record.md) de objetos de encabezado que se puede especificar una dirección URL absoluta que define un contexto en el parámetro *ActiveConnection* del **registro** . También se puede especificar una dirección URL absoluta como el valor de la nueva "dirección URL**=**" palabra clave en la **conexión de** objeto [Open](open-method-ado-connection.md) parámetro *ConnectionString* del método y el objeto [Recordset](recordset-object-ado.md) *ActiveConnection del método [Open](open-method-ado-recordset.md) *parámetro.

El contexto también se puede definir con un objeto **Record** o **Recordset** abierto que representa un directorio porque estos objetos ya tienen un objeto **Connection** implícita o explícitamente declarado que especifica el contexto.

## <a name="scoped-operations"></a>Operaciones con ámbito

El contexto define a la vez un *ámbito* ; es decir, el directorio y sus subdirectorios que pueden participar en las siguientes operaciones. El objeto **Record** tiene varios métodos con ámbito, incluidos [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md) y [DeleteRecord](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), que funcionan en un directorio y todos sus subdirectorios.

## <a name="relative-urls-as-command-text"></a>Direcciones URL relativas como texto de comando
=== Una dirección URL absoluta que define un contexto puede especificarse en el parámetro *ActiveConnection* del método [Open](open-method-ado-record.md) del objeto de **registro** . También se puede especificar una dirección URL absoluta como el valor de la nueva `URL=` palabra clave en la **conexión de** objeto [Open](open-method-ado-connection.md) parámetro *ConnectionString* del método y el objeto [Recordset](recordset-object-ado.md) *ActiveConnection* del método [Open](open-method-ado-recordset.md) parámetro.

El contexto también se puede definir con un objeto **Record** o **Recordset** abierto que representa un directorio porque estos objetos ya tienen un objeto **Connection** implícita o explícitamente declarado que especifica el contexto.

## <a name="scoped-operations"></a>Operaciones con ámbito

El contexto define a la vez un *ámbito*; es decir, el directorio y sus subdirectorios que pueden participar en las siguientes operaciones. El objeto **Record** tiene varios métodos con ámbito, incluidos [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md) y [DeleteRecord](deleterecord-method-ado.md), que funcionan en un directorio y todos sus subdirectorios.

## <a name="relative-urls-as-command-text"></a>Direcciones URL relativas como texto de comando
>>>>>>> master

Una cadena que especifica un comando que se ejecutará en el origen de datos puede especificarse en el parámetro *CommandText* del método de **conexión** objeto **Execute** y el parámetro del *origen de* **conjunto de registros de** objeto **Open** (método).

Una dirección URL relativa se puede especificar en el parámetro *CommandText* o *Source* . En realidad, la dirección URL relativa no especifica un comando (como un comando SQL); simplemente se especifica en esos parámetros. Además, el contexto de la conexión activa debe ser una dirección URL absoluta y el parámetro *opción* debe establecerse en **adCmdTableDirect**.

Por ejemplo, un objeto **Recordset** puede abrirse en el archivo Readme25.txt del directorio Winnt/system32 de la manera siguiente:

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

<<<<<<< Cabeza de la dirección URL absoluta en la cadena de conexión especifica el servidor (YourServer) y el () de la ruta de acceso y la ruta de acceso (Winnt). Esta dirección URL también define el contexto.

La dirección URL relativa en el texto de comando utiliza la dirección URL absoluta como punto de partida y especifica el resto de la ruta de acceso (system32) y el archivo para abrir () y el archivo para abrir (Readme25.txt).

<a name="the-options-field--indicates-that-the-command-type-is-a-relative-url"></a>El campo de opciones () indica que el tipo de comando es una dirección URL relativa.
=======
La dirección URL absoluta en la cadena de conexión especifica el servidor (YourServer) y la ruta de acceso (Winnt). Esta dirección URL también define el contexto.

La dirección URL relativa en el texto de comando utiliza la dirección URL absoluta como punto de partida y especifica el resto de la ruta de acceso (system32) y el archivo para abrir (Readme25.txt).

El campo de opciones indica que el tipo de comando es una dirección URL relativa.
>>>>>>> master

Como otro ejemplo, el siguiente código abrirá un **objeto Recordset** en el contenido del directorio:

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

<<<<<<< HEAD
## <a name="ole-db-provider-supplied-url-schemes"></a>Esquemas de direcciones URL proporcionados por el proveedor OLE DB

La parte inicial de una dirección URL completa es el *esquema* utilizado para obtener acceso al recurso identificado por el resto de la dirección URL. Por ejemplo, HTTP (Protocolo de transferencia de hipertexto) y FTP (Protocolo de transferencia de archivos).

ADO admite los proveedores OLE DB que reconocen sus propios esquemas URL. Por ejemplo, [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md),** que obtiene acceso a los archivos "publicados" de Windows 2000, reconoce el esquema HTTP existente.
=======
## <a name="ole-db-provider-supplied-url-schemes"></a>Esquemas de direcciones URL proporcionados por el proveedor OLE DB

La parte inicial de una dirección URL completa es el *esquema* utilizado para obtener acceso al recurso identificado por el resto de la dirección URL. Por ejemplo, HTTP (Protocolo de transferencia de hipertexto) y FTP (Protocolo de transferencia de archivos).

ADO admite proveedores OLE DB que reconocen sus propios esquemas de dirección URL. Por ejemplo, el [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), que obtiene acceso a los archivos de Windows 2000 "habían publicado", reconoce el esquema HTTP existente.
>>>>>>> master

