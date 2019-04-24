---
title: Registros y campos proporcionados por el proveedor
TOCTitle: Records and provider-supplied fields
ms:assetid: cde72d6a-b9b0-9636-581d-68239a3f522d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250022(v=office.15)
ms:contentKeyID: 48547776
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ebbfeb303bb575928f09858db5d3a34cf2171ce0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300759"
---
# <a name="records-and-provider-supplied-fields"></a>Registros y campos proporcionados por el proveedor

**Se aplica a:** Access 2013, Office 2013

Cuando se abre un objeto [Record](record-object-ado.md), su origen puede ser la actual fila de un objeto [Recordset](recordset-object-ado.md) abierto, una dirección URL absoluta o una dirección URL relativa junto con un objeto [Connection](connection-object-ado.md) abierto.

Si el objeto **Record** se abre desde un objeto **Recordset**, la colección **Fields** del objeto [Record](fields-collection-ado.md) contendrá todos los campos de **Recordset**, además de los campos agregados por el proveedor subyacente.

El proveedor puede insertar campos adicionales que sirven de características complementarias del objeto **Record**. Como resultado, un objeto **Record** puede tener campos únicos no incluidos en el objeto **Recordset** como conjunto o cualquier objeto **Record** derivado de otra fila del objeto **Recordset**.

Por ejemplo, todas las filas de un **objeto Recordset** derivado de un origen de datos de correo electrónico podrían tener columnas como from, to y Subject. Un objeto **Record** derivado de ese objeto **Recordset** tendrá los mismos campos. Sin embargo, el objeto **Record** también puede tener otros campos únicos para el mensaje concreto representado por ese **Record**, como Datos adjuntos y CC (Con copia).

Si bien el objeto **Record** y la actual fila del objeto **Recordset** tienen los mismos campos, son diferentes porque los objetos **Record** y **Recordset** tienen métodos y propiedades distintos.

Un campo que tienen en común **Record** y **Recordset** puede modificarse en cualquiera de los objetos. Sin embargo, el campo no se puede eliminar en el objeto **Record**, aunque el proveedor subyacente permita establecer el campo en null.

Tras abrir el objeto **Record**, puede agregar campos mediante programación. También puede eliminar los campos que agregó, pero no puede eliminar campos del objeto **Recordset** original.

Asimismo, puede abrir el objeto **Record** directamente desde una dirección URL. En este caso, los campos agregados al objeto **Record** dependen del proveedor subyacente. Actualmente, la mayoría de los proveedores agregan un conjunto de campos que describen la entidad representada por el objeto **Record**. Si la entidad consta de una secuencia de bytes, como un archivo simple, normalmente se puede abrir un objeto [Stream](stream-object-ado.md) desde el objeto **Record**.

## <a name="special-fields-for-document-source-providers"></a>Campos especiales para proveedores de orígenes de documentos

Una clase especial de proveedores, denominados *proveedores de orígenes de documentos*, administra las carpetas y los documentos. Cuando un objeto **Record** representa un documento o un objeto **Recordset** representa una carpeta de documentos, el proveedor de orígenes de documentos rellena esos objetos con un conjunto único de campos que describen las características del documento en lugar del propio documento. Normalmente, un campo contiene una referencia al objeto **Stream** que representa el documento.

Estos campos constituyen un objeto **Record** o **Recordset** de recurso y se enumeran para los proveedores específicos que los admiten en [Apéndice A: Proveedores](appendix-a-providers.md).

Dos constantes indican la colección **Fields** de un objeto **Record** o **Recordset** de recurso para recuperar un par de campos de uso común. La propiedad **Value** del objeto [Field](value-property-ado.md) devuelve el contenido deseado.

  - El campo al que se obtiene acceso con la constante **adDefaultStream** contiene una secuencia asociada al objeto **Record** o **Recordset**. El proveedor asigna una secuencia predeterminada a un objeto.

  - El campo al que se obtiene acceso con la constante **adRecordURL** contiene la dirección URL absoluta que identifica el documento.

Un proveedor de orígenes de documentos no admite la colección [Properties](properties-collection-ado.md) de los objetos **Record** y **Field**. El contenido de la colección **Properties** es nulo para dichos objetos.

Un proveedor de orígenes de documentos puede agregar una propiedad específica, como **Datasource Type**, para identificar si es un proveedor de orígenes de documentos. Para obtener más información sobre cómo determinar el tipo de proveedor, vea la documentación de su proveedor.

