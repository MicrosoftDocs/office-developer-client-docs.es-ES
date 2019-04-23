---
title: Constantes enumeradas de ADO
TOCTitle: ADO enumerated constants
ms:assetid: 7c983acd-8b38-dc3c-6704-46e649ebb7d6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249522(v=office.15)
ms:contentKeyID: 48545841
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 05e5d3a77dc7db5ef5a0d81a3f13d5fc5987f5de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283411"
---
# <a name="ado-enumerated-constants"></a>Constantes enumeradas de ADO

**Se aplica a:** Access 2013, Office 2013

Para ayudar en la depuración, las enumeraciones ADO muestran un valor para cada constante. Sin embargo, este valor es puramente consultivo y puede cambiar de una versión a otra de ADO. El código sólo debería depender del nombre, no del valor real, de cada constante enumerada.

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Constante enumerada</th>
<th>Descripción</th>
</tr>
<tr class="odd">
<td><p><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></p></td>
<td><p>Para un objeto <strong>Recordset</strong> RDS, especifica la prioridad de ejecución del subproceso asincrónico que recupera datos.</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></p></td>
<td><p>Especifica cuándo el proveedor <strong>MSDataShape</strong> vuelve a calcular columnas agregadas y calculadas en un objeto <strong>Recordset</strong> jerárquico.</p></td>
</tr>
<tr class="odd">
<td><p><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></p></td>
<td><p>Especifica qué campos se pueden usar para detectar conflictos durante una actualización optimista de una fila del origen de datos con un objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></p></td>
<td><p>Especifica si el método <strong>UpdateBatch</strong> va seguido de una operación implícita del método <strong>Resync</strong> y, en ese caso, el ámbito de esa operación.</p></td>
</tr>
<tr class="odd">
<td><p><a href="affectenum.md">AffectEnum</a></p></td>
<td><p>Especifica a qué registros afecta una operación.</p></td>
</tr>
<tr class="even">
<td><p><a href="bookmarkenum.md">BookmarkEnum</a></p></td>
<td><p>Especifica un marcador que indica dónde debe comenzar la operación.</p></td>
</tr>
<tr class="odd">
<td><p><a href="commandtypeenum.md">CommandTypeEnum</a></p></td>
<td><p>Especifica cómo se debe interpretar un argumento de comando.</p></td>
</tr>
<tr class="even">
<td><p><a href="compareenum.md">CompareEnum</a></p></td>
<td><p>Especifica la posición relativa de dos registros representados por sus marcadores.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectmodeenum.md">ConnectModeEnum</a></p></td>
<td><p>Especifica los permisos disponibles para modificar datos de un objeto <strong>Connection</strong>, abrir un <strong>Record</strong> o especificar valores para la propiedad <strong>Mode</strong> de los objetos <strong>Record</strong> y <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="connectoptionenum.md">ConnectOptionEnum</a></p></td>
<td><p>Especifica si el método <strong>Open</strong> de un objeto <strong>Connection</strong> debe volver después (sincrónicamente) o antes (asincrónicamente) de que la conexión se establezca.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectpromptenum.md">ConnectPromptEnum</a></p></td>
<td><p>Especifica si se debe mostrar un cuadro de diálogo para pedir parámetros que faltan al abrir una conexión con un origen de datos ODBC.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></p></td>
<td><p>Especifica el comportamiento del método <strong>CopyRecord</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocationenum.md">CursorLocationEnum</a></p></td>
<td><p>Especifica la ubicación del motor de cursor.</p></td>
</tr>
<tr class="even">
<td><p><a href="cursoroptionenum.md">CursorOptionEnum</a></p></td>
<td><p>Especifica qué funcionalidad debería probar el método <strong>Supports</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursortypeenum.md">CursorTypeEnum</a></p></td>
<td><p>Especifica el tipo de cursor usado en un objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="datatypeenum.md">DataTypeEnum</a></p></td>
<td><p>Especifica el tipo de datos de un <strong>campo</strong>, <strong>parámetro</strong> o <strong>propiedad</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="editmodeenum.md">EditModeEnum</a></p></td>
<td><p>Especifica el estado de edición de un registro.</p></td>
</tr>
<tr class="even">
<td><p><a href="errorvalueenum.md">ErrorValueEnum</a></p></td>
<td><p>Especifica el tipo de error ADO en tiempo de ejecución.</p></td>
</tr>
<tr class="odd">
<td><p><a href="eventreasonenum.md">EventReasonEnum</a></p></td>
<td><p>Especifica el motivo que ocasionó un evento.</p></td>
</tr>
<tr class="even">
<td><p><a href="eventstatusenum.md">EventStatusEnum</a></p></td>
<td><p>Especifica el estado actual de la ejecución de un evento.</p></td>
</tr>
<tr class="odd">
<td><p><a href="executeoptionenum.md">ExecuteOptionEnum</a></p></td>
<td><p>Especifica la forma en que un proveedor debe ejecutar un comando.</p></td>
</tr>
<tr class="even">
<td><p><a href="fieldenum.md">FieldEnum</a></p></td>
<td><p>Especifica los campos especiales a los que se hace referencia en la colección <strong>Fields</strong> de un objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="fieldattributeenum.md">FieldAttributeEnum</a></p></td>
<td><p>Especifica uno o más atributos de un objeto <strong>Field</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="fieldstatusenum.md">FieldStatusEnum</a></p></td>
<td><p>Especifica el estado de un objeto <strong>Field</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="filtergroupenum.md">FilterGroupEnum</a></p></td>
<td><p>Especifica el grupo de registros que se deben filtrar en un objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></p></td>
<td><p>Especifica cuántos registros se deben recuperar de un objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="isolationlevelenum.md">IsolationLevelEnum</a></p></td>
<td><p>Especifica el nivel de aislamiento de transacción para un objeto <strong>Connection</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></p></td>
<td><p>Especifica el carácter utilizado como separador de línea en objetos <strong>Stream</strong> de texto.</p></td>
</tr>
<tr class="odd">
<td><p><a href="locktypeenum.md">LockTypeEnum</a></p></td>
<td><p>Especifica el tipo de bloqueo colocado en registros durante su modificación.</p></td>
</tr>
<tr class="even">
<td><p><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></p></td>
<td><p>Especifica qué registros se deben devolver al servidor.</p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></p></td>
<td><p>Especifica el comportamiento del método <strong>MoveRecord</strong> del objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="objectstateenum.md">ObjectStateEnum</a></p></td>
<td><p>Especifica si un objeto está abierto o cerrado, conectando con un origen de datos, ejecutando un comando o recuperando datos.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameterattributesenum.md">ParameterAttributesEnum</a></p></td>
<td><p>Especifica los atributos de un objeto <strong>Parameter</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></p></td>
<td><p>Especifica si el objeto <strong>Parameter</strong> representa un parámetro de entrada, un parámetro de salida o ambos, o si el parámetro es el valor devuelto de un procedimiento almacenado.</p></td>
</tr>
<tr class="odd">
<td><p><a href="persistformatenum.md">PersistFormatEnum</a></p></td>
<td><p>Especifica el formato en que se guardará un objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="positionenum.md">PositionEnum</a></p></td>
<td><p>Especifica la posición actual del puntero de registro dentro de un objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="propertyattributesenum.md">PropertyAttributesEnum</a></p></td>
<td><p>Especifica los atributos de un objeto <strong>Property</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></p></td>
<td><p>Especifica, para el método <strong>Open</strong> del objeto <strong>Record</strong>, si se debe abrir un <strong>Record</strong> existente o crear un nuevo <strong>Record</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></p></td>
<td><p>Especifica opciones para abrir un <strong>Record</strong>. Estos valores se pueden combinar utilizando un operador OR.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordstatusenum.md">RecordStatusEnum</a></p></td>
<td><p>Especifica el estado de un registro con respecto a actualizaciones por lotes y otras operaciones masivas.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtypeenum.md">RecordTypeEnum</a></p></td>
<td><p>Especifica el tipo de objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="resyncenum.md">ResyncEnum</a></p></td>
<td><p>Especifica si los valores subyacentes se sobrescriben con una llamada a <strong>Resync</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="saveoptionsenum.md">SaveOptionsEnum</a></p></td>
<td><p>Especifica si un archivo se debe crear o sobrescribir al guardar desde un objeto <strong>Stream</strong>. Los valores se pueden combinar con un operador AND (Y).</p></td>
</tr>
<tr class="even">
<td><p><a href="schemaenum.md">SchemaEnum</a></p></td>
<td><p>Especifica el tipo de esquema <strong>Recordset</strong> recuperado por el método <strong>OpenSchema</strong>. Especifica la dirección de un registro dentro de un objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="searchdirectionenum.md">SearchDirectionEnum</a></p></td>
<td><p>Especifica la dirección de una búsqueda de registro dentro de un objeto <strong>Recordset</strong>. Especifica el tipo de búsqueda (<strong>Seek</strong>) que se debe ejecutar.</p></td>
</tr>
<tr class="even">
<td><p><a href="seekenum.md">SeekEnum</a></p></td>
<td><p>Especifica el tipo de búsqueda <strong>Seek</strong> que se va a ejecutar. Especifica opciones para abrir un objeto <strong>Stream</strong>. Los valores se pueden combinar con un operador AND.</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></p></td>
<td><p>Especifica opciones para abrir un objeto <strong>Stream</strong>. Los valores se pueden combinar con un operador AND. Especifica si se debe leer toda la secuencia o la línea siguiente de un objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="streamreadenum.md">StreamReadEnum</a></p></td>
<td><p>Especifica si se debe leer toda la secuencia o la línea siguiente de un objeto <strong>Stream</strong>. Especifica el tipo de datos almacenados en un objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamtypeenum.md">StreamTypeEnum</a></p></td>
<td><p>Especifica el tipo de datos almacenado en un objeto <strong>Stream</strong>. Especifica si se agrega un separador de línea a la cadena escrita en un objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="streamwriteenum.md">StreamWriteEnum</a></p></td>
<td><p>Especifica si se agrega un separador de línea a la cadena escrita en el objeto <strong>Stream</strong>. Especifica el formato que se aplica al recuperar un objeto <strong>Recordset</strong> como cadena.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stringformatenum.md">StringFormatEnum</a></p></td>
<td><p>Especifica el formato que se aplica al recuperar un objeto <strong>Recordset</strong> como cadena. Especifica los atributos de transacción de un objeto <strong>Connection</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="xactattributeenum.md">XactAttributeEnum</a></p></td>
<td><p>Especifica los atributos de transacción de un objeto <strong> Connection</strong>.</p></td>
</tr>
</tbody>
</table>

