---
title: Clone (método) - ActiveX Data Objects (ADO)
TOCTitle: Clone Method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a93fb7fd333156c6939311c0e247f4b5f8aec16
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25607042"
---
# <a name="clone-method-ado"></a><span data-ttu-id="8e399-102">Clone (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="8e399-102">Clone Method (ADO)</span></span>


<span data-ttu-id="8e399-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e399-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="8e399-p101">Crea un objeto [Recordset](recordset-object-ado.md) duplicado a partir de un objeto **Recordset** existente. Opcionalmente, especifica que el duplicado es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e399-p101">Creates a duplicate [Recordset](recordset-object-ado.md) object from an existing **Recordset** object. Optionally, specifies that the clone be read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e399-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e399-106">Syntax</span></span>

<span data-ttu-id="8e399-107">**Establecer** *rstDuplicate*  =  *rstOriginal*. Clone (*LockType*)</span><span class="sxs-lookup"><span data-stu-id="8e399-107">**Set** *rstDuplicate* = *rstOriginal*.Clone (*LockType*)</span></span>

<span data-ttu-id="8e399-108"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="8e399-108"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="8e399-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e399-109">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="8e399-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e399-110">Return value</span></span>
>>>>>>> <span data-ttu-id="8e399-111">master</span><span class="sxs-lookup"><span data-stu-id="8e399-111">master</span></span>

<span data-ttu-id="8e399-112">Devuelve una referencia al objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="8e399-112">Returns a **Recordset** object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e399-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e399-113">Parameters</span></span>

  - <span data-ttu-id="8e399-114">*rstDuplicate*</span><span class="sxs-lookup"><span data-stu-id="8e399-114">*rstDuplicate*</span></span>

  - <span data-ttu-id="8e399-115">Una variable de objeto que identifica el objeto **Recordset** duplicado que se creará.</span><span class="sxs-lookup"><span data-stu-id="8e399-115">An object variable that identifies the duplicate **Recordset** object to be created.</span></span>

  - <span data-ttu-id="8e399-116">*rstOriginal*</span><span class="sxs-lookup"><span data-stu-id="8e399-116">*rstOriginal*</span></span>

  - <span data-ttu-id="8e399-117">Una variable de objeto que identifica el objeto **Recordset** duplicado.</span><span class="sxs-lookup"><span data-stu-id="8e399-117">An object variable that identifies the **Recordset** object to be duplicated.</span></span>

  - <span data-ttu-id="8e399-118">*LockType*</span><span class="sxs-lookup"><span data-stu-id="8e399-118">*LockType*</span></span>

  - <span data-ttu-id="8e399-p102">Opcional. Valor de [LockTypeEnum](locktypeenum.md) que especifica el tipo de bloqueo del objeto **Recordset** original, o bien un **Recordset** de sólo lectura. Los valores válidos son **adLockUnspecified** o **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="8e399-p102">Optional. A [LockTypeEnum](locktypeenum.md) value that specifies either the lock type of the original **Recordset**, or a read-only **Recordset**. Valid values are **adLockUnspecified** or **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e399-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8e399-122">Remarks</span></span>

<span data-ttu-id="8e399-p103">Use el método **Clone** para crear varios objetos **Recordset** duplicados, sobre todo si desea mantener más de un registro actual en un conjunto determinado de registros. El método **Clone** es más eficaz que crear y abrir un nuevo objeto **Recordset** con la misma definición que el original.</span><span class="sxs-lookup"><span data-stu-id="8e399-p103">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records. Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="8e399-p104">La propiedad [Filter](filter-property-ado.md) del objeto **Recordset** original, si hay alguna, no se aplicarán a la copia. Establezca la propiedad **Filter** del nuevo **objeto Recordset** para filtrar los resultados. La forma más sencilla para copiar cualquier valor de **filtro** existente es asignarlo directamente, similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="8e399-p104">The [Filter](filter-property-ado.md) property of the original **Recordset**, if any, will not be applied to the clone. Set the **Filter** property of the new **Recordset** in order to filter the results. The simplest way to copy any existing **Filter** value is to assign it directly, like this:</span></span>

<span data-ttu-id="8e399-128">El registro actual de un clon recién creado se establece en el primer registro.</span><span class="sxs-lookup"><span data-stu-id="8e399-128">The current record of a newly created clone is set to the first record.</span></span>

