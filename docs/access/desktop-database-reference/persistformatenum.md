---
title: PersistFormatEnum (referencia de base de datos de escritorio de Access)
TOCTitle: PersistFormatEnum
ms:assetid: 5aa99a63-d422-0812-5aba-19305a3ad405
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249313(v=office.15)
ms:contentKeyID: 48545050
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4954c09c3eff67bb6f55dfc9e49464ad58fad5e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287611"
---
# <a name="persistformatenum"></a><span data-ttu-id="a29e1-102">PersistFormatEnum</span><span class="sxs-lookup"><span data-stu-id="a29e1-102">PersistFormatEnum</span></span>

<span data-ttu-id="a29e1-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a29e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a29e1-104">Especifica el formato en el que se guardará un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a29e1-104">Specifies the format in which to save a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a29e1-105">Constante</span><span class="sxs-lookup"><span data-stu-id="a29e1-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a29e1-106">Valor</span><span class="sxs-lookup"><span data-stu-id="a29e1-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a29e1-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a29e1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a29e1-108"><strong>adPersistADTG</strong></span><span class="sxs-lookup"><span data-stu-id="a29e1-108"><strong>adPersistADTG</strong></span></span></p></td>
<td><p><span data-ttu-id="a29e1-109">comprendi</span><span class="sxs-lookup"><span data-stu-id="a29e1-109">0</span></span></p></td>
<td><p><span data-ttu-id="a29e1-110">Indica formato ADTG (Advanced Data TableGram).</span><span class="sxs-lookup"><span data-stu-id="a29e1-110">Indicates Microsoft Advanced Data TableGram (ADTG) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a29e1-111"><strong>adPersistADO</strong></span><span class="sxs-lookup"><span data-stu-id="a29e1-111"><strong>adPersistADO</strong></span></span></p></td>
<td><p><span data-ttu-id="a29e1-112">1</span><span class="sxs-lookup"><span data-stu-id="a29e1-112">1</span></span></p></td>
<td><p><span data-ttu-id="a29e1-p101">Indica que se utilizará el lenguaje de marcado extensible (XML) propio de ADO. Este valor es el mismo que adPersistXML y se incluye para mantener la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="a29e1-p101">Indicates that ADO's own Extensible Markup Language (XML) format will be used. This value is the same as adPersistXML and is included for backwards compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a29e1-115"><strong>adPersistXML</strong></span><span class="sxs-lookup"><span data-stu-id="a29e1-115"><strong>adPersistXML</strong></span></span></p></td>
<td><p><span data-ttu-id="a29e1-116">1</span><span class="sxs-lookup"><span data-stu-id="a29e1-116">1</span></span></p></td>
<td><p><span data-ttu-id="a29e1-117">Indica formato de lenguaje XML.</span><span class="sxs-lookup"><span data-stu-id="a29e1-117">Indicates Extensible Markup Language (XML) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a29e1-118"><strong>adPersistProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="a29e1-118"><strong>adPersistProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="a29e1-119">segundo</span><span class="sxs-lookup"><span data-stu-id="a29e1-119">2</span></span></p></td>
<td><p><span data-ttu-id="a29e1-120">Indica que el proveedor guardará el objeto <strong>Recordset</strong> mediante su propio formato.</span><span class="sxs-lookup"><span data-stu-id="a29e1-120">Indicates that the provider will persist the <strong>Recordset</strong> using its own format.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="a29e1-121">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="a29e1-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="a29e1-122">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="a29e1-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a29e1-123">Constante</span><span class="sxs-lookup"><span data-stu-id="a29e1-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a29e1-124">AdoEnums. PersistFormat. ADTG</span><span class="sxs-lookup"><span data-stu-id="a29e1-124">AdoEnums.PersistFormat.ADTG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a29e1-125">AdoEnums. PersistFormat. XML</span><span class="sxs-lookup"><span data-stu-id="a29e1-125">AdoEnums.PersistFormat.XML</span></span></p></td>
</tr>
</tbody>
</table>

