---
title: Más (referencia de escritorio de la base de datos de Access)
TOCTitle: PersistFormatEnum
ms:assetid: 5aa99a63-d422-0812-5aba-19305a3ad405
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249313(v=office.15)
ms:contentKeyID: 48545050
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e3254d60c6daa032857227b1f16f9a9c085164dc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484551"
---
# <a name="persistformatenum"></a><span data-ttu-id="25122-102">Más</span><span class="sxs-lookup"><span data-stu-id="25122-102">PersistFormatEnum</span></span>


<span data-ttu-id="25122-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="25122-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="25122-104">Especifica el formato en el que se guardará un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="25122-104">Specifies the format in which to save a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="25122-105">Constante</span><span class="sxs-lookup"><span data-stu-id="25122-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="25122-106">Valor</span><span class="sxs-lookup"><span data-stu-id="25122-106">Value</span></span></p></th>
<th><p><span data-ttu-id="25122-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="25122-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25122-108"><strong>adPersistADTG</strong></span><span class="sxs-lookup"><span data-stu-id="25122-108"><strong>adPersistADTG</strong></span></span></p></td>
<td><p><span data-ttu-id="25122-109">0</span><span class="sxs-lookup"><span data-stu-id="25122-109">0</span></span></p></td>
<td><p><span data-ttu-id="25122-110">Indica formato ADTG (Advanced Data TableGram).</span><span class="sxs-lookup"><span data-stu-id="25122-110">Indicates Microsoft Advanced Data TableGram (ADTG) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25122-111"><strong>adPersistADO</strong></span><span class="sxs-lookup"><span data-stu-id="25122-111"><strong>adPersistADO</strong></span></span></p></td>
<td><p><span data-ttu-id="25122-112">1</span><span class="sxs-lookup"><span data-stu-id="25122-112">1</span></span></p></td>
<td><p><span data-ttu-id="25122-p101">Indica que se utilizará el lenguaje de marcado extensible (XML) propio de ADO. Este valor es el mismo que adPersistXML y se incluye para mantener la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="25122-p101">Indicates that ADO's own Extensible Markup Language (XML) format will be used. This value is the same as adPersistXML and is included for backwards compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25122-115"><strong>adPersistXML</strong></span><span class="sxs-lookup"><span data-stu-id="25122-115"><strong>adPersistXML</strong></span></span></p></td>
<td><p><span data-ttu-id="25122-116">1</span><span class="sxs-lookup"><span data-stu-id="25122-116">1</span></span></p></td>
<td><p><span data-ttu-id="25122-117">Indica formato de lenguaje XML.</span><span class="sxs-lookup"><span data-stu-id="25122-117">Indicates Extensible Markup Language (XML) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25122-118"><strong>adPersistProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="25122-118"><strong>adPersistProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="25122-119">2</span><span class="sxs-lookup"><span data-stu-id="25122-119">2</span></span></p></td>
<td><p><span data-ttu-id="25122-120">Indica que el proveedor guardará el objeto <strong>Recordset</strong> mediante su propio formato.</span><span class="sxs-lookup"><span data-stu-id="25122-120">Indicates that the provider will persist the <strong>Recordset</strong> using its own format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="25122-121">**Equivalente ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="25122-121">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="25122-122">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="25122-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="25122-123">Constante</span><span class="sxs-lookup"><span data-stu-id="25122-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25122-124">AdoEnums.PersistFormat.ADTG</span><span class="sxs-lookup"><span data-stu-id="25122-124">AdoEnums.PersistFormat.ADTG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25122-125">AdoEnums.PersistFormat.XML</span><span class="sxs-lookup"><span data-stu-id="25122-125">AdoEnums.PersistFormat.XML</span></span></p></td>
</tr>
</tbody>
</table>

