---
<span data-ttu-id="d706c-101"><<<<<<< Título HEAD: convertir código DAO en ADO TOCTitle: convertir código DAO en ADO ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: ms.date 48544585: 18/09/2015 === título: convertir DAO código de ADO TOCTitle: código DAO convertir a ADO ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: ms.date 48544585: 16/10/2018</span><span class="sxs-lookup"><span data-stu-id="d706c-101"><<<<<<< HEAD title: Converting DAO Code to ADO TOCTitle: Converting DAO Code to ADO ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: 48544585 ms.date: 09/18/2015 ======= title: Convert DAO code to ADO TOCTitle: Convert DAO code to ADO ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: 48544585 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="d706c-102">maestro mtps_version: Office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="d706c-102">master mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="d706c-103">vbaac10.chm5267115 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="d706c-103">vbaac10.chm5267115 f1_categories:</span></span>
- <span data-ttu-id="d706c-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="d706c-104">Office.Version=v15</span></span>
---

<span data-ttu-id="d706c-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="d706c-105"><<<<<<< HEAD</span></span>
# <a name="converting-dao-code-to-ado"></a><span data-ttu-id="d706c-106">Convertir código DAO en ADO</span><span class="sxs-lookup"><span data-stu-id="d706c-106">Converting DAO Code to ADO</span></span>
=======
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="d706c-107">Convertir código DAO en ADO</span><span class="sxs-lookup"><span data-stu-id="d706c-107">Convert DAO code to ADO</span></span>
>>>>>>> <span data-ttu-id="d706c-108">master</span><span class="sxs-lookup"><span data-stu-id="d706c-108">master</span></span>

