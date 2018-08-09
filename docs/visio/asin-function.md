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
description: Devuelve el arcoseno de un número, por ejemplo, el ángulo cuyo seno es ese número.
ms.openlocfilehash: e5ed8f9fc8c85ac4816fede03bfe6f6af5cbf5f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821562"
---
# <a name="asin-function"></a><span data-ttu-id="b4c4d-103">Función ASIN</span><span class="sxs-lookup"><span data-stu-id="b4c4d-103">ASIN Function</span></span>

<span data-ttu-id="b4c4d-104">Devuelve el arcoseno de un número, por ejemplo, el ángulo cuyo seno es ese *número* .</span><span class="sxs-lookup"><span data-stu-id="b4c4d-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b4c4d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4c4d-105">Syntax</span></span>

<span data-ttu-id="b4c4d-106">ASIN (** *número* **)</span><span class="sxs-lookup"><span data-stu-id="b4c4d-106">ASIN(** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b4c4d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4c4d-107">Parameters</span></span>

|<span data-ttu-id="b4c4d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b4c4d-108">**Name**</span></span>|<span data-ttu-id="b4c4d-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="b4c4d-109">**Required/Optional**</span></span>|<span data-ttu-id="b4c4d-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="b4c4d-110">**Data Type**</span></span>|<span data-ttu-id="b4c4d-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b4c4d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b4c4d-112">_number_</span><span class="sxs-lookup"><span data-stu-id="b4c4d-112">_number_</span></span> <br/> |<span data-ttu-id="b4c4d-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b4c4d-113">Required</span></span>  <br/> |<span data-ttu-id="b4c4d-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="b4c4d-114">**Numeric**</span></span> <br/> |<span data-ttu-id="b4c4d-115">El seno del ángulo.</span><span class="sxs-lookup"><span data-stu-id="b4c4d-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4c4d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4c4d-116">Remarks</span></span>

<span data-ttu-id="b4c4d-117">El valor de entrada debe estar en el intervalo entre -1 < = *número* < = 1, o un #NUM!</span><span class="sxs-lookup"><span data-stu-id="b4c4d-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="b4c4d-118">se devuelve el error.</span><span class="sxs-lookup"><span data-stu-id="b4c4d-118">error is returned.</span></span> <span data-ttu-id="b4c4d-119">El ángulo resultante está en el intervalo -PI/2 < = *ángulo* < = PI/2 radianes (-90 < = *ángulo* < = 90 grados).</span><span class="sxs-lookup"><span data-stu-id="b4c4d-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="b4c4d-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b4c4d-120">Example</span></span>

<span data-ttu-id="b4c4d-121">ASIN(1)</span><span class="sxs-lookup"><span data-stu-id="b4c4d-121">ASIN(1)</span></span>
  
<span data-ttu-id="b4c4d-122">Devuelve 90 grados.</span><span class="sxs-lookup"><span data-stu-id="b4c4d-122">Returns 90 deg</span></span>
  

