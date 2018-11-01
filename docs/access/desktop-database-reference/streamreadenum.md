---
title: StreamReadEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 665819da2a2d31068e50e91eafdddc083645f443
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872714"
---
# <a name="streamreadenum"></a><span data-ttu-id="e5e01-102">StreamReadEnum</span><span class="sxs-lookup"><span data-stu-id="e5e01-102">StreamReadEnum</span></span>

<span data-ttu-id="e5e01-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5e01-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e5e01-104">Especifica si se debe leer toda la secuencia o sólo la línea siguiente de un objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e5e01-104">Specifies whether the whole stream or the next line should be read from a [Stream](stream-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e5e01-105">Constante</span><span class="sxs-lookup"><span data-stu-id="e5e01-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e5e01-106">Valor</span><span class="sxs-lookup"><span data-stu-id="e5e01-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e5e01-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5e01-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e5e01-108"><strong>adReadAll</strong></span><span class="sxs-lookup"><span data-stu-id="e5e01-108"><strong>adReadAll</strong></span></span></p></td>
<td><p><span data-ttu-id="e5e01-109">-1</span><span class="sxs-lookup"><span data-stu-id="e5e01-109">-1</span></span></p></td>
<td><p><span data-ttu-id="e5e01-p101">Valor predeterminado. Se leen todos los bytes de la secuencia, desde la posición actual hasta el marcador <a href="eos-property-ado.md">EOS</a>. Éste es el único valor válido de <strong>StreamReadEnum</strong> para secuencias binarias (que es <a href="type-property-ado-stream.md">Type</a> es <strong>adTypeBinary</strong>).</span><span class="sxs-lookup"><span data-stu-id="e5e01-p101">Default. Reads all bytes from the stream, from the current position onwards to the <a href="eos-property-ado.md">EOS</a> marker. This is the only valid <strong>StreamReadEnum</strong> value with binary streams (<a href="type-property-ado-stream.md">Type</a> is <strong>adTypeBinary</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5e01-113"><strong>adReadLine</strong></span><span class="sxs-lookup"><span data-stu-id="e5e01-113"><strong>adReadLine</strong></span></span></p></td>
<td><p><span data-ttu-id="e5e01-114">-2</span><span class="sxs-lookup"><span data-stu-id="e5e01-114">-2</span></span></p></td>
<td><p><span data-ttu-id="e5e01-115">Se lee la línea siguiente de la secuencia (determinada por la propiedad <a href="lineseparator-property-ado.md">LineSeparator</a>).</span><span class="sxs-lookup"><span data-stu-id="e5e01-115">Reads the next line from the stream (designated by the <a href="lineseparator-property-ado.md">LineSeparator</a> property).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="e5e01-116">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="e5e01-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="e5e01-117">Estas constantes no tienen equivalentes ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="e5e01-117">These constants do not have ADO/WFC equivalents.</span></span>

