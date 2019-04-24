---
title: ASIN (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
localization_priority: Normal
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Devuelve el arcoseno de un número; por ejemplo, el ángulo cuyo seno es número.
ms.openlocfilehash: a7585dc07053466203f11cc04ce249ceb62fbda0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341527"
---
# <a name="asin-function"></a><span data-ttu-id="7128d-103">Función ASIN</span><span class="sxs-lookup"><span data-stu-id="7128d-103">ASIN Function</span></span>

<span data-ttu-id="7128d-104">Devuelve el arcoseno de un número; por ejemplo, el ángulo cuyo seno es *número* .</span><span class="sxs-lookup"><span data-stu-id="7128d-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7128d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7128d-105">Syntax</span></span>

<span data-ttu-id="7128d-106">ASENo (\* \* *número* \* \*)</span><span class="sxs-lookup"><span data-stu-id="7128d-106">ASIN(\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7128d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7128d-107">Parameters</span></span>

|<span data-ttu-id="7128d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="7128d-108">**Name**</span></span>|<span data-ttu-id="7128d-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="7128d-109">**Required/Optional**</span></span>|<span data-ttu-id="7128d-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="7128d-110">**Data Type**</span></span>|<span data-ttu-id="7128d-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7128d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7128d-112">_number_</span><span class="sxs-lookup"><span data-stu-id="7128d-112">_number_</span></span> <br/> |<span data-ttu-id="7128d-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7128d-113">Required</span></span>  <br/> |<span data-ttu-id="7128d-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="7128d-114">**Numeric**</span></span> <br/> |<span data-ttu-id="7128d-115">El seno del ángulo.</span><span class="sxs-lookup"><span data-stu-id="7128d-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7128d-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7128d-116">Remarks</span></span>

<span data-ttu-id="7128d-117">El valor de entrada debe estar en el intervalo-1 < = *número* < = 1, o un #NUM!</span><span class="sxs-lookup"><span data-stu-id="7128d-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="7128d-118">se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="7128d-118">error is returned.</span></span> <span data-ttu-id="7128d-119">El ángulo resultante está en el intervalo-PI/2 < = *Angle* _LT_ = pi/2 radianes (-90 < = *angle* < = 90 grados).</span><span class="sxs-lookup"><span data-stu-id="7128d-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="7128d-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7128d-120">Example</span></span>

<span data-ttu-id="7128d-121">ASENO (1)</span><span class="sxs-lookup"><span data-stu-id="7128d-121">ASIN(1)</span></span>
  
<span data-ttu-id="7128d-122">Devuelve 90 grados.</span><span class="sxs-lookup"><span data-stu-id="7128d-122">Returns 90 deg</span></span>
  

