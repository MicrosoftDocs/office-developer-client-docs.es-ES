---
title: RecordStatusEnum Enumeration (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c2d96c359a913660c146f4850a1846554e3b6856
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875122"
---
# <a name="recordstatusenum-enumeration-dao"></a><span data-ttu-id="31c47-102">RecordStatusEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="31c47-102">RecordStatusEnum Enumeration (DAO)</span></span>


<span data-ttu-id="31c47-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="31c47-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31c47-104">Se utiliza con la propiedad **RecordStatus** para indicar el estado de actualización del registro actual si forma parte de una actualización por lotes.</span><span class="sxs-lookup"><span data-stu-id="31c47-104">Used with the **RecordStatus** property to indicate the update status of the current record if it is part of a batch update.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31c47-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="31c47-105">Name</span></span></p></th>
<th><p><span data-ttu-id="31c47-106">Valor</span><span class="sxs-lookup"><span data-stu-id="31c47-106">Value</span></span></p></th>
<th><p><span data-ttu-id="31c47-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="31c47-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31c47-108">dbRecordDBDeleted</span><span class="sxs-lookup"><span data-stu-id="31c47-108">dbRecordDBDeleted</span></span></p></td>
<td><p><span data-ttu-id="31c47-109">4</span><span class="sxs-lookup"><span data-stu-id="31c47-109">4</span></span></p></td>
<td><p><span data-ttu-id="31c47-110">El registro se ha eliminado localmente y en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="31c47-110">The record has been deleted locally and in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31c47-111">dbRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="31c47-111">dbRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="31c47-112">3</span><span class="sxs-lookup"><span data-stu-id="31c47-112">3</span></span></p></td>
<td><p><span data-ttu-id="31c47-113">El registro se ha eliminado, pero permanece todavía en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="31c47-113">The record has been deleted, but not yet deleted in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31c47-114">dbRecordModified</span><span class="sxs-lookup"><span data-stu-id="31c47-114">dbRecordModified</span></span></p></td>
<td><p><span data-ttu-id="31c47-115">1</span><span class="sxs-lookup"><span data-stu-id="31c47-115">1</span></span></p></td>
<td><p><span data-ttu-id="31c47-116">El registro se ha modificado y no se ha actualizado en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="31c47-116">The record has been modified and not updated in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31c47-117">dbRecordNew</span><span class="sxs-lookup"><span data-stu-id="31c47-117">dbRecordNew</span></span></p></td>
<td><p><span data-ttu-id="31c47-118">2</span><span class="sxs-lookup"><span data-stu-id="31c47-118">2</span></span></p></td>
<td><p><span data-ttu-id="31c47-119">El registro se ha insertado con el método <strong>AddNew</strong>, pero no se ha insertado todavía en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="31c47-119">The record has been inserted with the <strong>AddNew</strong> method, but not yet inserted into the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31c47-120">dbRecordUnmodified</span><span class="sxs-lookup"><span data-stu-id="31c47-120">dbRecordUnmodified</span></span></p></td>
<td><p><span data-ttu-id="31c47-121">0</span><span class="sxs-lookup"><span data-stu-id="31c47-121">0</span></span></p></td>
<td><p><span data-ttu-id="31c47-122">(Valor predeterminado) El registro no se ha modificado o se ha actualizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="31c47-122">(Default) The record has not been modified or has been updated successfully.</span></span></p></td>
</tr>
</tbody>
</table>

