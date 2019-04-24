---
title: Proveedor de Microsoft OLE DB para ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f5ffae4880cadb90f47f1ac348ffc8b3ea58785
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288914"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a>Proveedor de Microsoft OLE DB para ODBC

**Se aplica a:** Access 2013, Office 2013

Para un programador de ADO o RDS, un mundo ideal sería aquel en que cada origen de datos expusiera una interfaz OLE DB, de modo que ADO pudiera llamar directamente al origen de datos. Aunque cada vez más proveedores de bases de datos están implementando interfaces OLE DB, algunos orígenes de datos aún no están expuestos de esta forma. Sin embargo, es posible obtener acceso a prácticamente todos los sistemas DBMS que se usan en la actualidad a través de ODBC.

Los controladores ODBC están disponibles para todos los principales DBMS que se utilizan hoy en día, incluidos Microsoft SQL Server, Microsoft Access (motor de bases de datos Microsoft Jet) y Microsoft FoxPro, además de otros productos de base de datos no pertenecientes a Microsoft, como Oracle.

Sin embargo, el Proveedor Microsoft ODBC permite a ADO conectarse a cualquier origen de datos ODBC. El proveedor es de subprocesamiento libre y está habilitado para Unicode.

El proveedor admite transacciones, aunque los diferentes motores DBMS ofrecen diferentes tipos de compatibilidad con ellas. Por ejemplo, Microsoft Access admite las transacciones anidadas de hasta cinco niveles.

Éste es el proveedor predeterminado para ADO y admite todas las propiedades y los métodos ADO dependientes del proveedor.

## <a name="connection-string-parameters"></a>Parámetros de la cadena de conexión

Para conectar con este proveedor, establezca el argumento **Provider=** de la propiedad [ConnectionString](connectionstring-property-ado.md) en:

```sql 
 
MSDASQL 
```

La lectura de la propiedad [Provider](provider-property-ado.md) devolverá también esta cadena.

## <a name="typical-connection-string"></a>Cadena de conexión típica

Una típica cadena de conexión de este proveedor es:

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

La cadena consta de estas palabras clave:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Palabra clave</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Provider</strong></p></td>
<td><p>Especifica el Proveedor OLE DB para ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong>DSN</strong></p></td>
<td><p>Especifica el nombre del origen de datos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>EXCLUSIVO</strong></p></td>
<td><p>Especifica el nombre de usuario.</p></td>
</tr>
<tr class="even">
<td><p><strong>PWD</strong></p></td>
<td><p>Especifica la contraseña de usuario.</p></td>
</tr>
<tr class="odd">
<td><p><strong>URL</strong></p></td>
<td><p>Especifica la dirección URL de un archivo o directorio publicado en una carpeta Web.</p></td>
</tr>
</tbody>
</table>


Dado que éste es el proveedor predeterminado para ADO, si se omite el parámetro **Provider=** de la cadena de conexión, ADO intentará establecer una conexión con este proveedor.

El proveedor no admite ningún parámetro de conexión específico además de los definidos por ADO. No obstante, pasará cualquier parámetro de conexión que no sea de ADO al controlador ODBC.

Dado que se puede omitir el parámetro **Provider**, es posible elaborar una cadena de conexión ADO idéntica a una cadena de conexión ODBC para el mismo origen de datos. Utilice los mismos nombres de parámetro (**DRIVER=**, **DATABASE=**, **DSN=**, etc.), los valores y la sintaxis que cuando elabora una cadena de conexión ODBC. Es posible conectar con o sin un nombre de origen de datos predefinido (DSN) o un FileDSN.

**Sintaxis con un DSN o un FileDSN:**

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

**Sintaxis sin ningún DSN (conexión sin DSN):**

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

Si se utiliza un **DSN** o un **FileDSN**, debe definirse mediante el Administrador de origen de datos ODBC del Panel de control de Windows. En Microsoft Windows 2000, el Administrador ODBC se encuentra en Herramientas administrativas. En versiones anteriores de Windows, el icono Administrador ODBC se denomina **ODBC de 32 bits** o simplemente **ODBC**.

Como alternativa al establecimiento de un **DSN**, puede especificar el controlador ODBC (**DRIVER=**), como "SQL Server;" el nombre del servidor (**SERVER=**); y el nombre de la base de datos (**DATABASE=**).

