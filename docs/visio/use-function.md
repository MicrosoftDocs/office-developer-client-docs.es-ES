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
description: Se aplica la trama de línea, trama de relleno o extremo de línea llamado nombre a la forma cuando se coloca en la celda LinePattern, FillPattern, BeginArrow o EndArrow.
ms.openlocfilehash: 0b6668e57a8f997a69fece51cbc5bd1b1574a576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823486"
---
# <a name="use-function"></a><span data-ttu-id="67973-103">Función USE</span><span class="sxs-lookup"><span data-stu-id="67973-103">USE Function</span></span>

<span data-ttu-id="67973-104">Se aplica la trama de línea, trama de relleno o extremo de línea llamado _nombre_ a la forma cuando se coloca en la celda LinePattern, FillPattern, BeginArrow o EndArrow.</span><span class="sxs-lookup"><span data-stu-id="67973-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="67973-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67973-105">Syntax</span></span>

<span data-ttu-id="67973-106">USE ("** *nombre* **")</span><span class="sxs-lookup"><span data-stu-id="67973-106">USE(" ** *name* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="67973-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67973-107">Parameters</span></span>

|<span data-ttu-id="67973-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="67973-108">**Name**</span></span>|<span data-ttu-id="67973-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="67973-109">**Required/Optional**</span></span>|<span data-ttu-id="67973-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="67973-110">**Data Type**</span></span>|<span data-ttu-id="67973-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="67973-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="67973-112">_nombre_</span><span class="sxs-lookup"><span data-stu-id="67973-112">_name_</span></span> <br/> |<span data-ttu-id="67973-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="67973-113">Required</span></span>  <br/> |<span data-ttu-id="67973-114">**String**</span><span class="sxs-lookup"><span data-stu-id="67973-114">**String**</span></span> <br/> |<span data-ttu-id="67973-115">Cualquier cadena de texto que sea un nombre de patrón válido.</span><span class="sxs-lookup"><span data-stu-id="67973-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="67973-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67973-116">Return value</span></span>

<span data-ttu-id="67973-117">Number</span><span class="sxs-lookup"><span data-stu-id="67973-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67973-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="67973-118">Remarks</span></span>

<span data-ttu-id="67973-119">Si un patrón con _nombre_ está presente en la Galería de símbolos de documento del documento, el patrón se aplica como patrón de línea, patrón de relleno, flecha inicial o flecha final.</span><span class="sxs-lookup"><span data-stu-id="67973-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="67973-120">Esta función siempre devuelve 254.</span><span class="sxs-lookup"><span data-stu-id="67973-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="67973-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="67973-121">Example</span></span>

<span data-ttu-id="67973-122">USE("Líneas de tren")</span><span class="sxs-lookup"><span data-stu-id="67973-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="67973-123">Aplica el patrón llamado Líneas de tren a la forma que contiene la fórmula para darle formato.</span><span class="sxs-lookup"><span data-stu-id="67973-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

