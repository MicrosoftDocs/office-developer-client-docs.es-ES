---
title: CursorType (propiedad, ADO)
TOCTitle: CursorType property (ADO)
ms:assetid: f42ded8f-9f92-ef03-a198-ffb892324611
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250239(v=office.15)
ms:contentKeyID: 48548682
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d9560ad975d545015a02bb0e594777ced3cc8d3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886661"
---
# <a name="cursortype-property-ado"></a>CursorType (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

Indica el tipo de cursor que se usa en un objeto [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo [CursorTypeEnum](cursortypeenum.md). El valor predeterminado es **adOpenForwardOnly**.

## <a name="remarks"></a>Comentarios

Use la propiedad **CursorType** para especificar el tipo de cursor que se va a usar cuando se abra el objeto **Recordset**.

Sólo se admite el valor **adOpenStatic** si la propiedad [CursorLocation](cursorlocation-property-ado.md) tiene el valor **adUseClient**. Si se establece un valor no admitido, no se generará ningún error sino que se utilizará el valor de **CursorType** admitido más próximo.

Si un proveedor no admite el tipo de cursor solicitado, puede que devuelva otro tipo de cursor. El valor de la propiedad **CursorType** cambia para que coincida con el tipo de cursor que se usa realmente cuando está abierto el objeto [Recordset](recordset-object-ado.md). Para comprobar la funcionalidad específica del cursor devuelto, use el método [Supports](supports-method-ado.md). Tras cerrarse el objeto **Recordset**, se restablece el valor original de la propiedad **CursorType**.

En el gráfico siguiente se muestra la funcionalidad (identificada mediante las constantes del método **Supports** ) del proveedor que se requiere para cada tipo de cursor.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Para un objeto Recordset con este valor de CursorType</p></th>
<th><p>El método Supports debe devolver True para todas estas constantes</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>ninguno</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p><strong>adMovePrevious</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> Si bien el método **Supports**(**adUpdateBatch**) puede tener el valor True para los cursores dinámicos y de sólo avance, para las actualizaciones por lotes se debe usar un cursor estático o un cursor de conjunto de claves. Establezca el valor de la propiedad [LockType](locktype-property-ado.md) en **adLockBatchOptimistic** y el valor de la propiedad **CursorLocation** en **adUseClient** para habilitar el Servicio de cursores para OLE DB, que se requiere para las actualizaciones por lotes.

La propiedad **CursorType** es de lectura y escritura cuando el objeto **Recordset** está cerrado, y es de sólo lectura cuando está abierto.

**Uso de servicio de datos remotos** Cuando se usa en un objeto Recordset de cliente, la propiedad **CursorType** puede establecerse sólo en **adOpenStatic**.

