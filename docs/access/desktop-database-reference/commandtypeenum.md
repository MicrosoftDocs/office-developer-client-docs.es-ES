---
title: CommandTypeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: a570aaed8f0b2da415c3866ec88e7023085a1319
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887946"
---
# <a name="commandtypeenum"></a><span data-ttu-id="13180-102">CommandTypeEnum</span><span class="sxs-lookup"><span data-stu-id="13180-102">CommandTypeEnum</span></span>

<span data-ttu-id="13180-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="13180-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="13180-104">Especifica cómo se debe interpretar un argumento de comando.</span><span class="sxs-lookup"><span data-stu-id="13180-104">Specifies how a command argument should be interpreted.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13180-105">Constante</span><span class="sxs-lookup"><span data-stu-id="13180-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="13180-106">Valor</span><span class="sxs-lookup"><span data-stu-id="13180-106">Value</span></span></p></th>
<th><p><span data-ttu-id="13180-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="13180-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13180-108"><strong>adCmdUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="13180-108"><strong>adCmdUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="13180-109">-1</span><span class="sxs-lookup"><span data-stu-id="13180-109">-1</span></span></p></td>
<td><p><span data-ttu-id="13180-110">No especifica el argumento de tipo de comando.</span><span class="sxs-lookup"><span data-stu-id="13180-110">Does not specify the command type argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13180-111"><strong>adCmdText</strong></span><span class="sxs-lookup"><span data-stu-id="13180-111"><strong>adCmdText</strong></span></span></p></td>
<td><p><span data-ttu-id="13180-112">1</span><span class="sxs-lookup"><span data-stu-id="13180-112">1</span></span></p></td>
<td><p><span data-ttu-id="13180-113">Evalúa <a href="commandtext-property-ado.md">CommandText</a> como definición de texto de una llamada a un comando o procedimiento almacenado.</span><span class="sxs-lookup"><span data-stu-id="13180-113">Evaluates <a href="commandtext-property-ado.md">CommandText</a> as a textual definition of a command or stored procedure call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13180-114"><strong>adCmdTable</strong></span><span class="sxs-lookup"><span data-stu-id="13180-114"><strong>adCmdTable</strong></span></span></p></td>
<td><p><span data-ttu-id="13180-115">2</span><span class="sxs-lookup"><span data-stu-id="13180-115">2</span></span></p></td>
<td><p><span data-ttu-id="13180-116">Evalúa <strong>CommandText</strong> como nombre de tabla cuyas columnas se devuelven todas mediante una consulta SQL generada internamente.</span><span class="sxs-lookup"><span data-stu-id="13180-116">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned by an internally generated SQL query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13180-117"><strong>adCmdStoredProc</strong></span><span class="sxs-lookup"><span data-stu-id="13180-117"><strong>adCmdStoredProc</strong></span></span></p></td>
<td><p><span data-ttu-id="13180-118">4</span><span class="sxs-lookup"><span data-stu-id="13180-118">4</span></span></p></td>
<td><p><span data-ttu-id="13180-119">Evalúa <strong>CommandText</strong> como nombre de procedimiento almacenado.</span><span class="sxs-lookup"><span data-stu-id="13180-119">Evaluates <strong>CommandText</strong> as a stored procedure name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13180-120"><strong>adCmdUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="13180-120"><strong>adCmdUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="13180-121">8</span><span class="sxs-lookup"><span data-stu-id="13180-121">8</span></span></p></td>
<td><p><span data-ttu-id="13180-p101">Valor predeterminado. Indica que el tipo de comando de la propiedad <strong>CommandText</strong> no se conoce.</span><span class="sxs-lookup"><span data-stu-id="13180-p101">Default. Indicates that the type of command in the <strong>CommandText</strong> property is not known.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13180-124"><strong>adCmdFile</strong></span><span class="sxs-lookup"><span data-stu-id="13180-124"><strong>adCmdFile</strong></span></span></p></td>
<td><p><span data-ttu-id="13180-125">256</span><span class="sxs-lookup"><span data-stu-id="13180-125">256</span></span></p></td>
<td><p><span data-ttu-id="13180-p102">Evalúa <strong>CommandText</strong> como el nombre de archivo de un objeto <a href="recordset-object-ado.md">Recordset</a> almacenado de forma persistente. Se usa únicamente con un objeto <strong>Recordset</strong><a href="open-method-ado-recordset.md">Open</a> o <a href="requery-method-ado.md">Requery</a>.</span><span class="sxs-lookup"><span data-stu-id="13180-p102">Evaluates <strong>CommandText</strong> as the file name of a persistently stored <a href="recordset-object-ado.md">Recordset</a>. Used with <strong>Recordset.</strong><a href="open-method-ado-recordset.md">Open</a> or <a href="requery-method-ado.md">Requery</a> only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13180-128"><strong>adCmdTableDirect</strong></span><span class="sxs-lookup"><span data-stu-id="13180-128"><strong>adCmdTableDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="13180-129">512</span><span class="sxs-lookup"><span data-stu-id="13180-129">512</span></span></p></td>
<td><p><span data-ttu-id="13180-130">Evalúa <strong>CommandText</strong> como nombre de tabla cuyas columnas se devuelven.</span><span class="sxs-lookup"><span data-stu-id="13180-130">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned.</span></span> <span data-ttu-id="13180-131">Sólo se utiliza con <strong>Recordset.Open</strong> o <strong>Requery</strong> .</span><span class="sxs-lookup"><span data-stu-id="13180-131">Used with <strong>Recordset.Open</strong> or <strong>Requery</strong> only.</span></span> <span data-ttu-id="13180-132">Para usar el método <a href="seek-method-ado.md">Seek</a> , el <strong>Recordset</strong> se debe abrir con <strong>adCmdTableDirect</strong>.</span><span class="sxs-lookup"><span data-stu-id="13180-132">To use the <a href="seek-method-ado.md">Seek</a> method, the <strong>Recordset</strong> must be opened with <strong>adCmdTableDirect</strong>.</span></span> <span data-ttu-id="13180-133">Este valor no se puede combinar con el valor <strong>adAsyncExecute</strong> de <a href="executeoptionenum.md">ExecuteOptionEnum</a>.</span><span class="sxs-lookup"><span data-stu-id="13180-133">This value cannot be combined with the <a href="executeoptionenum.md">ExecuteOptionEnum</a> value <strong>adAsyncExecute</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="13180-134">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="13180-134">ADO/WFC equivalent</span></span>

<span data-ttu-id="13180-135">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="13180-135">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13180-136">Constante</span><span class="sxs-lookup"><span data-stu-id="13180-136">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13180-137">AdoEnums.CommandType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="13180-137">AdoEnums.CommandType.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13180-138">AdoEnums.CommandType.TEXT</span><span class="sxs-lookup"><span data-stu-id="13180-138">AdoEnums.CommandType.TEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13180-139">AdoEnums.CommandType.TABLE</span><span class="sxs-lookup"><span data-stu-id="13180-139">AdoEnums.CommandType.TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13180-140">AdoEnums.CommandType.STOREDPROC</span><span class="sxs-lookup"><span data-stu-id="13180-140">AdoEnums.CommandType.STOREDPROC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13180-141">AdoEnums.CommandType.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="13180-141">AdoEnums.CommandType.UNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13180-142">AdoEnums.CommandType.FILE</span><span class="sxs-lookup"><span data-stu-id="13180-142">AdoEnums.CommandType.FILE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13180-143">AdoEnums.CommandType.TABLEDIRECT</span><span class="sxs-lookup"><span data-stu-id="13180-143">AdoEnums.CommandType.TABLEDIRECT</span></span></p></td>
</tr>
</tbody>
</table>

