---
title: FieldEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 6975017ed8867d794dce189de74f617636b9f223
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886665"
---
# <a name="fieldenum"></a><span data-ttu-id="0fc71-102">FieldEnum</span><span class="sxs-lookup"><span data-stu-id="0fc71-102">FieldEnum</span></span>

<span data-ttu-id="0fc71-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0fc71-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0fc71-104">Especifica los campos especiales a los que se hace referencia en la colección [Fields](record-object-ado.md) de un objeto [Record](fields-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0fc71-104">Specifies the special fields referenced in a [Record](record-object-ado.md) object's [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fc71-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0fc71-105">Remarks</span></span>

<span data-ttu-id="0fc71-p101">Estas constantes proporcionan "métodos abreviados" para obtener acceso a campos especiales asociados a un **Record**. Recupere el objeto [Field](field-object-ado.md) de la colección **Fields** y, a continuación, obtenga su contenido con la propiedad **Value** del objeto [Field](value-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0fc71-p101">These constants provide a "shortcut" to accessing special fields associated with a **Record**. Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0fc71-108">Constante</span><span class="sxs-lookup"><span data-stu-id="0fc71-108">Constant</span></span></p></th>
<th><p><span data-ttu-id="0fc71-109">Valor</span><span class="sxs-lookup"><span data-stu-id="0fc71-109">Value</span></span></p></th>
<th><p><span data-ttu-id="0fc71-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fc71-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0fc71-111"><strong>adDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="0fc71-111"><strong>adDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="0fc71-112">-1</span><span class="sxs-lookup"><span data-stu-id="0fc71-112">-1</span></span></p></td>
<td><p><span data-ttu-id="0fc71-113">Hace referencia al campo que contiene el objeto <a href="stream-object-ado.md">Stream</a> predeterminado asociado a un <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="0fc71-113">References the field containing the default <a href="stream-object-ado.md">Stream</a> object associated with a <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fc71-114"><strong>adRecordURL</strong></span><span class="sxs-lookup"><span data-stu-id="0fc71-114"><strong>adRecordURL</strong></span></span></p></td>
<td><p><span data-ttu-id="0fc71-115">-2</span><span class="sxs-lookup"><span data-stu-id="0fc71-115">-2</span></span></p></td>
<td><p><span data-ttu-id="0fc71-116">Hace referencia al campo que contiene la cadena URL absoluta para el <strong>Record</strong> actual.</span><span class="sxs-lookup"><span data-stu-id="0fc71-116">References the field containing the absolute URL string for the current <strong>Record</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

