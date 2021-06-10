---
title: Método DBEngine.SetOption (DAO)
TOCTitle: SetOption Method
ms:assetid: ea55c10c-2385-1b7e-0cba-32982c9b6643
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836236(v=office.15)
ms:contentKeyID: 48548461
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1088781
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5875a8935b1b44c3c36b29344af32df552f6e01c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294200"
---
# <a name="dbenginesetoption-method-dao"></a><span data-ttu-id="f02ac-102">Método DBEngine.SetOption (DAO)</span><span class="sxs-lookup"><span data-stu-id="f02ac-102">DBEngine.SetOption method (DAO)</span></span>

<span data-ttu-id="f02ac-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f02ac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f02ac-104">Anula temporalmente los valores para las claves del motor de base de datos de Microsoft Access en el Registro de Windows (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f02ac-104">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="f02ac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f02ac-105">Syntax</span></span>

<span data-ttu-id="f02ac-106">*expresión* . SetOption(***Option***, ***Value***)</span><span class="sxs-lookup"><span data-stu-id="f02ac-106">*expression* .SetOption(***Option***, ***Value***)</span></span>

<span data-ttu-id="f02ac-107">*expression* Expresión que devuelve un objeto **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="f02ac-107">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="f02ac-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="f02ac-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f02ac-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="f02ac-109">Name</span></span></p></th>
<th><p><span data-ttu-id="f02ac-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="f02ac-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="f02ac-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f02ac-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="f02ac-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f02ac-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f02ac-113"><em>Opción</em></span><span class="sxs-lookup"><span data-stu-id="f02ac-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="f02ac-114">Necesario</span><span class="sxs-lookup"><span data-stu-id="f02ac-114">Required</span></span></p></td>
<td><p><span data-ttu-id="f02ac-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="f02ac-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="f02ac-116">Constante tal como se describe en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f02ac-116">A constant as described in Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f02ac-117"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="f02ac-117"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="f02ac-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f02ac-118">Required</span></span></p></td>
<td><p><span data-ttu-id="f02ac-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f02ac-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f02ac-120">Valor en el que desea establecer la opción.</span><span class="sxs-lookup"><span data-stu-id="f02ac-120">The value that you want to set option to.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f02ac-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f02ac-121">Remarks</span></span>

<span data-ttu-id="f02ac-122">Cada constante hace referencia a la clave del Registro correspondiente en la ruta de acceso HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Office \_ \\ \\ \\ \\ 12.0 \\ Access Connectivity \\ Engines ACE (es decir, dbSharedAsyncDelay corresponde a la clave \\ HKEY LOCAL MACHINE SOFTWARE Microsoft Office  \_ \_ \\ \\ \\ \\ 12.0 \\ Access Connectivity \\ Engines ACE \\ \\ SharedAsyncDelay, y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="f02ac-122">Each constant refers to the corresponding registry key in the path HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE (that is, **dbSharedAsyncDelay** corresponds to the key HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE\\SharedAsyncDelay, and so on).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f02ac-123">Constante</span><span class="sxs-lookup"><span data-stu-id="f02ac-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="f02ac-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="f02ac-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f02ac-125"><strong>dbPageTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="f02ac-125"><strong>dbPageTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="f02ac-126">Clave PageTimeout</span><span class="sxs-lookup"><span data-stu-id="f02ac-126">The PageTimeout key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f02ac-127"><strong>dbSharedAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="f02ac-127"><strong>dbSharedAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="f02ac-128">Clave SharedAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="f02ac-128">The SharedAsyncDelay key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f02ac-129"><strong>dbExclusiveAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="f02ac-129"><strong>dbExclusiveAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="f02ac-130">Clave ExclusiveAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="f02ac-130">The ExclusiveAsyncDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f02ac-131"><strong>dbLockRetry</strong></span><span class="sxs-lookup"><span data-stu-id="f02ac-131"><strong>dbLockRetry</strong></span></span></p></td>
<td><p><span data-ttu-id="f02ac-132">Clave LockRetry</span><span class="sxs-lookup"><span data-stu-id="f02ac-132">The LockRetry key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f02ac-133"><strong>dbUserCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="f02ac-133"><strong>dbUserCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="f02ac-134">Clave UserCommitSync</span><span class="sxs-lookup"><span data-stu-id="f02ac-134">The UserCommitSync key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f02ac-135"><strong>dbImplicitCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="f02ac-135"><strong>dbImplicitCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="f02ac-136">Clave ImplicitCommitSync</span><span class="sxs-lookup"><span data-stu-id="f02ac-136">The ImplicitCommitSync key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f02ac-137"><strong>dbMaxBufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="f02ac-137"><strong>dbMaxBufferSize</strong></span></span></p></td>
<td><p><span data-ttu-id="f02ac-138">Clave MaxBufferSize</span><span class="sxs-lookup"><span data-stu-id="f02ac-138">The MaxBufferSize key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f02ac-139"><strong>dbMaxLocksPerFile</strong></span><span class="sxs-lookup"><span data-stu-id="f02ac-139"><strong>dbMaxLocksPerFile</strong></span></span></p></td>
<td><p><span data-ttu-id="f02ac-140">Clave MaxLocksPerFile</span><span class="sxs-lookup"><span data-stu-id="f02ac-140">The MaxLocksPerFile key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f02ac-141"><strong>dbLockDelay</strong></span><span class="sxs-lookup"><span data-stu-id="f02ac-141"><strong>dbLockDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="f02ac-142">Clave LockDelay</span><span class="sxs-lookup"><span data-stu-id="f02ac-142">The LockDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f02ac-143"><strong>dbRecycleLVs</strong></span><span class="sxs-lookup"><span data-stu-id="f02ac-143"><strong>dbRecycleLVs</strong></span></span></p></td>
<td><p><span data-ttu-id="f02ac-144">Clave RecycleLVs</span><span class="sxs-lookup"><span data-stu-id="f02ac-144">The RecycleLVs key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f02ac-145"><strong>dbFlushTransactionTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="f02ac-145"><strong>dbFlushTransactionTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="f02ac-146">Clave FlushTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="f02ac-146">The FlushTransactionTimeout key</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f02ac-p101">Utilice el método **SetOption** para anular los valores de registro en tiempo de ejecución. Los nuevos valores establecidos con el método **SetOption** siguen en vigor hasta que se cambien de nuevo mediante otra llamada **SetOption** o que se cierre el objeto **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="f02ac-p101">Use the **SetOption** method to override registry values at run-time. New values established with the **SetOption** method remain in effect until changed again by another **SetOption** call, or until the **DBEngine** object is closed.</span></span>

