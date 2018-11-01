---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3cd855adb62a1b97f99cdc34a9c27ee539ab1c2b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884225"
---
# <a name="recordcreateoptionsenum"></a><span data-ttu-id="165d3-102">RecordCreateOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="165d3-102">RecordCreateOptionsEnum</span></span>


<span data-ttu-id="165d3-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="165d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="165d3-p101">Especifica si se debe abrir un **Record** existente o crear un **Record** nuevo para el método [Open](record-object-ado.md) del objeto [Record](open-method-ado-record.md). Los valores se pueden combinar con un operador AND.</span><span class="sxs-lookup"><span data-stu-id="165d3-p101">Specifies whether an existing **Record** should be opened or a new **Record** created for the [Record](record-object-ado.md) object [Open](open-method-ado-record.md) method. The values can be combined with an AND operator.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="165d3-106">Constante</span><span class="sxs-lookup"><span data-stu-id="165d3-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="165d3-107">Valor</span><span class="sxs-lookup"><span data-stu-id="165d3-107">Value</span></span></p></th>
<th><p><span data-ttu-id="165d3-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="165d3-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="165d3-109"><strong>adCreateCollection</strong></span><span class="sxs-lookup"><span data-stu-id="165d3-109"><strong>adCreateCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="165d3-110">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="165d3-110">0x2000</span></span></p></td>
<td><p><span data-ttu-id="165d3-p102">Crea un <strong>Record</strong> nuevo en el nodo especificado por parámetro <em>Source</em> en lugar de abrir un <strong>Record</strong> existente. Si el origen apunta a un nodo existente, se produce un error de tiempo de ejecución, a menos que <strong>adCreateCollection</strong> se combine con <strong>adOpenIfExists</strong> o <strong>adCreateOverwrite</strong>.</span><span class="sxs-lookup"><span data-stu-id="165d3-p102">Creates a new <strong>Record</strong> at the node specified by <em>Source</em> parameter, instead of opening an existing <strong>Record</strong>. If the source points to an existing node, then a run-time error occurs, unless <strong>adCreateCollection</strong> is combined with <strong>adOpenIfExists</strong> or <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="165d3-113"><strong>adCreateNonCollection</strong></span><span class="sxs-lookup"><span data-stu-id="165d3-113"><strong>adCreateNonCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="165d3-114">0</span><span class="sxs-lookup"><span data-stu-id="165d3-114">0</span></span></p></td>
<td><p><span data-ttu-id="165d3-115">Crea un <strong>Record</strong> nuevo de tipo <a href="recordtypeenum.md">adSimpleRecord</a>.</span><span class="sxs-lookup"><span data-stu-id="165d3-115">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adSimpleRecord</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="165d3-116"><strong>adCreateOverwrite</strong></span><span class="sxs-lookup"><span data-stu-id="165d3-116"><strong>adCreateOverwrite</strong></span></span></p></td>
<td><p><span data-ttu-id="165d3-117">0x4000000</span><span class="sxs-lookup"><span data-stu-id="165d3-117">0x4000000</span></span></p></td>
<td><p><span data-ttu-id="165d3-p103">Modifica las marcas de creación <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong> y <strong>adCreateStructDoc</strong>. Cuando se usa el operador OR con este valor y uno de los valores de marca de creación, si la dirección URL de origen apunta a un nodo o <strong>Record</strong> existente, entonces el <strong>Record</strong> se sobrescribe y se crea uno nuevo en su lugar. Este valor no se puede usar junto con <strong>adOpenIfExists</strong>.</span><span class="sxs-lookup"><span data-stu-id="165d3-p103">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>. When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong>, then the existing <strong>Record</strong> is overwritten and a new one is created in its place. This value cannot be used together with <strong>adOpenIfExists</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="165d3-121"><strong>adCreateStructDoc</strong></span><span class="sxs-lookup"><span data-stu-id="165d3-121"><strong>adCreateStructDoc</strong></span></span></p></td>
<td><p><span data-ttu-id="165d3-122">0x80000000</span><span class="sxs-lookup"><span data-stu-id="165d3-122">0x80000000</span></span></p></td>
<td><p><span data-ttu-id="165d3-123">Crea un <strong>Record</strong> nuevo de tipo <a href="recordtypeenum.md">adStructDoc</a>, en lugar de abrir un <strong>Record</strong> existente.</span><span class="sxs-lookup"><span data-stu-id="165d3-123">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adStructDoc</a>, instead of opening an existing <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="165d3-124"><strong>adFailIfNotExists</strong></span><span class="sxs-lookup"><span data-stu-id="165d3-124"><strong>adFailIfNotExists</strong></span></span></p></td>
<td><p><span data-ttu-id="165d3-125">-1</span><span class="sxs-lookup"><span data-stu-id="165d3-125">-1</span></span></p></td>
<td><p><span data-ttu-id="165d3-p104">Valor predeterminado. Produce un error de tiempo de ejecución si <em>Source</em> apunta a un nodo inexistente.</span><span class="sxs-lookup"><span data-stu-id="165d3-p104">Default. Results in a run-time error if <em>Source</em> points to a non-existent node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="165d3-128"><strong>adOpenIfExists</strong></span><span class="sxs-lookup"><span data-stu-id="165d3-128"><strong>adOpenIfExists</strong></span></span></p></td>
<td><p><span data-ttu-id="165d3-129">0x2000000</span><span class="sxs-lookup"><span data-stu-id="165d3-129">0x2000000</span></span></p></td>
<td><p><span data-ttu-id="165d3-p105">Modifica las marcas de creación <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong> y <strong>adCreateStructDoc</strong>. Cuando se usa el operador OR con este valor y uno de los valores de marca de creación, si la dirección URL de origen apunta a un nodo o un objeto <strong>Record</strong> existente, entonces el proveedor debe abrir el <strong>Record</strong> existente en lugar de crear uno nuevo. Este valor no se puede usar junto con <strong>adCreateOverwrite</strong>.</span><span class="sxs-lookup"><span data-stu-id="165d3-p105">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>. When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong> object, then the provider must open the existing <strong>Record</strong> instead of creating a new one. This value cannot be used together with <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="165d3-133">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="165d3-133">ADO/WFC equivalent</span></span>

<span data-ttu-id="165d3-134">Estas constantes no tienen equivalentes ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="165d3-134">These constants do not have ADO/WFC equivalents.</span></span>

