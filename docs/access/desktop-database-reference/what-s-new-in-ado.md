---
title: ¿Qué es nuevo en ActiveX Data Objects (ADO)
TOCTitle: What's new in ADO
ms:assetid: fd3d0f9c-e9df-d130-13e3-757620e9400c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250297(v=office.15)
ms:contentKeyID: 48548905
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 593daf08da1b4ce435d17f2a6deedfa3e89dbd32
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713635"
---
# <a name="whats-new-in-ado"></a>Novedades de ADO

**Se aplica a**: Access 2013, Office 2013 
 
ADO 2.5 incluye las siguientes características nuevas y una documentación mejorada. Esta lista hace referencia a ADO, ADO MD y ADOX.

## <a name="new-features"></a>Nuevas características

- **[Objetos Record y Stream](chapter-10-records-and-streams.md)**

  Esta versión de ADO introduce el objeto [Record](record-object-ado.md) , que puede representar y administrar elementos como directorios y archivos en un sistema de archivos y carpetas y mensajes en un sistema de correo electrónico. Un objeto **Record** también puede representar una fila en un objeto [Recordset](recordset-object-ado.md), si bien los objetos **Record** y **Recordset** tienen métodos y propiedades diferentes.

  El nuevo objeto [Stream](stream-object-ado.md) permite leer, escribir y administrar la secuencia binaria de bytes o texto que componen una secuencia de archivos o mensajes.

- **[Uso de la dirección URL](absolute-and-relative-urls.md)**

  Esta versión también introduce el uso de Localizadores uniformes de recursos (URL), como alternativa a las cadenas de conexión y texto de comando, para denominar los objetos de un almacén de datos. Estos localizadores se pueden usar con los objetos [Connection](connection-object-ado.md) y **Recordset** existentes, así como con los nuevos objetos **Record** y **Stream**.

  Con esta versión, ADO admite proveedores OLE DB que reconocen sus propios esquemas URL. Por ejemplo, [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* que obtiene acceso al sistema de archivos de Windows 2000, reconoce el esquema HTTP existente.

- **[Campos especiales para proveedores de orígenes de documentos](records-and-provider-supplied-fields.md)**

  Una clase especial de proveedores, denominados proveedores de *orígenes de documentos* , administración de documentos y carpetas. Cuando un objeto **Record** representa un documento, o un objeto **Recordset** representa una carpeta de documentos, el proveedor de orígenes de documentos rellena esos objetos con un conjunto único de campos que describen las características del documento. Estos campos constituyen un objeto **Record** o **Recordset**de *recurso* .

## <a name="new-reference-topics"></a>Nuevos temas de referencia

### <a name="properties"></a>Propiedades

Esta versión incluye las siguientes propiedades nuevas.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Propiedad</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="charset-property-ado.md">Juego de caracteres</a></p></td>
<td><p>Indica el juego de caracteres al que debe convertirse el contenido de un objeto <strong>Stream</strong> de texto.</p></td>
</tr>
<tr class="even">
<td><p><a href="eos-property-ado.md">EOS</a></p></td>
<td><p>Indica si la posición actual se encuentra al final de la secuencia.</p></td>
</tr>
<tr class="odd">
<td><p><a href="lineseparator-property-ado.md">LineSeparator</a></p></td>
<td><p>Indica el carácter binario que se utiliza como separador de línea en objetos de texto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="mode-property-ado.md">Mode</a></p></td>
<td><p>Indica los permisos disponibles para modificar datos de un objeto <strong>Connection</strong>, <strong>Record</strong> o <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parenturl-property-ado.md">ParentURL</a></p></td>
<td><p>Indica una cadena URL absoluta que apunta al objeto <strong>Record</strong> primario del objeto <strong>Record</strong> actual.</p></td>
</tr>
<tr class="even">
<td><p><a href="position-property-ado.md">Position</a></p></td>
<td><p>Indica la posición actual dentro de un objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtype-property-ado.md">RecordType</a></p></td>
<td><p>Indica el tipo de objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Size</a></p></td>
<td><p>Indica el tamaño de la secuencia en número de bytes.</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-record.md">Source</a></p></td>
<td><p>Indica la entidad representada por el objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>En todos los objetos aplicables indica si el estado del objeto es abierto o cerrado. Indica para todos los objetos aplicables que ejecutan un método asincrónico si el objeto se encuentra actualmente en estado de conexión, ejecución o recuperación.</p></td>
</tr>
<tr class="odd">
<td><p><a href="type-property-ado-stream.md">Tipo</a></p></td>
<td><p>Indica el tipo de datos incluidos en el objeto <strong>Stream</strong> (binario o de texto).</p></td>
</tr>
</tbody>
</table>

### <a name="methods"></a>Métodos

Esta versión incluye los siguientes métodos nuevos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Método</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a></p></td>
<td><p>Copia un archivo o directorio y su contenidos en otra ubicación.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p>Copia el número especificado de caracteres o bytes (según el <strong>tipo</strong>) en el <strong>objeto</strong> de <strong>secuencia</strong> en otro objeto <strong>Stream</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>Elimina un archivo o directorio y todos sus subdirectorios.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Vaciar</a></p></td>
<td><p>Vacía el contenido del objeto <strong>Stream</strong> que permanece en el búfer de ADO en el objeto subyacente al que está asociado el objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Devuelve un objeto <strong>Recordset</strong> cuyas filas representan los archivos y subdirectorios del directorio representado por este objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
<td><p>Carga el contenido de un archivo existente en un objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>Mueve un archivo o directorio y su contenido a otra ubicación.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-record.md">Open</a></p></td>
<td><p>Abre un objeto <strong>Record</strong> existente o crea un nuevo archivo o directorio.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Open</a></p></td>
<td><p>Abre un objeto <strong>Stream</strong> para manipular secuencias de datos binarios o de texto.</p></td>
</tr>
<tr class="even">
<td><p><a href="read-method-ado.md">Read</a></p></td>
<td><p>Lee un número especificado de bytes de un objeto <strong>Stream</strong> binario.</p></td>
</tr>
<tr class="odd">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
<td><p>Lee un número especificado de caracteres de un objeto <strong>Stream</strong> de texto.</p></td>
</tr>
<tr class="even">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p>Guarda el contenido binario de un objeto <strong>Stream</strong> en un archivo.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Establece la posición que es el final de la secuencia.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Omite una línea completa al leer un objeto <strong>Stream</strong> de texto.</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Write</a></p></td>
<td><p>Escribe datos binarios en un objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">WriteText</a></p></td>
<td><p>Escribe una cadena de texto especificada en un objeto <strong>Stream</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a>Documentación nueva y mejorada

- **[Temas de ejemplo de código](ado-code-examples.md)**

  Los ejemplos se han ampliado para contienen ejemplos de código escritos en Microsoft Visual C++ y Microsoft Visual J ++. Estos ejemplos de código se pueden copiar y pegar en el editor.

- **[Temas de proveedor](appendix-a-providers.md)**

  Se ha incluido un tema nuevo en el que se explica cómo utilizar ADO con [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).

- **[Programar con ADO](appendix-c-programming-with-ado.md)**

  Esta nueva sección contiene sugerencias y trucos para utilizar ADO con diversos lenguajes de programación. Contiene los índices de sintaxis existentes para las extensiones de Visual C++ para ADO y ADO/WFC, así como nueva información específica para los desarrolladores que usan Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++, o Microsoft Visual J ++.

