---
title: Miembros del campo (DAO)
TOCTitle: Field Members
ms:assetid: 4b6a587f-1fd0-37fb-db7d-75b587a8dc60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193511(v=office.15)
ms:contentKeyID: 48544689
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a0e448662384572163fca074e554a5e30be30a7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703604"
---
# <a name="field-members-dao"></a>Miembros del campo (DAO)


**Se aplica a**: Access 2013, Office 2013

Un objeto Field representa una columna de datos con un tipo de datos común y un conjunto de propiedades común.

## <a name="methods"></a>Métodos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></p></td>
<td><p>Agrega datos de una expresión de cadena a un objeto <strong><a href="field-object-dao.md">Field</a></strong> de Memo o binario largo en un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Crea un nuevo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido por el usuario (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></p></td>
<td><p>Devuelve todo o parte del contenido de un objeto <strong>Memo</strong> o <strong>Long Binary</strong> <strong><a href="field-object-dao.md">Field</a></strong> en la colección <strong><a href="fields-collection-dao.md">Fields</a></strong> de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Propiedades

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="field-allowzerolength-property-dao.md">Permitir longitud cero</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica si una cadena de longitud cero (&quot;&quot;) es un valor válido para la propiedad <strong><a href="field-value-property-dao.md">Value</a></strong> del objeto <strong><a href="field-object-dao.md">Field</a></strong> con un tipo de datos texto o Memo (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-attributes-property-dao.md">Atributos</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica una o varias características de un objeto <strong><a href="field-object-dao.md">Field</a></strong>. <strong>Long</strong> de lectura y escritura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>Devuelve un valor que especifica la secuencia del criterio de ordenación en texto para comparación u ordenación de la cadena (sólo para áreas de trabajo de Microsoft Access). <strong>Long</strong> de solo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></p></td>
<td><p>Devuelve un valor que indica si los datos del campo representado por un objeto <strong><a href="field-object-dao.md">Field</a></strong> se pueden actualizar.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></p></td>
<td><p>Establece o devuelve el valor predeterminado de un objeto <strong><a href="field-object-dao.md">Field</a></strong>. Para un objeto <strong>Field</strong> que todavía no se ha anexado a la colección <strong><a href="fields-collection-dao.md">Fields</a></strong>, esta propiedad es de lectura y escritura (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-fieldsize-property-dao.md">TamañoDelCampo</a></strong></p></td>
<td><p>Devuelve el número de bytes usados en la base de datos (en lugar de en la memoria) de un objeto Memo o Long Binary <strong><a href="field-object-dao.md">Field</a></strong> en la colección <strong><a href="fields-collection-dao.md">Fields</a></strong> de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></p></td>
<td><p>Establece o devuelve un valor que especifica el nombre del objeto <strong><a href="field-object-dao.md">Field</a></strong> en una tabla externa que corresponde a un campo en una tabla primaria para una relación (sólo para áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-name-property-dao.md">Name</a></strong></p></td>
<td><p>Devuelve o establece el nombre del objeto especificado. <strong>String</strong> de lectura y escritura si el objeto no se anexó a una colección. <strong>String</strong> de solo lectura si el objeto se anexó a una colección.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></p></td>
<td><p>Establece o devuelve la posición relativa de un objeto <strong><a href="field-object-dao.md">Field</a></strong> en una colección <strong><a href="fields-collection-dao.md">Fields</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></p></td>
<td><p>Uno de los valores de <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</p>
<td><p><strong>Nota</strong>: las áreas de trabajo de ODBCDirect no son compatibles con Microsoft Access 2013. Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</p>
<p>Devuelve el valor de un <strong>Field</strong> en la base de datos existente cuando comienza la actualización del último lote (sólo para áreas de trabajo de ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-properties-property-dao.md">Propiedades</a></strong></p></td>
<td><p>Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado. solo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-required-property-dao.md">Necesario</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica si un objeto <strong><a href="field-object-dao.md">Field</a></strong> requiere un valor no Null.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-fieldsize-property-dao.md">Tamaño</a></strong></p></td>
<td><p>Devuelve el número de bytes usados en la base de datos (en lugar de en la memoria) de un objeto Memo o Long Binary <strong><a href="field-object-dao.md">Field</a></strong> en la colección <strong><a href="fields-collection-dao.md">Fields</a></strong> de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></p></td>
<td><p>Devuelve un valor que indica el nombre del campo que es el origen de los datos correspondientes a un objeto <strong>Field</strong>. <strong>String</strong> de sólo lectura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></p></td>
<td><p>Devuelve un valor que indica el nombre de la tabla que es la fuente original de los datos para un objeto <strong>Field</strong>. <strong>String</strong> de sólo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-type-property-dao.md">Tipo</a></strong></p></td>
<td><p>Establece un valor que indica el tipo operativo o de datos de un objeto. <strong>Integer</strong> de lectura y escritura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></p></td>
<td><p>Establece o devuelve un valor que especifica si el valor de un objeto <strong><a href="field-object-dao.md">Field</a></strong> se valida o no inmediatamente cuando se establece la propiedad <strong><a href="field-value-property-dao.md">Value</a></strong> del objeto (únicamente áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Establece o devuelve un valor que valida los datos de un campo cuando se cambia o agrega a una tabla (únicamente áreas de trabajo de Microsoft Access). <strong>String</strong> de lectura y escritura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Establece o devuelve un valor que especifica el texto del mensaje que la aplicación muestra si el valor de un objeto <strong>Field</strong> no cumple la regla de validación especificada por el valor de la propiedad <strong>ValidationRule</strong> (únicamente áreas de trabajo de Microsoft Access). <strong>String</strong> de lectura y escritura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-value-property-dao.md">Value</a></strong></p></td>
<td><p>Establece o devuelve el valor de un objeto. <strong>Variant</strong> de lectura y escritura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></p></td>
<td><p>Uno de los valores de <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</p>
<td><p><strong>Nota</strong>: las áreas de trabajo de ODBCDirect no son compatibles con Microsoft Access 2013. Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</p>
<p>Devuelve un valor existente en la base de datos que es más actual que la propiedad <strong>OriginalValue</strong> según lo determinado por un conflicto de actualización por lotes (sólo para áreas de trabajo de ODBCDirect).</p></td>
</tr>
</tbody>
</table>

