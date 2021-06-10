---
title: Miembros QueryDef (DAO)
TOCTitle: QueryDef Members
ms:assetid: 3f914d23-aa63-3ebd-1d86-4f53da71131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192855(v=office.15)
ms:contentKeyID: 48544403
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b3afc134636d5621f38ece4530be5312e42bc74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302985"
---
# <a name="querydef-members-dao"></a>Miembros QueryDef (DAO)


**Se aplica a:** Access 2013, Office 2013

Un objeto QueryDef es una definición de una consulta almacenada en una base de datos del motor de base de datos de Microsoft Access.

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
<td><p><strong><a href="querydef-cancel-method-dao.md">Cancel</a></strong></p></td>
<td><p><strong>NOTA</strong>: las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</p>
<p>Cancela la ejecución de una llamada a método asincrónica que está pendiente (sólo áreas de trabajo de ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-close-method-dao.md">Close</a></strong></p></td>
<td><p>Cierra un objeto <strong>QueryDef</strong> abierto.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Crea un nuevo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido por el usuario (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-execute-method-dao.md">Execute</a></strong></p></td>
<td><p>Ejecuta una instrucción SQL en el objeto especificado.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Crea un nuevo objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> y lo anexa a la colección <strong>Recordsets</strong>.</p></td>
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
<td><p><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></p></td>
<td><p>Establece o devuelve el número de registros recuperados de un origen de datos ODBC que se almacenarán localmente en caché. <strong>Long</strong> de lectura y escritura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-connect-property-dao.md">Conectar</a></strong></p></td>
<td><p>Establece o devuelve un valor que proporciona información sobre el origen de la base de datos utilizada en una consulta de paso a través. <strong>String</strong> de sólo lectura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Devuelve la fecha y la hora en la que se creó un objeto (sólo para áreas de trabajo de Microsoft Access). <strong>Variant</strong> de sólo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>Devuelve una colección <strong><a href="fields-collection-dao.md">Fields</a></strong> que representa todos los objetos <strong><a href="field-object-dao.md">Field</a></strong> almacenados para el objeto especificado. Es de solo lectura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Devuelve la fecha y la hora del último cambio realizado en un objeto. <strong>Variant</strong> de sólo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></p></td>
<td><p>Establece o devuelve el número máximo de registros que se devuelven desde una consulta en un origen de datos ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-name-property-dao.md">Name</a></strong></p></td>
<td><p>Devuelve o establece el nombre del objeto especificado. <strong>String</strong> de lectura y escritura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-odbctimeout-property-dao.md">ODBCTimeout</a></strong></p></td>
<td><p>Indica el número de segundos que hay que esperar antes de que se produzca un error de tiempo de espera cuando se ejecuta <strong><a href="querydef-object-dao.md">QueryDef</a></strong> en una base de datos ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-parameters-property-dao.md">Parameters</a></strong></p></td>
<td><p>Devuelve una colección <strong><a href="parameters-collection-dao.md">Parameters</a></strong> que contiene todos los objetos <strong><a href="parameter-object-dao.md">Parameter</a></strong> del objeto <strong>QueryDef</strong> especificado. Es de solo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-prepare-property-dao.md">Preparación</a></strong></p></td>
<td><p><strong>NOTA</strong>: las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013. Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</p>
<p>Establece o devuelve un valor que indica si la consulta debería prepararse en el servidor como un procedimiento almacenado temporal con la función API de ODBC <strong>SQLPrepare</strong> Aantes de la ejecución, o bien ejecutarse con la función API de ODBC <strong>SQLExecDirect</strong> (solo en áreas de trabajo de ODBCDirect). <strong><a href="querydefstateenum-enumeration-dao.md">QueryDefStateEnum</a></strong> de lectura y escritura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado. Sólo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-recordsaffected-property-dao.md">RecordsAffected</a></strong></p></td>
<td><p>Devuelve el número de registros afectados por el último método <strong><a href="querydef-execute-method-dao.md">Execute</a></strong> invocado.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-returnsrecords-property-dao.md">ReturnsRecords</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica si una consulta de paso a través SQL a una base de datos externa devuelve registros (únicamente áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></p></td>
<td><p>Establece o devuelve la instrucción SQL que define la consulta ejecutada por un objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p><strong>NOTA</strong>: las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</p>
<p>Indica si una operación asincrónica (es decir, un método invocado con la opción <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a>) ha finalizado o no su ejecución (sólo para áreas de trabajo de ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-type-property-dao.md">Tipo</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto. Integer de solo<strong>lectura.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Devuelve un valor que indica si el usuario puede cambiar un objeto DAO. <strong>Boolean</strong> de sólo lectura.</p></td>
</tr>
</tbody>
</table>