También puede especificar un nombre de cuenta de usuario (**UID=**) y la contraseña para esa cuenta (**PWD=**) en los parámetros específicos de ODBC o en los parámetros estándar *user* y *password* definidos por ADO.

Aunque una definición de **DSN** ya especifica una base de datos, puede especificar *un* parámetro *Database* además de un **DSN** para conectarse a una base de datos diferente. Es una buena idea incluir siempre el parámetro ** *Database* al usar un **DSN**. Eso garantizará la conexión a la base de datos adecuada en caso de que otro usuario haya modificado el parámetro desde la última vez que se comprobó la definición **DSN**.

## <a name="provider-specific-connection-properties"></a>Propiedades Connection específicas del proveedor

El Proveedor OLE DB para ODBC agrega varias propiedades a la colección [Properties](properties-collection-ado.md) del objeto **Connection**. En la tabla siguiente se enumeran estas propiedades con el nombre de propiedad de OLE DB correspondiente entre paréntesis.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de propiedad</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Procedimientos accesibles<br />
(KAGPROP_ACCESSIBLEPROCEDURES)</p></td>
<td><p>Indica si el usuario tiene acceso a procedimientos almacenados.</p></td>
</tr>
<tr class="even">
<td><p>Tablas accesibles<br />
(KAGPROP_ACCESSIBLETABLES)</p></td>
<td><p>Indica si el usuario tiene permiso para ejecutar instrucciones SELECT en las tablas de la base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>Instrucciones activas<br />
(KAGPROP_ACTIVESTATEMENTS)</p></td>
<td><p>Indica el número de controladores que puede admitir un controlador ODBC en una conexión.</p></td>
</tr>
<tr class="even">
<td><p>Nombre del controlador<br />
(KAGPROP_DRIVERNAME)</p></td>
<td><p>Indica el nombre de archivo del controlador ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Versión ODBC del controlador<br />
(KAGPROP_DRIVERODBCVER)</p></td>
<td><p>Indica la versión de ODBC que admite este controlador.</p></td>
</tr>
<tr class="even">
<td><p>Uso de archivo<br />
(KAGPROP_FILEUSAGE)</p></td>
<td><p>Indica cómo trata el controlador a un archivo de un origen de datos, como una tabla o como un catálogo.</p></td>
</tr>
<tr class="odd">
<td><p>Cláusula escape like<br />
(KAGPROP_LIKEESCAPECLAUSE)</p></td>
<td><p>Indica si el controlador admite la definición y el uso de un carácter de escape para el carácter de porcentaje (%) y de un carácter de subrayado (_) en el predicado LIKE de una cláusula WHERE.</p></td>
</tr>
<tr class="even">
<td><p>Número máximo de columnas en Group by<br />
(KAGPROP_MAXCOLUMNSINGROUPBY)</p></td>
<td><p>Indica el número máximo de columnas que se puede enumerar en la cláusula GROUP BY de una instrucción SELECT.</p></td>
</tr>
<tr class="odd">
<td><p>Número máximo de columnas en el índice<br />
(KAGPROP_MAXCOLUMNSININDEX)</p></td>
<td><p>Indica el número máximo de columnas que puede ser incluido en un índice.</p></td>
</tr>
<tr class="even">
<td><p>Número máximo de columnas en orden<br />
(KAGPROP_MAXCOLUMNSINORDERBY)</p></td>
<td><p>Indica el número máximo de columnas que se puede enumerar en la cláusula ORDER BY de una instrucción SELECT.</p></td>
</tr>
<tr class="odd">
<td><p>Número máximo de columnas en Select<br />
(KAGPROP_MAXCOLUMNSINSELECT)</p></td>
<td><p>Indica el número máximo de columnas que se puede enumerar en la parte SELECT de una instrucción SELECT.</p></td>
</tr>
<tr class="even">
<td><p>Número máximo de columnas de la tabla<br />
(KAGPROP_MAXCOLUMNSINTABLE)</p></td>
<td><p>Indica el número máximo de columnas permitido en una tabla.</p></td>
</tr>
<tr class="odd">
<td><p>Funciones numéricas<br />
(KAGPROP_NUMERICFUNCTIONS)</p></td>
<td><p>Indica las funciones numéricas admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Capacidades de combinaciones externas<br />
(KAGPROP_OJCAPABILITY)</p></td>
<td><p>Indica los tipos de combinaciones externas admitidos por el proveedor.</p></td>
</tr>
<tr class="odd">
<td><p>Combinaciones externas<br />
(KAGPROP_OUTERJOINS)</p></td>
<td><p>Indica si el proveedor admite combinaciones externas.</p></td>
</tr>
<tr class="even">
<td><p>Caracteres especiales<br />
(KAGPROP_SPECIALCHARACTERS)</p></td>
<td><p>Indica qué caracteres tienen un significado especial para el controlador ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Procedimientos almacenados<br />
(KAGPROP_PROCEDURES)</p></td>
<td><p>Indica si hay procedimientos almacenados disponibles para ser utilizados con este controlador ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Funciones de cadena<br />
(KAGPROP_STRINGFUNCTIONS)</p></td>
<td><p>Indica qué funciones de cadena son admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Funciones del sistema<br />
(KAGPROP_SYSTEMFUNCTIONS)</p></td>
<td><p>Indica las funciones del sistema admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Funciones de fecha y hora<br />
(KAGPROP_TIMEDATEFUNCTIONS)</p></td>
<td><p>Indica las funciones de fecha y hora admitidas por el controlador ODBC. Para obtener una lista de los nombres de las funciones y los valores asociados utilizados en esta máscara de bits, vea el Apéndice E: Funciones escalares en la documentación de ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Compatibilidad con la gramática de SQL<br />
(KAGPROP_ODBCSQLCONFORMANCE)</p></td>
<td><p>Indica la gramática SQL admitida por el controlador ODBC.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a>Propiedades Recordset y Command específicas del proveedor

