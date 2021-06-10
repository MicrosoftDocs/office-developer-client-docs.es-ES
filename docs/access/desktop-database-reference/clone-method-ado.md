---
title: 'Clone (método): ActiveX data objects (ADO)'
TOCTitle: Clone method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 095191bbfe55f2c38529cb1c260979c48dd2d5f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296349"
---
# <a name="clone-method-ado"></a><span data-ttu-id="c1be4-102">Método Clone (ADO)</span><span class="sxs-lookup"><span data-stu-id="c1be4-102">Clone method (ADO)</span></span>

<span data-ttu-id="c1be4-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c1be4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c1be4-p101">Crea un objeto [Recordset](recordset-object-ado.md) duplicado a partir de un objeto **Recordset** existente. Opcionalmente, especifica que el duplicado es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c1be4-p101">Creates a duplicate [Recordset](recordset-object-ado.md) object from an existing **Recordset** object. Optionally, specifies that the clone be read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1be4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1be4-106">Syntax</span></span>

<span data-ttu-id="c1be4-107">**Set** *rstDuplicate*  =  *rstOriginal*. Clone (*LockType*)</span><span class="sxs-lookup"><span data-stu-id="c1be4-107">**Set** *rstDuplicate* = *rstOriginal*.Clone (*LockType*)</span></span>

## <a name="return-value"></a><span data-ttu-id="c1be4-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1be4-108">Return value</span></span>

<span data-ttu-id="c1be4-109">Devuelve una referencia al objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c1be4-109">Returns a **Recordset** object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="c1be4-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1be4-110">Parameters</span></span>

|<span data-ttu-id="c1be4-111">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c1be4-111">Parameter</span></span>|<span data-ttu-id="c1be4-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1be4-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c1be4-113">*rstDuplicate*</span><span class="sxs-lookup"><span data-stu-id="c1be4-113">*rstDuplicate*</span></span> |<span data-ttu-id="c1be4-114">Una variable de objeto que identifica el objeto **Recordset** duplicado que se creará.</span><span class="sxs-lookup"><span data-stu-id="c1be4-114">An object variable that identifies the duplicate **Recordset** object to be created.</span></span>|
|<span data-ttu-id="c1be4-115">*rstOriginal*</span><span class="sxs-lookup"><span data-stu-id="c1be4-115">*rstOriginal*</span></span> |<span data-ttu-id="c1be4-116">Una variable de objeto que identifica el objeto **Recordset** duplicado.</span><span class="sxs-lookup"><span data-stu-id="c1be4-116">An object variable that identifies the **Recordset** object to be duplicated.</span></span>|
|<span data-ttu-id="c1be4-117">*LockType*</span><span class="sxs-lookup"><span data-stu-id="c1be4-117">*LockType*</span></span> |<span data-ttu-id="c1be4-p102">Opcional. Valor de [LockTypeEnum](locktypeenum.md) que especifica el tipo de bloqueo del objeto **Recordset** original, o bien un **Recordset** de sólo lectura. Los valores válidos son **adLockUnspecified** o **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="c1be4-p102">Optional. A [LockTypeEnum](locktypeenum.md) value that specifies either the lock type of the original **Recordset**, or a read-only **Recordset**. Valid values are **adLockUnspecified** or **adLockReadOnly**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c1be4-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1be4-121">Remarks</span></span>

<span data-ttu-id="c1be4-p103">Use el método **Clone** para crear varios objetos **Recordset** duplicados, sobre todo si desea mantener más de un registro actual en un conjunto determinado de registros. El método **Clone** es más eficaz que crear y abrir un nuevo objeto **Recordset** con la misma definición que el original.</span><span class="sxs-lookup"><span data-stu-id="c1be4-p103">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records. Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="c1be4-p104">La propiedad [Filter](filter-property-ado.md) del objeto **Recordset** original, si hay alguna, no se aplicarán a la copia. Establezca la propiedad **Filter** del nuevo **objeto Recordset** para filtrar los resultados. La forma más sencilla para copiar cualquier valor de **filtro** existente es asignarlo directamente, similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="c1be4-p104">The [Filter](filter-property-ado.md) property of the original **Recordset**, if any, will not be applied to the clone. Set the **Filter** property of the new **Recordset** in order to filter the results. The simplest way to copy any existing **Filter** value is to assign it directly, like this:</span></span>

<span data-ttu-id="c1be4-127">El registro actual de un clon recién creado se establece en el primer registro.</span><span class="sxs-lookup"><span data-stu-id="c1be4-127">The current record of a newly created clone is set to the first record.</span></span>

