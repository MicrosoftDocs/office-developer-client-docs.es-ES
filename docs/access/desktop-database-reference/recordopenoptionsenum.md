---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: caaf755ebd63f1805d0c77ef79a0f5863a85050e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300689"
---
# <a name="recordopenoptionsenum"></a><span data-ttu-id="977b8-102">RecordOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="977b8-102">RecordOpenOptionsEnum</span></span>


<span data-ttu-id="977b8-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="977b8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="977b8-p101">Especifica opciones para abrir un [Record](record-object-ado.md). Estos valores se pueden combinar mediante OR.</span><span class="sxs-lookup"><span data-stu-id="977b8-p101">Specifies options for opening a [Record](record-object-ado.md). These values may be combined by using OR.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="977b8-106">Constante</span><span class="sxs-lookup"><span data-stu-id="977b8-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="977b8-107">Valor</span><span class="sxs-lookup"><span data-stu-id="977b8-107">Value</span></span></p></th>
<th><p><span data-ttu-id="977b8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="977b8-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="977b8-109"><strong>adDelayFetchFields</strong></span><span class="sxs-lookup"><span data-stu-id="977b8-109"><strong>adDelayFetchFields</strong></span></span></p></td>
<td><p><span data-ttu-id="977b8-110">0x8000</span><span class="sxs-lookup"><span data-stu-id="977b8-110">0x8000</span></span></p></td>
<td><p><span data-ttu-id="977b8-p102">Indica al proveedor que los campos asociados al objeto <strong>Record</strong> no es necesario que se recuperen inicialmente, sino que se pueden recuperar en el primer intento de obtener acceso al campo. El comportamiento predeterminado, indicado por la ausencia de esta marca, consiste en recuperar todos los campos de un objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="977b8-p102">Indicates to the provider that the fields associated with the <strong>Record</strong> need not be retrieved initially, but can be retrieved at the first attempt to access the field. The default behavior, indicated by the absence of this flag, is to retrieve all the <strong>Record</strong> object fields.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="977b8-113"><strong>adDelayFetchStream</strong></span><span class="sxs-lookup"><span data-stu-id="977b8-113"><strong>adDelayFetchStream</strong></span></span></p></td>
<td><p><span data-ttu-id="977b8-114">0x4000</span><span class="sxs-lookup"><span data-stu-id="977b8-114">0x4000</span></span></p></td>
<td><p><span data-ttu-id="977b8-p103">Indica al proveedor que la secuencia (Stream) predeterminada asociada con el objeto <strong>Record</strong> no es necesario que se recupere inicialmente. El comportamiento predeterminado, indicado por la ausencia de esta marca, consiste en recuperar la secuencia predeterminada asociada al objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="977b8-p103">Indicates to the provider that the default stream associated with the <strong>Record</strong> need not be retrieved initially. The default behavior, indicated by the absence of this flag, is to retrieve the default stream associated with the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="977b8-117"><strong>adOpenAsync</strong></span><span class="sxs-lookup"><span data-stu-id="977b8-117"><strong>adOpenAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="977b8-118">0x1000</span><span class="sxs-lookup"><span data-stu-id="977b8-118">0x1000</span></span></p></td>
<td><p><span data-ttu-id="977b8-119">Indica que el objeto <strong>Record</strong> se abre en modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="977b8-119">Indicates that the <strong>Record</strong> object is opened in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="977b8-120"><strong>adOpenExecuteCommand</strong></span><span class="sxs-lookup"><span data-stu-id="977b8-120"><strong>adOpenExecuteCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="977b8-121">0x10000</span><span class="sxs-lookup"><span data-stu-id="977b8-121">0x10000</span></span></p></td>
<td><p><span data-ttu-id="977b8-p104">Indica que la cadena de origen (Source) contiene texto de un comando que se debe ejecutar. Este valor es equivalente a la opción <strong>adCmdText</strong> en <strong>Recordset.Open</strong>.</span><span class="sxs-lookup"><span data-stu-id="977b8-p104">Indicates that the Source string contains command text that should be executed. This value is equivalent to the <strong>adCmdText</strong> option on <strong>Recordset.Open</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="977b8-124"><strong>adOpenRecordUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="977b8-124"><strong>adOpenRecordUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="977b8-125">-1</span><span class="sxs-lookup"><span data-stu-id="977b8-125">-1</span></span></p></td>
<td><p><span data-ttu-id="977b8-p105">Valor predeterminado. Indica que no se especifica ninguna opción.</span><span class="sxs-lookup"><span data-stu-id="977b8-p105">Default. Indicates no options are specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="977b8-128"><strong>adOpenOutput</strong></span><span class="sxs-lookup"><span data-stu-id="977b8-128"><strong>adOpenOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="977b8-129">0x800000</span><span class="sxs-lookup"><span data-stu-id="977b8-129">0x800000</span></span></p></td>
<td><p><span data-ttu-id="977b8-p106">Indica que si el origen apunta a un nodo que contiene un script ejecutable (tal como una página .ASP), entonces el <strong>Record</strong> abierto contendrá los resultados del script ejecutado. Este valor sólo es válido con registros que no son de tipo colección.</span><span class="sxs-lookup"><span data-stu-id="977b8-p106">Indicates that if the source points to a node that contains an executable script (such as an .ASP page), then the opened <strong>Record</strong> will contain the results of the executed script. This value is only valid with non-collection records.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="977b8-132">Equivalente a ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="977b8-132">ADO/WFC equivalent</span></span>

<span data-ttu-id="977b8-133">Estas constantes no tienen equivalentes ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="977b8-133">These constants do not have ADO/WFC equivalents.</span></span>