<span data-ttu-id="d706c-109">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d706c-109">**Applies to**: Access 2013 | Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="d706c-110">Versiones de la biblioteca DAO anteriores a 3.6 no se proporcionan ni son compatibles en Access.</span><span class="sxs-lookup"><span data-stu-id="d706c-110">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="d706c-111">DAO al mapa de objetos de ADO</span><span class="sxs-lookup"><span data-stu-id="d706c-111">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d706c-112"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="d706c-112"><strong>DAO</strong></span></span></p></th>
<span data-ttu-id="d706c-113"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="d706c-113"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="d706c-114"><strong>ADO(ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="d706c-114"><strong>ADO(ADODB)</strong></span></span></p></th>
=======
<th><p><span data-ttu-id="d706c-115"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="d706c-115"><strong>ADO (ADODB)</strong></span></span></p></th><span data-ttu-id="d706c-116">
>>>>>>>patrón</span><span class="sxs-lookup"><span data-stu-id="d706c-116">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="d706c-117"><strong>Nota</strong></span><span class="sxs-lookup"><span data-stu-id="d706c-117"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d706c-118">DBEngine</span><span class="sxs-lookup"><span data-stu-id="d706c-118">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="d706c-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d706c-119">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d706c-120">Workspace</span><span class="sxs-lookup"><span data-stu-id="d706c-120">Workspace</span></span></p></td>
<td><p><span data-ttu-id="d706c-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d706c-121">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d706c-122">Base de datos</span><span class="sxs-lookup"><span data-stu-id="d706c-122">Database</span></span></p></td>
<td><p><span data-ttu-id="d706c-123">Connection</span><span class="sxs-lookup"><span data-stu-id="d706c-123">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d706c-124">Recordset</span><span class="sxs-lookup"><span data-stu-id="d706c-124">Recordset</span></span></p></td>
<td><p><span data-ttu-id="d706c-125">Recordset</span><span class="sxs-lookup"><span data-stu-id="d706c-125">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d706c-126">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="d706c-126">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="d706c-127">Keyset</span><span class="sxs-lookup"><span data-stu-id="d706c-127">Keyset</span></span></p></td>
<span data-ttu-id="d706c-128"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="d706c-128"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="d706c-129">Recupera un conjunto de punteros en los registros del conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="d706c-129">Retrieves a set of pointers to the records in the recordset</span></span></p></td>
=======
<td><p><span data-ttu-id="d706c-130">Recupera un conjunto de punteros a los registros del objeto Recordset.</span><span class="sxs-lookup"><span data-stu-id="d706c-130">Retrieves a set of pointers to the records in the recordset.</span></span></p></td><span data-ttu-id="d706c-131">
>>>>>>>patrón</span><span class="sxs-lookup"><span data-stu-id="d706c-131">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d706c-132">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="d706c-132">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="d706c-133">Static</span><span class="sxs-lookup"><span data-stu-id="d706c-133">Static</span></span></p></td>
<span data-ttu-id="d706c-134"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="d706c-134"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="d706c-135">Ambos recuperan registros completos pero puede actualizarse un conjunto de registros Static.</span><span class="sxs-lookup"><span data-stu-id="d706c-135">Both retrieve full records but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d706c-136">Table-Type</span><span class="sxs-lookup"><span data-stu-id="d706c-136">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="d706c-137">Keyset con la opción adCmdTableDirect</span><span class="sxs-lookup"><span data-stu-id="d706c-137">Keyset with adCmdTableDirect Option</span></span></p></td>
=======
<td><p><span data-ttu-id="d706c-138">Ambos recuperan registros completos pero puede actualizarse un conjunto de registros estático.</span><span class="sxs-lookup"><span data-stu-id="d706c-138">Both retrieve full records, but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d706c-139">Table-Type</span><span class="sxs-lookup"><span data-stu-id="d706c-139">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="d706c-140">Keyset con la opción adCmdTableDirect.</span><span class="sxs-lookup"><span data-stu-id="d706c-140">Keyset with adCmdTableDirect option.</span></span></p></td><span data-ttu-id="d706c-141">
>>>>>>>patrón</span><span class="sxs-lookup"><span data-stu-id="d706c-141">
>>>>>>> master</span></span>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d706c-142">Field</span><span class="sxs-lookup"><span data-stu-id="d706c-142">Field</span></span></p></td>
<td><p><span data-ttu-id="d706c-143">Field</span><span class="sxs-lookup"><span data-stu-id="d706c-143">Field</span></span></p></td>
<span data-ttu-id="d706c-144"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="d706c-144"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="d706c-145">Cuando se hace referencia a él en un conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="d706c-145">When referred to in a recordset</span></span></p></td>
=======
<td><p><span data-ttu-id="d706c-146">Cuando se hace referencia en un conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="d706c-146">When referred to in a recordset.</span></span></p></td><span data-ttu-id="d706c-147">
>>>>>>>patrón</span><span class="sxs-lookup"><span data-stu-id="d706c-147">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="d706c-148">DAO</span><span class="sxs-lookup"><span data-stu-id="d706c-148">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="d706c-149">Abrir un objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="d706c-149">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="d706c-150">Modificar un objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="d706c-150">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="d706c-151">ADO</span><span class="sxs-lookup"><span data-stu-id="d706c-151">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="d706c-152">Abrir un objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="d706c-152">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="d706c-153">Modificar un objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="d706c-153">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
<span data-ttu-id="d706c-154"><<<<<<< HEAD mover el foco del registro actual por medio de **MoveNext, MoveLast, MoveFirst, MovePrevious** sin utilizar primero el método **CancelUpdate** , se ejecutará implícitamente el método **Update** .</span><span class="sxs-lookup"><span data-stu-id="d706c-154"><<<<<<< HEAD Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method will implicitly execute the **Update** method.</span></span>
> <span data-ttu-id="d706c-155">=== Moviendo enfoque desde el registro actual por medio de **MoveNext, MoveLast, MoveFirst, MovePrevious** sin utilizar primero el método **CancelUpdate** implícitamente, ejecuta el método **Update** .</span><span class="sxs-lookup"><span data-stu-id="d706c-155">======= Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method implicitly executes the **Update** method.</span></span>
>>>>>>> <span data-ttu-id="d706c-156">master</span><span class="sxs-lookup"><span data-stu-id="d706c-156">master</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="d706c-157">Acerca de los colaboradores</span><span class="sxs-lookup"><span data-stu-id="d706c-157">About the contributors</span></span>

<span data-ttu-id="d706c-158">**Vínculo proporcionado por** la Comunidad [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="d706c-158">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="d706c-159">UtterAccess es el principal foro de ayuda y wiki sobre Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="d706c-159">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="d706c-160">Elegir entre DAO y ADO</span><span class="sxs-lookup"><span data-stu-id="d706c-160">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<span data-ttu-id="d706c-161"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="d706c-161"><<<<<<< HEAD</span></span>

=======
<br/>
>>>>>>> <span data-ttu-id="d706c-162">master</span><span class="sxs-lookup"><span data-stu-id="d706c-162">master</span></span>

