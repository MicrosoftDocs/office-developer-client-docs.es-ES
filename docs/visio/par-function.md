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
description: Devuelve las coordenadas x, y de un punto en el sistema de coordenadas de principal la forma.
ms.openlocfilehash: a3f7afd3f9bc988a20526451a6d7d7081d27a2d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822729"
---
# <a name="par-function"></a><span data-ttu-id="146a5-103">Función PAR</span><span class="sxs-lookup"><span data-stu-id="146a5-103">PAR Function</span></span>

<span data-ttu-id="146a5-104">Devuelve las coordenadas _x, y_ de un punto en el sistema de coordenadas de principal la forma.</span><span class="sxs-lookup"><span data-stu-id="146a5-104">Returns the  _x,y_ coordinates of a point in the coordinate system of the shape's parent.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="146a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="146a5-105">Syntax</span></span>

<span data-ttu-id="146a5-106">NOMINAL (** *Elija* **)</span><span class="sxs-lookup"><span data-stu-id="146a5-106">PAR(** *point* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="146a5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="146a5-107">Parameters</span></span>

|<span data-ttu-id="146a5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="146a5-108">**Name**</span></span>|<span data-ttu-id="146a5-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="146a5-109">**Required/Optional**</span></span>|<span data-ttu-id="146a5-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="146a5-110">**Data Type**</span></span>|<span data-ttu-id="146a5-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="146a5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="146a5-112">_punto_</span><span class="sxs-lookup"><span data-stu-id="146a5-112">_point_</span></span> <br/> |<span data-ttu-id="146a5-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="146a5-113">Required</span></span>  <br/> |<span data-ttu-id="146a5-114">**Number, Number**</span><span class="sxs-lookup"><span data-stu-id="146a5-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="146a5-115">Coordenadas del punto en el sistema de coordenadas de la forma actual.</span><span class="sxs-lookup"><span data-stu-id="146a5-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="146a5-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="146a5-116">Remarks</span></span>

<span data-ttu-id="146a5-117">En Microsoft Visio, un punto es un valor único que incluye un par de *x* e *y* -coordenadas.</span><span class="sxs-lookup"><span data-stu-id="146a5-117">In Microsoft Visio, a point is a single value that embodies a pair of  *x*  - and  *y*  -coordinates.</span></span> <span data-ttu-id="146a5-118">Si la forma está en un grupo, su elemento primario es el grupo.</span><span class="sxs-lookup"><span data-stu-id="146a5-118">If the shape is in a group, its parent is the group.</span></span> <span data-ttu-id="146a5-119">Si la forma no es un grupo, su forma principal es la página.</span><span class="sxs-lookup"><span data-stu-id="146a5-119">If the shape is not in a group, its parent is the page.</span></span> 
  
## <a name="example"></a><span data-ttu-id="146a5-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="146a5-120">Example</span></span>

<span data-ttu-id="146a5-121">PAR(PNT(PinX,PinY))</span><span class="sxs-lookup"><span data-stu-id="146a5-121">PAR(PNT(PinX,PinY))</span></span> 
  
<span data-ttu-id="146a5-p102">En esta expresión, PNT convierte en un punto un par de coordenadas dentro de la forma actual. PAR convierte a continuación el punto en un par de coordenadas cuyo origen es la esquina inferior izquierda de la página o del grupo que contiene la forma actual.</span><span class="sxs-lookup"><span data-stu-id="146a5-p102">In this expression, PNT converts a pair of coordinates in the current shape into a point. PAR then converts the point into a pair of coordinates in relation to the lower-left corner of the page or group that contains the current shape.</span></span> 
  