## <a name="resource-recordset-columns"></a>Columnas de conjuntos de registros de recurso

Un *conjunto de registros de recurso* consta de las columnas siguientes.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de columna</p></th>
<th><p>Tipo</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RESOURCE_PARSENAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Sólo lectura.

Indica la dirección URL del recurso.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_PARENTNAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Sólo lectura.

Indica la dirección URL absoluta del registro primario.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_ABSOLUTEPARSENAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Sólo lectura.

Indica la dirección URL absoluta del recurso, que es la concatenación de PARENTNAME y PARSENAME.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_ISHIDDEN</p></td>
<td><p>AdBoolean</p></td>
<td><p>Es True si el recurso está oculto.

No se devolverá ninguna fila, a menos que el comando que crea el conjunto de filas seleccione explícitamente filas donde el valor de RESOURCE_ISHIDDEN es True.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_ISREADONLY</p></td>
<td><p>AdBoolean</p></td>
<td><p>Es True si el recurso es de sólo lectura.

Al intentar abrir este recurso con DBBINDFLAG_WRITE, se generará un error con DB_E_READONLY.

Esta propiedad se puede modificar, incluso si el recurso se ha abierto sólo para leerlo.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_CONTENTTYPE</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Indica el uso probable del documento; por ejemplo, un expediente de abogado. Esto puede corresponder a la plantilla de Office utilizada para crear el documento.&quot;&quot;</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_CONTENTCLASS</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Indica el tipo MIME del documento, que indica el formato como &quot;text/HTML&quot;'.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_CONTENTLANGUAGE</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Indica el idioma en el que se almacena el contenido.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_CREATIONTIME</p></td>
<td><p>adFileTime</p></td>
<td><p>Sólo lectura.

Indica una estructura FILETIME que contiene la hora de creación del recurso.

El tiempo se indica en formato UTC (Horario universal coordinado).</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_LASTACCESSTIME</p></td>
<td><p>AdFileTime</p></td>
<td><p>Sólo lectura.

Indica una estructura FILETIME que contiene la hora del último acceso al recurso. La hora está en formato UTC. Los miembros de FILETIME son cero si el proveedor no admite este miembro de hora.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_LASTWRITETIME</p></td>
<td><p>AdFileTime</p></td>
<td><p>Sólo lectura.

Indica una estructura FILETIME que contiene la hora a la que se escribió el recurso por última vez.

La hora se especifica en formato UTC.

Los miembros de FILETIME son cero si el proveedor no admite este miembro de hora.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_STREAMSIZE</p></td>
<td><p>asUnsignedBigInt</p></td>
<td><p>Sólo lectura.

Indica el tamaño, en bytes, de la secuencia predeterminada del recurso.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_ISCOLLECTION</p></td>
<td><p>AdBoolean</p></td>
<td><p>Sólo lectura.

Es True si el recurso es una colección, como un directorio.

Es False si el recurso es un archivo simple.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_ISSTRUCTUREDDOCUMENT</p></td>
<td><p>AdBoolean</p></td>
<td><p>Es True si el recurso es un documento estructurado.

Es False si el recurso no es un documento estructurado.

Podría ser una colección o un archivo simple.</p></td>
</tr>
<tr class="odd">
<td><p>DEFAULT_DOCUMENT</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Sólo lectura.

Indica que este recurso contiene una dirección URL al documento simple predeterminado de una carpeta o un documento estructurado.

Se utiliza cuando se solicita la secuencia predeterminada de un recurso.

Esta propiedad está en blanco en el caso de un archivo simple.</p></td>
</tr>
<tr class="even">
<td><p>CHAPTERED_CHILDREN</p></td>
<td><p>AdChapter</p></td>
<td><p>Sólo lectura. Es opcional. Indica el capítulo del conjunto de filas que contiene los objetos secundarios del recurso. (<em>OLE DB Provider for Internet Publishing</em> no utiliza esta columna.)</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_DISPLAYNAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Sólo lectura.

Indica el nombre para mostrar del recurso.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_ISROOT</p></td>
<td><p>AdBoolean</p></td>
<td><p>Sólo lectura.

Es True si el recurso es la raíz de una colección o un documento estructurado.</p></td>
</tr>
</tbody>
</table>