El Proveedor OLE DB para ODBC agrega varias propiedades a la colección **Properties** de los objetos **Recordset** y **Connection**. En la tabla siguiente se enumeran estas propiedades con el nombre de propiedad de OLE DB correspondiente entre paréntesis.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de propiedad</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Actualizaciones/eliminaciones/inSerciones basadas en consultas<br />
(KAGPROP_QUERYBASEDUPDATES)</p></td>
<td><p>Indica si se pueden realizar actualizaciones, eliminaciones e inserciones mediante consultas SQL.</p></td>
</tr>
<tr class="even">
<td><p>Tipo de concurrencia ODBC<br />
(KAGPROP_CONCURRENCY)</p></td>
<td><p>Indica el método utilizado para minimizar los problemas potenciales causados por el intento de dos usuarios de obtener acceso a los mismos datos del origen de datos de forma simultánea.</p></td>
</tr>
<tr class="odd">
<td><p>Accesibilidad de BLOB en un cursor de sólo avance<br />
(KAGPROP_BLOBSONFOCURSOR)</p></td>
<td><p>Indica si es posible obtener acceso a <strong>campos</strong> BLOB cuando se utiliza un cursor de sólo avance.</p></td>
</tr>
<tr class="even">
<td><p>Incluir SQL_FLOAT, SQL_DOUBLE y SQL_REAL en QBU cláusulas WHERE<br />
(KAGPROP_INCLUDENONEXACT)</p></td>
<td><p>Indica si se pueden incluir valores SQL_FLOAT, SQL_DOUBLE y SQL_REAL en una cláusula QBU WHERE.</p></td>
</tr>
<tr class="odd">
<td><p>Posición en la última fila después de insertar<br />
(KAGPROP_POSITIONONNEWROW)</p></td>
<td><p>Indica que tras haber insertado un nuevo registro en una tabla, la última fila de la misma se convertirá en la fila actual.</p></td>
</tr>
<tr class="even">
<td><p>IRowsetChangeExtInfo<br />
(KAGPROP_IROWSETCHANGEEXTINFO)</p></td>
<td><p>Indica si la interfaz <strong>IRowsetChange</strong> admite información ampliada.</p></td>
</tr>
<tr class="odd">
<td><p>Tipo de cursor ODBC<br />
(KAGPROP_CURSOR)</p></td>
<td><p>Indica el tipo de cursor usado por el objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Generar un conjunto de filas que se puede ordenar<br />
(KAGPROP_MARSHALLABLE)</p></td>
<td><p>Indica que el controlador ODBC genera un conjunto de registros que se puede ordenar.</p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a>Texto del comando

La forma de utilizar el objeto [Command](command-object-ado.md) depende en gran medida del origen de datos y del tipo de consulta o instrucción de comando que acepte.

ODBC proporciona una sintaxis específica para llamar a los procedimientos almacenados. Para la propiedad [CommandText](commandtext-property-ado.md) de un objeto **Command**, el argumento *CommandText* del método **Execute** de un objeto [Connection](connection-object-ado.md) o el argumento *Source* del método **Open** de un objeto [Recordset](recordset-object-ado.md), pasa una cadena con esta sintaxis:

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

