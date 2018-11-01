---
title: ConnectOptionEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 37420ab37b350f0f852305958edbf414d9aecdb3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867317"
---
# <a name="connectoptionenum"></a><span data-ttu-id="39026-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="39026-102">ConnectOptionEnum</span></span>

<span data-ttu-id="39026-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39026-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39026-104">Especifica si el método [Open](open-method-ado-connection.md) de un objeto [Connection](connection-object-ado.md) debe volver después (sincrónicamente) o antes (asincrónicamente) de que la conexión se establezca.</span><span class="sxs-lookup"><span data-stu-id="39026-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39026-105">Constante</span><span class="sxs-lookup"><span data-stu-id="39026-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="39026-106">Valor</span><span class="sxs-lookup"><span data-stu-id="39026-106">Value</span></span></p></th>
<th><p><span data-ttu-id="39026-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="39026-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39026-108"><strong>adAsyncConnect</strong></span><span class="sxs-lookup"><span data-stu-id="39026-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="39026-109">16</span><span class="sxs-lookup"><span data-stu-id="39026-109">16</span></span></p></td>
<td><p><span data-ttu-id="39026-p101">Abre la conexión asincrónicamente. El evento <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> se puede utilizar para determinar en qué momento está disponible la conexión.</span><span class="sxs-lookup"><span data-stu-id="39026-p101">Opens the connection asynchronously. The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39026-112"><strong>adConnectUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="39026-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="39026-113">-1</span><span class="sxs-lookup"><span data-stu-id="39026-113">-1</span></span></p></td>
<td><p><span data-ttu-id="39026-p102">Valor predeterminado. Abre la conexión sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="39026-p102">Default. Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="39026-116">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="39026-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="39026-117">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="39026-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39026-118">Constante</span><span class="sxs-lookup"><span data-stu-id="39026-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39026-119">AdoEnums.ConnectOption.ASYNCCONNECT</span><span class="sxs-lookup"><span data-stu-id="39026-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39026-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="39026-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

