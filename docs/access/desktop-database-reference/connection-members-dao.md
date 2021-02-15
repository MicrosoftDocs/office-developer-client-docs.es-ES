---
title: Miembros de conexión (DAO)
TOCTitle: Connection Members
ms:assetid: 94fc60ee-b6f2-cf08-b008-ed51bf7e7f8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197681(v=office.15)
ms:contentKeyID: 48546422
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 098f44d87390351c23e61000ecbe47eae35810ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295908"
---
# <a name="connection-members-dao"></a><span data-ttu-id="06f2a-102">Miembros de conexión (DAO)</span><span class="sxs-lookup"><span data-stu-id="06f2a-102">Connection members (DAO)</span></span>

<span data-ttu-id="06f2a-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="06f2a-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="06f2a-104">[!NOTA] Las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="06f2a-104">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="06f2a-105">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="06f2a-105">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span> <span data-ttu-id="06f2a-106">Un objeto Connection representa una conexión a una base de datos ODBC (sólo áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="06f2a-106">A Connection object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>
 
## <a name="methods"></a><span data-ttu-id="06f2a-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="06f2a-107">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="06f2a-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="06f2a-108">Name</span></span></p></th>
<th><p><span data-ttu-id="06f2a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="06f2a-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06f2a-110"><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></span><span class="sxs-lookup"><span data-stu-id="06f2a-110"><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p><span data-ttu-id="06f2a-111">Cancela la ejecución de una llamada a método asincrónica que está pendiente (sólo áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="06f2a-111">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06f2a-112"><strong><a href="connection-close-method-dao.md">Close</a></strong></span><span class="sxs-lookup"><span data-stu-id="06f2a-112"><strong><a href="connection-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="06f2a-113">Cierra un objeto <strong>Connection</strong> abierto.</span><span class="sxs-lookup"><span data-stu-id="06f2a-113">Closes an open <strong>Connection</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06f2a-114"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="06f2a-114"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="06f2a-115">Crea un nuevo objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="06f2a-115">Creates a new <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06f2a-116"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span><span class="sxs-lookup"><span data-stu-id="06f2a-116"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="06f2a-117">Ejecuta una consulta de acciones o ejecuta una instrucción SQL en el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="06f2a-117">Runs an action query or executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06f2a-118"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="06f2a-118"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="06f2a-119">Crea un nuevo objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> y lo anexa a la colección <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="06f2a-119">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="06f2a-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="06f2a-120">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="06f2a-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="06f2a-121">Name</span></span></p></th>
<th><p><span data-ttu-id="06f2a-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="06f2a-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06f2a-123"><strong><a href="connection-connect-property-dao.md">Connect</a></strong></span><span class="sxs-lookup"><span data-stu-id="06f2a-123"><strong><a href="connection-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="06f2a-124">Establece o devuelve un valor que proporciona información acerca del origen de una conexión abierta.</span><span class="sxs-lookup"><span data-stu-id="06f2a-124">Sets or returns a value that provides information about the source of an open connection.</span></span> <span data-ttu-id="06f2a-125"><strong>String</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="06f2a-125">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06f2a-126"><strong><a href="connection-database-property-dao.md">Database</a></strong></span><span class="sxs-lookup"><span data-stu-id="06f2a-126"><strong><a href="connection-database-property-dao.md">Database</a></strong></span></span></p></td>
<td><p><span data-ttu-id="06f2a-127">Devuelve el objeto <strong><a href="database-object-dao.md">Database</a></strong> que corresponde a esta conexión (sólo áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="06f2a-127">Returns the <strong><a href="database-object-dao.md">Database</a></strong> object that corresponds to this connection (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06f2a-128"><strong><a href="connection-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="06f2a-128"><strong><a href="connection-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="06f2a-129">Devuelve el nombre de un objeto <strong><a href="connection-object-dao.md">Connection</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="06f2a-129">Rreturns the name of a <strong><a href="connection-object-dao.md">Connection</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06f2a-130"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span><span class="sxs-lookup"><span data-stu-id="06f2a-130"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span></span></p></td>
<td><p><span data-ttu-id="06f2a-131">Devuelve una colección <strong>QueryDefs</strong> que contiene todos los objetos <strong>QueryDef</strong> de la conexión especificada.</span><span class="sxs-lookup"><span data-stu-id="06f2a-131">Returns a <strong>QueryDefs</strong> collection that contains all of the <strong>QueryDef</strong> objects of the specified connection.</span></span> <span data-ttu-id="06f2a-132">Sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="06f2a-132">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06f2a-133"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="06f2a-133"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="06f2a-134">Establece o devuelve un valor que especifica el número de segundos que se deben esperar antes de que se produzca un error de tiempo de espera cuando se ejecuta una consulta en un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="06f2a-134">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06f2a-135"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="06f2a-135"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="06f2a-136">Devuelve el número de registros afectados por el último método <strong><a href="connection-execute-method-dao.md">Execute</a></strong> invocado.</span><span class="sxs-lookup"><span data-stu-id="06f2a-136">Returns the number of records affected by the most recently invoked <strong><a href="connection-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06f2a-137"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span><span class="sxs-lookup"><span data-stu-id="06f2a-137"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span></span></p></td>
<td><p><span data-ttu-id="06f2a-138">Devuelve una colección <strong>Recordsets</strong> que contiene todos los conjuntos de registros abiertos para la conexión especificada.</span><span class="sxs-lookup"><span data-stu-id="06f2a-138">Returns a <strong>Recordsets</strong> collection that contains all of the open recordsets in the for the specified connection.</span></span> <span data-ttu-id="06f2a-139">Es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="06f2a-139">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06f2a-140"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="06f2a-140"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p><span data-ttu-id="06f2a-141">Indica si una operación asincrónica (es decir, un método invocado con la opción <strong>dbRunAsync</strong>) ha finalizado o no su ejecución (sólo para áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="06f2a-141">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06f2a-142"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="06f2a-142"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="06f2a-143">Devuelve un valor que indica si un objeto admite transacciones.</span><span class="sxs-lookup"><span data-stu-id="06f2a-143">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="06f2a-144"><strong>Boolean</strong> de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="06f2a-144">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06f2a-145"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="06f2a-145"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="06f2a-146">Devuelve un valor que indica si el usuario puede cambiar un objeto DAO.</span><span class="sxs-lookup"><span data-stu-id="06f2a-146">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="06f2a-147"><strong>Boolean</strong> de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="06f2a-147">Read-only <strong>Boolean</strong>.Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

