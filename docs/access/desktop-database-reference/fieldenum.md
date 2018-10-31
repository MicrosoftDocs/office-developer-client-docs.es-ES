---
title: FieldEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 9ab46fc7c3817cbfa83c78816a42472e425d2d71
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860052"
---
# <a name="fieldenum"></a><span data-ttu-id="f53cd-102">FieldEnum</span><span class="sxs-lookup"><span data-stu-id="f53cd-102">FieldEnum</span></span>

<span data-ttu-id="f53cd-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f53cd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f53cd-104">Especifica los campos especiales a los que se hace referencia en la colección [Fields](record-object-ado.md) de un objeto [Record](fields-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f53cd-104">Specifies the special fields referenced in a [Record](record-object-ado.md) object's [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="f53cd-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f53cd-105">Remarks</span></span>

<span data-ttu-id="f53cd-p101">Estas constantes proporcionan "métodos abreviados" para obtener acceso a campos especiales asociados a un **Record**. Recupere el objeto [Field](field-object-ado.md) de la colección **Fields** y, a continuación, obtenga su contenido con la propiedad **Value** del objeto [Field](value-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f53cd-p101">These constants provide a "shortcut" to accessing special fields associated with a **Record**. Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f53cd-108">Constante</span><span class="sxs-lookup"><span data-stu-id="f53cd-108">Constant</span></span></p></th>
<th><p><span data-ttu-id="f53cd-109">Valor</span><span class="sxs-lookup"><span data-stu-id="f53cd-109">Value</span></span></p></th>
<th><p><span data-ttu-id="f53cd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f53cd-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f53cd-111"><strong>adDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="f53cd-111"><strong>adDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="f53cd-112">-1</span><span class="sxs-lookup"><span data-stu-id="f53cd-112">-1</span></span></p></td>
<td><p><span data-ttu-id="f53cd-113">Hace referencia al campo que contiene el objeto <a href="stream-object-ado.md">Stream</a> predeterminado asociado a un <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="f53cd-113">References the field containing the default <a href="stream-object-ado.md">Stream</a> object associated with a <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f53cd-114"><strong>adRecordURL</strong></span><span class="sxs-lookup"><span data-stu-id="f53cd-114"><strong>adRecordURL</strong></span></span></p></td>
<td><p><span data-ttu-id="f53cd-115">-2</span><span class="sxs-lookup"><span data-stu-id="f53cd-115">-2</span></span></p></td>
<td><p><span data-ttu-id="f53cd-116">Hace referencia al campo que contiene la cadena URL absoluta para el <strong>Record</strong> actual.</span><span class="sxs-lookup"><span data-stu-id="f53cd-116">References the field containing the absolute URL string for the current <strong>Record</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

