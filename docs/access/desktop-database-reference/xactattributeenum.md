---
title: XactAttributeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e79a6143c65637660b2d59b7c7efb6a21e8935bd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718556"
---
# <a name="xactattributeenum"></a><span data-ttu-id="b9d47-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="b9d47-102">XactAttributeEnum</span></span>

<span data-ttu-id="b9d47-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9d47-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b9d47-104">Especifica los atributos de transacción de un objeto [ Connection ](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b9d47-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9d47-105">Constante</span><span class="sxs-lookup"><span data-stu-id="b9d47-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b9d47-106">Valor</span><span class="sxs-lookup"><span data-stu-id="b9d47-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b9d47-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9d47-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9d47-108"><strong>adXactAbortRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="b9d47-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="b9d47-109">262144</span><span class="sxs-lookup"><span data-stu-id="b9d47-109">262144</span></span></p></td>
<td><p><span data-ttu-id="b9d47-110">Realiza anulaciones con retención; es decir, una llamada a <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automáticamente, inicia una transacción nueva.</span><span class="sxs-lookup"><span data-stu-id="b9d47-110">Performs retaining aborts; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="b9d47-111">No todos los proveedores admiten esto.</span><span class="sxs-lookup"><span data-stu-id="b9d47-111">Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9d47-112"><strong>adXactCommitRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="b9d47-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="b9d47-113">131072</span><span class="sxs-lookup"><span data-stu-id="b9d47-113">131072</span></span></p></td>
<td><p><span data-ttu-id="b9d47-114">Realiza confirmaciones con retención; es decir, una llamada a <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automáticamente, inicia una transacción nueva.</span><span class="sxs-lookup"><span data-stu-id="b9d47-114">Performs retaining commits; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="b9d47-115">No todos los proveedores admiten esto.</span><span class="sxs-lookup"><span data-stu-id="b9d47-115">Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="b9d47-116">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="b9d47-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="b9d47-117">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="b9d47-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9d47-118">Constante</span><span class="sxs-lookup"><span data-stu-id="b9d47-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9d47-119">AdoEnums.XactAttribute.ABORTRETAINING</span><span class="sxs-lookup"><span data-stu-id="b9d47-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9d47-120">AdoEnums.XactAttribute.COMMITRETAINING</span><span class="sxs-lookup"><span data-stu-id="b9d47-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>

