---
title: USE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251510
localization_priority: Normal
ms.assetid: 410c4187-21f3-d959-750e-9dc6095fba9a
description: Aplica el patrón de línea, el patrón de relleno o el nombre del extremo de línea llamado a la forma cuando se coloca en la celda LinePattern, FillPattern, BeginArrow o EndArrow.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422827"
---
# <a name="use-function"></a><span data-ttu-id="62705-103">Función USE</span><span class="sxs-lookup"><span data-stu-id="62705-103">USE Function</span></span>

<span data-ttu-id="62705-104">Aplica el patrón de línea, el  patrón de relleno o el nombre del extremo de línea llamado a la forma cuando se coloca en la celda LinePattern, FillPattern, BeginArrow o EndArrow.</span><span class="sxs-lookup"><span data-stu-id="62705-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="62705-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62705-105">Syntax</span></span>

<span data-ttu-id="62705-106">USE(" \*\* *name* \*\* ")</span><span class="sxs-lookup"><span data-stu-id="62705-106">USE(" \*\* *name* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="62705-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62705-107">Parameters</span></span>

|<span data-ttu-id="62705-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="62705-108">**Name**</span></span>|<span data-ttu-id="62705-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="62705-109">**Required/Optional**</span></span>|<span data-ttu-id="62705-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="62705-110">**Data Type**</span></span>|<span data-ttu-id="62705-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="62705-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="62705-112">_nombre_</span><span class="sxs-lookup"><span data-stu-id="62705-112">_name_</span></span> <br/> |<span data-ttu-id="62705-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="62705-113">Required</span></span>  <br/> |<span data-ttu-id="62705-114">**String**</span><span class="sxs-lookup"><span data-stu-id="62705-114">**String**</span></span> <br/> |<span data-ttu-id="62705-115">Cualquier cadena de texto que sea un nombre de patrón válido.</span><span class="sxs-lookup"><span data-stu-id="62705-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="62705-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62705-116">Return value</span></span>

<span data-ttu-id="62705-117">Número</span><span class="sxs-lookup"><span data-stu-id="62705-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="62705-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="62705-118">Remarks</span></span>

<span data-ttu-id="62705-119">Si un patrón con nombre  _de nombre_ está presente en la galería de símbolos del documento, el patrón se aplica como un patrón de línea, patrón de relleno, flecha de inicio o flecha final.</span><span class="sxs-lookup"><span data-stu-id="62705-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="62705-120">Esta función siempre devuelve 254.</span><span class="sxs-lookup"><span data-stu-id="62705-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="62705-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="62705-121">Example</span></span>

<span data-ttu-id="62705-122">USE("Líneas de tren")</span><span class="sxs-lookup"><span data-stu-id="62705-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="62705-123">Aplica el patrón llamado Líneas de tren a la forma que contiene la fórmula para darle formato.</span><span class="sxs-lookup"><span data-stu-id="62705-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

