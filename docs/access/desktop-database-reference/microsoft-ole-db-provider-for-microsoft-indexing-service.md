---
title: Proveedor de Microsoft OLE DB para Servicios de Index Server de Microsoft
TOCTitle: Microsoft OLE DB Provider for Microsoft Indexing Service
ms:assetid: 01c2e75c-950a-dd8a-2b20-bbd916315ec5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248786(v=office.15)
ms:contentKeyID: 48542942
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e41633ddb2730af66ddeee400ad035d5a17ed90d
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25607056"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a>Proveedor de Microsoft OLE DB para Servicios de Index Server de Microsoft


**Se aplica a**: Access 2013 | Office 2013

<<<<<<< HEAD el proveedor Microsoft OLE DB para Microsoft Indexing Service proporciona acceso de sólo lectura mediante programación al sistema de archivos y datos Web indizados por los servicios de Index Server de Microsoft. Las aplicaciones ADO pueden emitir consultas SQL para recuperar contenido e información sobre las propiedades de los archivos.
=== El proveedor Microsoft OLE DB para Microsoft Indexing Service proporciona acceso de sólo lectura mediante programación a los datos del sistema y web de archivo indizados por el servicio de Index Server de Microsoft. Las aplicaciones ADO pueden emitir consultas SQL para recuperar contenido e información sobre las propiedades de los archivos.
>>>>>>> master

El proveedor es de subprocesamiento libre y está habilitado para Unicode.

## <a name="connection-string-parameters"></a>Parámetros de la cadena de conexión

Para conectar con este proveedor, establezca el argumento **Provider=** de la propiedad [ConnectionString](connectionstring-property-ado.md) en:

```vb 
 
MSIDXS 
```

La lectura de la propiedad [Provider](provider-property-ado.md) devolverá también esta cadena.

## <a name="typical-connection-string"></a>Cadena de conexión típica

Una típica cadena de conexión de este proveedor es:

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
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
<td><p>Especifica el Proveedor OLE DB para los Servicios de Index Server. Normalmente ésta es la única palabra clave especificada en la cadena de conexión.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Source</strong></p></td>
<td><p>Especifica el nombre de catálogo de los Servicios de Index Server. Si no se especifica esta palabra clave, se utiliza el catálogo predeterminado del sistema.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Locale Identifier</strong></p></td>
<td><p>Especifica un número exclusivo de 32 bits (por ejemplo, 1033) que indica preferencias relacionadas con el idioma del usuario. Estas preferencias indican el formato de las fechas y las horas, el modo en que los elementos se ordenan alfabéticamente, en que se comparan las cadenas, etc. Si no se especifica esta palabra clave, se utiliza el identificador de configuración regional predeterminado del sistema.</p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a>Texto del comando

La sintaxis de las consultas SQL de los Servicios de Index Server se compone de extensiones de la instrucción **SELECT** de SQL-92 y sus cláusulas **FROM** y **WHERE**. Los resultados de la consulta se devuelven a través de conjuntos de filas de OLE DB, que pueden ser usados por ADO y manipulados como objetos [Recordset](recordset-object-ado.md).

Puede buscar palabras o frases exactas o utilizar comodines para buscar patrones o raíces de palabras. La búsqueda lógica se puede basar en decisiones booleanas, términos sopesados o proximidad a otras palabras. También se puede buscar por "texto libre", que busca coincidencias basadas en el significado en lugar de en palabras exactas.

El proveedor no acepta llamadas a procedimientos almacenados o nombres de tabla simples (por ejemplo, la propiedad [CommandType](commandtype-property-ado.md) siempre será **adCmdText**).

## <a name="recordset-behavior"></a>Comportamiento de Recordset

En las tablas siguientes se enumeran las características disponibles en un objeto **Recordset** abierto con este proveedor. El tipo de cursor estático (**adOpenStatic**) está disponible.

Para obtener información más detallada acerca del comportamiento del objeto **Recordset** para la configuración del proveedor, ejecute el método [Supports](supports-method-ado.md) y enumere la colección [Properties](properties-collection-ado.md) del objeto **Recordset** para determinar si las propiedades dinámicas específicas del proveedor están presentes.

Disponibilidad de las propiedades estándar del objeto **Recordset** de ADO:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Propiedad</p></th>
<th><p>Disponibilidad</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="odd">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>solo lectura</p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">BOF</a></p></td>
<td><p>solo lectura</p></td>
</tr>
<tr class="odd">
<td><p><a href="bookmark-property-ado.md">Marcador</a>*</p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>siempre <strong>adUseServer</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>siempre <strong>adOpenStatic</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>siempre <strong>adEditNone</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">EOF</a></p></td>
<td><p>solo lectura</p></td>
</tr>
<tr class="odd">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="odd">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>No disponible</p></td>
</tr>
<tr class="even">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>solo lectura</p></td>
</tr>
<tr class="even">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>solo lectura</p></td>
</tr>
<tr class="even">
<td><p><a href="source-property-ado-recordset.md">Source</a></p></td>
<td><p>lectura y escritura</p></td>
</tr>
<tr class="odd">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>solo lectura</p></td>
</tr>
<tr class="even">
<td><p><a href="status-property-ado-recordset.md">Status</a></p></td>
<td><p>solo lectura</p></td>
</tr>
</tbody>
</table>


\*Marcadores deben estar habilitados en el proveedor en orden para esta característica de que existan en el **conjunto de registros**.

Disponibilidad de métodos estándar **Recordset** ADO:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Método</p></th>
<th><p>¿Disponible?</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="move-method-ado.md">Mover</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Métodos MoveFirst</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">Open</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="supports-method-ado.md">Admite</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="update-method-ado.md">Actualizar</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>No</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

Para detalles de implementación específicos e información funcional acerca del proveedor de Microsoft OLE DB para Microsoft Indexing Service, consulte referencia de Microsoft OLE DB del programador.

