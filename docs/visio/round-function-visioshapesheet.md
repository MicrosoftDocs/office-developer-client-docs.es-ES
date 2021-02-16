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
description: Redondea un número a la precisión representada por numberofdigits .
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439971"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="2eedd-103">Función ROUND (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="2eedd-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="2eedd-104">Redondea un número a la precisión representada por  *numberofdigits*  .</span><span class="sxs-lookup"><span data-stu-id="2eedd-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2eedd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2eedd-105">Syntax</span></span>

<span data-ttu-id="2eedd-106">ROUND(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span><span class="sxs-lookup"><span data-stu-id="2eedd-106">ROUND(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2eedd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2eedd-107">Parameters</span></span>

|<span data-ttu-id="2eedd-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2eedd-108">**Name**</span></span>|<span data-ttu-id="2eedd-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="2eedd-109">**Required/Optional**</span></span>|<span data-ttu-id="2eedd-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="2eedd-110">**Data Type**</span></span>|<span data-ttu-id="2eedd-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2eedd-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2eedd-112">_number_</span><span class="sxs-lookup"><span data-stu-id="2eedd-112">_number_</span></span> <br/> |<span data-ttu-id="2eedd-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2eedd-113">Required</span></span>  <br/> |<span data-ttu-id="2eedd-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="2eedd-114">**Number**</span></span> <br/> |<span data-ttu-id="2eedd-115">El número que desea redondear.</span><span class="sxs-lookup"><span data-stu-id="2eedd-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="2eedd-116">_numberofdigits_</span><span class="sxs-lookup"><span data-stu-id="2eedd-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="2eedd-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2eedd-117">Required</span></span>  <br/> |<span data-ttu-id="2eedd-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="2eedd-118">**Number**</span></span> <br/> |<span data-ttu-id="2eedd-119">El número de posiciones decimales de precisión.</span><span class="sxs-lookup"><span data-stu-id="2eedd-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2eedd-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2eedd-120">Remarks</span></span>

<span data-ttu-id="2eedd-121">Si  _numberofdigits_ es mayor que 0,  _el_ número se redondea  _por numberofdigits_ a la derecha del decimal.</span><span class="sxs-lookup"><span data-stu-id="2eedd-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="2eedd-122">Si  _numberofdigits es_ 0,  _el número_ se redondea a un entero.</span><span class="sxs-lookup"><span data-stu-id="2eedd-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="2eedd-123">Si  _numberofdigits_ es menor que 0,  _el_ número se redondea  _por numberofdigits_ a la izquierda del decimal.</span><span class="sxs-lookup"><span data-stu-id="2eedd-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="2eedd-124">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="2eedd-124">Example 1</span></span>

<span data-ttu-id="2eedd-125">ROUND(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="2eedd-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="2eedd-126">Devuelve 123,65.</span><span class="sxs-lookup"><span data-stu-id="2eedd-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="2eedd-127">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="2eedd-127">Example 2</span></span>

<span data-ttu-id="2eedd-128">ROUND(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="2eedd-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="2eedd-129">Devuelve 124.</span><span class="sxs-lookup"><span data-stu-id="2eedd-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="2eedd-130">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="2eedd-130">Example 3</span></span>

<span data-ttu-id="2eedd-131">ROUND(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="2eedd-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="2eedd-132">Devuelve 120.</span><span class="sxs-lookup"><span data-stu-id="2eedd-132">Returns 120.</span></span>
  