Cada **?** hace referencia a un objeto de la colección [Parameters](parameters-collection-ado.md). El primer **?** hace **** referencia a Parameters (0), la siguiente **?** hace referencia a **los parámetros**(1) y así sucesivamente.

Las referencias del parámetro son opcionales y dependen de la estructura del procedimiento almacenado. Si desea llamar a un procedimiento almacenado que no define parámetros, la cadena tendrá este aspecto:

`"{ call procedure }"`

Si tiene dos parámetros de consulta, la cadena tendrá este aspecto:

`"{ call procedure ( ?, ? ) }"`

Si el procedimiento almacenado va a devolver un valor, el valor devuelto se trata como otro parámetro. Si no dispone de parámetros de consulta pero tiene un valor devuelto, la cadena tendrá este aspecto:

`"{ ? = call procedure }"`

Por último, si tiene un valor devuelto y dos parámetros de consulta, la cadena tendrá este aspecto:

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a>Comportamiento del objeto Recordset

En las tablas siguientes se enumeran los métodos y las propiedades ADO estándar disponibles en un objeto **Recordset** abierto con este proveedor.

Para obtener información más detallada acerca del comportamiento del objeto **Recordset** para la configuración del proveedor, ejecute el método [Supports](supports-method-ado.md) y enumere la colección **Properties** del objeto **Recordset** para determinar si las propiedades dinámicas específicas del proveedor están presentes.

Disponibilidad de las propiedades estándar del objeto **Recordset** de ADO:

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Propiedad</p></th>
<th><p>ForwardOnly</p></th>
<th><p>Dinámico</p></th>
<th><p>Claves</p></th>
<th><p>Static</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>no disponible</p></td>
<td><p>no disponible</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>no disponible</p></td>
<td><p>no disponible</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="odd">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">BOF</a></p></td>
<td><p>solo lectura</p></td>
<td><p>solo lectura</p></td>
<td><p>solo lectura</p></td>
<td><p>solo lectura</p></td>
</tr>
<tr class="odd">
<td><p><a href="bookmark-property-ado.md">Bookmark</a></p></td>
<td><p>no disponible</p></td>
<td><p>no disponible</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="even">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="odd">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>solo lectura</p></td>
<td><p>solo lectura</p></td>
<td><p>solo lectura</p></td>
<td><p>solo lectura</p></td>
</tr>
<tr class="even">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="odd">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="even">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="odd">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="even">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>lectura y escritura</p></td>
<td><p>no disponible</p></td>
<td><p>solo lectura</p></td>
<td><p>solo lectura</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="even">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>lectura y escritura</p></td>
<td><p>no disponible</p></td>
<td><p>solo lectura</p></td>
<td><p>solo lectura</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-recordset.md">Source</a></p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="even">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>solo lectura</p></td>
<td><p>solo lectura</p></td>
<td><p>solo lectura</p></td>
<td><p>solo lectura</p></td>
</tr>
<tr class="odd">
<td><p><a href="status-property-ado-recordset.md">Estado</a></p></td>
<td><p>solo lectura</p></td>
<td><p>solo lectura</p></td>
<td><p>solo lectura</p></td>
<td><p>solo lectura</p></td>
</tr>
</tbody>
</table>


Las propiedades [AbsolutePosition](absoluteposition-property-ado.md) y [AbsolutePage](absolutepage-property-ado.md) son de sólo escritura cuando se utiliza ADO con la versión 1.0 del Proveedor de Microsoft OLE DB para ODBC.

Disponibilidad de métodos estándar **Recordset** ADO:

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Método</p></th>
<th><p>ForwardOnly</p></th>
<th><p>Dinámico</p></th>
<th><p>Claves</p></th>
<th><p>Static</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">Funcionan</a></p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete</a></p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Velas</a></p></td>
<td><p>No</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></p></td>
<td><p>No</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a>*</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-recordset.md">Open</a></p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Admita</a></p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Actualización</a></p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
<td><p>Sí</p></td>
</tr>
</tbody>
</table>


\*No compatible con las bases de datos de Microsoft Access.

## <a name="dynamic-properties"></a>Propiedades dinámicas

El Proveedor OLE DB para ODBC inserta varias propiedades dinámicas en la colección **Properties** de los objetos [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) y [Command](command-object-ado.md) sin abrir.

