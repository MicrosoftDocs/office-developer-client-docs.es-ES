---
title: PAR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251477
localization_priority: Normal
ms.assetid: 9caf424d-cb70-8f1a-b984-64cf776bdfb4
description: Devuelve las coordenadas x,y de un punto en el sistema de coordenadas del elemento primario de la forma.
ms.openlocfilehash: 4e7517c4210db31f1c3f5dc8bf98185b6f4104aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414511"
---
# <a name="par-function"></a><span data-ttu-id="f1daa-103">Función PAR</span><span class="sxs-lookup"><span data-stu-id="f1daa-103">PAR Function</span></span>

<span data-ttu-id="f1daa-104">Devuelve las  _coordenadas x,y_ de un punto en el sistema de coordenadas del elemento primario de la forma.</span><span class="sxs-lookup"><span data-stu-id="f1daa-104">Returns the  _x,y_ coordinates of a point in the coordinate system of the shape's parent.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f1daa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1daa-105">Syntax</span></span>

<span data-ttu-id="f1daa-106">PAR(\*\* *point* \*\* )</span><span class="sxs-lookup"><span data-stu-id="f1daa-106">PAR(\*\* *point* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f1daa-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1daa-107">Parameters</span></span>

|<span data-ttu-id="f1daa-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f1daa-108">**Name**</span></span>|<span data-ttu-id="f1daa-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="f1daa-109">**Required/Optional**</span></span>|<span data-ttu-id="f1daa-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="f1daa-110">**Data Type**</span></span>|<span data-ttu-id="f1daa-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1daa-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f1daa-112">_punto_</span><span class="sxs-lookup"><span data-stu-id="f1daa-112">_point_</span></span> <br/> |<span data-ttu-id="f1daa-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f1daa-113">Required</span></span>  <br/> |<span data-ttu-id="f1daa-114">**Number, Number**</span><span class="sxs-lookup"><span data-stu-id="f1daa-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="f1daa-115">Coordenadas del punto en el sistema de coordenadas de la forma actual.</span><span class="sxs-lookup"><span data-stu-id="f1daa-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1daa-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1daa-116">Remarks</span></span>

<span data-ttu-id="f1daa-117">En Microsoft Visio, un punto es un valor único que incluye un par de *coordenadas x* e *y.*</span><span class="sxs-lookup"><span data-stu-id="f1daa-117">In Microsoft Visio, a point is a single value that embodies a pair of  *x*  - and  *y*  -coordinates.</span></span> <span data-ttu-id="f1daa-118">Si la forma se encuentra en un grupo, su forma principal es el propio grupo.</span><span class="sxs-lookup"><span data-stu-id="f1daa-118">If the shape is in a group, its parent is the group.</span></span> <span data-ttu-id="f1daa-119">Si no se encuentra en un grupo, su forma principal es la página.</span><span class="sxs-lookup"><span data-stu-id="f1daa-119">If the shape is not in a group, its parent is the page.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f1daa-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f1daa-120">Example</span></span>

<span data-ttu-id="f1daa-121">PAR(PNT(PinX,PinY))</span><span class="sxs-lookup"><span data-stu-id="f1daa-121">PAR(PNT(PinX,PinY))</span></span> 
  
<span data-ttu-id="f1daa-p102">En esta expresión, PNT convierte en un punto un par de coordenadas dentro de la forma actual. PAR convierte a continuación el punto en un par de coordenadas cuyo origen es la esquina inferior izquierda de la página o del grupo que contiene la forma actual.</span><span class="sxs-lookup"><span data-stu-id="f1daa-p102">In this expression, PNT converts a pair of coordinates in the current shape into a point. PAR then converts the point into a pair of coordinates in relation to the lower-left corner of the page or group that contains the current shape.</span></span> 
  

