---
title: PNT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
localization_priority: Normal
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: Devuelve el punto representado por las coordenadas x e y como un valor único.
ms.openlocfilehash: be00f7d5ae55f70407e35eca43881a6d3f70ec13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822819"
---
# <a name="pnt-function"></a><span data-ttu-id="28465-103">PNT (función)</span><span class="sxs-lookup"><span data-stu-id="28465-103">PNT Function</span></span>

<span data-ttu-id="28465-104">Devuelve el punto representado por las coordenadas _x_ e _y_ como un valor único.</span><span class="sxs-lookup"><span data-stu-id="28465-104">Returns the point represented by the coordinates  _x_ and  _y_ as a single value.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="28465-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28465-105">Syntax</span></span>

<span data-ttu-id="28465-106">PNT (** *x, y* **)</span><span class="sxs-lookup"><span data-stu-id="28465-106">PNT(** *x,y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="28465-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28465-107">Parameters</span></span>

|<span data-ttu-id="28465-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="28465-108">**Name**</span></span>|<span data-ttu-id="28465-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="28465-109">**Required/Optional**</span></span>|<span data-ttu-id="28465-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="28465-110">**Data Type**</span></span>|<span data-ttu-id="28465-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28465-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="28465-112">_x, y_</span><span class="sxs-lookup"><span data-stu-id="28465-112">_x,y_</span></span> <br/> |<span data-ttu-id="28465-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="28465-113">Required</span></span>  <br/> |<span data-ttu-id="28465-114">**Número, número**</span><span class="sxs-lookup"><span data-stu-id="28465-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="28465-115">Coordenadas del punto en el sistema de coordenadas de la forma actual.</span><span class="sxs-lookup"><span data-stu-id="28465-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="28465-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28465-116">Return value</span></span>

<span data-ttu-id="28465-117">Punto</span><span class="sxs-lookup"><span data-stu-id="28465-117">Point</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28465-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28465-118">Remarks</span></span>

<span data-ttu-id="28465-119">Convertir las coordenadas en puntos permite cambiar la geometría de una forma sin tener que manipular *x* e *y* -coordina por separado.</span><span class="sxs-lookup"><span data-stu-id="28465-119">Converting coordinates to points allows you to change a shape's geometry without having to manipulate  *x*  - and  *y*  -coordinates separately.</span></span> 
  
## <a name="example"></a><span data-ttu-id="28465-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="28465-120">Example</span></span>

<span data-ttu-id="28465-121">PNT(PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="28465-121">PNT(PinX,PinY)</span></span> 
  
<span data-ttu-id="28465-122">Devuelve el punto representado por las coordenadas PinX y PinY.</span><span class="sxs-lookup"><span data-stu-id="28465-122">Returns the point represented by PinX and PinY.</span></span> 
  

