---
title: Miembros Recordset (DAO)
TOCTitle: Recordset Members
ms:assetid: cfaae9ec-1b88-4285-1ebe-637564e99dc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834683(v=office.15)
ms:contentKeyID: 48547815
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2989159683b668c798181c2e99d58fade8fba467
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485764"
---
# <a name="recordset-members-dao"></a>Miembros Recordset (DAO)


**Se aplica a**: Access 2013 | Office 2013

Un objeto Recordset representa los registros de una tabla base o los registros que son el resultado de ejecutar una consulta.

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
<td><p><strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong></p></td>
<td><p>Crea un nuevo registro de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> actualizable.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-cancel-method-dao.md">Cancel</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</P>


<p>Cancela la ejecución de una llamada a método asincrónica que está pendiente (sólo áreas de trabajo de ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></p></td>
<td><p>Cancela todas las actualizaciones pendientes para un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></p></td>
<td><p>Crea un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> duplicado que hace referencia al objeto <strong>Recordset</strong> original.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-close-method-dao.md">Cerrar</a></strong></p></td>
<td><p>Cierra un objeto <strong>Recordset</strong> abierto.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-copyquerydef-method-dao.md">CopyQueryDef</a></strong></p></td>
<td><p>Devuelve un objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong> que es una copia del <strong>objeto QueryDef</strong> utilizado para crear el objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> representado por el marcador de posición de recordset (sólo áreas de trabajo de Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-delete-method-dao.md">Eliminar</a></strong></p></td>
<td><p>No está admitido para este objeto.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></p></td>
<td><p>Copia el registro actual de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> actualizable en el búfer de copias para su posterior modificación.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></p></td>
<td><p>Rellena parcial o totalmente una memoria caché local de un objeto <strong>Recordset</strong> que contiene datos de un origen de datos ODBC conectado al motor de base de datos de Microsoft Access (solo bases de datos ODBC conectadas al motor de base de datos de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></p></td>
<td><p>Busca el primer registro de un objeto <strong>Recordset</strong> de tipo Dynaset o instantánea que satisfaga los criterios especificados y convierte el registro en el registro actual (solo en áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></p></td>
<td><p>Busca el último registro de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> de tipo Dynaset o de instantánea que satisfaga los criterios especificados y hace que el registro sea el registro activo (solo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></p></td>
<td><p>Localiza el registro siguiente de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> de tipo dynaset o de tipo snapshot que satisface los criterios especificados y hace que el registro sea el registro activo (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></p></td>
<td><p>Busca el registro anterior de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> de tipo Dynaset o de instantánea que satisfaga los criterios especificados y hace que el registro sea el registro activo (solo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></p></td>
<td><p>Recupera varias filas de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-move-method-dao.md">Move</a></strong></p></td>
<td><p>Mueve la posición del registro activo de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-movefirst-method-dao.md">Métodos MoveFirst</a></strong></p></td>
<td><p>Se desplaza al primer registro de un objeto <strong>Recordset</strong> especificado y convierte ese registro en el registro activo.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></p></td>
<td><p>Se desplaza al último registro de un objeto <strong>Recordset</strong> especificado y convierte ese registro en el registro activo.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-movenext-method-dao.md">MoveNext</a></strong></p></td>
<td><p>Se desplaza al siguiente registro de un objeto <strong>Recordset</strong> especificado y convierte ese registro en el registro activo.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-moveprevious-method-dao.md">MovePrevious</a></strong></p></td>
<td><p>Se desplaza al registro anterior de un objeto <strong>Recordset</strong> especificado y convierte ese registro en el registro activo.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-nextrecordset-method-dao.md">NextRecordset</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</P>


<p>Obtiene el siguiente conjunto de registros, si existe, devuelto por una consulta de selección de varias partes en una llamada <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> y devuelve un valor <strong>Boolean</strong> que indica si hay uno o más registros adicionales pendientes (solo áreas de trabajo de ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Crea un nuevo objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> y lo anexa a la colección <strong>Recordsets</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-requery-method-dao.md">Requery</a></strong></p></td>
<td><p>Actualiza los datos de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> volviendo a ejecutar la consulta en la que se basa el objeto.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-seek-method-dao.md">Seek</a></strong></p></td>
<td><p>Busca el registro en un objeto <strong>Recordset</strong> de tipo tabla indizada que satisface los criterios especificados para el índice activo y hace de este registro el registro activo (solo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-update-method-dao.md">Update</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</P>


<p>Guarda el contenido del búfer de copia en un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> actualizable.</p></td>
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
<td><p><strong><a href="recordset-absoluteposition-property-dao.md">AbsolutePosition</a></strong></p></td>
<td><p>Configura o devuelve el número de registros con respecto al registro actual de un objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</P>


<p>Devuelve el número de registros que no finalizaron la última actualización del lote (sólo áreas de trabajo de ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</P>


<p>Devuelve una matriz de marcadores que indican las filas que generaron conflictos en la última operación de actualización del lote (sólo áreas de trabajo de ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-batchsize-property-dao.md">BatchSize</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</P>


<p>Establece o devuelve el número de instrucciones devueltas al servidor en cada lote (sólo áreas de trabajo de ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></p></td>
<td><p>Devuelve un valor que indica si la posición del registro actual está delante del primer registro en un objeto <strong>Recordset</strong>. <strong>Boolean</strong> de solo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-bookmark-property-dao.md">Marcador</a></strong></p></td>
<td><p>Establece o devuelve un marcador que identifica de forma exclusiva el registro actual de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></p></td>
<td><p>Devuelve un valor que indica si un objeto <strong>Recordset</strong> admite marcadores, que se pueden establecer mediante la propiedad <strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong></p></td>
<td><p>Establece o devuelve el número de registros recuperados de un origen de datos ODBC que se almacenarán localmente en caché. <strong>Long</strong> de lectura y escritura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong></p></td>
<td><p>Establece o devuelve un valor que especifica el marcador del primer registro de un objeto Recordset de tipo Dynaset que contiene datos que se almacenarán en caché localmente de un origen de datos ODBC (solo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-connection-property-dao.md">Connection</a></strong></p></td>
<td><p>Devuelve el objeto <strong><a href="connection-object-dao.md">Connection</a></strong> que corresponde a la base de datos.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Devuelve la fecha y la hora en la que se creó una tabla base (sólo para áreas de trabajo de Microsoft Access). <strong>Variant</strong> de solo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-editmode-property-dao.md">EditMode</a></strong></p></td>
<td><p>Devuelve un valor que indica el estado de edición del registro actual.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></p></td>
<td><p>Devuelve un valor que indica si la posición actual del registro se encuentra después del último registro en un objeto <strong>Recordset</strong>. <strong>Boolean</strong> de solo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>Devuelve una colección <strong>Fields</strong> que representa todos los objetos <strong>Field</strong> almacenados para el objeto especificado. Sólo lectura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-filter-property-dao.md">Filtro</a></strong></p></td>
<td><p>Establece o devuelve un valor que determina los registros incluidos en un objeto <strong>Recordset</strong> abierto posteriormente (solo en áreas de trabajo de Microsoft Access). <strong>String</strong> de lectura y escritura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-index-property-dao.md">Índice</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica el nombre del objeto actual <strong><a href="index-object-dao.md">Index</a></strong> en un objeto de tipo de tabla <strong><a href="recordset-object-dao.md">Recordset</a></strong> (solo en áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-lastmodified-property-dao.md">LastModified</a></strong></p></td>
<td><p>Devuelve Bookmark que indica el último registro agregado o modificado.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Devuelve la fecha y la hora del último cambio realizado en una tabla base. <strong>Variant</strong> de sólo lectura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-lockedits-property-dao.md">LockEdits</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica el tipo de bloqueo que está activo mientras se modifica.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-name-property-dao.md">Name</a></strong></p></td>
<td><p>Devuelve el nombre del objeto especificado. <strong>String</strong> de sólo lectura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-nomatch-property-dao.md">NoMatch</a></strong></p></td>
<td><p>Indica si se encontró un registro concreto al utilizar el método <strong><a href="recordset-seek-method-dao.md">Seek</a></strong> o uno de los métodos <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong> (sólo para áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-percentposition-property-dao.md">PercentPosition</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica la ubicación aproximada del registro actual en el objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> a partir de un porcentaje de los registros en <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-properties-property-dao.md">Propiedades</a></strong></p></td>
<td><p>Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado. solo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></p></td>
<td><p>Devuelve el número de registros a los que se tuvo acceso en un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>, o el número total de registros en un objeto <strong>Recordset</strong> u objeto <strong><a href="tabledef-object-dao.md">TableDef</a></strong> tipo tabla. <strong>Long</strong> de solo lectura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-recordstatus-property-dao.md">RecordStatus</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</P>


<p>Devuelve un valor que indica el estado de actualización del registro actual si es parte de una actualización por lotes (sólo para áreas de trabajo de ODBCDirect). <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong> de solo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></p></td>
<td><p>Devuelve un valor que indica si un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> admite el método <strong><a href="recordset-requery-method-dao.md">Requery</a></strong>, método que vuelve a ejecutar la consulta en la que se basa el objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></p></td>
<td><p>Establece o devuelve el criterio de ordenación para los registros de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> (solo en áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</P>


<p>Indica si una operación asincrónica (es decir, un método invocado con la opción <strong>dbRunAsync</strong>) ha finalizado o no su ejecución (sólo para áreas de trabajo de ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-transactions-property-dao.md">Transacciones</a></strong></p></td>
<td><p>Devuelve un valor que indica si un objeto admite transacciones. <strong>Boolean</strong> de solo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tipo</strong></p></td>
<td><p>La descripción de este miembro aparecerá en la versión final de Office 14.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Devuelve un valor que indica si el usuario puede cambiar un objeto DAO. <strong>Boolean</strong> de sólo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</P>


<p>Establece o devuelve un valor que indica cómo se construye la cláusula WHERE para cada registro durante una actualización por lotes, y si la actualización por lotes debería utilizar una instrucción UPDATE o DELETE seguida de INSERT (sólo para áreas de trabajo de ODBCDirect). <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong> de lectura y escritura</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Establece o devuelve un valor que valida los datos en un campo mientras se modifica o se agrega a una tabla (sólo para áreas de trabajo de Microsoft Access). <strong>String</strong> de lectura y escritura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Establece o devuelve un valor que especifica el texto del mensaje que su aplicación muestra si el valor de un objeto <strong>Field</strong> no satisface la regla de validación especificada por el valor de la propiedad <strong>ValidationRule</strong> (sólo para áreas de trabajo de Microsoft Access). <strong>String</strong> de solo lectura.</p></td>
</tr>
</tbody>
</table>

