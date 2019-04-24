---
title: Características de cursores y bloqueos
TOCTitle: Cursor and lock characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41a42aa3b0c49a5d871fa7b079a26c7d8076116a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295292"
---
# <a name="cursor-and-lock-characteristics"></a><span data-ttu-id="ed59a-102">Características de cursores y bloqueos</span><span class="sxs-lookup"><span data-stu-id="ed59a-102">Cursor and lock characteristics</span></span>

<span data-ttu-id="ed59a-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed59a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ed59a-104">Aunque las características de un cursor dependen de la funcionalidades del proveedor, las ventajas y desventajas siguientes generalmente son de aplicación para los diversos tipos de cursores y bloqueos.</span><span class="sxs-lookup"><span data-stu-id="ed59a-104">While the characteristics of a cursor depend upon capabilities of the provider, the following advantages and disadvantages generally apply to the various types of cursors and locks.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ed59a-105">Tipo de cursor o bloqueo</span><span class="sxs-lookup"><span data-stu-id="ed59a-105">Cursor or lock type</span></span></p></th>
<th><p><span data-ttu-id="ed59a-106">Ventajas</span><span class="sxs-lookup"><span data-stu-id="ed59a-106">Advantages</span></span></p></th>
<th><p><span data-ttu-id="ed59a-107">Desventajas</span><span class="sxs-lookup"><span data-stu-id="ed59a-107">Disadvantages</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed59a-108"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="ed59a-108"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="ed59a-109">Pocos requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="ed59a-109">Low resource requirements</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="ed59a-110">No se puede efectuar un desplazamiento hacia atrás</span><span class="sxs-lookup"><span data-stu-id="ed59a-110">Cannot scroll backward</span></span></p></li>
<li><p><span data-ttu-id="ed59a-111">No hay coincidencia de datos</span><span class="sxs-lookup"><span data-stu-id="ed59a-111">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed59a-112"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="ed59a-112"><strong>adOpenStatic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="ed59a-113">Desplazable</span><span class="sxs-lookup"><span data-stu-id="ed59a-113">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="ed59a-114">No hay coincidencia de datos</span><span class="sxs-lookup"><span data-stu-id="ed59a-114">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed59a-115"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="ed59a-115"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="ed59a-116">Hay alguna coincidencia de datos</span><span class="sxs-lookup"><span data-stu-id="ed59a-116">Some data concurrency</span></span></p></li>
<li><p><span data-ttu-id="ed59a-117">Desplazable</span><span class="sxs-lookup"><span data-stu-id="ed59a-117">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="ed59a-118">Más requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="ed59a-118">Higher resource requirements</span></span></p></li>
<li><p><span data-ttu-id="ed59a-119">No disponible en escenario de desconexión</span><span class="sxs-lookup"><span data-stu-id="ed59a-119">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed59a-120"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="ed59a-120"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="ed59a-121">Elevada coincidencia de datos</span><span class="sxs-lookup"><span data-stu-id="ed59a-121">High data concurrency</span></span></p></li>
<li><p><span data-ttu-id="ed59a-122">Desplazable</span><span class="sxs-lookup"><span data-stu-id="ed59a-122">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="ed59a-123">Requisitos de recursos máximos</span><span class="sxs-lookup"><span data-stu-id="ed59a-123">Highest resource requirements</span></span></p></li>
<li><p><span data-ttu-id="ed59a-124">No disponible en escenario de desconexión</span><span class="sxs-lookup"><span data-stu-id="ed59a-124">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed59a-125"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="ed59a-125"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="ed59a-126">Pocos requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="ed59a-126">Low resource requirements</span></span></p></li>
<li><p><span data-ttu-id="ed59a-127">Altamente escalable</span><span class="sxs-lookup"><span data-stu-id="ed59a-127">Highly scalable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="ed59a-128">Datos no actualizables a través de cursor</span><span class="sxs-lookup"><span data-stu-id="ed59a-128">Data not updatable through cursor</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed59a-129"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="ed59a-129"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="ed59a-130">Actualizaciones por lotes</span><span class="sxs-lookup"><span data-stu-id="ed59a-130">Batch updates</span></span></p></li>
<li><p><span data-ttu-id="ed59a-131">Permite escenarios de desconexión</span><span class="sxs-lookup"><span data-stu-id="ed59a-131">Allows disconnected scenarios</span></span></p></li>
<li><p><span data-ttu-id="ed59a-132">Otros usuarios pueden tener acceso a datos</span><span class="sxs-lookup"><span data-stu-id="ed59a-132">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="ed59a-133">Varios usuarios pueden cambiar los datos simultáneamente</span><span class="sxs-lookup"><span data-stu-id="ed59a-133">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed59a-134"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="ed59a-134"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="ed59a-135">Otros usuarios no pueden cambiar los datos mientras están bloqueados</span><span class="sxs-lookup"><span data-stu-id="ed59a-135">Data cannot be changed by other users while locked</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="ed59a-136">Impide a otros usuarios el acceso a los datos mientras están bloqueados</span><span class="sxs-lookup"><span data-stu-id="ed59a-136">Prevents other users from accessing data while locked</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed59a-137"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="ed59a-137"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="ed59a-138">Otros usuarios pueden tener acceso a datos</span><span class="sxs-lookup"><span data-stu-id="ed59a-138">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="ed59a-139">Varios usuarios pueden cambiar los datos simultáneamente</span><span class="sxs-lookup"><span data-stu-id="ed59a-139">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

