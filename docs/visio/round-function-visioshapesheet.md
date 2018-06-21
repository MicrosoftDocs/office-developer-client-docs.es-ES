---
title: Función ROUND (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Redondea un número a la precisión representada por númeroDeDígitos.
ms.openlocfilehash: 2457bdf6b46a2bb44b203497f02cc9b2ff034847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19823014"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="88437-103">Función ROUND (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="88437-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="88437-104">Redondea un número a la precisión representada por *númeroDeDígitos* .</span><span class="sxs-lookup"><span data-stu-id="88437-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="88437-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88437-105">Syntax</span></span>

<span data-ttu-id="88437-106">ROUND (** *número* **, ** *númeroDeDígitos* **)</span><span class="sxs-lookup"><span data-stu-id="88437-106">ROUND(** *number* **, ** *numberofdigits* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="88437-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88437-107">Parameters</span></span>

|<span data-ttu-id="88437-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="88437-108">**Name**</span></span>|<span data-ttu-id="88437-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="88437-109">**Required/Optional**</span></span>|<span data-ttu-id="88437-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="88437-110">**Data Type**</span></span>|<span data-ttu-id="88437-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="88437-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="88437-112">_number_</span><span class="sxs-lookup"><span data-stu-id="88437-112">_number_</span></span> <br/> |<span data-ttu-id="88437-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="88437-113">Required</span></span>  <br/> |<span data-ttu-id="88437-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="88437-114">**Number**</span></span> <br/> |<span data-ttu-id="88437-115">El número que desea redondear.</span><span class="sxs-lookup"><span data-stu-id="88437-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="88437-116">_igual_</span><span class="sxs-lookup"><span data-stu-id="88437-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="88437-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="88437-117">Required</span></span>  <br/> |<span data-ttu-id="88437-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="88437-118">**Number**</span></span> <br/> |<span data-ttu-id="88437-119">El número de posiciones decimales de precisión.</span><span class="sxs-lookup"><span data-stu-id="88437-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88437-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88437-120">Remarks</span></span>

<span data-ttu-id="88437-121">Si _es mayor que 0,_ _número_ se redondea dejando el _númeroDeDígitos_ a la derecha del separador decimal.</span><span class="sxs-lookup"><span data-stu-id="88437-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="88437-122">Si es _igual_ a 0, _número_ se redondeará al entero.</span><span class="sxs-lookup"><span data-stu-id="88437-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="88437-123">Si _es menor que 0,_ _número_ se redondea dejando el _númeroDeDígitos_ a la izquierda del separador decimal.</span><span class="sxs-lookup"><span data-stu-id="88437-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="88437-124">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="88437-124">Example 1</span></span>

<span data-ttu-id="88437-125">ROUND(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="88437-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="88437-126">Devuelve 123,65.</span><span class="sxs-lookup"><span data-stu-id="88437-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="88437-127">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="88437-127">Example 2</span></span>

<span data-ttu-id="88437-128">ROUND(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="88437-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="88437-129">Devuelve 124.</span><span class="sxs-lookup"><span data-stu-id="88437-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="88437-130">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="88437-130">Example 3</span></span>

<span data-ttu-id="88437-131">ROUND(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="88437-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="88437-132">Devuelve 120.</span><span class="sxs-lookup"><span data-stu-id="88437-132">Returns 120.</span></span>
  

