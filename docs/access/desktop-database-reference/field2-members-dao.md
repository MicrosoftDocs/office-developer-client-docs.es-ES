---
title: Field2 (miembros) (DAO)
TOCTitle: Field2 Members
ms:assetid: 27829bbc-8b4e-c7eb-f29b-bcbef341f9fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191913(v=office.15)
ms:contentKeyID: 48543839
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf3deac487f1e114bea2a69d5423a210a51a5944
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707146"
---
# <a name="field2-members-dao"></a>Field2 (miembros) (DAO)


**Se aplica a**: Access 2013, Office 2013

Un objeto Field2 representa una columna de datos con un tipo de datos común y un conjunto de propiedades común.

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
<td><p><strong><a href="field2-appendchunk-method-dao.md">AppendChunk</a></strong></p></td>
<td><p>Agrega datos de una expresión de cadena a un objeto <strong>Field2</strong> Memo o Binario largo en un <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Crea un nuevo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido por el usuario (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-getchunk-method-dao.md">GetChunk</a></strong></p></td>
<td><p>Devuelve todo o parte del contenido de un objeto <strong>Memo</strong> o <strong>Long BinaryField2</strong> en la colección <strong><a href="fields-collection-dao.md">Fields</a></strong> de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-loadfromfile-method-dao.md">LoadFromFile</a></strong></p></td>
<td><p>Carga el archivo especificado desde el disco.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-savetofile-method-dao.md">SaveToFile</a></strong></p></td>
<td><p>Guarda datos adjuntos en el disco.</p></td>
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
<td><p><strong><a href="field2-allowzerolength-property-dao.md">Permitir longitud cero</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica si una cadena de longitud cero (&quot;&quot;) es un valor válido para la propiedad <strong><a href="field-value-property-dao.md">Value</a></strong> del objeto <strong>Field2</strong> con un tipo de datos texto o Memo (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-appendonly-property-dao.md">AppendOnly</a></strong></p></td>
<td><p>Obtiene o establece un valor de tipo <strong>Boolean</strong> que indica si el campo especificado está configurado para que se puedan agregar nuevos valores al contenido existente en el campo. Lectura y escritura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-attributes-property-dao.md">Atributos</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica una o varias características de un objeto <strong>Field2</strong>. <strong>Long</strong> de lectura y escritura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>Devuelve un valor que especifica la secuencia del criterio de ordenación en texto para comparación u ordenación de la cadena (sólo para áreas de trabajo de Microsoft Access). <strong>Long</strong> de solo lectura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-complextype-property-dao.md">ComplexType</a></strong></p></td>
<td><p>Devuelve un objeto <strong><a href="complextype-object-dao.md">ComplexType</a></strong> que representa un campo multivalor. Sólo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-dataupdatable-property-dao.md">DataUpdatable</a></strong></p></td>
<td><p>Devuelve un valor que indica si se pueden actualizar los datos en el campo representado por un objeto <strong>Field2</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-defaultvalue-property-dao.md">DefaultValue</a></strong></p></td>
<td><p>Establece o devuelve el valor predeterminado de un objeto <strong>Field2</strong>. Para un objeto <strong>Field2</strong> no anexado todavía a la colección <strong><a href="fields-collection-dao.md">Fields</a></strong>, esta propiedad es de lectura y escritura (sólo para áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-expression-property-dao.md">Expresión</a></strong></p></td>
<td><p>Es de lectura y escritura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-fieldsize-property-dao.md">TamañoDelCampo</a></strong></p></td>
<td><p>Devuelve el número de bytes usados en la base de datos (en lugar de en la memoria) de un objeto Memo o Long Binary <strong>Field2</strong> en la colección <strong><a href="fields-collection-dao.md">Fields</a></strong> de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-foreignname-property-dao.md">ForeignName</a></strong></p></td>
<td><p>Establece o devuelve un valor que especifica el nombre del objeto <strong>Field2</strong> en una tabla externa que corresponde a un campo de una tabla primaria para una relación (sólo para áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-iscomplex-property-dao.md">IsComplex</a></strong></p></td>
<td><p>Devuelve un valor de tipo <strong>Boolean</strong> que indica si el campo especificado es un campo multivalor. Sólo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-name-property-dao.md">Name</a></strong></p></td>
<td><p>Devuelve o establece el nombre del objeto especificado. <strong>String</strong> de lectura y escritura si el objeto no se anexó a una colección. <strong>String</strong> de solo lectura si el objeto se anexó a una colección.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-ordinalposition-property-dao.md">OrdinalPosition</a></strong></p></td>
<td><p>Establece o devuelve la posición relativa de un objeto <strong>Field2</strong> en una colección <strong><a href="fields-collection-dao.md">Fields</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-originalvalue-property-dao.md">OriginalValue</a></strong></p></td>
<td><p>Uno de los valores de <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</p>
<td><p><strong>Nota</strong>: las áreas de trabajo de ODBCDirect no son compatibles con Microsoft Access 2013. Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</p>
<p>Devuelve el valor de un <strong>Field2</strong> en la base de datos existente cuando comienza la actualización del último lote (sólo para áreas de trabajo de ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-properties-property-dao.md">Propiedades</a></strong></p></td>
<td><p>Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado. solo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-required-property-dao.md">Necesario</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica si un objeto <strong>Field2</strong> requiere un valor no Null.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-size-property-dao.md">Tamaño</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica el tamaño máximo, en bytes, de un objeto <strong>Field2</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-sourcefield-property-dao.md">SourceField</a></strong></p></td>
<td><p>Devuelve un valor que indica el nombre del campo que es la fuente original de los datos para un objeto <strong>Field2</strong>. <strong>String</strong> de sólo lectura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-sourcetable-property-dao.md">SourceTable</a></strong></p></td>
<td><p>Devuelve un valor que indica el nombre de la tabla que es la fuente original de los datos para un objeto <strong>Field2</strong>. <strong>String</strong> de sólo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-type-property-dao.md">Tipo</a></strong></p></td>
<td><p>Establece un valor que indica el tipo operativo o de datos de un objeto. <strong>Integer</strong> de lectura y escritura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validateonset-property-dao.md">ValidateOnSet</a></strong></p></td>
<td><p>Establece o devuelve un valor que especifica si el valor de un objeto <strong>Field2</strong> se valida inmediatamente cuando se establece la propiedad del objeto <strong>Value</strong> (sólo para áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Establece o devuelve un valor que valida los datos de un campo cuando se cambia o agrega a una tabla (únicamente áreas de trabajo de Microsoft Access). <strong>String</strong> de lectura y escritura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Establece o devuelve un valor que especifica el texto del mensaje que su aplicación muestra si el valor de un objeto <strong>Field2</strong> no satisface la regla de validación que especifica el valor de la propiedad <strong>ValidationRule</strong> (sólo para áreas de trabajo de Microsoft Access). <strong>String</strong> de lectura y escritura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-value-property-dao.md">Value</a></strong></p></td>
<td><p>Establece o devuelve el valor de un objeto. <strong>Variant</strong> de lectura y escritura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-visiblevalue-property-dao.md">VisibleValue</a></strong></p></td>
<td><p>Uno de los valores de <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</p>
<td><p><strong>Nota</strong>: las áreas de trabajo de ODBCDirect no son compatibles con Microsoft Access 2013. Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</p>
<p>Devuelve un valor existente en la base de datos que es más actual que la propiedad <strong>OriginalValue</strong> según lo determinado por un conflicto de actualización por lotes (sólo para áreas de trabajo de ODBCDirect).</p></td>
</tr>
</tbody>
</table>

