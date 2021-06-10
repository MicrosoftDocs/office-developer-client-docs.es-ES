---
title: XactAttributeEnum (referencia de base de datos de escritorio de Access)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e79a6143c65637660b2d59b7c7efb6a21e8935bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302572"
---
# <a name="xactattributeenum"></a><span data-ttu-id="1459a-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="1459a-102">XactAttributeEnum</span></span>

<span data-ttu-id="1459a-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1459a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1459a-104">Especifica los atributos de transacción de un objeto [ Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1459a-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1459a-105">Constante</span><span class="sxs-lookup"><span data-stu-id="1459a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="1459a-106">Valor</span><span class="sxs-lookup"><span data-stu-id="1459a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1459a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1459a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1459a-108"><strong>adXactAbortRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="1459a-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="1459a-109">262144</span><span class="sxs-lookup"><span data-stu-id="1459a-109">262144</span></span></p></td>
<td><p><span data-ttu-id="1459a-110">Realiza las anulaciones de retención; es decir, al llamar <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">a RollbackTrans</a> se inicia automáticamente una nueva transacción.</span><span class="sxs-lookup"><span data-stu-id="1459a-110">Performs retaining aborts; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="1459a-111">No todos los proveedores admiten esto.</span><span class="sxs-lookup"><span data-stu-id="1459a-111">Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459a-112"><strong>adXactCommitRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="1459a-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="1459a-113">131072</span><span class="sxs-lookup"><span data-stu-id="1459a-113">131072</span></span></p></td>
<td><p><span data-ttu-id="1459a-114">Realiza confirmaciones de retención; es decir, al llamar <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">a CommitTrans</a> se inicia automáticamente una nueva transacción.</span><span class="sxs-lookup"><span data-stu-id="1459a-114">Performs retaining commits; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="1459a-115">No todos los proveedores admiten esto.</span><span class="sxs-lookup"><span data-stu-id="1459a-115">Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="1459a-116">Equivalente a ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="1459a-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="1459a-117">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="1459a-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1459a-118">Constante</span><span class="sxs-lookup"><span data-stu-id="1459a-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1459a-119">AdoEnums.XactAttribute.ABORTRETAINING</span><span class="sxs-lookup"><span data-stu-id="1459a-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1459a-120">AdoEnums.XactAttribute.COMMITRETAINING</span><span class="sxs-lookup"><span data-stu-id="1459a-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>

