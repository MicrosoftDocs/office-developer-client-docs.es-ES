---
title: StreamWriteEnum (referencia de base de datos de escritorio de Access)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 87144e5409fb54cf0cb8f59ad4d593ab05d694a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308480"
---
# <a name="streamwriteenum"></a><span data-ttu-id="c8930-102">StreamWriteEnum</span><span class="sxs-lookup"><span data-stu-id="c8930-102">StreamWriteEnum</span></span>

<span data-ttu-id="c8930-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8930-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c8930-104">Especifica si se agrega un separador de línea a la cadena escrita en un objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c8930-104">Specifies whether a line separator is appended to the string written to a [Stream](stream-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c8930-105">Constante</span><span class="sxs-lookup"><span data-stu-id="c8930-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c8930-106">Valor</span><span class="sxs-lookup"><span data-stu-id="c8930-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c8930-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8930-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8930-108"><strong>adWriteChar</strong></span><span class="sxs-lookup"><span data-stu-id="c8930-108"><strong>adWriteChar</strong></span></span></p></td>
<td><p><span data-ttu-id="c8930-109">0</span><span class="sxs-lookup"><span data-stu-id="c8930-109">0</span></span></p></td>
<td><p><span data-ttu-id="c8930-p101">Valor predeterminado. Se escribe la cadena de texto (especificada por el parámetro <em>Data</em>) en el objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="c8930-p101">Default. Writes the specified text string (specified by the <em>Data</em> parameter) to the <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8930-112"><strong>adWriteLine</strong></span><span class="sxs-lookup"><span data-stu-id="c8930-112"><strong>adWriteLine</strong></span></span></p></td>
<td><p><span data-ttu-id="c8930-113">1 </span><span class="sxs-lookup"><span data-stu-id="c8930-113">1</span></span></p></td>
<td><p><span data-ttu-id="c8930-p102">Escribe una cadena de texto y un carácter separador de línea en un objeto <strong>Stream</strong>. Si la propiedad <a href="lineseparator-property-ado.md">LineSeparator</a> no está definida, se devuelve un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="c8930-p102">Writes a text string and a line separator character to a <strong>Stream</strong> object. If the <a href="lineseparator-property-ado.md">LineSeparator</a> property is not defined, then this returns a run-time error.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="c8930-116">Equivalente de ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="c8930-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="c8930-117">Estas constantes no tienen equivalentes ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="c8930-117">These constants do not have ADO/WFC equivalents.</span></span>

