---
title: Función NOW (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Devuelve el valor de fecha y hora actual.
ms.openlocfilehash: 9e28f51b0e1d1c09a70e54e432a865968c721940
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414084"
---
# <a name="now-function-visioshapesheet"></a><span data-ttu-id="bbb3b-103">Función NOW (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="bbb3b-103">NOW Function (VisioShapeSheet)</span></span>

<span data-ttu-id="bbb3b-104">Devuelve el valor de fecha y hora actual.</span><span class="sxs-lookup"><span data-stu-id="bbb3b-104">Returns the current date and time value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bbb3b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bbb3b-105">Syntax</span></span>

<span data-ttu-id="bbb3b-106">NOW ( )</span><span class="sxs-lookup"><span data-stu-id="bbb3b-106">NOW ( )</span></span>
  
### <a name="return-value"></a><span data-ttu-id="bbb3b-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bbb3b-107">Return value</span></span>

<span data-ttu-id="bbb3b-108">DateTime</span><span class="sxs-lookup"><span data-stu-id="bbb3b-108">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bbb3b-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bbb3b-109">Remarks</span></span>

<span data-ttu-id="bbb3b-110">NOW se calcula automáticamente cada minuto.</span><span class="sxs-lookup"><span data-stu-id="bbb3b-110">NOW is automatically recalculated every minute.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="bbb3b-111">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="bbb3b-111">Example 1</span></span>

<span data-ttu-id="bbb3b-112">NOW( )</span><span class="sxs-lookup"><span data-stu-id="bbb3b-112">NOW( )</span></span>
  
<span data-ttu-id="bbb3b-113">Devuelve la fecha y hora actuales, por ejemplo 27/9/2010 16:03:30.</span><span class="sxs-lookup"><span data-stu-id="bbb3b-113">Returns the current date and time, such as 9/27/2010 12:03:30 PM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="bbb3b-114">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="bbb3b-114">Example 2</span></span>

<span data-ttu-id="bbb3b-115">FORMAT(NOW(),"dd MMM., aaaa hh:mm")</span><span class="sxs-lookup"><span data-stu-id="bbb3b-115">FORMAT(NOW(),"dd MMM., yyyy hh:mm")</span></span>
  
<span data-ttu-id="bbb3b-116">Devuelve la fecha y hora actuales en el formato especificado, por ejemplo 27 Sep., 2010 12:03.</span><span class="sxs-lookup"><span data-stu-id="bbb3b-116">Returns the current date and time formatted as 27 Sep., 2010 12:03.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="bbb3b-117">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="bbb3b-117">Example 3</span></span>

<span data-ttu-id="bbb3b-118">AHORA () + 2EW.</span><span class="sxs-lookup"><span data-stu-id="bbb3b-118">NOW()+2EW.</span></span>
  
<span data-ttu-id="bbb3b-119">Devuelve la fecha y hora actuales más dos semanas, por ejemplo 11/10/10 16:03:30.</span><span class="sxs-lookup"><span data-stu-id="bbb3b-119">Returns the current date and time plus two elapsed weeks, such as 10/11/10 12:03:30 PM.</span></span>
  

