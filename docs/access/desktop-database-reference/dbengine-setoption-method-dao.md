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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699894"
---
# <a name="dbenginesetoption-method-dao"></a><span data-ttu-id="61901-102">Método DBEngine.SetOption (DAO)</span><span class="sxs-lookup"><span data-stu-id="61901-102">DBEngine.SetOption method (DAO)</span></span>

<span data-ttu-id="61901-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="61901-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="61901-104">Anula temporalmente los valores para las claves del motor de base de datos de Microsoft Access en el Registro de Windows (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="61901-104">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="61901-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61901-105">Syntax</span></span>

<span data-ttu-id="61901-106">*expresión* . SetOption (***opción***, ***valor***)</span><span class="sxs-lookup"><span data-stu-id="61901-106">*expression* .SetOption(***Option***, ***Value***)</span></span>

<span data-ttu-id="61901-107">*expresión* Una expresión que devuelve un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="61901-107">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="61901-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61901-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="61901-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="61901-109">Name</span></span></p></th>
<th><p><span data-ttu-id="61901-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="61901-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="61901-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="61901-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="61901-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="61901-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61901-113"><em>Opción</em></span><span class="sxs-lookup"><span data-stu-id="61901-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="61901-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="61901-114">Required</span></span></p></td>
<td><p><span data-ttu-id="61901-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="61901-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="61901-116">Constante tal como se describe en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="61901-116">A constant as described in Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61901-117"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="61901-117"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="61901-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="61901-118">Required</span></span></p></td>
<td><p><span data-ttu-id="61901-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="61901-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="61901-120">El valor que se desea establecer la opción.</span><span class="sxs-lookup"><span data-stu-id="61901-120">The value that you want to set option to.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="61901-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61901-121">Remarks</span></span>

<span data-ttu-id="61901-122">Cada constante hace referencia a la clave del registro correspondiente en la ruta de acceso HKEY\_LOCAL\_máquina\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\motores\\ACE (es decir, **dbSharedAsyncDelay** corresponde a la clave HKEY\_LOCAL\_máquina\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\motores\\ACE \\SharedAsyncDelay, y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="61901-122">Each constant refers to the corresponding registry key in the path HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE (that is, **dbSharedAsyncDelay** corresponds to the key HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE\\SharedAsyncDelay, and so on).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="61901-123">Constante</span><span class="sxs-lookup"><span data-stu-id="61901-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="61901-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="61901-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61901-125"><strong>dbPageTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="61901-125"><strong>dbPageTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="61901-126">Clave PageTimeout</span><span class="sxs-lookup"><span data-stu-id="61901-126">The PageTimeout key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61901-127"><strong>dbSharedAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="61901-127"><strong>dbSharedAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="61901-128">Clave SharedAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="61901-128">The SharedAsyncDelay key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61901-129"><strong>dbExclusiveAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="61901-129"><strong>dbExclusiveAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="61901-130">Clave ExclusiveAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="61901-130">The ExclusiveAsyncDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61901-131"><strong>dbLockRetry</strong></span><span class="sxs-lookup"><span data-stu-id="61901-131"><strong>dbLockRetry</strong></span></span></p></td>
<td><p><span data-ttu-id="61901-132">Clave LockRetry</span><span class="sxs-lookup"><span data-stu-id="61901-132">The LockRetry key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61901-133"><strong>dbUserCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="61901-133"><strong>dbUserCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="61901-134">Clave UserCommitSync</span><span class="sxs-lookup"><span data-stu-id="61901-134">The UserCommitSync key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61901-135"><strong>dbImplicitCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="61901-135"><strong>dbImplicitCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="61901-136">Clave ImplicitCommitSync</span><span class="sxs-lookup"><span data-stu-id="61901-136">The ImplicitCommitSync key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61901-137"><strong>dbMaxBufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="61901-137"><strong>dbMaxBufferSize</strong></span></span></p></td>
<td><p><span data-ttu-id="61901-138">Clave MaxBufferSize</span><span class="sxs-lookup"><span data-stu-id="61901-138">The MaxBufferSize key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61901-139"><strong>dbMaxLocksPerFile</strong></span><span class="sxs-lookup"><span data-stu-id="61901-139"><strong>dbMaxLocksPerFile</strong></span></span></p></td>
<td><p><span data-ttu-id="61901-140">Clave MaxLocksPerFile</span><span class="sxs-lookup"><span data-stu-id="61901-140">The MaxLocksPerFile key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61901-141"><strong>dbLockDelay</strong></span><span class="sxs-lookup"><span data-stu-id="61901-141"><strong>dbLockDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="61901-142">Clave LockDelay</span><span class="sxs-lookup"><span data-stu-id="61901-142">The LockDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61901-143"><strong>dbRecycleLVs</strong></span><span class="sxs-lookup"><span data-stu-id="61901-143"><strong>dbRecycleLVs</strong></span></span></p></td>
<td><p><span data-ttu-id="61901-144">Clave RecycleLVs</span><span class="sxs-lookup"><span data-stu-id="61901-144">The RecycleLVs key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61901-145"><strong>dbFlushTransactionTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="61901-145"><strong>dbFlushTransactionTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="61901-146">Clave FlushTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="61901-146">The FlushTransactionTimeout key</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="61901-p101">Utilice el método **SetOption** para anular los valores de registro en tiempo de ejecución. Los nuevos valores establecidos con el método **SetOption** siguen en vigor hasta que se cambien de nuevo mediante otra llamada **SetOption** o que se cierre el objeto **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="61901-p101">Use the **SetOption** method to override registry values at run-time. New values established with the **SetOption** method remain in effect until changed again by another **SetOption** call, or until the **DBEngine** object is closed.</span></span>

