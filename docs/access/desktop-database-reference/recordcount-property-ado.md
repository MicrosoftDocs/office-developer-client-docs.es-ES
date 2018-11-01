---
title: RecordCount (propiedad, ADO)
TOCTitle: RecordCount property (ADO)
ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15)
ms:contentKeyID: 48548304
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41fb9d8bdcb626fefe2e98fe4c1849554a73a6c3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876165"
---
# <a name="recordcount-property-ado"></a><span data-ttu-id="9737f-102">RecordCount (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="9737f-102">RecordCount property (ADO)</span></span>


<span data-ttu-id="9737f-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9737f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9737f-104">Indica el número de registros de un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9737f-104">Indicates the number of records in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="9737f-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9737f-105">Return value</span></span>

<span data-ttu-id="9737f-106">Devuelve un valor de tipo **Long** que indica el número de registros del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9737f-106">Returns a **Long** value that indicates the number of records in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9737f-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9737f-107">Remarks</span></span>

<span data-ttu-id="9737f-p101">Use la propiedad **RecordCount** para descubrir cuántos registros hay en un objeto **Recordset**. La propiedad devuelve -1 cuando ADO no puede determinar el número de registros o si el proveedor o el tipo de cursor no admite la propiedad **RecordCount**. Al leer la propiedad **RecordCount** en un objeto **Recordset** cerrado se produce un error.</span><span class="sxs-lookup"><span data-stu-id="9737f-p101">Use the **RecordCount** property to find out how many records are in a **Recordset** object. The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**. Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="9737f-p102">Si el objeto **Recordset** es compatible con un posicionamiento aproximado o con marcadores, es decir, **Supports (adApproxPosition)** o **Supports (adBookmark)** devuelven respectivamente **True**, este valor será el número exacto de registros en el objeto **Recordset**, independientemente de si se ha rellenado por completo. Si el objeto **Recordset** no es compatible con un posicionamiento aproximado, esta propiedad puede suponer una considerable pérdida de recursos, dado que será necesario recuperar y contar todos los registros para devolver un valor de **RecordCount** preciso.</span><span class="sxs-lookup"><span data-stu-id="9737f-p102">If the **Recordset** object supports approximate positioning or bookmarks — that is, **Supports (adApproxPosition)** or **Supports (adBookmark)**, respectively, return **True** — this value will be the exact number of records in the **Recordset**, regardless of whether it has been fully populated. If the **Recordset** object does not support approximate positioning, this property may be a significant drain on resources because all records will have to be retrieved and counted to return an accurate **RecordCount** value.</span></span>

<span data-ttu-id="9737f-p103">El tipo de cursor del objeto **Recordset** afecta a la posibilidad de determinar el número de registros. La propiedad **RecordCount** devolverá -1 para un cursor de sólo avance, el recuento real para un cursor estático o de conjunto de claves y -1 o el recuento real para un cursor dinámico, según el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="9737f-p103">The cursor type of the **Recordset** object affects whether the number of records can be determined. The **RecordCount** property will return -1 for a forward-only cursor; the actual count for a static or keyset cursor; and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

