---
title: FieldEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e42dcfe63194364986e5b235c59b011231307a7c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726088"
---
# <a name="fieldenum"></a><span data-ttu-id="5c566-102">FieldEnum</span><span class="sxs-lookup"><span data-stu-id="5c566-102">FieldEnum</span></span>

<span data-ttu-id="5c566-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c566-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5c566-104">Especifica los campos especiales a los que se hace referencia en la colección [Fields](record-object-ado.md) de un objeto [Record](fields-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5c566-104">Specifies the special fields referenced in a [Record](record-object-ado.md) object's [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c566-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c566-105">Remarks</span></span>

<span data-ttu-id="5c566-p101">Estas constantes proporcionan "métodos abreviados" para obtener acceso a campos especiales asociados a un **Record**. Recupere el objeto [Field](field-object-ado.md) de la colección **Fields** y, a continuación, obtenga su contenido con la propiedad **Value** del objeto [Field](value-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5c566-p101">These constants provide a "shortcut" to accessing special fields associated with a **Record**. Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c566-108">Constante</span><span class="sxs-lookup"><span data-stu-id="5c566-108">Constant</span></span></p></th>
<th><p><span data-ttu-id="5c566-109">Valor</span><span class="sxs-lookup"><span data-stu-id="5c566-109">Value</span></span></p></th>
<th><p><span data-ttu-id="5c566-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c566-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c566-111"><strong>adDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="5c566-111"><strong>adDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="5c566-112">-1</span><span class="sxs-lookup"><span data-stu-id="5c566-112">-1</span></span></p></td>
<td><p><span data-ttu-id="5c566-113">Hace referencia al campo que contiene el objeto <a href="stream-object-ado.md">Stream</a> predeterminado asociado a un <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="5c566-113">References the field containing the default <a href="stream-object-ado.md">Stream</a> object associated with a <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c566-114"><strong>adRecordURL</strong></span><span class="sxs-lookup"><span data-stu-id="5c566-114"><strong>adRecordURL</strong></span></span></p></td>
<td><p><span data-ttu-id="5c566-115">-2</span><span class="sxs-lookup"><span data-stu-id="5c566-115">-2</span></span></p></td>
<td><p><span data-ttu-id="5c566-116">Hace referencia al campo que contiene la cadena URL absoluta para el <strong>Record</strong> actual.</span><span class="sxs-lookup"><span data-stu-id="5c566-116">References the field containing the absolute URL string for the current <strong>Record</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

