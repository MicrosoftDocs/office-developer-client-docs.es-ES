---
title: PropertyAttributesEnum
TOCTitle: PropertyAttributesEnum
ms:assetid: cbe93f65-a3ee-4741-1ac7-1c98ac53cdde
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250012(v=office.15)
ms:contentKeyID: 48547726
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8f01efcc98ed12858712c28f080fb066d3dc1b41
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484611"
---
# <a name="propertyattributesenum"></a><span data-ttu-id="57c16-102">PropertyAttributesEnum</span><span class="sxs-lookup"><span data-stu-id="57c16-102">PropertyAttributesEnum</span></span>


<span data-ttu-id="57c16-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="57c16-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="57c16-104">Especifica los atributos de un objeto [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="57c16-104">Specifies the attributes of a [Property](property-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="57c16-105">Constante</span><span class="sxs-lookup"><span data-stu-id="57c16-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="57c16-106">Valor</span><span class="sxs-lookup"><span data-stu-id="57c16-106">Value</span></span></p></th>
<th><p><span data-ttu-id="57c16-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="57c16-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57c16-108"><strong>adPropNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="57c16-108"><strong>adPropNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="57c16-109">0</span><span class="sxs-lookup"><span data-stu-id="57c16-109">0</span></span></p></td>
<td><p><span data-ttu-id="57c16-110">Indica que la propiedad no es admitida por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="57c16-110">Indicates that the property is not supported by the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57c16-111"><strong>adPropRequired</strong></span><span class="sxs-lookup"><span data-stu-id="57c16-111"><strong>adPropRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="57c16-112">1</span><span class="sxs-lookup"><span data-stu-id="57c16-112">1</span></span></p></td>
<td><p><span data-ttu-id="57c16-113">Indica que el usuario debe especificar un valor para esta propiedad antes de que se inicialice el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="57c16-113">Indicates that the user must specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57c16-114"><strong>adPropOptional</strong></span><span class="sxs-lookup"><span data-stu-id="57c16-114"><strong>adPropOptional</strong></span></span></p></td>
<td><p><span data-ttu-id="57c16-115">2</span><span class="sxs-lookup"><span data-stu-id="57c16-115">2</span></span></p></td>
<td><p><span data-ttu-id="57c16-116">Indica que el usuario no necesita especificar un valor para esta propiedad antes de que se inicialice el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="57c16-116">Indicates that the user does not need to specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57c16-117"><strong>adPropRead</strong></span><span class="sxs-lookup"><span data-stu-id="57c16-117"><strong>adPropRead</strong></span></span></p></td>
<td><p><span data-ttu-id="57c16-118">512</span><span class="sxs-lookup"><span data-stu-id="57c16-118">512</span></span></p></td>
<td><p><span data-ttu-id="57c16-119">Indica que el usuario puede leer la propiedad.</span><span class="sxs-lookup"><span data-stu-id="57c16-119">Indicates that the user can read the property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57c16-120"><strong>adPropWrite</strong></span><span class="sxs-lookup"><span data-stu-id="57c16-120"><strong>adPropWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="57c16-121">1024</span><span class="sxs-lookup"><span data-stu-id="57c16-121">1024</span></span></p></td>
<td><p><span data-ttu-id="57c16-122">Indica que el usuario puede establecer la propiedad.</span><span class="sxs-lookup"><span data-stu-id="57c16-122">Indicates that the user can set the property.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="57c16-123">**Equivalente ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="57c16-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="57c16-124">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="57c16-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="57c16-125">Constante</span><span class="sxs-lookup"><span data-stu-id="57c16-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57c16-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="57c16-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57c16-127">AdoEnums.PropertyAttributes.REQUIRED</span><span class="sxs-lookup"><span data-stu-id="57c16-127">AdoEnums.PropertyAttributes.REQUIRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57c16-128">AdoEnums.PropertyAttributes.OPTIONAL</span><span class="sxs-lookup"><span data-stu-id="57c16-128">AdoEnums.PropertyAttributes.OPTIONAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57c16-129">AdoEnums.PropertyAttributes.READ</span><span class="sxs-lookup"><span data-stu-id="57c16-129">AdoEnums.PropertyAttributes.READ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57c16-130">AdoEnums.PropertyAttributes.WRITE</span><span class="sxs-lookup"><span data-stu-id="57c16-130">AdoEnums.PropertyAttributes.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

