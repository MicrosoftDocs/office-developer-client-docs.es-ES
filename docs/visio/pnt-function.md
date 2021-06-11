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
description: Devuelve el punto representado por las coordenadas x e y como un único valor.
ms.openlocfilehash: c0a12aa18f4c766ea1f5b0fa1d827804d766713c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435715"
---
# <a name="pnt-function"></a><span data-ttu-id="88983-103">Función PNT</span><span class="sxs-lookup"><span data-stu-id="88983-103">PNT Function</span></span>

<span data-ttu-id="88983-104">Devuelve el punto representado por las coordenadas  _x_  _e y_ como un único valor.</span><span class="sxs-lookup"><span data-stu-id="88983-104">Returns the point represented by the coordinates  _x_ and  _y_ as a single value.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="88983-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88983-105">Syntax</span></span>

<span data-ttu-id="88983-106">PNT(\*\* *x,y* \*\* )</span><span class="sxs-lookup"><span data-stu-id="88983-106">PNT(\*\* *x,y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="88983-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88983-107">Parameters</span></span>

|<span data-ttu-id="88983-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="88983-108">**Name**</span></span>|<span data-ttu-id="88983-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="88983-109">**Required/Optional**</span></span>|<span data-ttu-id="88983-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="88983-110">**Data Type**</span></span>|<span data-ttu-id="88983-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="88983-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="88983-112">_x,y_</span><span class="sxs-lookup"><span data-stu-id="88983-112">_x,y_</span></span> <br/> |<span data-ttu-id="88983-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="88983-113">Required</span></span>  <br/> |<span data-ttu-id="88983-114">**Number, Number**</span><span class="sxs-lookup"><span data-stu-id="88983-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="88983-115">Coordenadas del punto en el sistema de coordenadas de la forma actual.</span><span class="sxs-lookup"><span data-stu-id="88983-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="88983-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88983-116">Return value</span></span>

<span data-ttu-id="88983-117">Point</span><span class="sxs-lookup"><span data-stu-id="88983-117">Point</span></span>
  
## <a name="remarks"></a><span data-ttu-id="88983-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="88983-118">Remarks</span></span>

<span data-ttu-id="88983-119">La conversión de coordenadas en puntos permite cambiar la geometría de una forma sin tener que manipular las coordenadas  *x*  -  *e y*  por separado.</span><span class="sxs-lookup"><span data-stu-id="88983-119">Converting coordinates to points allows you to change a shape's geometry without having to manipulate  *x*  - and  *y*  -coordinates separately.</span></span> 
  
## <a name="example"></a><span data-ttu-id="88983-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88983-120">Example</span></span>

<span data-ttu-id="88983-121">PNT(PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="88983-121">PNT(PinX,PinY)</span></span> 
  
<span data-ttu-id="88983-122">Devuelve el punto representado por las coordenadas PinX y PinY.</span><span class="sxs-lookup"><span data-stu-id="88983-122">Returns the point represented by PinX and PinY.</span></span> 
  

