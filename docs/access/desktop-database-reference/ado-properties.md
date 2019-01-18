---
title: Propiedades de ActiveX Data Objects (ADO)
TOCTitle: ADO properties
ms:assetid: 04f08f22-6327-c603-229e-d06a9f1c0d83
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248809(v=office.15)
ms:contentKeyID: 48543020
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a0efb40d1b5e4c5d675d8add7cdb7a05760578a9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704263"
---
# <a name="ado-properties"></a>Propiedades de ADO

**Se aplica a**: Access 2013, Office 2013

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Propiedad</th>
<th>Descripción</th>
</tr>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>Indica en qué página reside el registro actual.</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>Indica la posición ordinal del registro actual de un objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="activecommand-property-ado.md">ActiveCommand</a></p></td>
<td><p>Indica el objeto <strong>Command</strong> que ha creado el objeto <strong>Recordset</strong> asociado.</p></td>
</tr>
<tr class="even">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>Indica a qué objeto <strong>Connection</strong> pertenece actualmente el objeto <strong>Command</strong>, <strong>Recordset</strong> o <strong>Record</strong> especificado.</p></td>
</tr>
<tr class="odd">
<td><p><a href="actualsize-property-ado.md">ActualSize</a></p></td>
<td><p>Indica la longitud real del valor de un campo.</p></td>
</tr>
<tr class="even">
<td><p><a href="attributes-property-ado.md">Atributos</a></p></td>
<td><p>Indica una o varias características de un objeto.</p></td>
</tr>
<tr class="odd">
<td><p><a href="bof-eof-properties-ado.md">BOF y EOF</a></p></td>
<td><p><strong>BOF</strong> : indica que la posición del registro actual está antes del primer registro en un objeto <strong>Recordset</strong> . <strong>EOF</strong> : indica que la posición del registro actual está después del último registro de un objeto <strong>Recordset</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="bookmark-property-ado.md">Bookmark</a></p></td>
<td><p>Indica un marcador que identifica de manera única el registro actual de un objeto <strong>Recordset</strong> o que establece el registro actual de un objeto <strong>Recordset</strong> en el registro identificado por un marcador válido.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>Indica el número de registros de un objeto <strong>Recordset</strong> que están almacenados en la memoria caché local.</p></td>
</tr>
<tr class="even">
<td><p><a href="chapter-property-ado.md">Capítulo</a></p></td>
<td><p>Obtiene o establece un objeto <strong>Chapter</strong> de OLE DB de/en un objeto <strong>ADORecordsetConstruction</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="charset-property-ado.md">CharSet</a></p></td>
<td><p>Indica el juego de caracteres en el cual se debería traducir el contenido de un <strong>Stream</strong> de texto.</p></td>
</tr>
<tr class="even">
<td><p><a href="commandtext-property-ado.md">CommandText</a></p></td>
<td><p>Indica el texto de un comando que se va a emitir en un proveedor.</p></td>
</tr>
<tr class="odd">
<td><p><a href="commandtimeout-property-ado.md">CommandTimeout</a></p></td>
<td><p>Indica el tiempo que se va a esperar durante la ejecución de un comando para que finalice el intento y se genere un error.</p></td>
</tr>
<tr class="even">
<td><p><a href="commandtype-property-ado.md">CommandType</a></p></td>
<td><p>Indica el tipo de un objeto <strong>Command</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectionstring-property-ado.md">Propiedad ConnectionString</a></p></td>
<td><p>Indica la información utilizada para establecer una conexión con un origen de datos.</p></td>
</tr>
<tr class="even">
<td><p><a href="connectiontimeout-property-ado.md">ConnectionTimeout</a></p></td>
<td><p>Indica el tiempo que se va a esperar durante el establecimiento de una conexión para que finalice el intento y se genere un error.</p></td>
</tr>
<tr class="odd">
<td><p><a href="count-property-ado.md">Count</a></p></td>
<td><p>Indica el número de objetos de una colección.</p></td>
</tr>
<tr class="even">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>Indica la ubicación del servicio de cursores.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>Indica el tipo de cursor que se usa en un objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="datamember-property-ado.md">DataMember</a></p></td>
<td><p>Indica el nombre del miembro de datos que se va a recuperar del objeto al que hace referencia la propiedad <strong>DataSource</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="datasource-property-ado.md">DataSource</a></p></td>
<td><p>Indica un objeto que contiene los datos que se van a representar como un objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="defaultdatabase-property-ado.md">DefaultDatabase</a></p></td>
<td><p>Indica la base de datos predeterminada de un objeto <strong>Connection</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="definedsize-property-ado.md">DefinedSize</a></p></td>
<td><p>Indica la capacidad de datos de un objeto <strong>Field</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="description-property-ado.md">Descripción</a></p></td>
<td><p>Describe un objeto <strong>Error</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="direction-property-ado.md">Direction</a></p></td>
<td><p>Indica si el <strong> Parámetro</strong> representa un parámetro de entrada, un parámetro de salida o ambos, o si el parámetro es el valor devuelto desde un procedimiento almacenado.</p></td>
</tr>
<tr class="even">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>Indica el estado de modificación del registro actual.</p></td>
</tr>
<tr class="odd">
<td><p><a href="eos-property-ado.md">EOS</a></p></td>
<td><p>Indica si la posición actual se encuentra al final de la secuencia.</p></td>
</tr>
<tr class="even">
<td><p><a href="filter-property-ado.md">Filtro</a></p></td>
<td><p>Indica un filtro para datos en un objeto <strong> Recordset </strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="helpcontext-helpfile-properties-ado.md">HelpContext y HelpFile</a></p></td>
<td><p>Indican el archivo de Ayuda y el tema asociados a un objeto <strong>Error</strong>. <strong>HelpContextID</strong>: devuelve un identificador de contexto, como un valor de tipo <strong>Long</strong>, de un tema de un archivo de Ayuda. <strong>HelpFile</strong>: devuelve un valor de tipo <strong>String</strong> que evalúa una ruta de acceso completa resuelta a un archivo de Ayuda.</p></td>
</tr>
<tr class="even">
<td><p><a href="index-property-ado.md">Índice</a></p></td>
<td><p>Indica el nombre del índice en vigor para un objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="isolationlevel-property-ado.md">IsolationLevel</a></p></td>
<td><p>Indica el nivel de aislamiento de un objeto <strong>Connection</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="item-property-ado.md">Item</a></p></td>
<td><p>Indica un miembro específico de una colección, por nombre o número ordinal.</p></td>
</tr>
<tr class="odd">
<td><p><a href="lineseparator-property-ado.md">LineSeparator</a></p></td>
<td><p>Indica el carácter binario que se utiliza como separador de línea en objetos de texto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>Indica el tipo de bloqueos colocados en registros durante la modificación.</p></td>
</tr>
<tr class="odd">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>Indica qué registros se van a ordenar de nuevo en el servidor.</p></td>
</tr>
<tr class="even">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>Indica el número máximo de registros que se va a devolver a un objeto <strong>Recordset</strong> desde una consulta.</p></td>
</tr>
<tr class="odd">
<td><p><a href="mode-property-ado.md">Mode</a></p></td>
<td><p>Indica los permisos disponibles para modificar datos de un objeto <strong>Connection</strong>, <strong>Record</strong> o <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="name-property-ado.md">Nombre</a></p></td>
<td><p>Indica el nombre de un objeto.</p></td>
</tr>
<tr class="odd">
<td><p><a href="nativeerror-property-ado.md">NativeError</a></p></td>
<td><p>Indica el código de error específico de un proveedor para un objeto <strong>Error</strong> dado.</p></td>
</tr>
<tr class="even">
<td><p><a href="number-property-ado.md">Número</a></p></td>
<td><p>Indica el número que identifica de forma exclusiva a un objeto <strong>Error</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="numericscale-property-ado.md">NumericScale</a></p></td>
<td><p>Indica la escala de valores numéricos de un objeto <strong>Parameter</strong> o <strong>Field</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="originalvalue-property-ado.md">OriginalValue</a></p></td>
<td><p>Indica el valor de un objeto <strong>Field</strong> que existía en el registro antes de la realización de cualquier cambio.</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>Indica cuántas páginas de datos contiene el objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>Indica cuántos registros constituyen una página en el objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parentrow-property-ado.md">ParentRow</a></p></td>
<td><p>Establece el contenedor de un objeto <strong>Row</strong> de OLE DB en un objeto <strong>ADORecordConstruction</strong>, de modo que la página origen de la fila se convierta en un objeto <strong>Record</strong> de ADO.</p></td>
</tr>
<tr class="even">
<td><p><a href="parenturl-property-ado.md">ParentURL</a></p></td>
<td><p>Indica una cadena URL absoluta que apunta al objeto <strong>Record</strong> primario del objeto <strong>Record</strong> actual.</p></td>
</tr>
<tr class="odd">
<td><p><a href="position-property-ado.md">Position</a></p></td>
<td><p>Indica la posición actual dentro de un objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="precision-property-ado.md">Precision</a></p></td>
<td><p>Indica el grado de precisión de los valores numéricos de un objeto <strong>Parameter</strong> o de los objetos numéricos <strong>Field</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="prepared-property-ado.md">Preparado</a></p></td>
<td><p>Indica si se va a guardar una versión compilada de un comando antes de la ejecución.</p></td>
</tr>
<tr class="even">
<td><p><a href="provider-property-ado.md">Provider</a></p></td>
<td><p>Indica el nombre del proveedor para un objeto <strong>Connection</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>Indica el número de registros de un objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordtype-property-ado.md">RecordType</a></p></td>
<td><p>Indica el tipo de objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="row-property-ado.md">Fila</a></p></td>
<td><p>Obtiene o establece un objeto <strong>Row</strong> de OLE DB desde o en un objeto <strong>ADORecordConstruction</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p>Obtiene o establece un objeto <strong>RowPosition</strong> de OLE DB desde o en un objeto <strong>ADORecordsetConstruction</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">Conjunto de filas</a></p></td>
<td><p>Obtiene o establece un objeto <strong>Rowset</strong> de OLE DB desde o en un objeto <strong>ADORecordsetConstruction</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="size-property-ado.md">Size</a></p></td>
<td><p>Indica el tamaño máximo en bytes o caracteres de un objeto <strong>Parameter</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Tamaño (objeto Stream de ADO)</a></p></td>
<td><p>Indica el tamaño total de la secuencia en número de bytes.</p></td>
</tr>
<tr class="even">
<td><p><a href="sort-property-ado.md">Sort</a></p></td>
<td><p>Indica uno o más nombres de campo por los que se ordena el objeto <strong>Recordset</strong>, así como si el orden es ascendente o descendente.</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-error.md">Origen (Error ADO)</a></p></td>
<td><p>Indica el nombre del objeto o de la aplicación que ha generado un error originariamente.</p></td>
</tr>
<tr class="even">
<td><p><a href="source-property-ado-record.md">Origen (objeto Record de ADO)</a></p></td>
<td><p>Indica la entidad representada por el objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-recordset.md">Origen (objeto Recordset de ADO)</a></p></td>
<td><p>Indica el origen para los datos de un objeto <strong>Recordset</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="sqlstate-property-ado.md">SQLState</a></p></td>
<td><p>Indica el estado SQL de un objeto <strong>Error</strong> especificado.</p></td>
</tr>
<tr class="odd">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>En todos los objetos aplicables indica si el estado del objeto es abierto o cerrado. Indica, para todos los objetos aplicables que ejecutan un método asincrónico, si el estado actual del objeto está en conexión, ejecución o recuperación</p></td>
</tr>
<tr class="even">
<td><p><a href="status-property-ado-field.md">Estado (campo de ADO)</a></p></td>
<td><p>Indica el estado de un objeto <strong>Field</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="status-property-ado-recordset.md">Estado (objeto Recordset de ADO)</a></p></td>
<td><p>Indica el estado del registro actual con respecto a actualizaciones por lotes u otras operaciones masivas.</p></td>
</tr>
<tr class="even">
<td><p><a href="stayinsync-property-ado.md">StayInSync</a></p></td>
<td><p>En un objeto <strong>Recordset</strong> jerárquico, indica si la referencia a los registros secundarios subyacentes (es decir, el <em>capítulo</em>) cambia cuando la posición de la fila superior en la jerarquía (elemento principal) cambia.</p></td>
</tr>
<tr class="odd">
<td><p><a href="type-property-ado.md">Tipo</a></p></td>
<td><p>Indica el tipo operativo o tipo de datos de un objeto <strong>Parameter</strong>, <strong>Field</strong> o <strong>Property</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="type-property-ado-stream.md">Tipo (objeto Stream de ADO)</a></p></td>
<td><p>Indica el tipo de tipo de datos incluidos en el objeto <strong>Stream</strong> (binarios o texto).</p></td>
</tr>
<tr class="odd">
<td><p><a href="underlyingvalue-property-ado.md">UnderlyingValue</a></p></td>
<td><p>Indica el valor actual de un objeto <strong>Field</strong> de la base de datos.</p></td>
</tr>
<tr class="even">
<td><p><a href="value-property-ado.md">Value</a></p></td>
<td><p>Indica el valor asignado a un objeto <strong>Field</strong>, <strong>Parameter</strong> o <strong>Property</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="version-property-ado.md">Versión</a></p></td>
<td><p>Indica el número de versión de ADO.</p></td>
</tr>
</tbody>
</table>

<br/>
