---
title: Enumeración RecordsetOptionEnum (DAO)
TOCTitle: RecordsetOptionEnum Enumeration
ms:assetid: 3a9d8664-dcb6-cb60-7cf6-e229eb699ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192649(v=office.15)
ms:contentKeyID: 48544266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 45d4b67eecc54f526c8a88296b48784468118e67
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483785"
---
# <a name="recordsetoptionenum-enumeration-dao"></a><span data-ttu-id="921d8-102">Enumeración RecordsetOptionEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="921d8-102">RecordsetOptionEnum Enumeration (DAO)</span></span>


<span data-ttu-id="921d8-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="921d8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="921d8-104">Se usa con el método **OpenRecordset** para especificar las características de un nuevo objeto de **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="921d8-104">Used with the **OpenRecordset** method to specify characteristics of a new **Recordset** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="921d8-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="921d8-105">Name</span></span></p></th>
<th><p><span data-ttu-id="921d8-106">Valor</span><span class="sxs-lookup"><span data-stu-id="921d8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="921d8-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="921d8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="921d8-108">dbAppendOnly</span><span class="sxs-lookup"><span data-stu-id="921d8-108">dbAppendOnly</span></span></p></td>
<td><p><span data-ttu-id="921d8-109">8</span><span class="sxs-lookup"><span data-stu-id="921d8-109">8</span></span></p></td>
<td><p><span data-ttu-id="921d8-110">Permite al usuario agregar nuevos registros al conjunto de registros de tipo dynaset, pero le impide leer los registros existentes.</span><span class="sxs-lookup"><span data-stu-id="921d8-110">Allows user to add new records to the dynaset, but prevents user from reading existing records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="921d8-111">dbConsistent</span><span class="sxs-lookup"><span data-stu-id="921d8-111">dbConsistent</span></span></p></td>
<td><p><span data-ttu-id="921d8-112">32</span><span class="sxs-lookup"><span data-stu-id="921d8-112">32</span></span></p></td>
<td><p><span data-ttu-id="921d8-113">Aplica actualizaciones sólo a los campos que no afectarán a otros registros en el conjunto de registros de tipo dynaset (tipo dynaset y snapshot únicamente).</span><span class="sxs-lookup"><span data-stu-id="921d8-113">Applies updates only to those fields that will not affect other records in the dynaset (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="921d8-114">dbDenyRead</span><span class="sxs-lookup"><span data-stu-id="921d8-114">dbDenyRead</span></span></p></td>
<td><p><span data-ttu-id="921d8-115">2</span><span class="sxs-lookup"><span data-stu-id="921d8-115">2</span></span></p></td>
<td><p><span data-ttu-id="921d8-116">Impide a otros usuario leer registros del conjunto de registros (tipo tabla únicamente).</span><span class="sxs-lookup"><span data-stu-id="921d8-116">Prevents other users from reading Recordset records (table-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="921d8-117">dbDenyWrite</span><span class="sxs-lookup"><span data-stu-id="921d8-117">dbDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="921d8-118">1</span><span class="sxs-lookup"><span data-stu-id="921d8-118">1</span></span></p></td>
<td><p><span data-ttu-id="921d8-119">Impide a otros usuario cambiar registros del conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="921d8-119">Prevents other users from changing Recordset records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="921d8-120">dbExecDirect</span><span class="sxs-lookup"><span data-stu-id="921d8-120">dbExecDirect</span></span></p></td>
<td><p><span data-ttu-id="921d8-121">2048</span><span class="sxs-lookup"><span data-stu-id="921d8-121">2048</span></span></p></td>
<td><p><span data-ttu-id="921d8-122">Ejecuta la consulta sin llamar primero a la función de ODBC de SQLPrepare.</span><span class="sxs-lookup"><span data-stu-id="921d8-122">Executes the query without first calling the SQLPrepare ODBC function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="921d8-123">dbFailOnError</span><span class="sxs-lookup"><span data-stu-id="921d8-123">dbFailOnError</span></span></p></td>
<td><p><span data-ttu-id="921d8-124">128</span><span class="sxs-lookup"><span data-stu-id="921d8-124">128</span></span></p></td>
<td><p><span data-ttu-id="921d8-125">Deshace las actualizaciones si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="921d8-125">Rolls back updates if an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="921d8-126">dbForwardOnly</span><span class="sxs-lookup"><span data-stu-id="921d8-126">dbForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="921d8-127">256</span><span class="sxs-lookup"><span data-stu-id="921d8-127">256</span></span></p></td>
<td><p><span data-ttu-id="921d8-128">Crea un conjunto de registros de tipo snapshot que sólo admite desplazamientos hacia delante (tipo snapshot únicamente).</span><span class="sxs-lookup"><span data-stu-id="921d8-128">Creates a forward-only scrolling snapshot-type Recordset (snapshot-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="921d8-129">dbInconsistent</span><span class="sxs-lookup"><span data-stu-id="921d8-129">dbInconsistent</span></span></p></td>
<td><p><span data-ttu-id="921d8-130">16</span><span class="sxs-lookup"><span data-stu-id="921d8-130">16</span></span></p></td>
<td><p><span data-ttu-id="921d8-131">Aplica actualizaciones a todos los campos del conjunto de registros de tipo dynaset, aunque otros registros se vean afectados (tipo dynaset y snapshot únicamente).</span><span class="sxs-lookup"><span data-stu-id="921d8-131">Applies updates to all dynaset fields, even if other records are affected (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="921d8-132">dbReadOnly</span><span class="sxs-lookup"><span data-stu-id="921d8-132">dbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="921d8-133">4</span><span class="sxs-lookup"><span data-stu-id="921d8-133">4</span></span></p></td>
<td><p><span data-ttu-id="921d8-134">Abre el conjunto de registros en modo de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="921d8-134">Opens the Recordset as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="921d8-135">dbRunAsync</span><span class="sxs-lookup"><span data-stu-id="921d8-135">dbRunAsync</span></span></p></td>
<td><p><span data-ttu-id="921d8-136">1024</span><span class="sxs-lookup"><span data-stu-id="921d8-136">1024</span></span></p></td>
<td><p><span data-ttu-id="921d8-137">Ejecuta la consulta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="921d8-137">Executes the query asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="921d8-138">dbSeeChanges</span><span class="sxs-lookup"><span data-stu-id="921d8-138">dbSeeChanges</span></span></p></td>
<td><p><span data-ttu-id="921d8-139">512</span><span class="sxs-lookup"><span data-stu-id="921d8-139">512</span></span></p></td>
<td><p><span data-ttu-id="921d8-140">Genera un error en tiempo de ejecución si otro usuario cambia datos que se estén editando (tipo dynaset únicamente).</span><span class="sxs-lookup"><span data-stu-id="921d8-140">Generates a run-time error if another user is changing data you are editing (dynaset-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="921d8-141">dbSQLPassThrough</span><span class="sxs-lookup"><span data-stu-id="921d8-141">dbSQLPassThrough</span></span></p></td>
<td><p><span data-ttu-id="921d8-142">64</span><span class="sxs-lookup"><span data-stu-id="921d8-142">64</span></span></p></td>
<td><p><span data-ttu-id="921d8-143">Envía una instrucción SQL a una base de datos ODBC (tipo snapshot únicamente).</span><span class="sxs-lookup"><span data-stu-id="921d8-143">Sends an SQL statement to an ODBC database (snapshot-type only).</span></span></p></td>
</tr>
</tbody>
</table>

