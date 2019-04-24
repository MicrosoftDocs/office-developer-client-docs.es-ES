---
title: Van (referencia de base de datos de escritorio de Access)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4d9c96a7bb34fe0ab3512a316a92e1f7a01ef4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314724"
---
# <a name="streamreadenum"></a><span data-ttu-id="9c8ae-102">StreamReadEnum</span><span class="sxs-lookup"><span data-stu-id="9c8ae-102">StreamReadEnum</span></span>

<span data-ttu-id="9c8ae-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9c8ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9c8ae-104">Especifica si se debe leer toda la secuencia o sólo la línea siguiente de un objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9c8ae-104">Specifies whether the whole stream or the next line should be read from a [Stream](stream-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9c8ae-105">Constante</span><span class="sxs-lookup"><span data-stu-id="9c8ae-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="9c8ae-106">Valor</span><span class="sxs-lookup"><span data-stu-id="9c8ae-106">Value</span></span></p></th>
<th><p><span data-ttu-id="9c8ae-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c8ae-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c8ae-108"><strong>adReadAll</strong></span><span class="sxs-lookup"><span data-stu-id="9c8ae-108"><strong>adReadAll</strong></span></span></p></td>
<td><p><span data-ttu-id="9c8ae-109">-1</span><span class="sxs-lookup"><span data-stu-id="9c8ae-109">-1</span></span></p></td>
<td><p><span data-ttu-id="9c8ae-p101">Valor predeterminado. Se leen todos los bytes de la secuencia, desde la posición actual hasta el marcador <a href="eos-property-ado.md">EOS</a>. Éste es el único valor válido de <strong>StreamReadEnum</strong> para secuencias binarias (que es <a href="type-property-ado-stream.md">Type</a> es <strong>adTypeBinary</strong>).</span><span class="sxs-lookup"><span data-stu-id="9c8ae-p101">Default. Reads all bytes from the stream, from the current position onwards to the <a href="eos-property-ado.md">EOS</a> marker. This is the only valid <strong>StreamReadEnum</strong> value with binary streams (<a href="type-property-ado-stream.md">Type</a> is <strong>adTypeBinary</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c8ae-113"><strong>adReadLine</strong></span><span class="sxs-lookup"><span data-stu-id="9c8ae-113"><strong>adReadLine</strong></span></span></p></td>
<td><p><span data-ttu-id="9c8ae-114">-2</span><span class="sxs-lookup"><span data-stu-id="9c8ae-114">-2</span></span></p></td>
<td><p><span data-ttu-id="9c8ae-115">Se lee la línea siguiente de la secuencia (determinada por la propiedad <a href="lineseparator-property-ado.md">LineSeparator</a>).</span><span class="sxs-lookup"><span data-stu-id="9c8ae-115">Reads the next line from the stream (designated by the <a href="lineseparator-property-ado.md">LineSeparator</a> property).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="9c8ae-116">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="9c8ae-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="9c8ae-117">Estas constantes no tienen equivalentes ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="9c8ae-117">These constants do not have ADO/WFC equivalents.</span></span>

