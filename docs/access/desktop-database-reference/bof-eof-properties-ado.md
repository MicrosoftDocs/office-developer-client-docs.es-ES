---
<span data-ttu-id="f8862-101"><<<<<<< Título HEAD: BOF, EOF propiedades (ADO) TOCTitle: BOF, EOF propiedades (ADO) === título: BOF, EOF (propiedades) (ADO) TOCTitle: BOF, propiedades EOF (ADO)</span><span class="sxs-lookup"><span data-stu-id="f8862-101"><<<<<<< HEAD title: BOF, EOF Properties (ADO) TOCTitle: BOF, EOF Properties (ADO) ======= title: BOF, EOF properties (ADO) TOCTitle: BOF, EOF properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="f8862-102">Master ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15) ms:contentKeyID: ms.date 48548768: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="f8862-102">master ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15) ms:contentKeyID: 48548768 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="f8862-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f8862-103"><<<<<<< HEAD</span></span>
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="f8862-104">Propiedades BOF y EOF (ADO)</span><span class="sxs-lookup"><span data-stu-id="f8862-104">BOF, EOF Properties (ADO)</span></span>
=======
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="f8862-105">BOF, EOF (propiedades) (ADO)</span><span class="sxs-lookup"><span data-stu-id="f8862-105">BOF, EOF properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="f8862-106">master</span><span class="sxs-lookup"><span data-stu-id="f8862-106">master</span></span>


<span data-ttu-id="f8862-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8862-107">**Applies to**: Access 2013 | Office 2013</span></span>

  - <span data-ttu-id="f8862-108">**BOF**: indica que la posición de registro actual se sitúa delante del primer registro de un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f8862-108">**BOF** — Indicates that the current record position is before the first record in a [Recordset](recordset-object-ado.md) object.</span></span>

  - <span data-ttu-id="f8862-109">**EOF**: indica que la posición de registro actual se sitúa después del último registro de un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f8862-109">**EOF** — Indicates that the current record position is after the last record in a **Recordset** object.</span></span>

<span data-ttu-id="f8862-110"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f8862-110"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="f8862-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8862-111">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="f8862-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8862-112">Return value</span></span>
>>>>>>> <span data-ttu-id="f8862-113">master</span><span class="sxs-lookup"><span data-stu-id="f8862-113">master</span></span>

<span data-ttu-id="f8862-114">Las propiedades **BOF** y **EOF** devuelven valores **booleanos**.</span><span class="sxs-lookup"><span data-stu-id="f8862-114">The **BOF** and **EOF** properties return **Boolean** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8862-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8862-115">Remarks</span></span>