Las tablas siguientes son un índice cruzado de los nombres ADO y OLE DB de cada propiedad dinámica. La Referencia del programador de OLE DB hace referencia a un nombre de propiedad de ADO por el término, "Descripción". Puede buscar más información sobre estas propiedades en la Referencia del programador de OLE DB. Busque el nombre de propiedad de OLE DB en el Índice o vea el Apéndice C: Propiedades de OLE DB.

## <a name="connection-dynamic-properties"></a>Propiedades dinámicas de Connection

Las propiedades siguientes se agregan a la colección **Properties** del objeto **Connection**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de propiedad de ADO</p></th>
<th><p>Nombre de propiedad de OLE DB</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Active Sessions</p></td>
<td><p>DBPROP_ACTIVESESSIONS</p></td>
</tr>
<tr class="even">
<td><p>Asynchable Abort</p></td>
<td><p>DBPROP_ASYNCTXNABORT</p></td>
</tr>
<tr class="odd">
<td><p>Asynchable Commit</p></td>
<td><p>DBPROP_ASYNCTNXCOMMIT</p></td>
</tr>
<tr class="even">
<td><p>Autocommit Isolation Levels</p></td>
<td><p>DBPROP_SESS_AUTOCOMMITISOLEVELS</p></td>
</tr>
<tr class="odd">
<td><p>Catalog Location</p></td>
<td><p>DBPROP_CATALOGLOCATION</p></td>
</tr>
<tr class="even">
<td><p>Catalog Term</p></td>
<td><p>DBPROP_CATALOGTERM</p></td>
</tr>
<tr class="odd">
<td><p>Column Definition</p></td>
<td><p>DBPROP_COLUMNDEFINITION</p></td>
</tr>
<tr class="even">
<td><p>Connect Timeout</p></td>
<td><p>DBPROP_INIT_TIMEOUT</p></td>
</tr>
<tr class="odd">
<td><p>Current Catalog</p></td>
<td><p>DBPROP_CURRENTCATALOG</p></td>
</tr>
<tr class="even">
<td><p>Data Source</p></td>
<td><p>DBPROP_INIT_DATASOURCE</p></td>
</tr>
<tr class="odd">
<td><p>Data Source Name</p></td>
<td><p>DBPROP_DATASOURCENAME</p></td>
</tr>
<tr class="even">
<td><p>Data Source Object Threading Model</p></td>
<td><p>DBPROP_DSOTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>DBMS Name</p></td>
<td><p>DBPROP_DBMSNAME</p></td>
</tr>
<tr class="even">
<td><p>DBMS Version</p></td>
<td><p>DBPROP_DBMSVER</p></td>
</tr>
<tr class="odd">
<td><p>Extended Properties</p></td>
<td><p>DBPROP_INIT_PROVIDERSTRING</p></td>
</tr>
<tr class="even">
<td><p>GROUP BY Support</p></td>
<td><p>DBPROP_GROUPBY</p></td>
</tr>
<tr class="odd">
<td><p>Heterogeneous Table Support</p></td>
<td><p>DBPROP_HETEROGENEOUSTABLES</p></td>
</tr>
<tr class="even">
<td><p>Identifier Case Sensitivity</p></td>
<td><p>DBPROP_IDENTIFIERCASE</p></td>
</tr>
<tr class="odd">
<td><p>Initial Catalog</p></td>
<td><p>DBPROP_INIT_CATALOG</p></td>
</tr>
<tr class="even">
<td><p>Isolation Levels</p></td>
<td><p>DBPROP_SUPPORTEDTXNISOLEVELS</p></td>
</tr>
<tr class="odd">
<td><p>Isolation Retention</p></td>
<td><p>DBPROP_SUPPORTEDTXNISORETAIN</p></td>
</tr>
<tr class="even">
<td><p>Locale Identifier</p></td>
<td><p>DBPROP_INIT_LCID</p></td>
</tr>
<tr class="odd">
<td><p>Location</p></td>
<td><p>DBPROP_INIT_LOCATION</p></td>
</tr>
<tr class="even">
<td><p>Maximum Index Size</p></td>
<td><p>DBPROP_MAXINDEXSIZE</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Row Size</p></td>
<td><p>DBPROP_MAXROWSIZE</p></td>
</tr>
<tr class="even">
<td><p>Maximum Row Size Includes BLOB</p></td>
<td><p>DBPROP_MAXROWSIZEINCLUDESBLOB</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Tables in SELECT</p></td>
<td><p>DBPROP_MAXTABLESINSELECT</p></td>
</tr>
<tr class="even">
<td><p>Mode</p></td>
<td><p>DBPROP_INIT_MODE</p></td>
</tr>
<tr class="odd">
<td><p>Multiple Parameter Sets</p></td>
<td><p>DBPROP_MULTIPLEPARAMSETS</p></td>
</tr>
<tr class="even">
<td><p>Multiple Results</p></td>
<td><p>DBPROP_MULTIPLERESULTS</p></td>
</tr>
<tr class="odd">
<td><p>Multiple Storage Objects</p></td>
<td><p>DBPROP_MULTIPLESTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Multi-Table Update</p></td>
<td><p>DBPROP_MULTITABLEUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>NULL Collation Order</p></td>
<td><p>DBPROP_NULLCOLLATION</p></td>
</tr>
<tr class="even">
<td><p>NULL Concatenation Behavior</p></td>
<td><p>DBPROP_CONCATNULLBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>OLE DB Services</p></td>
<td><p>DBPROP_INIT_OLEDBSERVICES</p></td>
</tr>
<tr class="even">
<td><p>OLE DB Version</p></td>
<td><p>DBPROP_PROVIDEROLEDBVER</p></td>
</tr>
<tr class="odd">
<td><p>OLE Object Support</p></td>
<td><p>DBPROP_OLEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Open Rowset Support</p></td>
<td><p>DBPROP_OPENROWSETSUPPORT</p></td>
</tr>
<tr class="odd">
<td><p>ORDER BY Columns in Select List</p></td>
<td><p>DBPROP_ORDERBYCOLUMNSINSELECT</p></td>
</tr>
<tr class="even">
<td><p>Output Parameter Availability</p></td>
<td><p>DBPROP_OUTPUTPARAMETERAVAILABILITY</p></td>
</tr>
<tr class="odd">
<td><p>Password</p></td>
<td><p>DBPROP_AUTH_PASSWORD</p></td>
</tr>
<tr class="even">
<td><p>Pass By Ref Accessors</p></td>
<td><p>DBPROP_BYREFACCESSORS</p></td>
</tr>
<tr class="odd">
<td><p>Persist Security Info</p></td>
<td><p>DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</p></td>
</tr>
<tr class="even">
<td><p>Persistent ID Type</p></td>
<td><p>DBPROP_PERSISTENTIDTYPE</p></td>
</tr>
<tr class="odd">
<td><p>Prepare Abort Behavior</p></td>
<td><p>DBPROP_PREPAREABORTBEHAVIOR</p></td>
</tr>
<tr class="even">
<td><p>Prepare Commit Behavior</p></td>
<td><p>DBPROP_PREPARECOMMITBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>Procedure Term</p></td>
<td><p>DBPROP_PROCEDURETERM</p></td>
</tr>
<tr class="even">
<td><p>Prompt</p></td>
<td><p>DBPROP_INIT_PROMPT</p></td>
</tr>
<tr class="odd">
<td><p>Provider Friendly Name</p></td>
<td><p>DBPROP_PROVIDERFRIENDLYNAME</p></td>
</tr>
<tr class="even">
<td><p>Provider Name</p></td>
<td><p>DBPROP_PROVIDERFILENAME</p></td>
</tr>
<tr class="odd">
<td><p>Provider Version</p></td>
<td><p>DBPROP_PROVIDERVER</p></td>
</tr>
<tr class="even">
<td><p>Read-Only Data Source</p></td>
<td><p>DBPROP_DATASOURCEREADONLY</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Conversions on Command</p></td>
<td><p>DBPROP_ROWSETCONVERSIONSONCOMMAND</p></td>
</tr>
<tr class="even">
<td><p>Schema Term</p></td>
<td><p>DBPROP_SCHEMATERM</p></td>
</tr>
<tr class="odd">
<td><p>Schema Usage</p></td>
<td><p>DBPROP_SCHEMAUSAGE</p></td>
</tr>
<tr class="even">
<td><p>SQL Support</p></td>
<td><p>DBPROP_SQLSUPPORT</p></td>
</tr>
<tr class="odd">
<td><p>Structured Storage</p></td>
<td><p>DBPROP_STRUCTUREDSTORAGE</p></td>
</tr>
<tr class="even">
<td><p>Subquery Support</p></td>
<td><p>DBPROP_SUBQUERIES</p></td>
</tr>
<tr class="odd">
<td><p>Table Term</p></td>
<td><p>DBPROP_TABLETERM</p></td>
</tr>
<tr class="even">
<td><p>Transaction DDL</p></td>
<td><p>DBPROP_SUPPORTEDTXNDDL</p></td>
</tr>
<tr class="odd">
<td><p>User ID</p></td>
<td><p>DBPROP_AUTH_USERID</p></td>
</tr>
<tr class="even">
<td><p>User Name</p></td>
<td><p>DBPROP_USERNAME</p></td>
</tr>
<tr class="odd">
<td><p>Window Handle</p></td>
<td><p>DBPROP_INIT_HWND</p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a>Propiedades dinámicas del objeto Recordset

