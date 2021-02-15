---
title: StreamOpenOptionsEnum
TOCTitle: StreamOpenOptionsEnum
ms:assetid: d4bbd6be-41f1-cdf2-9d8f-b77ce83fb88e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250069(v=office.15)
ms:contentKeyID: 48547951
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f335f8572fbade23b949abacce8dd3690d205e32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314752"
---
# <a name="streamopenoptionsenum"></a><span data-ttu-id="8f74a-102">StreamOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="8f74a-102">StreamOpenOptionsEnum</span></span>


<span data-ttu-id="8f74a-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f74a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8f74a-104">Especifica opciones para abrir un objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8f74a-104">Specifies options for opening a [Stream](stream-object-ado.md) object.</span></span> <span data-ttu-id="8f74a-105">Los valores se pueden combinar con una operación booleana OR (O).</span><span class="sxs-lookup"><span data-stu-id="8f74a-105">The values can be combined with an OR operation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f74a-106">Constante</span><span class="sxs-lookup"><span data-stu-id="8f74a-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="8f74a-107">Valor</span><span class="sxs-lookup"><span data-stu-id="8f74a-107">Value</span></span></p></th>
<th><p><span data-ttu-id="8f74a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f74a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-109"><strong>adOpenStreamAsync</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-109"><strong>adOpenStreamAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-110">1 </span><span class="sxs-lookup"><span data-stu-id="8f74a-110">1</span></span></p></td>
<td><p><span data-ttu-id="8f74a-111">Abre el objeto <strong>Stream</strong> en modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="8f74a-111">Opens the <strong>Stream</strong> object in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f74a-112"><strong>adOpenStreamFromRecord</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-112"><strong>adOpenStreamFromRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-113">4 </span><span class="sxs-lookup"><span data-stu-id="8f74a-113">4</span></span></p></td>
<td><p><span data-ttu-id="8f74a-p102">Identifica el contenido del parámetro <em>Source</em> (origen) como un objeto <a href="record-object-ado.md">Record</a> ya abierto. El comportamiento predeterminado consiste en tratar <em>Source</em> como una dirección URL que señala directamente a un nodo de una estructura de árbol. Se abre la secuencia predeterminada asociada a ese nodo.</span><span class="sxs-lookup"><span data-stu-id="8f74a-p102">Identifies the contents of the <em>Source</em> parameter to be an already open <a href="record-object-ado.md">Record</a> object. The default behavior is to treat <em>Source</em> as a URL that points directly to a node in a tree structure. The default stream associated with that node is opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-117"><strong>adOpenStreamUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-117"><strong>adOpenStreamUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-118">-1</span><span class="sxs-lookup"><span data-stu-id="8f74a-118">-1</span></span></p></td>
<td><p><span data-ttu-id="8f74a-p103">Valor predeterminado. Especifica que el objeto <strong>Stream</strong> se abra con opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="8f74a-p103">Default. Specifies opening the <strong>Stream</strong> object with default options.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8f74a-121">Equivalente de ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="8f74a-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="8f74a-122">Estas constantes no tienen equivalentes ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="8f74a-122">These constants do not have ADO/WFC equivalents.</span></span>