<span data-ttu-id="f8862-116">Use las propiedades **BOF** y **EOF** para determinar si un objeto **Recordset** contiene registros o si se ha desplazado más allá de los límites de un objeto **Recordset** cuando se mueve de un registro a otro.</span><span class="sxs-lookup"><span data-stu-id="f8862-116">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="f8862-117">La propiedad **BOF** devuelve **True** (-1) si la posición de registro actual se sitúa delante del primer registro y devuelve **False** (0) si la posición de registro actual se sitúa en el primer registro o después del mismo.</span><span class="sxs-lookup"><span data-stu-id="f8862-117">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="f8862-118">La propiedad **EOF** devuelve **True** si la posición de registro actual se sitúa después del último registro y devuelve **False** si la posición de registro actual se sitúa en el último registro o delante del mismo.</span><span class="sxs-lookup"><span data-stu-id="f8862-118">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="f8862-119">Si la propiedad **BOF** o **EOF** es **True**, no hay ningún registro actual.</span><span class="sxs-lookup"><span data-stu-id="f8862-119">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="f8862-p101">Si se abre un objeto **Recordset** que no contiene registros, las propiedades **BOF** y **EOF** tienen el valor **True** (vea la propiedad [RecordCount](recordcount-property-ado.md) para obtener más información sobre este estado de un objeto **Recordset**). Si se abre un objeto **Recordset** que contiene al menos un registro, el primer registro es el registro actual y las propiedades **BOF** y **EOF** tienen el valor **False**.</span><span class="sxs-lookup"><span data-stu-id="f8862-p101">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True** (see the [RecordCount](recordcount-property-ado.md) property for more information about this state of a **Recordset**). When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="f8862-122">Si se elimina el último registro que queda en el objeto **Recordset**, puede que el valor de las propiedades **BOF** y **EOF** siga siendo **False** hasta que se intente ajustar la posición del registro actual.</span><span class="sxs-lookup"><span data-stu-id="f8862-122">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="f8862-123">En esta tabla se muestran los métodos **Move** permitidos con diferentes combinaciones de las propiedades **BOF** y **EOF**.</span><span class="sxs-lookup"><span data-stu-id="f8862-123">This table shows which **Move** methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="f8862-124">Métodos MoveFirst,</span><span class="sxs-lookup"><span data-stu-id="f8862-124">MoveFirst,</span></span><br />
<span data-ttu-id="f8862-125">MoveLast</span><span class="sxs-lookup"><span data-stu-id="f8862-125">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="f8862-126">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="f8862-126">MovePrevious,</span></span><br />
<span data-ttu-id="f8862-127">Mover &lt; 0</span><span class="sxs-lookup"><span data-stu-id="f8862-127">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="f8862-128">Move 0</span><span class="sxs-lookup"><span data-stu-id="f8862-128">Move 0</span></span></p></th>
<th><p><span data-ttu-id="f8862-129">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="f8862-129">MoveNext,</span></span><br />
<span data-ttu-id="f8862-130">Mover &gt; 0</span><span class="sxs-lookup"><span data-stu-id="f8862-130">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8862-131"><strong>BOF = True,</strong></span><span class="sxs-lookup"><span data-stu-id="f8862-131"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="f8862-132">
<strong>EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="f8862-132">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="f8862-133">Permitido</span><span class="sxs-lookup"><span data-stu-id="f8862-133">Allowed</span></span></p></td>
<td><p><span data-ttu-id="f8862-134">Error</span><span class="sxs-lookup"><span data-stu-id="f8862-134">Error</span></span></p></td>
<td><p><span data-ttu-id="f8862-135">Error</span><span class="sxs-lookup"><span data-stu-id="f8862-135">Error</span></span></p></td>
<td><p><span data-ttu-id="f8862-136">Permitido</span><span class="sxs-lookup"><span data-stu-id="f8862-136">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8862-137"><strong>BOF = False,</strong></span><span class="sxs-lookup"><span data-stu-id="f8862-137"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="f8862-138">
<strong>EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="f8862-138">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="f8862-139">Permitido</span><span class="sxs-lookup"><span data-stu-id="f8862-139">Allowed</span></span></p></td>
<td><p><span data-ttu-id="f8862-140">Permitido</span><span class="sxs-lookup"><span data-stu-id="f8862-140">Allowed</span></span></p></td>
<td><p><span data-ttu-id="f8862-141">Error</span><span class="sxs-lookup"><span data-stu-id="f8862-141">Error</span></span></p></td>
<td><p><span data-ttu-id="f8862-142">Error</span><span class="sxs-lookup"><span data-stu-id="f8862-142">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8862-143">Ambas propiedades son <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="f8862-143">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="f8862-144">Error</span><span class="sxs-lookup"><span data-stu-id="f8862-144">Error</span></span></p></td>
<td><p><span data-ttu-id="f8862-145">Error</span><span class="sxs-lookup"><span data-stu-id="f8862-145">Error</span></span></p></td>
<td><p><span data-ttu-id="f8862-146">Error</span><span class="sxs-lookup"><span data-stu-id="f8862-146">Error</span></span></p></td>
<td><p><span data-ttu-id="f8862-147">Error</span><span class="sxs-lookup"><span data-stu-id="f8862-147">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8862-148">Ambas propiedades son <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="f8862-148">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="f8862-149">Permitido</span><span class="sxs-lookup"><span data-stu-id="f8862-149">Allowed</span></span></p></td>
<td><p><span data-ttu-id="f8862-150">Permitido</span><span class="sxs-lookup"><span data-stu-id="f8862-150">Allowed</span></span></p></td>
<td><p><span data-ttu-id="f8862-151">Permitido</span><span class="sxs-lookup"><span data-stu-id="f8862-151">Allowed</span></span></p></td>
<td><p><span data-ttu-id="f8862-152">Permitido</span><span class="sxs-lookup"><span data-stu-id="f8862-152">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f8862-153">Si un método **Move** está permitido, esto no garantiza que busque correctamente un registro; sólo significa que las llamadas al método **Move** especificado no generarán un error.</span><span class="sxs-lookup"><span data-stu-id="f8862-153">Allowing a **Move** method doesn't guarantee that the method will successfully locate a record; it only means that calling the specified **Move** method won't generate an error.</span></span>

<span data-ttu-id="f8862-154">En la tabla siguiente se muestra lo que les sucede a los valores de configuración de **BOF** y **EOF** cuando se llama a varios métodos **Move** y no se puede encontrar un registro.</span><span class="sxs-lookup"><span data-stu-id="f8862-154">The following table shows what happens to the **BOF** and **EOF** property settings when you call various **Move** methods but are unable to successfully locate a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="f8862-155">BOF</span><span class="sxs-lookup"><span data-stu-id="f8862-155">BOF</span></span></p></th>
<th><p><span data-ttu-id="f8862-156">EOF</span><span class="sxs-lookup"><span data-stu-id="f8862-156">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8862-157"><strong>Métodos MoveFirst</strong>, <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="f8862-157"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="f8862-158">Establecer en <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="f8862-158">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="f8862-159">Establecer en <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="f8862-159">Set to <strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8862-160"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="f8862-160"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="f8862-161">No cambia</span><span class="sxs-lookup"><span data-stu-id="f8862-161">No change</span></span></p></td>
<td><p><span data-ttu-id="f8862-162">No cambia</span><span class="sxs-lookup"><span data-stu-id="f8862-162">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8862-163"><strong>MovePrevious</strong>, <strong>mueva</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="f8862-163"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="f8862-164">Se establece en <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="f8862-164">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="f8862-165">No cambia</span><span class="sxs-lookup"><span data-stu-id="f8862-165">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8862-166"><strong>MoveNext</strong>, <strong>mueva</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="f8862-166"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="f8862-167">No cambia</span><span class="sxs-lookup"><span data-stu-id="f8862-167">No change</span></span></p></td>
<td><p><span data-ttu-id="f8862-168">Se establece en <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="f8862-168">Set to <strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