<span data-ttu-id="c1be4-p105">Los cambios realizados en un objeto **Recordset** se ven en todos sus duplicados, independientemente del tipo de cursor. Sin embargo, después de ejecutar [Requery](requery-method-ado.md) en el objeto **Recordset** original, los duplicados ya no estarán sincronizados con el original.</span><span class="sxs-lookup"><span data-stu-id="c1be4-p105">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type. However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="c1be4-130">Al cerrar el objeto **Recordset** original, no se cierran sus copias; como tampoco se cierra el original ni ninguna de las demás copias al cerrarse una copia.</span><span class="sxs-lookup"><span data-stu-id="c1be4-130">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="c1be4-p106">Sólo se puede duplicar un objeto **Recordset** que admite marcadores. Los valores de marcador son intercambiables; es decir, una referencia de marcador de un objeto **Recordset** hace referencia al mismo registro en todos sus duplicados.</span><span class="sxs-lookup"><span data-stu-id="c1be4-p106">You can only clone a **Recordset** object that supports bookmarks. Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

<span data-ttu-id="c1be4-p107">Algunos de los eventos de **Recordset** también se desencadenan en todos los duplicados de **Recordset**. Sin embargo, dado que el registro actual puede diferir entre clonada **conjuntos de registros**, los eventos no sea válidos para el duplicado.</span><span class="sxs-lookup"><span data-stu-id="c1be4-p107">Some **Recordset** events that are triggered will also fire in all **Recordset** clones. However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span></span>

<span data-ttu-id="c1be4-135">Por ejemplo, si cambia un valor de un campo, se producirá un evento [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) en el **objeto Recordset** modificado y en todos los duplicados.</span><span class="sxs-lookup"><span data-stu-id="c1be4-135">For example, if you change a value of a field, a [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) event will occur in the changed **Recordset** and in all clones.</span></span> <span data-ttu-id="c1be4-136">El parámetro *Fields* del evento **WillChangeField** de un **objeto Recordset** clonado (donde no se realizó el cambio) se referirá simplemente a los campos del registro actual del clon, que puede ser un registro diferente al registro actual del objeto **Recordset** original donde se produjo el cambio.</span><span class="sxs-lookup"><span data-stu-id="c1be4-136">The *Fields* parameter of the **WillChangeField** event of a cloned **Recordset** (where the change was not made) will simply refer to the fields of the current record of the clone, which may be a different record than the current record of the original **Recordset** where the change occurred.</span></span>

<span data-ttu-id="c1be4-137">La siguiente tabla recoge una lista completa de todos los eventos de **conjunto de registros** y se indica si son válidas y desencadenadas para cualquier generados mediante el método **Clone** los duplicados de recordset.</span><span class="sxs-lookup"><span data-stu-id="c1be4-137">The following table provided a full listing of all **Recordset** events and indicates whether they are valid and triggered for any recordset clones generated using the **Clone** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c1be4-138">Evento</span><span class="sxs-lookup"><span data-stu-id="c1be4-138">Event</span></span></p></th>
<th><p><span data-ttu-id="c1be4-139">¿Se desencadena en los duplicados?</span><span class="sxs-lookup"><span data-stu-id="c1be4-139">Triggered in clones?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1be4-140"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="c1be4-140"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="c1be4-141">No</span><span class="sxs-lookup"><span data-stu-id="c1be4-141">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1be4-142"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="c1be4-142"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="c1be4-143">No</span><span class="sxs-lookup"><span data-stu-id="c1be4-143">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1be4-144"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="c1be4-144"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="c1be4-145">No</span><span class="sxs-lookup"><span data-stu-id="c1be4-145">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1be4-146"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="c1be4-146"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="c1be4-147">Sí</span><span class="sxs-lookup"><span data-stu-id="c1be4-147">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1be4-148"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="c1be4-148"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="c1be4-149">No</span><span class="sxs-lookup"><span data-stu-id="c1be4-149">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1be4-150"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="c1be4-150"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="c1be4-151">Sí</span><span class="sxs-lookup"><span data-stu-id="c1be4-151">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1be4-152"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="c1be4-152"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="c1be4-153">No</span><span class="sxs-lookup"><span data-stu-id="c1be4-153">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1be4-154"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="c1be4-154"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="c1be4-155">Sí</span><span class="sxs-lookup"><span data-stu-id="c1be4-155">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1be4-156"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="c1be4-156"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="c1be4-157">Sí</span><span class="sxs-lookup"><span data-stu-id="c1be4-157">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1be4-158"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="c1be4-158"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="c1be4-159">No</span><span class="sxs-lookup"><span data-stu-id="c1be4-159">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1be4-160"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="c1be4-160"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="c1be4-161">No</span><span class="sxs-lookup"><span data-stu-id="c1be4-161">No</span></span></p></td>
</tr>
</tbody>
</table>

