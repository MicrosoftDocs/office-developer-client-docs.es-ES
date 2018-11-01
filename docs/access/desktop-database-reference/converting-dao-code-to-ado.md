---
title: Convertir código DAO en ADO
TOCTitle: Convert DAO code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 60baeabfce93c2987cb9621c7cc877a7525a954c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876746"
---
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="97c69-102">Convertir código DAO en ADO</span><span class="sxs-lookup"><span data-stu-id="97c69-102">Convert DAO code to ADO</span></span>

<span data-ttu-id="97c69-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97c69-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="97c69-104">Versiones de la biblioteca DAO anteriores a 3.6 no se proporcionan ni son compatibles en Access.</span><span class="sxs-lookup"><span data-stu-id="97c69-104">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="97c69-105">DAO al mapa de objetos de ADO</span><span class="sxs-lookup"><span data-stu-id="97c69-105">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97c69-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="97c69-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="97c69-107"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="97c69-107"><strong>ADO (ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="97c69-108"><strong>Nota</strong></span><span class="sxs-lookup"><span data-stu-id="97c69-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97c69-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="97c69-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="97c69-110">Ninguna</span><span class="sxs-lookup"><span data-stu-id="97c69-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97c69-111">Workspace</span><span class="sxs-lookup"><span data-stu-id="97c69-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="97c69-112">Ninguna</span><span class="sxs-lookup"><span data-stu-id="97c69-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97c69-113">Base de datos</span><span class="sxs-lookup"><span data-stu-id="97c69-113">Database</span></span></p></td>
<td><p><span data-ttu-id="97c69-114">Connection</span><span class="sxs-lookup"><span data-stu-id="97c69-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97c69-115">Recordset</span><span class="sxs-lookup"><span data-stu-id="97c69-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="97c69-116">Recordset</span><span class="sxs-lookup"><span data-stu-id="97c69-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97c69-117">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="97c69-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="97c69-118">Keyset</span><span class="sxs-lookup"><span data-stu-id="97c69-118">Keyset</span></span></p></td>
<td><p><span data-ttu-id="97c69-119">Recupera un conjunto de punteros a los registros del objeto Recordset.</span><span class="sxs-lookup"><span data-stu-id="97c69-119">Retrieves a set of pointers to the records in the recordset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97c69-120">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="97c69-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="97c69-121">Static</span><span class="sxs-lookup"><span data-stu-id="97c69-121">Static</span></span></p></td>
<td><p><span data-ttu-id="97c69-122">Ambos recuperan registros completos pero puede actualizarse un conjunto de registros estático.</span><span class="sxs-lookup"><span data-stu-id="97c69-122">Both retrieve full records, but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97c69-123">Table-Type</span><span class="sxs-lookup"><span data-stu-id="97c69-123">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="97c69-124">Keyset con la opción adCmdTableDirect.</span><span class="sxs-lookup"><span data-stu-id="97c69-124">Keyset with adCmdTableDirect option.</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97c69-125">Field</span><span class="sxs-lookup"><span data-stu-id="97c69-125">Field</span></span></p></td>
<td><p><span data-ttu-id="97c69-126">Field</span><span class="sxs-lookup"><span data-stu-id="97c69-126">Field</span></span></p></td>
<td><p><span data-ttu-id="97c69-127">Cuando se hace referencia en un conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="97c69-127">When referred to in a recordset.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="97c69-128">DAO</span><span class="sxs-lookup"><span data-stu-id="97c69-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="97c69-129">Abrir un objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="97c69-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="97c69-130">Modificar un objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="97c69-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="97c69-131">ADO</span><span class="sxs-lookup"><span data-stu-id="97c69-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="97c69-132">Abrir un objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="97c69-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="97c69-133">Modificar un objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="97c69-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="97c69-134">Mover el enfoque desde el registro actual por medio de **MoveNext, MoveLast, MoveFirst, MovePrevious** sin utilizar primero el método **CancelUpdate** implícitamente, ejecuta el método **Update** .</span><span class="sxs-lookup"><span data-stu-id="97c69-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method implicitly executes the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="97c69-135">Acerca de los colaboradores</span><span class="sxs-lookup"><span data-stu-id="97c69-135">About the contributors</span></span>

<span data-ttu-id="97c69-136">**Vínculo proporcionado por** la Comunidad [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="97c69-136">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="97c69-137">UtterAccess es el principal foro de ayuda y wiki sobre Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="97c69-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="97c69-138">Elegir entre DAO y ADO</span><span class="sxs-lookup"><span data-stu-id="97c69-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

