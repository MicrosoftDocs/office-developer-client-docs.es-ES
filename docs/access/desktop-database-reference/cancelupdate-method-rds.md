---
title: Método CancelUpdate (RDS)
TOCTitle: CancelUpdate method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b0c02a9ca72add763e1d3ccf62d5ede8adaecc6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296671"
---
# <a name="cancelupdate-method-rds"></a><span data-ttu-id="3c1dd-102">Método CancelUpdate (RDS)</span><span class="sxs-lookup"><span data-stu-id="3c1dd-102">CancelUpdate method (RDS)</span></span>

<span data-ttu-id="3c1dd-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c1dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c1dd-104">Cancela los cambios realizados en la fila actual o nueva de un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3c1dd-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c1dd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c1dd-105">Syntax</span></span>

<span data-ttu-id="3c1dd-106">*DataControl*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="3c1dd-106">*DataControl*.CancelUpdate</span></span>

## <a name="parameters"></a><span data-ttu-id="3c1dd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c1dd-107">Parameters</span></span>

|<span data-ttu-id="3c1dd-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3c1dd-108">Parameter</span></span>|<span data-ttu-id="3c1dd-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c1dd-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3c1dd-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="3c1dd-110">*DataControl*</span></span> |<span data-ttu-id="3c1dd-111">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="3c1dd-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3c1dd-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3c1dd-112">Remarks</span></span>

<span data-ttu-id="3c1dd-p101">El Servicio de cursor para OLE DB mantiene una copia de los valores originales y una caché de los cambios. Al llamar a **CancelUpdate**, la caché de cambios se restablece en una caché vacía y los controles enlazados se actualizan con los datos originales.</span><span class="sxs-lookup"><span data-stu-id="3c1dd-p101">The Cursor Service for OLE DB keeps both a copy of the original values and a cache of changes. When you call **CancelUpdate**, the cache of changes is reset to empty, and any bound controls are refreshed with the original data.</span></span>

