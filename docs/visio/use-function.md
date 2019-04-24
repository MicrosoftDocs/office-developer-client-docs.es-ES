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
description: Aplica la trama de línea, la trama de relleno o el final de línea denominado nombre a la forma cuando se coloca en la celda LinePattern, FillPattern, BeginArrow o endArrow.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337152"
---
# <a name="use-function"></a><span data-ttu-id="ad14d-103">Función USE</span><span class="sxs-lookup"><span data-stu-id="ad14d-103">USE Function</span></span>

<span data-ttu-id="ad14d-104">Aplica la trama de línea, la trama de relleno o el final de línea denominado _nombre_ a la forma cuando se coloca en la celda LinePattern, FillPattern, BeginArrow o EndArrow.</span><span class="sxs-lookup"><span data-stu-id="ad14d-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ad14d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad14d-105">Syntax</span></span>

<span data-ttu-id="ad14d-106">USE ("\* \* *Name* \* \*")</span><span class="sxs-lookup"><span data-stu-id="ad14d-106">USE(" \*\* *name* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ad14d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad14d-107">Parameters</span></span>

|<span data-ttu-id="ad14d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ad14d-108">**Name**</span></span>|<span data-ttu-id="ad14d-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="ad14d-109">**Required/Optional**</span></span>|<span data-ttu-id="ad14d-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ad14d-110">**Data Type**</span></span>|<span data-ttu-id="ad14d-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad14d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ad14d-112">_nombre_</span><span class="sxs-lookup"><span data-stu-id="ad14d-112">_name_</span></span> <br/> |<span data-ttu-id="ad14d-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ad14d-113">Required</span></span>  <br/> |<span data-ttu-id="ad14d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ad14d-114">**String**</span></span> <br/> |<span data-ttu-id="ad14d-115">Cualquier cadena de texto que sea un nombre de patrón válido.</span><span class="sxs-lookup"><span data-stu-id="ad14d-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ad14d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad14d-116">Return value</span></span>

<span data-ttu-id="ad14d-117">Número</span><span class="sxs-lookup"><span data-stu-id="ad14d-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad14d-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad14d-118">Remarks</span></span>

<span data-ttu-id="ad14d-119">Si un patrón denominado _nombre_ está presente en la galería de símbolos de documento del documento, el patrón se aplica como trama de línea, trama de relleno, flecha inicial o flecha final.</span><span class="sxs-lookup"><span data-stu-id="ad14d-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="ad14d-120">Esta función siempre devuelve 254.</span><span class="sxs-lookup"><span data-stu-id="ad14d-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="ad14d-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad14d-121">Example</span></span>

<span data-ttu-id="ad14d-122">USE("Líneas de tren")</span><span class="sxs-lookup"><span data-stu-id="ad14d-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="ad14d-123">Aplica el patrón llamado Líneas de tren a la forma que contiene la fórmula para darle formato.</span><span class="sxs-lookup"><span data-stu-id="ad14d-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

