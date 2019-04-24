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
description: Devuelve un número truncado en el número de dígitos especificado.
ms.openlocfilehash: 5b2138ff3091f70313344d5b38d8225d572d8e70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335178"
---
# <a name="trunc-function"></a><span data-ttu-id="16160-103">Función TRUNC</span><span class="sxs-lookup"><span data-stu-id="16160-103">TRUNC Function</span></span>

<span data-ttu-id="16160-104">Devuelve un número truncado en el número de dígitos especificado.</span><span class="sxs-lookup"><span data-stu-id="16160-104">Returns a number truncated to the specified number of digits.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="16160-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16160-105">Syntax</span></span>

<span data-ttu-id="16160-106">TRUNC (\* \* *número* \* \*, \* \* *númeroDeDígitos* \* \*)</span><span class="sxs-lookup"><span data-stu-id="16160-106">TRUNC(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="16160-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16160-107">Parameters</span></span>

|<span data-ttu-id="16160-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="16160-108">**Name**</span></span>|<span data-ttu-id="16160-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="16160-109">**Required/Optional**</span></span>|<span data-ttu-id="16160-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="16160-110">**Data Type**</span></span>|<span data-ttu-id="16160-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="16160-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="16160-112">_number_</span><span class="sxs-lookup"><span data-stu-id="16160-112">_number_</span></span> <br/> |<span data-ttu-id="16160-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="16160-113">Required</span></span>  <br/> |<span data-ttu-id="16160-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="16160-114">**Numeric**</span></span> <br/> |<span data-ttu-id="16160-115">El número que desea truncar.</span><span class="sxs-lookup"><span data-stu-id="16160-115">The number to truncate.</span></span>  <br/> |
| <span data-ttu-id="16160-116">_númeroDeDígitos_</span><span class="sxs-lookup"><span data-stu-id="16160-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="16160-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="16160-117">Required</span></span>  <br/> |<span data-ttu-id="16160-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="16160-118">**Numeric**</span></span> <br/> |<span data-ttu-id="16160-119">Número de dígitos al que se va a truncar el _número_.</span><span class="sxs-lookup"><span data-stu-id="16160-119">The number of digits to which to truncate  _number_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="16160-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16160-120">Return value</span></span>

<span data-ttu-id="16160-121">Numérico.</span><span class="sxs-lookup"><span data-stu-id="16160-121">Numeric.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16160-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="16160-122">Remarks</span></span>

<span data-ttu-id="16160-123">Si _númeroDeDígitos_ es mayor que 0, el _número_ se trunca a _númeroDeDígitos_ a la derecha del separador decimal.</span><span class="sxs-lookup"><span data-stu-id="16160-123">If  _numberofdigits_ is greater than 0,  _number_ is truncated to  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="16160-124">Si _númeroDeDígitos_ es 0, el _número_ se trunca a un entero.</span><span class="sxs-lookup"><span data-stu-id="16160-124">If  _numberofdigits_ is 0,  _number_ is truncated to an integer.</span></span> <span data-ttu-id="16160-125">Si _númeroDeDígitos_ es menor que 0, el _número_ se trunca _dejando númeroDeDígitos_ a la izquierda del separador decimal.</span><span class="sxs-lookup"><span data-stu-id="16160-125">If  _numberofdigits_ is less than 0,  _number_ is truncated to  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="16160-126">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="16160-126">Example 1</span></span>

<span data-ttu-id="16160-127">TRUNC (123.654, 2)</span><span class="sxs-lookup"><span data-stu-id="16160-127">TRUNC(123.654,2)</span></span>
  
<span data-ttu-id="16160-128">Devuelve 123,65.</span><span class="sxs-lookup"><span data-stu-id="16160-128">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="16160-129">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="16160-129">Example 2</span></span>

<span data-ttu-id="16160-130">TRUNC (123.654, 0)</span><span class="sxs-lookup"><span data-stu-id="16160-130">TRUNC(123.654,0)</span></span>
  
<span data-ttu-id="16160-131">Devuelve 123.</span><span class="sxs-lookup"><span data-stu-id="16160-131">Returns 123.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="16160-132">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="16160-132">Example 3</span></span>

<span data-ttu-id="16160-133">TRUNC (123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="16160-133">TRUNC(123.654,-1)</span></span>
  
<span data-ttu-id="16160-134">Devuelve 120.</span><span class="sxs-lookup"><span data-stu-id="16160-134">Returns 120.</span></span>
  

