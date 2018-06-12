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
ms.openlocfilehash: 48870c679251a666a5756b2b684d262fe059eee0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822855"
---
# <a name="pow-function"></a><span data-ttu-id="92634-103">POW (función)</span><span class="sxs-lookup"><span data-stu-id="92634-103">POW Function</span></span>

<span data-ttu-id="92634-104">Devuelve un número elevado a la potencia de un exponente.</span><span class="sxs-lookup"><span data-stu-id="92634-104">Returns a number raised to the power of an exponent.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="92634-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92634-105">Syntax</span></span>

<span data-ttu-id="92634-106">POW (** *número* **, ** *exponente* **)</span><span class="sxs-lookup"><span data-stu-id="92634-106">POW(** *number* **, ** *exponent* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="92634-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92634-107">Parameters</span></span>

|<span data-ttu-id="92634-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="92634-108">**Name**</span></span>|<span data-ttu-id="92634-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="92634-109">**Required/Optional**</span></span>|<span data-ttu-id="92634-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="92634-110">**Data Type**</span></span>|<span data-ttu-id="92634-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="92634-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="92634-112">_number_</span><span class="sxs-lookup"><span data-stu-id="92634-112">_number_</span></span> <br/> |<span data-ttu-id="92634-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="92634-113">Required</span></span>  <br/> |<span data-ttu-id="92634-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="92634-114">**Number**</span></span> <br/> |<span data-ttu-id="92634-115">El número para elevar la potencia del exponente.</span><span class="sxs-lookup"><span data-stu-id="92634-115">The number to raise to the power of an exponent.</span></span>  <br/> |
| <span data-ttu-id="92634-116">_exponente_</span><span class="sxs-lookup"><span data-stu-id="92634-116">_exponent_</span></span> <br/> |<span data-ttu-id="92634-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="92634-117">Required</span></span>  <br/> |<span data-ttu-id="92634-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="92634-118">**Number**</span></span> <br/> |<span data-ttu-id="92634-119">El exponente.</span><span class="sxs-lookup"><span data-stu-id="92634-119">The exponent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92634-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92634-120">Remarks</span></span>

<span data-ttu-id="92634-121">_Número_ y _exponente_ pueden ser que no son enteros, y pueden ser negativos.</span><span class="sxs-lookup"><span data-stu-id="92634-121">Both  _number_ and  _exponent_ may be non-integers, and they may be negative.</span></span> <span data-ttu-id="92634-122">Si _número_ no es 0 y _exponente_ es 0, esta función devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="92634-122">If  _number_ is not 0 and  _exponent_ is 0, this function returns 1.</span></span> <span data-ttu-id="92634-123">Si _número_ es 0 y _exponente_ es negativo, esta función devuelve 0,0.</span><span class="sxs-lookup"><span data-stu-id="92634-123">If  _number_ is 0 and  _exponent_ is negative, this function returns 0.0.</span></span> <span data-ttu-id="92634-124">Si tanto _número_ como _exponente_ son 0 o si _número_ es negativo y _exponente_ no es un entero, esta función devuelve 0,0.</span><span class="sxs-lookup"><span data-stu-id="92634-124">If both  _number_ and  _exponent_ are 0, or if  _number_ is negative and  _exponent_ is not an integer, this function returns 0.0.</span></span> <span data-ttu-id="92634-125">Si tanto _número_ como _exponente_ son negativos, esta función devuelve -1. #IND.</span><span class="sxs-lookup"><span data-stu-id="92634-125">If both  _number_ and  _exponent_ are negative, this function returns -1.#IND.</span></span> 
  
## <a name="example"></a><span data-ttu-id="92634-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="92634-126">Example</span></span>

<span data-ttu-id="92634-127">POW(5;2)</span><span class="sxs-lookup"><span data-stu-id="92634-127">POW(5,2)</span></span> 
  
<span data-ttu-id="92634-128">Devuelve 25.</span><span class="sxs-lookup"><span data-stu-id="92634-128">Returns 25.</span></span> 
  

