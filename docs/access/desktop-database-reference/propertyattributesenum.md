---
title: PropertyAttributesEnum
TOCTitle: PropertyAttributesEnum
ms:assetid: cbe93f65-a3ee-4741-1ac7-1c98ac53cdde
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250012(v=office.15)
ms:contentKeyID: 48547726
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c929bcf5dc7f5267c2e7d3a8dac5ed6bfb55b20b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302880"
---
# <a name="propertyattributesenum"></a><span data-ttu-id="8ddab-102">PropertyAttributesEnum</span><span class="sxs-lookup"><span data-stu-id="8ddab-102">PropertyAttributesEnum</span></span>


<span data-ttu-id="8ddab-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ddab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ddab-104">Especifica los atributos de un objeto [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8ddab-104">Specifies the attributes of a [Property](property-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ddab-105">Constante</span><span class="sxs-lookup"><span data-stu-id="8ddab-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="8ddab-106">Valor</span><span class="sxs-lookup"><span data-stu-id="8ddab-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8ddab-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ddab-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ddab-108"><strong>adPropNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="8ddab-108"><strong>adPropNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddab-109">0</span><span class="sxs-lookup"><span data-stu-id="8ddab-109">0</span></span></p></td>
<td><p><span data-ttu-id="8ddab-110">Indica que la propiedad no es admitida por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="8ddab-110">Indicates that the property is not supported by the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddab-111"><strong>adPropRequired</strong></span><span class="sxs-lookup"><span data-stu-id="8ddab-111"><strong>adPropRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddab-112">1</span><span class="sxs-lookup"><span data-stu-id="8ddab-112">1</span></span></p></td>
<td><p><span data-ttu-id="8ddab-113">Indica que el usuario debe especificar un valor para esta propiedad antes de que se inicialice el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="8ddab-113">Indicates that the user must specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddab-114"><strong>adPropOptional</strong></span><span class="sxs-lookup"><span data-stu-id="8ddab-114"><strong>adPropOptional</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddab-115">2</span><span class="sxs-lookup"><span data-stu-id="8ddab-115">2</span></span></p></td>
<td><p><span data-ttu-id="8ddab-116">Indica que el usuario no necesita especificar un valor para esta propiedad antes de que se inicialice el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="8ddab-116">Indicates that the user does not need to specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddab-117"><strong>adPropRead</strong></span><span class="sxs-lookup"><span data-stu-id="8ddab-117"><strong>adPropRead</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddab-118">512</span><span class="sxs-lookup"><span data-stu-id="8ddab-118">512</span></span></p></td>
<td><p><span data-ttu-id="8ddab-119">Indica que el usuario puede leer la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8ddab-119">Indicates that the user can read the property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddab-120"><strong>adPropWrite</strong></span><span class="sxs-lookup"><span data-stu-id="8ddab-120"><strong>adPropWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddab-121">1024</span><span class="sxs-lookup"><span data-stu-id="8ddab-121">1024</span></span></p></td>
<td><p><span data-ttu-id="8ddab-122">Indica que el usuario puede establecer la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8ddab-122">Indicates that the user can set the property.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8ddab-123">Equivalente a ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="8ddab-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="8ddab-124">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="8ddab-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ddab-125">Constante</span><span class="sxs-lookup"><span data-stu-id="8ddab-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ddab-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="8ddab-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddab-127">AdoEnums.PropertyAttributes.REQUIRED</span><span class="sxs-lookup"><span data-stu-id="8ddab-127">AdoEnums.PropertyAttributes.REQUIRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddab-128">AdoEnums.PropertyAttributes.OPTIONAL</span><span class="sxs-lookup"><span data-stu-id="8ddab-128">AdoEnums.PropertyAttributes.OPTIONAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddab-129">AdoEnums.PropertyAttributes.READ</span><span class="sxs-lookup"><span data-stu-id="8ddab-129">AdoEnums.PropertyAttributes.READ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddab-130">AdoEnums.PropertyAttributes.WRITE</span><span class="sxs-lookup"><span data-stu-id="8ddab-130">AdoEnums.PropertyAttributes.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

