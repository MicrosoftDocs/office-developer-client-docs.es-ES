---
title: IF (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251442
localization_priority: Normal
ms.assetid: 66771ad3-0fb3-68ff-81da-d1162d37c05a
description: Devuelve valorSiTrue en si expresiónLógica es TRUE. De lo contrario, devuelve valorSiFalse.
ms.openlocfilehash: 55938e8bd78c02badb98f90665c5c26cdd70f3b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822318"
---
# <a name="if-function"></a><span data-ttu-id="04df6-104">Función IF</span><span class="sxs-lookup"><span data-stu-id="04df6-104">IF Function</span></span>

<span data-ttu-id="04df6-105">Devuelve _valorSiTrue en_ si _expresiónLógica_ es TRUE.</span><span class="sxs-lookup"><span data-stu-id="04df6-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="04df6-106">De lo contrario, devuelve _valorSiFalse_.</span><span class="sxs-lookup"><span data-stu-id="04df6-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="04df6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04df6-107">Syntax</span></span>

<span data-ttu-id="04df6-108">IF (** *expresiónLógica* **, ** *ValorSiVerdadero* **, ** *valorSiFalse* **)</span><span class="sxs-lookup"><span data-stu-id="04df6-108">IF(** *logicalexpression* **, ** *valueiftrue* **, ** *valueiffalse* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="04df6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04df6-109">Parameters</span></span>

|<span data-ttu-id="04df6-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="04df6-110">**Name**</span></span>|<span data-ttu-id="04df6-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="04df6-111">**Required/Optional**</span></span>|<span data-ttu-id="04df6-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="04df6-112">**Data Type**</span></span>|<span data-ttu-id="04df6-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="04df6-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="04df6-114">_expresiónLógica_</span><span class="sxs-lookup"><span data-stu-id="04df6-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="04df6-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="04df6-115">Required</span></span>  <br/> |<span data-ttu-id="04df6-116">**String**</span><span class="sxs-lookup"><span data-stu-id="04df6-116">**String**</span></span> <br/> |<span data-ttu-id="04df6-117">Expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="04df6-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="04df6-118">_ValorSiVerdadero_</span><span class="sxs-lookup"><span data-stu-id="04df6-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="04df6-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="04df6-119">Required</span></span>  <br/> |<span data-ttu-id="04df6-120">**Varían**</span><span class="sxs-lookup"><span data-stu-id="04df6-120">**Varies**</span></span> <br/> |<span data-ttu-id="04df6-121">Valor que para devolver si _expresiónLógica_ es true.</span><span class="sxs-lookup"><span data-stu-id="04df6-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="04df6-122">_valorSiFalse_</span><span class="sxs-lookup"><span data-stu-id="04df6-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="04df6-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="04df6-123">Required</span></span>  <br/> |<span data-ttu-id="04df6-124">**Varían**</span><span class="sxs-lookup"><span data-stu-id="04df6-124">**Varies**</span></span> <br/> | <span data-ttu-id="04df6-125">Valor que para devolver si _expresiónLógica_ es false.</span><span class="sxs-lookup"><span data-stu-id="04df6-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="04df6-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04df6-126">Return value</span></span>

<span data-ttu-id="04df6-127">Varies</span><span class="sxs-lookup"><span data-stu-id="04df6-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="04df6-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="04df6-128">Example</span></span>

<span data-ttu-id="04df6-129">IF (Height \> 1,25 pda, 5, 7)</span><span class="sxs-lookup"><span data-stu-id="04df6-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="04df6-p103">Devuelve 5 si el alto de la forma es mayor de 1,25 pulgadas. Devuelve 7 si el alto de la forma es menor o igual que 1,25 pulgadas.</span><span class="sxs-lookup"><span data-stu-id="04df6-p103">Returns 5 if the shape's height is greater than 1.25 inches. Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

