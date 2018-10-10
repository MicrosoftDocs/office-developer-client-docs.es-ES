---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9538e1fb4a712b109e021512a3d28d299deaeb3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484809"
---
# <a name="recordopenoptionsenum"></a><span data-ttu-id="00e75-102">RecordOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="00e75-102">RecordOpenOptionsEnum</span></span>


<span data-ttu-id="00e75-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="00e75-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="00e75-p101">Especifica opciones para abrir un [Record](record-object-ado.md). Estos valores se pueden combinar mediante OR.</span><span class="sxs-lookup"><span data-stu-id="00e75-p101">Specifies options for opening a [Record](record-object-ado.md). These values may be combined by using OR.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="00e75-106">Constante</span><span class="sxs-lookup"><span data-stu-id="00e75-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="00e75-107">Valor</span><span class="sxs-lookup"><span data-stu-id="00e75-107">Value</span></span></p></th>
<th><p><span data-ttu-id="00e75-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="00e75-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00e75-109"><strong>adDelayFetchFields</strong></span><span class="sxs-lookup"><span data-stu-id="00e75-109"><strong>adDelayFetchFields</strong></span></span></p></td>
<td><p><span data-ttu-id="00e75-110">0 x 8000</span><span class="sxs-lookup"><span data-stu-id="00e75-110">0x8000</span></span></p></td>
<td><p><span data-ttu-id="00e75-p102">Indica al proveedor que los campos asociados al objeto <strong>Record</strong> no es necesario que se recuperen inicialmente, sino que se pueden recuperar en el primer intento de obtener acceso al campo. El comportamiento predeterminado, indicado por la ausencia de esta marca, consiste en recuperar todos los campos de un objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="00e75-p102">Indicates to the provider that the fields associated with the <strong>Record</strong> need not be retrieved initially, but can be retrieved at the first attempt to access the field. The default behavior, indicated by the absence of this flag, is to retrieve all the <strong>Record</strong> object fields.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00e75-113"><strong>adDelayFetchStream</strong></span><span class="sxs-lookup"><span data-stu-id="00e75-113"><strong>adDelayFetchStream</strong></span></span></p></td>
<td><p><span data-ttu-id="00e75-114">0x4000</span><span class="sxs-lookup"><span data-stu-id="00e75-114">0x4000</span></span></p></td>
<td><p><span data-ttu-id="00e75-p103">Indica al proveedor que la secuencia (Stream) predeterminada asociada con el objeto <strong>Record</strong> no es necesario que se recupere inicialmente. El comportamiento predeterminado, indicado por la ausencia de esta marca, consiste en recuperar la secuencia predeterminada asociada al objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="00e75-p103">Indicates to the provider that the default stream associated with the <strong>Record</strong> need not be retrieved initially. The default behavior, indicated by the absence of this flag, is to retrieve the default stream associated with the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00e75-117"><strong>adOpenAsync</strong></span><span class="sxs-lookup"><span data-stu-id="00e75-117"><strong>adOpenAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="00e75-118">0x1000</span><span class="sxs-lookup"><span data-stu-id="00e75-118">0x1000</span></span></p></td>
<td><p><span data-ttu-id="00e75-119">Indica que el objeto <strong>Record</strong> se abre en modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="00e75-119">Indicates that the <strong>Record</strong> object is opened in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00e75-120"><strong>adOpenExecuteCommand</strong></span><span class="sxs-lookup"><span data-stu-id="00e75-120"><strong>adOpenExecuteCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="00e75-121">0 x 10000</span><span class="sxs-lookup"><span data-stu-id="00e75-121">0x10000</span></span></p></td>
<td><p><span data-ttu-id="00e75-p104">Indica que la cadena de origen (Source) contiene texto de un comando que se debe ejecutar. Este valor es equivalente a la opción <strong>adCmdText</strong> en <strong>Recordset.Open</strong>.</span><span class="sxs-lookup"><span data-stu-id="00e75-p104">Indicates that the Source string contains command text that should be executed. This value is equivalent to the <strong>adCmdText</strong> option on <strong>Recordset.Open</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00e75-124"><strong>adOpenRecordUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="00e75-124"><strong>adOpenRecordUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="00e75-125">-1</span><span class="sxs-lookup"><span data-stu-id="00e75-125">-1</span></span></p></td>
<td><p><span data-ttu-id="00e75-p105">Valor predeterminado. Indica que no se especifica ninguna opción.</span><span class="sxs-lookup"><span data-stu-id="00e75-p105">Default. Indicates no options are specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00e75-128"><strong>adOpenOutput</strong></span><span class="sxs-lookup"><span data-stu-id="00e75-128"><strong>adOpenOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="00e75-129">0 x 800000</span><span class="sxs-lookup"><span data-stu-id="00e75-129">0x800000</span></span></p></td>
<td><p><span data-ttu-id="00e75-p106">Indica que si el origen apunta a un nodo que contiene un script ejecutable (tal como una página .ASP), entonces el <strong>Record</strong> abierto contendrá los resultados del script ejecutado. Este valor sólo es válido con registros que no son de tipo colección.</span><span class="sxs-lookup"><span data-stu-id="00e75-p106">Indicates that if the source points to a node that contains an executable script (such as an .ASP page), then the opened <strong>Record</strong> will contain the results of the executed script. This value is only valid with non-collection records.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="00e75-132">**Equivalente ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="00e75-132">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="00e75-133">Estas constantes no tienen equivalentes ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="00e75-133">These constants do not have ADO/WFC equivalents.</span></span>

