---
title: Cancel (método, RDS)
TOCTitle: Cancel Method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8455496e8d426d26f56b902d9a089d236bde1a6a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868752"
---
# <a name="cancel-method-rds"></a><span data-ttu-id="4d081-102">Cancel (método, RDS)</span><span class="sxs-lookup"><span data-stu-id="4d081-102">Cancel Method (RDS)</span></span>


<span data-ttu-id="4d081-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d081-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4d081-104">Cancela la ejecución de una llamada de método asincrónico pendiente.</span><span class="sxs-lookup"><span data-stu-id="4d081-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d081-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d081-105">Syntax</span></span>

<span data-ttu-id="4d081-106">*RDS*.</span><span class="sxs-lookup"><span data-stu-id="4d081-106">*RDS*.</span></span> <span data-ttu-id="4d081-107">*DataControl*. Cancelar</span><span class="sxs-lookup"><span data-stu-id="4d081-107">*DataControl*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="4d081-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d081-108">Remarks</span></span>

<span data-ttu-id="4d081-109">Al llamar a **Cancel**, [ReadyState](readystate-property-rds.md) se establece automáticamente en **adcReadyStateLoaded** y el objeto [Recordset](recordset-object-ado.md) estará vacío.</span><span class="sxs-lookup"><span data-stu-id="4d081-109">When you call **Cancel**, [ReadyState](readystate-property-rds.md) is automatically set to **adcReadyStateLoaded**, and the [Recordset](recordset-object-ado.md) will be empty.</span></span>

