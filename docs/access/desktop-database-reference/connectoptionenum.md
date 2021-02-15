---
title: ConnectOptionEnum (referencia de base de datos de escritorio de Access)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95b622d2216b085ffd0f76c8a26533187c17bd7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295684"
---
# <a name="connectoptionenum"></a><span data-ttu-id="73da9-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="73da9-102">ConnectOptionEnum</span></span>

<span data-ttu-id="73da9-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="73da9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="73da9-104">Especifica si el método [Open](open-method-ado-connection.md) de un objeto [Connection](connection-object-ado.md) debe volver después (sincrónicamente) o antes (asincrónicamente) de que la conexión se establezca.</span><span class="sxs-lookup"><span data-stu-id="73da9-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73da9-105">Constante</span><span class="sxs-lookup"><span data-stu-id="73da9-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="73da9-106">Valor</span><span class="sxs-lookup"><span data-stu-id="73da9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="73da9-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="73da9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73da9-108"><strong>adAsyncConnect</strong></span><span class="sxs-lookup"><span data-stu-id="73da9-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="73da9-109">16 </span><span class="sxs-lookup"><span data-stu-id="73da9-109">16</span></span></p></td>
<td><p><span data-ttu-id="73da9-p101">Abre la conexión asincrónicamente. El evento <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> se puede utilizar para determinar en qué momento está disponible la conexión.</span><span class="sxs-lookup"><span data-stu-id="73da9-p101">Opens the connection asynchronously. The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73da9-112"><strong>adConnectUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="73da9-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="73da9-113">-1</span><span class="sxs-lookup"><span data-stu-id="73da9-113">-1</span></span></p></td>
<td><p><span data-ttu-id="73da9-p102">Valor predeterminado. Abre la conexión sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="73da9-p102">Default. Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="73da9-116">Equivalente de ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="73da9-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="73da9-117">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="73da9-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73da9-118">Constante</span><span class="sxs-lookup"><span data-stu-id="73da9-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73da9-119">AdoEnums.ConnectOption.ASYNCCONNECT</span><span class="sxs-lookup"><span data-stu-id="73da9-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73da9-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="73da9-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

