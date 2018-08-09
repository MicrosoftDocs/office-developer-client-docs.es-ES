---
title: TRUNC (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
localization_priority: Normal
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: Devuelve un número truncado al número de decimales especificado.
ms.openlocfilehash: 8f6a9798391d308a234469d93bc8f481de5fc8da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823442"
---
# <a name="trunc-function"></a><span data-ttu-id="ced98-103">Función TRUNC</span><span class="sxs-lookup"><span data-stu-id="ced98-103">TRUNC Function</span></span>

<span data-ttu-id="ced98-104">Devuelve un número truncado al número de decimales especificado.</span><span class="sxs-lookup"><span data-stu-id="ced98-104">Returns a number truncated to the specified number of digits.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ced98-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ced98-105">Syntax</span></span>

<span data-ttu-id="ced98-106">TRUNC (** *número* **, ** *númeroDeDígitos* **)</span><span class="sxs-lookup"><span data-stu-id="ced98-106">TRUNC(** *number* **, ** *numberofdigits* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ced98-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ced98-107">Parameters</span></span>

|<span data-ttu-id="ced98-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ced98-108">**Name**</span></span>|<span data-ttu-id="ced98-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="ced98-109">**Required/Optional**</span></span>|<span data-ttu-id="ced98-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ced98-110">**Data Type**</span></span>|<span data-ttu-id="ced98-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ced98-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ced98-112">_number_</span><span class="sxs-lookup"><span data-stu-id="ced98-112">_number_</span></span> <br/> |<span data-ttu-id="ced98-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ced98-113">Required</span></span>  <br/> |<span data-ttu-id="ced98-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="ced98-114">**Numeric**</span></span> <br/> |<span data-ttu-id="ced98-115">El número que desea truncar.</span><span class="sxs-lookup"><span data-stu-id="ced98-115">The number to truncate.</span></span>  <br/> |
| <span data-ttu-id="ced98-116">_igual_</span><span class="sxs-lookup"><span data-stu-id="ced98-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="ced98-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ced98-117">Required</span></span>  <br/> |<span data-ttu-id="ced98-118">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="ced98-118">**Numeric**</span></span> <br/> |<span data-ttu-id="ced98-119">El número de dígitos al que se trunque _número_.</span><span class="sxs-lookup"><span data-stu-id="ced98-119">The number of digits to which to truncate  _number_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ced98-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ced98-120">Return value</span></span>

<span data-ttu-id="ced98-121">Numeric.</span><span class="sxs-lookup"><span data-stu-id="ced98-121">Numeric.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ced98-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ced98-122">Remarks</span></span>

<span data-ttu-id="ced98-123">Si _es mayor que 0,_ _número_ se trunca a _númeroDeDígitos_ a la derecha del separador decimal.</span><span class="sxs-lookup"><span data-stu-id="ced98-123">If  _numberofdigits_ is greater than 0,  _number_ is truncated to  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="ced98-124">Si es _igual_ a 0, _número_ se trunca a un valor entero.</span><span class="sxs-lookup"><span data-stu-id="ced98-124">If  _numberofdigits_ is 0,  _number_ is truncated to an integer.</span></span> <span data-ttu-id="ced98-125">Si _es menor que 0,_ _número_ se trunca a _númeroDeDígitos_ a la izquierda del separador decimal.</span><span class="sxs-lookup"><span data-stu-id="ced98-125">If  _numberofdigits_ is less than 0,  _number_ is truncated to  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ced98-126">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="ced98-126">Example 1</span></span>

<span data-ttu-id="ced98-127">TRUNC(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="ced98-127">TRUNC(123.654,2)</span></span>
  
<span data-ttu-id="ced98-128">Devuelve 123,65.</span><span class="sxs-lookup"><span data-stu-id="ced98-128">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ced98-129">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="ced98-129">Example 2</span></span>

<span data-ttu-id="ced98-130">TRUNC(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="ced98-130">TRUNC(123.654,0)</span></span>
  
<span data-ttu-id="ced98-131">Devuelve 123.</span><span class="sxs-lookup"><span data-stu-id="ced98-131">Returns 123.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ced98-132">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="ced98-132">Example 3</span></span>

<span data-ttu-id="ced98-133">TRUNC(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="ced98-133">TRUNC(123.654,-1)</span></span>
  
<span data-ttu-id="ced98-134">Devuelve 120.</span><span class="sxs-lookup"><span data-stu-id="ced98-134">Returns 120.</span></span>
  