<span data-ttu-id="8e399-p105">Los cambios realizados en un objeto **Recordset** se ven en todos sus duplicados, independientemente del tipo de cursor. Sin embargo, después de ejecutar [Requery](requery-method-ado.md) en el objeto **Recordset** original, los duplicados ya no estarán sincronizados con el original.</span><span class="sxs-lookup"><span data-stu-id="8e399-p105">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type. However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="8e399-131">Al cerrar el objeto **Recordset** original, no se cierran sus copias; como tampoco se cierra el original ni ninguna de las demás copias al cerrarse una copia.</span><span class="sxs-lookup"><span data-stu-id="8e399-131">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="8e399-p106">Sólo se puede duplicar un objeto **Recordset** que admite marcadores. Los valores de marcador son intercambiables; es decir, una referencia de marcador de un objeto **Recordset** hace referencia al mismo registro en todos sus duplicados.</span><span class="sxs-lookup"><span data-stu-id="8e399-p106">You can only clone a **Recordset** object that supports bookmarks. Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

<span data-ttu-id="8e399-p107">Algunos de los eventos de **Recordset** también se desencadenan en todos los duplicados de **Recordset**. Sin embargo, dado que el registro actual puede diferir entre clonada **conjuntos de registros**, los eventos no sea válidos para el duplicado.</span><span class="sxs-lookup"><span data-stu-id="8e399-p107">Some **Recordset** events that are triggered will also fire in all **Recordset** clones. However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span></span>

<span data-ttu-id="8e399-136">Por ejemplo, si cambia un valor de un campo, se producirá un evento [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) en el **objeto Recordset** modificado y en todos los duplicados.</span><span class="sxs-lookup"><span data-stu-id="8e399-136">For example, if you change a value of a field, a [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) event will occur in the changed **Recordset** and in all clones.</span></span> <span data-ttu-id="8e399-137">El parámetro *Fields* del evento **WillChangeField** de un clonado **Recordset** (donde no se ha realizado el cambio) hará simplemente referencia a los campos del actual registro del duplicado, el cual puede ser diferente del actual registro de la original **Recordset** donde se produjo el cambio.</span><span class="sxs-lookup"><span data-stu-id="8e399-137">The *Fields* parameter of the **WillChangeField** event of a cloned **Recordset** (where the change was not made) will simply refer to the fields of the current record of the clone, which may be a different record than the current record of the original **Recordset** where the change occurred.</span></span>

<span data-ttu-id="8e399-138">La siguiente tabla recoge una lista completa de todos los eventos de **conjunto de registros** y se indica si son válidas y desencadenadas para cualquier generados mediante el método **Clone** los duplicados de recordset.</span><span class="sxs-lookup"><span data-stu-id="8e399-138">The following table provided a full listing of all **Recordset** events and indicates whether they are valid and triggered for any recordset clones generated using the **Clone** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e399-139">Evento</span><span class="sxs-lookup"><span data-stu-id="8e399-139">Event</span></span></p></th>
<th><p><span data-ttu-id="8e399-140">¿Se desencadena en los duplicados?</span><span class="sxs-lookup"><span data-stu-id="8e399-140">Triggered in clones?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e399-141"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="8e399-141"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="8e399-142">No</span><span class="sxs-lookup"><span data-stu-id="8e399-142">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e399-143"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="8e399-143"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="8e399-144">No</span><span class="sxs-lookup"><span data-stu-id="8e399-144">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e399-145"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="8e399-145"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="8e399-146">No</span><span class="sxs-lookup"><span data-stu-id="8e399-146">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e399-147"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="8e399-147"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="8e399-148">Sí</span><span class="sxs-lookup"><span data-stu-id="8e399-148">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e399-149"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="8e399-149"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="8e399-150">No</span><span class="sxs-lookup"><span data-stu-id="8e399-150">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e399-151"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="8e399-151"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="8e399-152">Sí</span><span class="sxs-lookup"><span data-stu-id="8e399-152">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e399-153"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="8e399-153"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="8e399-154">No</span><span class="sxs-lookup"><span data-stu-id="8e399-154">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e399-155"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="8e399-155"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="8e399-156">Sí</span><span class="sxs-lookup"><span data-stu-id="8e399-156">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e399-157"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="8e399-157"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="8e399-158">Sí</span><span class="sxs-lookup"><span data-stu-id="8e399-158">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e399-159"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="8e399-159"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="8e399-160">No</span><span class="sxs-lookup"><span data-stu-id="8e399-160">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e399-161"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="8e399-161"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="8e399-162">No</span><span class="sxs-lookup"><span data-stu-id="8e399-162">No</span></span></p></td>
</tr>
</tbody>
</table>

