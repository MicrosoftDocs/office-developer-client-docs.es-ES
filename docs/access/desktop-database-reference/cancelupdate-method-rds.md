---
title: CancelUpdate (método, RDS)
TOCTitle: CancelUpdate Method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28216cbeb98a0ebc7dfbc6115ea8bc05fadc057f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887750"
---
# <a name="cancelupdate-method-rds"></a><span data-ttu-id="f2ebc-102">CancelUpdate (método, RDS)</span><span class="sxs-lookup"><span data-stu-id="f2ebc-102">CancelUpdate Method (RDS)</span></span>


<span data-ttu-id="f2ebc-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2ebc-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="f2ebc-104">Cancela los cambios realizados en la fila actual o nueva de un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f2ebc-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2ebc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2ebc-105">Syntax</span></span>

<span data-ttu-id="f2ebc-106">*DataControl*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="f2ebc-106">*DataControl*.CancelUpdate</span></span>

## <a name="parameters"></a><span data-ttu-id="f2ebc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2ebc-107">Parameters</span></span>

  - <span data-ttu-id="f2ebc-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="f2ebc-108">*DataControl*</span></span>

  - <span data-ttu-id="f2ebc-109">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="f2ebc-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2ebc-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f2ebc-110">Remarks</span></span>

<span data-ttu-id="f2ebc-p101">El Servicio de cursor para OLE DB mantiene una copia de los valores originales y una caché de los cambios. Al llamar a **CancelUpdate**, la caché de cambios se restablece en una caché vacía y los controles enlazados se actualizan con los datos originales.</span><span class="sxs-lookup"><span data-stu-id="f2ebc-p101">The Cursor Service for OLE DB keeps both a copy of the original values and a cache of changes. When you call **CancelUpdate**, the cache of changes is reset to empty, and any bound controls are refreshed with the original data.</span></span>