Las propiedades siguientes se agregan a la colección **Properties** del objeto **Recordset**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de propiedad de ADO</p></th>
<th><p>Nombre de propiedad de OLE DB</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Access Order</p></td>
<td><p>DBPROP_ACCESSORDER</p></td>
</tr>
<tr class="even">
<td><p>Blocking Storage Objects</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Bookmark Type</p></td>
<td><p>DBPROP_BOOKMARKTYPE</p></td>
</tr>
<tr class="even">
<td><p>Bookmarkable</p></td>
<td><p>DBPROP_IROWSETLOCATE</p></td>
</tr>
<tr class="odd">
<td><p>Change Inserted Rows</p></td>
<td><p>DBPROP_CHANGEINSERTEDROWS</p></td>
</tr>
<tr class="even">
<td><p>Column Privileges</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Column Set Notification</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="even">
<td><p>Delay Storage Object Updates</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Fetch Backwards</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Hold Rows</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="odd">
<td><p>IAccessor</p></td>
<td><p>DBPROP_IAccessor</p></td>
</tr>
<tr class="even">
<td><p>IColumnsInfo</p></td>
<td><p>DBPROP_IColumnsInfo</p></td>
</tr>
<tr class="odd">
<td><p>IColumnsRowset</p></td>
<td><p>DBPROP_IColumnsRowset</p></td>
</tr>
<tr class="even">
<td><p>IConnectionPointContainer</p></td>
<td><p>DBPROP_IConnectionPointContainer</p></td>
</tr>
<tr class="odd">
<td><p>IConvertType</p></td>
<td><p>DBPROP_IConvertType</p></td>
</tr>
<tr class="even">
<td><p>Immobile Rows</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="odd">
<td><p>IRowset</p></td>
<td><p>DBPROP_IRowset</p></td>
</tr>
<tr class="even">
<td><p>IRowsetChange</p></td>
<td><p>DBPROP_IRowsetChange</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetIdentity</p></td>
<td><p>DBPROP_IRowsetIdentity</p></td>
</tr>
<tr class="even">
<td><p>IRowsetInfo</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetLocate</p></td>
<td><p>DBPROP_IRowsetLocate</p></td>
</tr>
<tr class="even">
<td><p>IRowsetResynch</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>IRowsetUpdate</p></td>
<td><p>DBPROP_IRowsetUpdate</p></td>
</tr>
<tr class="even">
<td><p>ISequentialStream</p></td>
<td><p>DBPROP_ISequentialStream</p></td>
</tr>
<tr class="odd">
<td><p>ISupportErrorInfo</p></td>
<td><p>DBPROP_ISupportErrorInfo</p></td>
</tr>
<tr class="even">
<td><p>Literal Bookmarks</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Literal Row Identity</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Maximum Open Rows</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Pending Rows</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Maximum Rows</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="odd">
<td><p>Notification Granularity</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="even">
<td><p>Notification Phases</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="odd">
<td><p>Objects Transacted</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="even">
<td><p>Own Changes Visible</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Own Inserts Visible</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="even">
<td><p>Preserve on Abort</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Preserve on Commit</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Quick Restart</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="odd">
<td><p>Reentrant Events</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="even">
<td><p>Remove Deleted Rows</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="odd">
<td><p>Report Multiple Changes</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="even">
<td><p>Return Pending Inserts</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="odd">
<td><p>Row Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="even">
<td><p>Row First Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Row Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Privileges</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Row Resynchronization Notification</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Row Threading Model</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Row Undo Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Update Notification</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Fetch Position Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Rowset Release Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>Scroll Backwards</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Skip Deleted Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKSKIPPED</p></td>
</tr>
<tr class="odd">
<td><p>Strong Row Identity</p></td>
<td><p>DBPROP_STRONGITDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Unique Rows</p></td>
<td><p>DBPROP_UNIQUEROWS</p></td>
</tr>
<tr class="odd">
<td><p>Updatability</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="even">
<td><p>Use Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a>Propiedades dinámicas de Command

