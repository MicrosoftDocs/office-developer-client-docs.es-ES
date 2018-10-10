---
title: Connection Members (DAO)
TOCTitle: Connection Members
ms:assetid: 94fc60ee-b6f2-cf08-b008-ed51bf7e7f8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197681(v=office.15)
ms:contentKeyID: 48546422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 001cb1372acf4a4a55b3841a3f4ca8d6598f55e8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484107"
---
# <a name="connection-members-dao"></a><span data-ttu-id="b048a-102">Connection Members (DAO)</span><span class="sxs-lookup"><span data-stu-id="b048a-102">Connection Members (DAO)</span></span>


<span data-ttu-id="b048a-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b048a-103">**Applies to**: Access 2013 | Office 2013</span></span>


> [!NOTE]
> <P><span data-ttu-id="b048a-104">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="b048a-104">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="b048a-105">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.Un objeto Connection representa una conexión a una base de datos ODBC (solo áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="b048a-105">Use ADO if you want to access external data sources without using the Microsoft Access database engine.A Connection object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span></P>



## <a name="methods"></a><span data-ttu-id="b048a-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="b048a-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b048a-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="b048a-107">Name</span></span></p></th>
<th><p><span data-ttu-id="b048a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b048a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b048a-109"><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></span><span class="sxs-lookup"><span data-stu-id="b048a-109"><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="b048a-p102">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b048a-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="b048a-112">Cancela la ejecución de una llamada a método asincrónica que está pendiente (sólo áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="b048a-112">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b048a-113"><strong><a href="connection-close-method-dao.md">Cerrar</a></strong></span><span class="sxs-lookup"><span data-stu-id="b048a-113"><strong><a href="connection-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b048a-114">Cierra un objeto <strong>Connection</strong> abierto.</span><span class="sxs-lookup"><span data-stu-id="b048a-114">Closes an open <strong>Connection</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b048a-115"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="b048a-115"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b048a-116">Crea un nuevo objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="b048a-116">Creates a new <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b048a-117"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span><span class="sxs-lookup"><span data-stu-id="b048a-117"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b048a-118">Ejecuta una consulta de acción o una instrucción SQL en el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="b048a-118">Runs an action query or executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b048a-119"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="b048a-119"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b048a-120">Crea un nuevo objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> y lo anexa a la colección <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="b048a-120">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="b048a-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b048a-121">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b048a-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="b048a-122">Name</span></span></p></th>
<th><p><span data-ttu-id="b048a-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="b048a-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b048a-124"><strong><a href="connection-connect-property-dao.md">Conectar</a></strong></span><span class="sxs-lookup"><span data-stu-id="b048a-124"><strong><a href="connection-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b048a-p103">Establece o devuelve un valor que proporciona información acerca del origen de una conexión abierta. <strong>String</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b048a-p103">Sets or returns a value that provides information about the source of an open connection. Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b048a-127"><strong><a href="connection-database-property-dao.md">Base de datos</a></strong></span><span class="sxs-lookup"><span data-stu-id="b048a-127"><strong><a href="connection-database-property-dao.md">Database</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="b048a-p104">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b048a-p104">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="b048a-130">Devuelve el objeto <strong><a href="database-object-dao.md">Database</a></strong> que corresponde a esta conexión (sólo áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="b048a-130">Returns the <strong><a href="database-object-dao.md">Database</a></strong> object that corresponds to this connection (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b048a-131"><strong><a href="connection-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="b048a-131"><strong><a href="connection-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b048a-132">Devuelve el nombre de un objeto <strong><a href="connection-object-dao.md">Connection</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="b048a-132">Rreturns the name of a <strong><a href="connection-object-dao.md">Connection</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b048a-133"><strong><a href="connection-querydefs-property-dao.md">Definiciones de consulta</a></strong></span><span class="sxs-lookup"><span data-stu-id="b048a-133"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b048a-p105">Devuelve una colección <strong>QueryDefs</strong> que contiene todos los objetos <strong>QueryDef</strong> de la conexión especificada. Sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="b048a-p105">Returns a <strong>QueryDefs</strong> collection that contains all of the <strong>QueryDef</strong> objects of the specified connection. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b048a-136"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="b048a-136"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b048a-137">Establece o devuelve un valor que especifica el número de segundos que hay que esperar antes de que se produzca un error en tiempo de tiempo de espera cuando se ejecuta una consulta en un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="b048a-137">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b048a-138"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="b048a-138"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b048a-139">Devuelve el número de registros afectados por el último método <strong><a href="connection-execute-method-dao.md">Execute</a></strong> invocado.</span><span class="sxs-lookup"><span data-stu-id="b048a-139">Returns the number of records affected by the most recently invoked <strong><a href="connection-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b048a-140"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span><span class="sxs-lookup"><span data-stu-id="b048a-140"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b048a-p106">Devuelve una colección <strong>Recordsets</strong> que contiene todos los conjuntos de registros abiertos para la conexión especificada. Es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b048a-p106">Returns a <strong>Recordsets</strong> collection that contains all of the open recordsets in the for the specified connection. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b048a-143"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="b048a-143"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="b048a-p107">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b048a-p107">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="b048a-146">Indica si una operación asincrónica (es decir, un método invocado con la opción <strong>dbRunAsync</strong>) ha finalizado o no su ejecución (sólo para áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="b048a-146">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b048a-147"><strong><a href="connection-transactions-property-dao.md">Transacciones</a></strong></span><span class="sxs-lookup"><span data-stu-id="b048a-147"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b048a-p108">Devuelve un valor que indica si un objeto admite transacciones. <strong>Boolean</strong> de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b048a-p108">Returns a value that indicates whether an object supports transactions. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b048a-150"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="b048a-150"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b048a-p109">Devuelve un valor que indica si puede cambiar un objeto DAO. <strong>Boolean</strong> de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b048a-p109">Returns a value that indicates whether you can change a DAO object. Read-only <strong>Boolean</strong>.Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

