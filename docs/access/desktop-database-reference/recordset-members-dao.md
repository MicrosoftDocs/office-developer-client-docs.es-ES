---
title: Miembros Recordset (DAO)
TOCTitle: Recordset Members
ms:assetid: cfaae9ec-1b88-4285-1ebe-637564e99dc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834683(v=office.15)
ms:contentKeyID: 48547815
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c36187eef0b55681b2ba426d979f42ee8a6efea8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284809"
---
# <a name="recordset-members-dao"></a><span data-ttu-id="dd778-102">Miembros Recordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="dd778-102">Recordset Members (DAO)</span></span>


<span data-ttu-id="dd778-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd778-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dd778-104">Un objeto Recordset representa los registros de una tabla base o los registros que son el resultado de ejecutar una consulta.</span><span class="sxs-lookup"><span data-stu-id="dd778-104">A Recordset object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="methods"></a><span data-ttu-id="dd778-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="dd778-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dd778-106">Nombre</span><span class="sxs-lookup"><span data-stu-id="dd778-106">Name</span></span></p></th>
<th><p><span data-ttu-id="dd778-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd778-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd778-108"><strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-108"><a href="recordset-addnew-method-dao.md">expression</a>  . <strong>AddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-109">Crea un nuevo registro de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> actualizable.</span><span class="sxs-lookup"><span data-stu-id="dd778-109">Creates a new record for an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-110"><strong><a href="recordset-cancel-method-dao.md">Cancel</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-110"><strong><a href="recordset-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-111"><strong>NOTA</strong>: las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="dd778-111">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="dd778-112">Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dd778-112">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="dd778-113">Cancela la ejecución de una llamada a método asincrónica que está pendiente (sólo áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="dd778-113">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-114"><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-114"><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-115">Cancela todas las actualizaciones pendientes para un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="dd778-115">Cancels any pending updates for a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-116"><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-116"><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-117">Crea un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> duplicado que hace referencia al objeto <strong>Recordset</strong> original.</span><span class="sxs-lookup"><span data-stu-id="dd778-117">Creates a duplicate <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that refers to the original <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-118"><strong><a href="recordset-close-method-dao.md">Close</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-118"><strong><a href="recordset-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-119">Cierra un <strong>Recordset</strong> abierto.</span><span class="sxs-lookup"><span data-stu-id="dd778-119">Closes an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-120"><strong><a href="recordset-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-120"><a href="recordset-copyquerydef-method-dao.md">expression</a>  . <strong>CopyQueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-121">Devuelve un objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong> que es una copia del objeto <strong>QueryDef</strong> usado para crear el objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> representado por el marcador de posición recordset (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="dd778-121">Returns a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object that is a copy of the <strong>QueryDef</strong> used to create the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object represented by the  recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="dd778-122">.</span><span class="sxs-lookup"><span data-stu-id="dd778-122"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-123"><strong><a href="recordset-delete-method-dao.md">Delete</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-123"><strong><a href="recordset-delete-method-dao.md">Delete</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-124">No compatible con este objeto.</span><span class="sxs-lookup"><span data-stu-id="dd778-124">Not supported for this object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-125"><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-125"><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-126">Copia el registro actual de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> actualizable al búfer de copia para su posterior edición.</span><span class="sxs-lookup"><span data-stu-id="dd778-126">Copies the current record from an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object to the copy buffer for subsequent editing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-127"><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-127"><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-128">Rellena parcial o totalmente una memoria caché local de un objeto <strong>Recordset</strong> que contiene datos de un origen de datos ODBC conectado al motor de base de datos de Microsoft Access (solo bases de datos ODBC conectadas al motor de base de datos de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="dd778-128">Fills all or a part of a local cache for a <strong>Recordset</strong> object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-129"><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-129"><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-130">Busca el primer registro de un objeto <strong>Recordset</strong> de tipo conjunto de registros dinámicos o de tipo instantánea que cumpla los criterios especificados, y convierte ese registro en el registro actual (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="dd778-130">Locates the first record in a dynaset- or snapshot-type <strong>Recordset</strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-131"><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-131"><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-132">Busca el último registro de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> de tipo Dynaset o de instantánea que satisfaga los criterios especificados y hace que el registro sea el registro activo (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="dd778-132">Locates the last record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-133"><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-133"><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-p103">Localiza el registro siguiente de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> de tipo dynaset o de tipo snapshot que satisface los criterios especificados y hace que el registro sea el registro activo (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="dd778-p103">Locates the next record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-136"><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-136"><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-p104">Busca el registro anterior de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> de tipo Dynaset o de instantánea que satisfaga los criterios especificados y hace que el registro sea el registro activo (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="dd778-p104">Locates the previous record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-139"><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-139"><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-140">Recupera varias filas de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="dd778-140">Retrieves multiple rows from a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-141"><strong><a href="recordset-move-method-dao.md">Move</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-141"><strong><a href="recordset-move-method-dao.md">Move</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-142">Mueve la posición del registro actual de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="dd778-142">Moves the position of the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-143"><strong><a href="recordset-movefirst-method-dao.md">MoveFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-143"><a href="recordset-movefirst-method-dao.md">expression</a>  . <strong>MoveFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-144">Se desplaza al primer registro de un objeto <strong>Recordset</strong> especificado y convierte ese registro en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="dd778-144">Moves to the first record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-145"><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-145"><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-146">Se desplaza al último registro de un objeto <strong>Recordset</strong> especificado y convierte ese registro en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="dd778-146">Moves to the last record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-147"><strong><a href="recordset-movenext-method-dao.md">MoveNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-147"><a href="recordset-movenext-method-dao.md">expression</a>  . <strong>MoveNext</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-148">Se desplaza al siguiente registro de un objeto <strong>Recordset</strong> especificado y convierte ese registro en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="dd778-148">Moves to the next record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-149"><strong><a href="recordset-moveprevious-method-dao.md">MovePrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-149"><a href="recordset-moveprevious-method-dao.md">expression</a>  . <strong>MovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-150">Se desplaza al registro anterior de un objeto <strong>Recordset</strong> especificado y convierte ese registro en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="dd778-150">Moves to the previous record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-151"><strong><a href="recordset-nextrecordset-method-dao.md">NextRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-151"><a href="recordset-nextrecordset-method-dao.md">expression</a>  . <strong>NextRecordset</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-152"><strong>NOTA</strong>: las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="dd778-152">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="dd778-153">Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dd778-153">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="dd778-154">Obtiene el siguiente conjunto de registros, si existe, devuelto por una consulta de selección de varias partes en una llamada <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> y devuelve un valor <strong>Boolean</strong> que indica si hay uno o más registros adicionales pendientes (sólo áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="dd778-154">Gets the next set of records, if any, returned by a multi-part select query in an <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> call, and returns a <strong>Boolean</strong> value indicating whether one or more additional records are pending (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-155"><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-155"><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-156">Crea un nuevo objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> y lo anexa a la colección <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="dd778-156">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-157"><strong><a href="recordset-requery-method-dao.md">Requery</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-157"><strong><a href="recordset-requery-method-dao.md">Requery</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-158">Actualiza los datos en un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> al volver a ejecutar la consulta en la que se basa el objeto.</span><span class="sxs-lookup"><span data-stu-id="dd778-158">Updates the data in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-159"><strong><a href="recordset-seek-method-dao.md">Seek</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-159"><strong><a href="recordset-seek-method-dao.md">Seek</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-160">Busca el registro en un objeto <strong>Recordset</strong> indexado de tipo tabla que satisface los criterios especificados para el índice actual y convierte a ese registro en el registro actual (espacios de trabajo de Microsoft Access solamente).</span><span class="sxs-lookup"><span data-stu-id="dd778-160">Locates the record in an indexed table-type <strong>Recordset</strong> object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-161"><strong><a href="recordset-update-method-dao.md">Update</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-161"><strong><a href="recordset-update-method-dao.md">Update</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-162"><strong>NOTA</strong>: las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="dd778-162">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="dd778-163">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dd778-163">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="dd778-164">Guarda el contenido del búfer de copia en un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> actualizable.</span><span class="sxs-lookup"><span data-stu-id="dd778-164">Saves the contents of the copy buffer to an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="dd778-165">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd778-165">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dd778-166">Nombre</span><span class="sxs-lookup"><span data-stu-id="dd778-166">Name</span></span></p></th>
<th><p><span data-ttu-id="dd778-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd778-167">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd778-168"><strong><a href="recordset-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-168"><a href="recordset-absoluteposition-property-dao.md">expression</a>  . <strong>AbsolutePosition</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-169">Configura o devuelve el número de registros con respecto al registro actual de un objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="dd778-169">Sets or returns the relative record number of a <strong>Recordset</strong> object's current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-170"><strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-170"><a href="recordset-batchcollisioncount-property-dao.md">expression</a>  . <strong>BatchCollisionCount</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-171"><strong>NOTA</strong>: las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="dd778-171">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="dd778-172">Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dd778-172">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="dd778-173">Devuelve el número de registros que no completaron la última actualización por lotes (sólo para áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="dd778-173">Returns the number of records that did not complete the last batch update (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-174"><strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-174"><a href="recordset-batchcollisions-property-dao.md">expression</a>  . <strong>BatchCollisions</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-175"><strong>NOTA</strong>: las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="dd778-175">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="dd778-176">Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dd778-176">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="dd778-177">Devuelve una matriz de marcadores que indica las filas que generaron conflictos en la última operación de actualización por lotes (sólo para áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="dd778-177">Returns an array of bookmarks indicating the rows that generated collisions in the last batch update operation (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-178"><strong><a href="recordset-batchsize-property-dao.md">BatchSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-178"><a href="recordset-batchsize-property-dao.md">expression</a>  . <strong>BatchSize</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-179"><strong>NOTA</strong>: las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="dd778-179">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="dd778-180">Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dd778-180">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="dd778-181">Establece o devuelve el número instrucciones enviadas otra vez al servidor en cada lote (sólo para áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="dd778-181">Sets or returns the number of statements sent back to the server in each batch (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-182"><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-182"><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-183">Devuelve un valor que indica si la posición del registro actual está delante del primer registro en un objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="dd778-183">Returns a value that indicates whether the current record position is before the first record in a <strong>Recordset</strong> object.</span></span> <span data-ttu-id="dd778-184"><strong>Booleano</strong> de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd778-184">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-185"><strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-185"><strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-186">Establece o devuelve un marcador que identifica de forma única el registro actual en un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="dd778-186">Sets or returns a bookmark that uniquely identifies the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-187"><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-187"><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-188">Devuelve un valor que indica si un objeto <strong>Recordset</strong> admite marcadores, que puede configurar utilizando la propiedad <strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="dd778-188">Returns a value that indicates whether a <strong>Recordset</strong> object supports bookmarks, which you can set by using the <strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-189"><strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-189"><a href="recordset-cachesize-property-dao.md">expression</a>  . <strong>CacheSize</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-190">Establece o devuelve el número de registros recuperados de un origen de datos ODBC que se almacenarán localmente en caché.</span><span class="sxs-lookup"><span data-stu-id="dd778-190">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="dd778-191"><strong>Long</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="dd778-191">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-192"><strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-192">CacheStart Property</span></span></p></td>
<td><p><span data-ttu-id="dd778-193">Establece o devuelve un valor que especifica el marcador del primer registro en un objeto Recordset de tipo Dynaset que contiene datos para almacenar en la memoria caché localmente desde un origen de datos ODBC (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="dd778-193">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-194"><strong><a href="recordset-connection-property-dao.md">Connection</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-194"><strong><a href="recordset-connection-property-dao.md">Connection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-195">Devuelve el objeto <strong><a href="connection-object-dao.md">Connection</a></strong> que corresponde a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="dd778-195">Returns the <strong><a href="connection-object-dao.md">Connection</a></strong> object that corresponds to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-196"><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-196"><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-197">Devuelve la fecha y la hora en la que se creó una tabla base (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="dd778-197">Returns the date and time a base table was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="dd778-198"><strong>Variant</strong> de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd778-198">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-199"><strong><a href="recordset-editmode-property-dao.md">EditMode</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-199"><a href="recordset-editmode-property-dao.md">expression</a>  . <strong>EditMode</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-200">Devuelve un valor que indica el estado de edición del registro actual.</span><span class="sxs-lookup"><span data-stu-id="dd778-200">Returns a value that indicates the state of editing for the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-201"><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-201"><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-202">Devuelve un valor que indica si la posición actual del registro se encuentra después del último registro en un objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="dd778-202">Returns a value that indicates whether the current record position is after the last record in a <strong>Recordset</strong> object.</span></span> <span data-ttu-id="dd778-203"><strong>Boolean</strong> de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd778-203">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-204"><strong><a href="recordset-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-204"><strong><a href="recordset-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-205">Devuelve una colección <strong>Fields</strong> que representa todos los objetos <strong>Field</strong> almacenados para el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="dd778-205">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="dd778-206">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd778-206">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-207"><strong><a href="recordset-filter-property-dao.md">Filter</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-207"><strong><a href="recordset-filter-property-dao.md">Filter</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-208">Establece o devuelve un valor que determina los registros incluidos en un objeto <strong>Recordset</strong> abierto posteriormente (solo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="dd778-208">Sets or returns a value that determines the records included in a subsequently opened <strong>Recordset</strong> object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="dd778-209"><strong>String</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="dd778-209">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-210"><strong><a href="recordset-index-property-dao.md">Index</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-210"><strong><a href="recordset-index-property-dao.md">Index</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-211">Establece o devuelve un valor que indica el nombre del objeto actual <strong><a href="index-object-dao.md">Index</a></strong> en un objeto de tipo de tabla <strong><a href="recordset-object-dao.md">Recordset</a></strong> (solo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="dd778-211">Sets or returns a value that indicates the name of the current <strong><a href="index-object-dao.md">Index</a></strong> object in a table-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-212"><strong><a href="recordset-lastmodified-property-dao.md">LastModified</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-212"><a href="recordset-lastmodified-property-dao.md">expression</a>  . <strong>LastModified</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-213">Devuelve un marcador que indica el último registro agregado o cambiado.</span><span class="sxs-lookup"><span data-stu-id="dd778-213">Returns a ookmark indicating the most recently added or changed record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-214"><strong><a href="recordset-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-214">LastUpdated Property</span></span></p></td>
<td><p><span data-ttu-id="dd778-215">Devuelve la fecha y la hora del último cambio realizado en una tabla base.</span><span class="sxs-lookup"><span data-stu-id="dd778-215">Returns the date and time of the most recent change made to a base table.</span></span> <span data-ttu-id="dd778-216"><strong>Variant</strong> de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd778-216">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-217"><strong><a href="recordset-lockedits-property-dao.md">LockEdits</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-217"><a href="recordset-lockedits-property-dao.md">expression</a>  . <strong>LockEdits</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-218">Establece o devuelve un valor que indica el tipo de bloqueo que está en vigor mientras edita.</span><span class="sxs-lookup"><span data-stu-id="dd778-218">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-219"><strong><a href="recordset-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-219"><strong><a href="recordset-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-220">Devuelve el nombre del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="dd778-220">Returns the name of the specified object.</span></span> <span data-ttu-id="dd778-221"><strong>String</strong> de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd778-221">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-222"><strong><a href="recordset-nomatch-property-dao.md">NoMatch</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-222"><a href="recordset-nomatch-property-dao.md">expression</a>  . <strong>NoMatch</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-223">Indica si se ha encontrado un registro determinado utilizando el método <strong><a href="recordset-seek-method-dao.md">Seek</a></strong> o uno de los métodos <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong> (solo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="dd778-223">Indicates whether a particular record was found by using the <strong><a href="recordset-seek-method-dao.md">Seek</a></strong> method or one of the <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong> methods (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-224"><strong><a href="recordset-percentposition-property-dao.md">PercentPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-224"><a href="recordset-percentposition-property-dao.md">expression</a>  . <strong>PercentPosition</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-225">Establece o devuelve un valor que indica la ubicación aproximada del registro actual en el objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> a partir de un porcentaje de los registros en <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="dd778-225">Sets or returns a value indicating the approximate location of the current record in the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object based on a percentage of the records in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-226"><strong><a href="recordset-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-226"><strong><a href="recordset-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-227">Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="dd778-227">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="dd778-228">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd778-228">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-229"><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-229"><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-p119">Devuelve el número de registros a los que se tuvo acceso en un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>, o el número total de registros en un objeto <strong>Recordset</strong> u objeto <strong><a href="tabledef-object-dao.md">TableDef</a></strong> tipo tabla. <strong>Long</strong> de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd778-p119">Returns the number of records accessed in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object, or the total number of records in a table-type <strong>Recordset</strong> object. or <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object. Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-233"><strong><a href="recordset-recordstatus-property-dao.md">RecordStatus</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-233"><a href="recordset-recordstatus-property-dao.md">expression</a>  . <strong>RecordStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-234"><strong>NOTA</strong>: las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="dd778-234">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="dd778-235">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dd778-235">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="dd778-p121">Devuelve un valor que indica el estado de actualización del registro actual si es parte de una actualización por lotes (sólo para áreas de trabajo de ODBCDirect). <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong> de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd778-p121">Returns a value indicating the update status of the current record if it is part of a batch update (ODBCDirect workspaces only). Read-only <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-238"><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-238"><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-239">Devuelve un valor que indica si un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> admite el método <strong><a href="recordset-requery-method-dao.md">Requery</a></strong>, método que vuelve a ejecutar la consulta en la que se basa el objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="dd778-239">Returns a value that indicates whether a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object supports the <strong><a href="recordset-requery-method-dao.md">Requery</a></strong> method, which re-executes the query on which the <strong>Recordset</strong> object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-240"><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-240"><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-241">Establece o devuelve el criterio de ordenación para los registros de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> (solo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="dd778-241">Sets or returns the sort order for records in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-242"><strong><a href="recordset-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-242"><a href="recordset-stillexecuting-property-dao.md">expression</a>  . <strong>StillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-243"><strong>NOTA</strong>: las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="dd778-243">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="dd778-244">Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dd778-244">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="dd778-245">Indica si una operación asincrónica (es decir, un método invocado con la opción <strong>dbRunAsync</strong>) ha finalizado o no su ejecución (sólo para áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="dd778-245">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-246"><strong><a href="recordset-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-246"><strong><a href="recordset-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-247">Devuelve un valor que indica si un objeto admite transacciones.</span><span class="sxs-lookup"><span data-stu-id="dd778-247">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="dd778-248"><strong>Boolean</strong> de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd778-248">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-249"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="dd778-249"><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-250">La descripción de este miembro se mostrará en la versión final de Office 14.</span><span class="sxs-lookup"><span data-stu-id="dd778-250">The description for this member will appear in the final release of Office 14.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-251"><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-251"><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-252">Devuelve un valor que indica si el usuario puede cambiar un objeto DAO.</span><span class="sxs-lookup"><span data-stu-id="dd778-252">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="dd778-253"><strong>Booleano</strong> de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd778-253">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-254"><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-254"><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-255"><strong>NOTA</strong>: las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="dd778-255">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="dd778-256">Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dd778-256">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="dd778-p126">Establece o devuelve un valor que indica cómo se construye la cláusula WHERE para cada registro durante una actualización por lotes, y si la actualización por lotes debería utilizar una instrucción UPDATE o DELETE seguida de INSERT (sólo para áreas de trabajo de ODBCDirect). <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong> de lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="dd778-p126">Sets or returns a value that indicates how the WHERE clause is constructed for each record during a batch update, and whether the batch update should use an UPDATE statement or a DELETE followed by an INSERT (ODBCDirect workspaces only). Read/write <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd778-259"><strong><a href="recordset-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-259"><strong><a href="recordset-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-260">Establece o devuelve un valor que valida los datos en un campo mientras se modifica o se agrega a una tabla (sólo para áreas de trabajo de Microsoft Access). <strong>String</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="dd778-260">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd778-261"><strong><a href="recordset-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="dd778-261"><strong><a href="recordset-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="dd778-p127">Establece o devuelve un valor que especifica el texto del mensaje que su aplicación muestra si el valor de un objeto <strong>Field</strong> no satisface la regla de validación especificada por el valor de la propiedad <strong>ValidationRule</strong> (sólo para áreas de trabajo de Microsoft Access). <strong>String</strong> de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd778-p127">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only). Read-only <strong>String</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

