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
localization_priority: Priority
ms.openlocfilehash: 77d56efd63d6a0841b595f12456baa808751706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295523"
---
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="9b725-102">Convertir código DAO en ADO</span><span class="sxs-lookup"><span data-stu-id="9b725-102">Convert DAO code to ADO</span></span>

<span data-ttu-id="9b725-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b725-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="9b725-104">Las versiones de la biblioteca DAO anteriores a 3.6 no se proporcionan ni son compatibles con Access.</span><span class="sxs-lookup"><span data-stu-id="9b725-104">Versions of the DAO library prior to 3.6 are not provided or supported in Microsoft Access 2010.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="9b725-105">Equivalencias entre objeto DAO y objeto ADO</span><span class="sxs-lookup"><span data-stu-id="9b725-105">DAO to ADO object Map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b725-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="9b725-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="9b725-107"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="9b725-107"><strong>ADO (ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="9b725-108"><strong>Nota</strong></span><span class="sxs-lookup"><span data-stu-id="9b725-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b725-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="9b725-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="9b725-110">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9b725-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b725-111">Workspace</span><span class="sxs-lookup"><span data-stu-id="9b725-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="9b725-112">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9b725-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b725-113">Database</span><span class="sxs-lookup"><span data-stu-id="9b725-113">Database</span></span></p></td>
<td><p><span data-ttu-id="9b725-114">Connection</span><span class="sxs-lookup"><span data-stu-id="9b725-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b725-115">Recordset</span><span class="sxs-lookup"><span data-stu-id="9b725-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="9b725-116">Recordset</span><span class="sxs-lookup"><span data-stu-id="9b725-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b725-117">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="9b725-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="9b725-118">Keyset</span><span class="sxs-lookup"><span data-stu-id="9b725-118">Keyset cursors</span></span></p></td>
<td><p><span data-ttu-id="9b725-119">Recupera un conjunto de punteros en los registros del conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="9b725-119">Retrieves a set of pointers to the records in the recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b725-120">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="9b725-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="9b725-121">Static</span><span class="sxs-lookup"><span data-stu-id="9b725-121">Static</span></span></p></td>
<td><p><span data-ttu-id="9b725-122">Ambos recuperan registros completos, pero un conjunto de registros Static puede actualizarse.</span><span class="sxs-lookup"><span data-stu-id="9b725-122">Both retrieve full records but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b725-123">Table-Type</span><span class="sxs-lookup"><span data-stu-id="9b725-123">TableType</span></span></p></td>
<td><p><span data-ttu-id="9b725-124">Keyset con la opción adCmdTableDirect</span><span class="sxs-lookup"><span data-stu-id="9b725-124">Keyset with adCmdTableDirect Option</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b725-125">Field</span><span class="sxs-lookup"><span data-stu-id="9b725-125">Field</span></span></p></td>
<td><p><span data-ttu-id="9b725-126">Field</span><span class="sxs-lookup"><span data-stu-id="9b725-126">Field</span></span></p></td>
<td><p><span data-ttu-id="9b725-127">Cuando se hace referencia a él en un conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="9b725-127">When referred to in a recordset</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="9b725-128">DAO</span><span class="sxs-lookup"><span data-stu-id="9b725-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="9b725-129">Abrir un Recordset</span><span class="sxs-lookup"><span data-stu-id="9b725-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="9b725-130">Editar un Recordset</span><span class="sxs-lookup"><span data-stu-id="9b725-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="9b725-131">ADO</span><span class="sxs-lookup"><span data-stu-id="9b725-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="9b725-132">Abrir un Recordset</span><span class="sxs-lookup"><span data-stu-id="9b725-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="9b725-133">Editar un Recordset</span><span class="sxs-lookup"><span data-stu-id="9b725-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="9b725-134">Si se mueve el enfoque desde el registro actual por medio de **MoveNext, MoveLast, MoveFirst, MovePrevious** sin utilizar primero el método **CancelUpdate**, se ejecutará implícitamente el método **Update**.</span><span class="sxs-lookup"><span data-stu-id="9b725-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method will implicitly execute the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="9b725-135">Información sobre los colaboradores</span><span class="sxs-lookup"><span data-stu-id="9b725-135">About the contributors</span></span>

<span data-ttu-id="9b725-136">**Vínculo proporcionado por** la comunidad de [UtterAccess](https://www.utteraccess.com).</span><span class="sxs-lookup"><span data-stu-id="9b725-136">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="9b725-137">UtterAccess es el principal foro de ayuda y wiki de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9b725-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="9b725-138">Elegir entre DAO y ADO</span><span class="sxs-lookup"><span data-stu-id="9b725-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

