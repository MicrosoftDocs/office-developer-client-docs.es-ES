---
title: Clone (método) - ActiveX Data Objects (ADO)
TOCTitle: Clone method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 17284fd61c44fe17f1c2661eff204c8827bf8e80
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922345"
---
# <a name="clone-method-ado"></a>Clone (método, ADO)


**Se aplica a**: Access 2013, Office 2013



Crea un objeto [Recordset](recordset-object-ado.md) duplicado a partir de un objeto **Recordset** existente. Opcionalmente, especifica que el duplicado es de solo lectura.

## <a name="syntax"></a>Sintaxis

**Establecer** *rstDuplicate*  =  *rstOriginal*. Clone (*LockType*)

## <a name="return-value"></a>Valor devuelto

Devuelve una referencia al objeto **Recordset**.

## <a name="parameters"></a>Sintaxis

  - *rstDuplicate*

  - Una variable de objeto que identifica el objeto **Recordset** duplicado que se creará.

  - *rstOriginal*

  - Una variable de objeto que identifica el objeto **Recordset** duplicado.

  - *LockType*

  - Opcional. Valor de [LockTypeEnum](locktypeenum.md) que especifica el tipo de bloqueo del objeto **Recordset** original, o bien un **Recordset** de sólo lectura. Los valores válidos son **adLockUnspecified** o **adLockReadOnly**.

## <a name="remarks"></a>Comentarios

Use el método **Clone** para crear varios objetos **Recordset** duplicados, sobre todo si desea mantener más de un registro actual en un conjunto determinado de registros. El método **Clone** es más eficaz que crear y abrir un nuevo objeto **Recordset** con la misma definición que el original.

La propiedad [Filter](filter-property-ado.md) del objeto **Recordset** original, si hay alguna, no se aplicarán a la copia. Establezca la propiedad **Filter** del nuevo **objeto Recordset** para filtrar los resultados. La forma más sencilla para copiar cualquier valor de **filtro** existente es asignarlo directamente, similar a la siguiente:

El registro actual de un clon recién creado se establece en el primer registro.

Los cambios realizados en un objeto **Recordset** se ven en todos sus duplicados, independientemente del tipo de cursor. Sin embargo, después de ejecutar [Requery](requery-method-ado.md) en el objeto **Recordset** original, los duplicados ya no estarán sincronizados con el original.

Al cerrar el objeto **Recordset** original, no se cierran sus copias; como tampoco se cierra el original ni ninguna de las demás copias al cerrarse una copia.

Sólo se puede duplicar un objeto **Recordset** que admite marcadores. Los valores de marcador son intercambiables; es decir, una referencia de marcador de un objeto **Recordset** hace referencia al mismo registro en todos sus duplicados.

Algunos de los eventos de **Recordset** también se desencadenan en todos los duplicados de **Recordset**. Sin embargo, dado que el registro actual puede diferir entre clonada **conjuntos de registros**, los eventos no sea válidos para el duplicado.

Por ejemplo, si cambia un valor de un campo, se producirá un evento [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) en el **objeto Recordset** modificado y en todos los duplicados. El parámetro *Fields* del evento **WillChangeField** de un clonado **Recordset** (donde no se ha realizado el cambio) hará simplemente referencia a los campos del actual registro del duplicado, el cual puede ser diferente del actual registro de la original **Recordset** donde se produjo el cambio.

La siguiente tabla recoge una lista completa de todos los eventos de **conjunto de registros** y se indica si son válidas y desencadenadas para cualquier generados mediante el método **Clone** los duplicados de recordset.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Evento</p></th>
<th><p>¿Se desencadena en los duplicados?</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="endofrecordset-event-ado.md">EndOfRecordset</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p><a href="fetchcomplete-event-ado.md">FetchComplete</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></p></td>
<td><p>No</p></td>
</tr>
</tbody>
</table>

