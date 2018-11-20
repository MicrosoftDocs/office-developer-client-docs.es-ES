---
title: Miembros del objeto QueryDef (DAO)
TOCTitle: QueryDef Members
ms:assetid: 3f914d23-aa63-3ebd-1d86-4f53da71131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192855(v=office.15)
ms:contentKeyID: 48544403
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a6e62d302dc1164e70d83dcbb06ac56c21898b82
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026263"
---
# <a name="querydef-members-dao"></a><span data-ttu-id="1145f-102">Miembros del objeto QueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="1145f-102">QueryDef members (DAO)</span></span>


<span data-ttu-id="1145f-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1145f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1145f-104">Un objeto QueryDef es una definición de una consulta almacenada en una base de datos del motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1145f-104">A QueryDef object is a stored definition of a query in a Microsoft Access database engine database.</span></span>

## <a name="methods"></a><span data-ttu-id="1145f-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="1145f-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1145f-106">Nombre</span><span class="sxs-lookup"><span data-stu-id="1145f-106">Name</span></span></p></th>
<th><p><span data-ttu-id="1145f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1145f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1145f-108"><strong><a href="querydef-cancel-method-dao.md">Cancel</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-108"><strong><a href="querydef-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-109"><strong>Nota</strong>: las áreas de trabajo de ODBCDirect no son compatibles con Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="1145f-109"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="1145f-110">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1145f-110">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="1145f-111">Cancela la ejecución de una llamada a método asincrónica que está pendiente (sólo áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="1145f-111">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1145f-112"><strong><a href="querydef-close-method-dao.md">Cerrar</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-112"><strong><a href="querydef-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-113">Cierra un objeto <strong>QueryDef</strong> abierto.</span><span class="sxs-lookup"><span data-stu-id="1145f-113">Closes an open <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1145f-114"><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-114"><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-115">Crea un nuevo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido por el usuario (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="1145f-115">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1145f-116"><strong><a href="querydef-execute-method-dao.md">Execute</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-116"><strong><a href="querydef-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-117">Ejecuta una instrucción SQL en el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="1145f-117">Executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1145f-118"><strong><a href="querydef-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-118"><strong><a href="querydef-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-119">Crea un nuevo objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> y lo anexa a la colección <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="1145f-119">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="1145f-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1145f-120">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1145f-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="1145f-121">Name</span></span></p></th>
<th><p><span data-ttu-id="1145f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="1145f-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1145f-123"><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-123"><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-p102">Establece o devuelve el número de registros recuperados de un origen de datos ODBC que se almacenarán localmente en caché. <strong>Long</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="1145f-p102">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally. Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1145f-126"><strong><a href="querydef-connect-property-dao.md">Connect</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-126"><strong><a href="querydef-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-p103">Establece o devuelve un valor que proporciona información sobre el origen de la base de datos utilizada en una consulta de paso a través. <strong>String</strong> de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="1145f-p103">Sets or returns a value that provides information about the source of database used in a pass-through query. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1145f-129"><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-129"><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-p104">Devuelve la fecha y la hora en que se creó un objeto (únicamente áreas de trabajo de Microsoft). <strong>Variant</strong> de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="1145f-p104">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1145f-132"><strong><a href="querydef-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-132"><strong><a href="querydef-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-p105">Devuelve una colección <strong><a href="fields-collection-dao.md">Fields</a></strong> que representa todos los objetos <strong><a href="field-object-dao.md">Field</a></strong> almacenados para el objeto especificado. Es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1145f-p105">Returns a <strong><a href="fields-collection-dao.md">Fields</a></strong> collection that represents all stored <strong><a href="field-object-dao.md">Field</a></strong> objects for the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1145f-135"><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-135"><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-p106">Devuelve la fecha y la hora del último cambio efectuado en un objeto. <strong>Variant</strong> de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="1145f-p106">Returns the date and time of the most recent change made to an object. Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1145f-138"><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-138"><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-139">Establece o devuelve el número máximo de registros que se devuelven desde una consulta en un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="1145f-139">Sets or returns the maximum number of records to return from a query against an ODBC data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1145f-140"><strong><a href="querydef-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-140"><strong><a href="querydef-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-p107">Devuelve o establece el nombre del objeto especificado. <strong>String</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="1145f-p107">Returns or sets the name of the specified object. Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1145f-143"><strong><a href="querydef-odbctimeout-property-dao.md">ODBCTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-143"><strong><a href="querydef-odbctimeout-property-dao.md">ODBCTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-144">Indica el número de segundos que hay que esperar antes de que se produzca un error de tiempo de espera cuando se ejecuta <strong><a href="querydef-object-dao.md">QueryDef</a></strong> en una base de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="1145f-144">Indicates the number of seconds to wait before a timeout error occurs when a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> is executed on an ODBC database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1145f-145"><strong><a href="querydef-parameters-property-dao.md">Parámetros</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-145"><strong><a href="querydef-parameters-property-dao.md">Parameters</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-p108">Devuelve una colección <strong><a href="parameters-collection-dao.md">Parameters</a></strong> que contiene todos los objetos <strong><a href="parameter-object-dao.md">Parameter</a></strong> del objeto <strong>QueryDef</strong> especificado. Es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1145f-p108">Returns a <strong><a href="parameters-collection-dao.md">Parameters</a></strong> collection that contains all of the <strong><a href="parameter-object-dao.md">Parameter</a></strong> objects of the specified <strong>QueryDef</strong>. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1145f-148"><strong><a href="querydef-prepare-property-dao.md">Prepare</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-148"><strong><a href="querydef-prepare-property-dao.md">Prepare</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-149"><strong>Nota</strong>: las áreas de trabajo de ODBCDirect no son compatibles con Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="1145f-149"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="1145f-150">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1145f-150">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="1145f-p110">Establece o devuelve un valor que indica si la consulta debería prepararse en el servidor como un procedimiento almacenado temporal con la función API de ODBC <strong>SQLPrepare</strong> Aantes de la ejecución, o bien ejecutarse con la función API de ODBC <strong>SQLExecDirect</strong> (solo en áreas de trabajo de ODBCDirect). <strong><a href="querydefstateenum-enumeration-dao.md">QueryDefStateEnum</a></strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="1145f-p110">Sets or returns a value that indicates whether the query should be prepared on the server as a temporary stored procedure, using the ODBC <strong>SQLPrepare</strong> API function, prior to execution, or just executed using the ODBC <strong>SQLExecDirect</strong> API function (ODBCDirect workspaces only). Read/Write <strong><a href="querydefstateenum-enumeration-dao.md">QueryDefStateEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1145f-153"><strong><a href="querydef-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-153"><strong><a href="querydef-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-p111">Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado. solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1145f-p111">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1145f-156"><strong><a href="querydef-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-156"><strong><a href="querydef-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-157">Devuelve el número de registros afectados por el último método <strong><a href="querydef-execute-method-dao.md">Execute</a></strong> invocado.</span><span class="sxs-lookup"><span data-stu-id="1145f-157">Returns the number of records affected by the most recently invoked <strong><a href="querydef-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1145f-158"><strong><a href="querydef-returnsrecords-property-dao.md">ReturnsRecords</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-158"><strong><a href="querydef-returnsrecords-property-dao.md">ReturnsRecords</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-159">Establece o devuelve un valor que indica si una consulta de paso a través SQL a una base de datos externa devuelve registros (únicamente áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="1145f-159">Sets or returns a value that indicates whether an SQL pass-through query to an external database returns records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1145f-160"><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-160"><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-161">Establece o devuelve la instrucción SQL que define la consulta ejecutada por un objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="1145f-161">Sets or returns the SQL statement that defines the query executed by a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1145f-162"><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-162"><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-163"><strong>Nota</strong>: las áreas de trabajo de ODBCDirect no son compatibles con Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="1145f-163"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="1145f-164">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1145f-164">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="1145f-165">Indica si una operación asincrónica (es decir, un método invocado con la opción <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a>) ha finalizado o no su ejecución (sólo para áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="1145f-165">Indicates whether or not an asynchronous operation (that is, a method called with the <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1145f-166"><strong><a href="querydef-type-property-dao.md">Type</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-166"><strong><a href="querydef-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-167">Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto.</span><span class="sxs-lookup"><span data-stu-id="1145f-167">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="1145f-168">Read-only<strong>entero</strong>.</span><span class="sxs-lookup"><span data-stu-id="1145f-168">Read-only<strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1145f-169"><strong><a href="querydef-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="1145f-169"><strong><a href="querydef-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1145f-p114">Devuelve un valor que indica si el usuario puede cambiar un objeto DAO. <strong>Boolean</strong> de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="1145f-p114">Returns a value that indicates whether you can change a DAO object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

