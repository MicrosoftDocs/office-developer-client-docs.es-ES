---
title: Proveedor de Microsoft OLE DB para Servicio de Active Directory de Microsoft
TOCTitle: Microsoft OLE DB Provider for Microsoft Active Directory Service
ms:assetid: 92d1c967-aa61-f3b5-1c0a-301ef236894c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249647(v=office.15)
ms:contentKeyID: 48546385
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23e1cab32fee6103a046219a7cda8c90f02d9f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288942"
---
# <a name="microsoft-ole-db-provider-for-microsoft-active-directory-service"></a>Proveedor de Microsoft OLE DB para el servicio Microsoft Active Directory

**Se aplica a:** Access 2013, Office 2013

El proveedor de interfaces del servicio de Active Directory (ADSI) de Microsoft permite a ADO conectarse a servicios de directorio heterogéneos mediante ADSI. Esto ofrece a las aplicaciones ADO acceso de solo lectura a los servicios de directorio de Microsoft Windows NT 4.0 y Microsoft Windows 2000, además de a cualquier servicio de directorio compatible con LDAP y a Novell Directory Services. ADSI se basa en un modelo de proveedor, de modo que si hay un nuevo proveedor que ofrece acceso a otro directorio, la aplicación ADO podrá obtener acceso a él sin problemas. El proveedor de ADSI es de subprocesamiento libre y está habilitado para Unicode.

## <a name="connection-string-parameters"></a>Parámetros de la cadena de conexión

Para conectar con este proveedor, establezca el argumento **Provider** de la propiedad [ConnectionString](connectionstring-property-ado.md) en:

```vb 
 
ADSDSOObject 
```

La lectura de la propiedad [Provider](provider-property-ado.md) devolverá también esta cadena.

## <a name="typical-connection-string"></a>Cadena de conexión típica

Una típica cadena de conexión de este proveedor es:

```vb 
 
"Provider=ADSDSOObject;User ID=userName;Password=userPassword;" 
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
<td><p>Especifica el Proveedor OLE DB para Servicio de Active Directory de Microsoft.</p></td>
</tr>
<tr class="even">
<td><p><strong>User ID</strong></p></td>
<td><p>Especifica el nombre de usuario. Si se omite la palabra clave, se utiliza el inicio de sesión actual.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Password</strong></p></td>
<td><p>Especifica la contraseña de usuario. Si se omite la palabra clave, se utiliza el inicio de sesión actual.</p></td>
</tr>
</tbody>
</table>


**Texto del comando**

El proveedor reconoce una cadena de texto de comando de cuatro partes en la siguiente sintaxis:

`"Root; Filter; Attributes[; Scope]"`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Root</em></p></td>
<td><p>Indica el objeto <strong>ADsPath</strong> desde el que se inicia la búsqueda (es decir, la raíz de la búsqueda).</p></td>
</tr>
<tr class="even">
<td><p><em>Filter</em></p></td>
<td><p>Indica el filtro de búsqueda en el formato RFC 1960.</p></td>
</tr>
<tr class="odd">
<td><p><em>Atributos</em></p></td>
<td><p>Indica una lista de los atributos que se van a devolver delimitada por comas.</p></td>
</tr>
<tr class="even">
<td><p><em>Scope</em></p></td>
<td><p>Opcional. Un valor de tipo <strong>String</strong> que especifica el ámbito de la búsqueda. Puede ser uno de los siguientes: Base: buscar solo el objeto base (raíz de la búsqueda).<br />
OneLevel: busque solo un nivel.<br />
Subárbol: busque todo el subárbol.</p></td>
</tr>
</tbody>
</table>


Por ejemplo:

```vb 
 
"<LDAP://DC=ArcadiaBay,DC=COM>;(objectClass=*);sn, givenName; subtree" 
```

El proveedor también admite una instrucción SELECT de SQL como texto del comando. Por ejemplo:

```vb 
 
"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'" 
```

El proveedor no acepta llamadas a procedimientos almacenados o nombres de tabla simples (por ejemplo, la propiedad [CommandType](commandtype-property-ado.md) siempre será **adCmdText**). Vea la documentación de las Interfaces del servicio de Active Directory para obtener una descripción más completa de los elementos de texto de un comando.

## <a name="recordset-behavior"></a>Comportamiento del objeto Recordset

En las tablas siguientes se enumeran las características disponibles en un objeto [Recordset](recordset-object-ado.md) abierto con este proveedor. Solo está disponible el tipo de cursor Estático (**adOpenStatic**).

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
<td><p><a href="bookmark-property-ado.md">Bookmark</a></p></td>
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
<td><p>no disponible</p></td>
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
<td><p><a href="state-property-ado.md">Estado</a></p></td>
<td><p>solo lectura</p></td>
</tr>
<tr class="even">
<td><p><a href="status-property-ado-recordset.md">Estado</a></p></td>
<td><p>solo lectura</p></td>
</tr>
</tbody>
</table>


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
<td><p>No</p></td>
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
<td><p><a href="delete-method-ado-recordset.md">Eliminar</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-recordset.md">Open</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Volver a sincronizar</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Compatible</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Actualizar</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>No</p></td>
</tr>
</tbody>
</table>

