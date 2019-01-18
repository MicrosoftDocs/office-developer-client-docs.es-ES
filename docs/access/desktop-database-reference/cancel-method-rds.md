---
title: Cancel (método, RDS)
TOCTitle: Cancel method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 35322ec058d31f92288fd06a4e8434a4256c2d74
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720768"
---
# <a name="cancel-method-rds"></a><span data-ttu-id="94325-102">Cancel (método, RDS)</span><span class="sxs-lookup"><span data-stu-id="94325-102">Cancel method (RDS)</span></span>


<span data-ttu-id="94325-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="94325-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="94325-104">Cancela la ejecución de una llamada de método asincrónico pendiente.</span><span class="sxs-lookup"><span data-stu-id="94325-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="94325-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94325-105">Syntax</span></span>

<span data-ttu-id="94325-106">*RDS*.</span><span class="sxs-lookup"><span data-stu-id="94325-106">*RDS*.</span></span> <span data-ttu-id="94325-107">*DataControl*. Cancelar</span><span class="sxs-lookup"><span data-stu-id="94325-107">*DataControl*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="94325-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="94325-108">Remarks</span></span>

<span data-ttu-id="94325-109">Al llamar a **Cancel**, [ReadyState](readystate-property-rds.md) se establece automáticamente en **adcReadyStateLoaded** y el objeto [Recordset](recordset-object-ado.md) estará vacío.</span><span class="sxs-lookup"><span data-stu-id="94325-109">When you call **Cancel**, [ReadyState](readystate-property-rds.md) is automatically set to **adcReadyStateLoaded**, and the [Recordset](recordset-object-ado.md) will be empty.</span></span>