Las propiedades siguientes se agregan a la colección **Properties** del objeto **Command**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de propiedad de ADO</p></th>
<th><p>Nombre de propiedad de OLE DB</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Access Order</p></td>
<td><p>DBPROP_ACCESSORDER</p></td>
</tr>
<tr class="even">
<td><p>Blocking Storage Objects</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Bookmark Type</p></td>
<td><p>DBPROP_BOOKMARKTYPE</p></td>
</tr>
<tr class="even">
<td><p>Bookmarkable</p></td>
<td><p>DBPROP_IROWSETLOCATE</p></td>
</tr>
<tr class="odd">
<td><p>Change Inserted Rows</p></td>
<td><p>DBPROP_CHANGEINSERTEDROWS</p></td>
</tr>
<tr class="even">
<td><p>Column Privileges</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Column Set Notification</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="even">
<td><p>Delay Storage Object Updates</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Fetch Backwards</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Hold Rows</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="odd">
<td><p>IAccessor</p></td>
<td><p>DBPROP_IAccessor</p></td>
</tr>
<tr class="even">
<td><p>IColumnsInfo</p></td>
<td><p>DBPROP_IColumnsInfo</p></td>
</tr>
<tr class="odd">
<td><p>IColumnsRowset</p></td>
<td><p>DBPROP_IColumnsRowset</p></td>
</tr>
<tr class="even">
<td><p>IConnectionPointContainer</p></td>
<td><p>DBPROP_IConnectionPointContainer</p></td>
</tr>
<tr class="odd">
<td><p>IConvertType</p></td>
<td><p>DBPROP_IConvertType</p></td>
</tr>
<tr class="even">
<td><p>Immobile Rows</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="odd">
<td><p>IRowset</p></td>
<td><p>DBPROP_IRowset</p></td>
</tr>
<tr class="even">
<td><p>IRowsetChange</p></td>
<td><p>DBPROP_IRowsetChange</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetIdentity</p></td>
<td><p>DBPROP_IRowsetIdentity</p></td>
</tr>
<tr class="even">
<td><p>IRowsetInfo</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetLocate</p></td>
<td><p>DBPROP_IRowsetLocate</p></td>
</tr>
<tr class="even">
<td><p>IRowsetResynch</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>IRowsetUpdate</p></td>
<td><p>DBPROP_IRowsetUpdate</p></td>
</tr>
<tr class="even">
<td><p>ISequentialStream</p></td>
<td><p>DBPROP_ISequentialStream</p></td>
</tr>
<tr class="odd">
<td><p>ISupportErrorInfo</p></td>
<td><p>DBPROP_ISupportErrorInfo</p></td>
</tr>
<tr class="even">
<td><p>Literal Bookmarks</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Literal Row Identity</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Maximum Open Rows</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Pending Rows</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Maximum Rows</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="odd">
<td><p>Notification Granularity</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="even">
<td><p>Notification Phases</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="odd">
<td><p>Objects Transacted</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="even">
<td><p>Own Changes Visible</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Own Inserts Visible</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="even">
<td><p>Preserve on Abort</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Preserve on Commit</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Quick Restart</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="odd">
<td><p>Reentrant Events</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="even">
<td><p>Remove Deleted Rows</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="odd">
<td><p>Report Multiple Changes</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="even">
<td><p>Return Pending Inserts</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="odd">
<td><p>Row Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="even">
<td><p>Row First Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Row Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Privileges</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Row Resynchronization Notification</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Row Threading Model</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Row Undo Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Update Notification</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Fetch Position Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Rowset Release Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>Scroll Backwards</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Skip Deleted Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKSKIP</p></td>
</tr>
<tr class="odd">
<td><p>Strong Row Identity</p></td>
<td><p>DBPROP_STRONGIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Updatability</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="odd">
<td><p>Use Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

Para obtener información detallada acerca de la implementación específica e información funcional acerca del proveedor de Microsoft OLE DB para ODBC, consulte la [Guía del programador de OLE DB](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) o visite el centro de desarrollo de la [plataforma de datos](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).

