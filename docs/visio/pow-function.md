---
title: POW (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
localization_priority: Normal
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: Devuelve un número elevado a la potencia de un exponente.
ms.openlocfilehash: 7a1102aa13f54d7e323247b83af3732ebb63acf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406314"
---
# <a name="pow-function"></a><span data-ttu-id="c5198-103">Función POW</span><span class="sxs-lookup"><span data-stu-id="c5198-103">POW Function</span></span>

<span data-ttu-id="c5198-104">Devuelve un número elevado a la potencia de un exponente.</span><span class="sxs-lookup"><span data-stu-id="c5198-104">Returns a number raised to the power of an exponent.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c5198-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5198-105">Syntax</span></span>

<span data-ttu-id="c5198-106">POW(\*\* *number* \*\*, \*\* *exponent* \*\* )</span><span class="sxs-lookup"><span data-stu-id="c5198-106">POW(\*\* *number* \*\*, \*\* *exponent* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c5198-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5198-107">Parameters</span></span>

|<span data-ttu-id="c5198-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c5198-108">**Name**</span></span>|<span data-ttu-id="c5198-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="c5198-109">**Required/Optional**</span></span>|<span data-ttu-id="c5198-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="c5198-110">**Data Type**</span></span>|<span data-ttu-id="c5198-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5198-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c5198-112">_number_</span><span class="sxs-lookup"><span data-stu-id="c5198-112">_number_</span></span> <br/> |<span data-ttu-id="c5198-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c5198-113">Required</span></span>  <br/> |<span data-ttu-id="c5198-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="c5198-114">**Number**</span></span> <br/> |<span data-ttu-id="c5198-115">El número para elevar la potencia del exponente.</span><span class="sxs-lookup"><span data-stu-id="c5198-115">The number to raise to the power of an exponent.</span></span>  <br/> |
| <span data-ttu-id="c5198-116">_exponent_</span><span class="sxs-lookup"><span data-stu-id="c5198-116">_exponent_</span></span> <br/> |<span data-ttu-id="c5198-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c5198-117">Required</span></span>  <br/> |<span data-ttu-id="c5198-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="c5198-118">**Number**</span></span> <br/> |<span data-ttu-id="c5198-119">El exponente.</span><span class="sxs-lookup"><span data-stu-id="c5198-119">The exponent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5198-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c5198-120">Remarks</span></span>

<span data-ttu-id="c5198-121">Tanto  _el número_ como el  _exponente_ pueden no ser enteros y pueden ser negativos.</span><span class="sxs-lookup"><span data-stu-id="c5198-121">Both  _number_ and  _exponent_ may be non-integers, and they may be negative.</span></span> <span data-ttu-id="c5198-122">Si  _el_ número no es 0 y  _el exponente_ es 0, esta función devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="c5198-122">If  _number_ is not 0 and  _exponent_ is 0, this function returns 1.</span></span> <span data-ttu-id="c5198-123">Si  _el_ número es 0 y  _el exponente_ es negativo, esta función devuelve 0,0.</span><span class="sxs-lookup"><span data-stu-id="c5198-123">If  _number_ is 0 and  _exponent_ is negative, this function returns 0.0.</span></span> <span data-ttu-id="c5198-124">Si el _número_ y _el exponente_ son 0, o si el número es negativo y el _exponente_ no es un entero, esta función devuelve 0,0. </span><span class="sxs-lookup"><span data-stu-id="c5198-124">If both  _number_ and  _exponent_ are 0, or if  _number_ is negative and  _exponent_ is not an integer, this function returns 0.0.</span></span> <span data-ttu-id="c5198-125">Si el  _número_ y  _el exponente_ son negativos, esta función devuelve -1,#IND.</span><span class="sxs-lookup"><span data-stu-id="c5198-125">If both  _number_ and  _exponent_ are negative, this function returns -1.#IND.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c5198-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c5198-126">Example</span></span>

<span data-ttu-id="c5198-127">POW(5,2)</span><span class="sxs-lookup"><span data-stu-id="c5198-127">POW(5,2)</span></span> 
  
<span data-ttu-id="c5198-128">Devuelve 25.</span><span class="sxs-lookup"><span data-stu-id="c5198-128">Returns 25.</span></span> 
  

