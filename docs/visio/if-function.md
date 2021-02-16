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
description: Devuelve valueiftrue si la expresión lógica es TRUE. De lo contrario, devuelve valueiffalse.
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405474"
---
# <a name="if-function"></a><span data-ttu-id="e98e5-104">Función IF</span><span class="sxs-lookup"><span data-stu-id="e98e5-104">IF Function</span></span>

<span data-ttu-id="e98e5-105">Devuelve  _valueiftrue_ si  _la expresión lógica_ es TRUE.</span><span class="sxs-lookup"><span data-stu-id="e98e5-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="e98e5-106">De lo contrario, devuelve  _valueiffalse_.</span><span class="sxs-lookup"><span data-stu-id="e98e5-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e98e5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e98e5-107">Syntax</span></span>

<span data-ttu-id="e98e5-108">IF(\*\* *logicalexpression* \*\*, \*\* *valueiftrue* \*\*, \*\* *valueiffalse* \*\* )</span><span class="sxs-lookup"><span data-stu-id="e98e5-108">IF(\*\* *logicalexpression* \*\*, \*\* *valueiftrue* \*\*, \*\* *valueiffalse* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e98e5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e98e5-109">Parameters</span></span>

|<span data-ttu-id="e98e5-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="e98e5-110">**Name**</span></span>|<span data-ttu-id="e98e5-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e98e5-111">**Required/Optional**</span></span>|<span data-ttu-id="e98e5-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="e98e5-112">**Data Type**</span></span>|<span data-ttu-id="e98e5-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e98e5-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e98e5-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="e98e5-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="e98e5-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e98e5-115">Required</span></span>  <br/> |<span data-ttu-id="e98e5-116">**String**</span><span class="sxs-lookup"><span data-stu-id="e98e5-116">**String**</span></span> <br/> |<span data-ttu-id="e98e5-117">Expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="e98e5-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="e98e5-118">_valueiftrue_</span><span class="sxs-lookup"><span data-stu-id="e98e5-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="e98e5-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e98e5-119">Required</span></span>  <br/> |<span data-ttu-id="e98e5-120">**Varía**</span><span class="sxs-lookup"><span data-stu-id="e98e5-120">**Varies**</span></span> <br/> |<span data-ttu-id="e98e5-121">Valor que se devuelve si  _la expresión lógica_ es true.</span><span class="sxs-lookup"><span data-stu-id="e98e5-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="e98e5-122">_valueiffalse_</span><span class="sxs-lookup"><span data-stu-id="e98e5-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="e98e5-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e98e5-123">Required</span></span>  <br/> |<span data-ttu-id="e98e5-124">**Varía**</span><span class="sxs-lookup"><span data-stu-id="e98e5-124">**Varies**</span></span> <br/> | <span data-ttu-id="e98e5-125">Valor que se devuelve si  _la expresión lógica_ es false.</span><span class="sxs-lookup"><span data-stu-id="e98e5-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e98e5-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e98e5-126">Return value</span></span>

<span data-ttu-id="e98e5-127">Varía</span><span class="sxs-lookup"><span data-stu-id="e98e5-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="e98e5-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e98e5-128">Example</span></span>

<span data-ttu-id="e98e5-129">IF(Height \> 1.25 in,5,7)</span><span class="sxs-lookup"><span data-stu-id="e98e5-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="e98e5-130">Devuelve 5 si el alto de la forma es mayor de 1,25 pulgadas.</span><span class="sxs-lookup"><span data-stu-id="e98e5-130">Returns 5 if the shape's height is greater than 1.25 inches.</span></span> <span data-ttu-id="e98e5-131">Devuelve 7 si el alto de la forma es menor o igual que 1,25 pulgadas.</span><span class="sxs-lookup"><span data-stu-id="e98e5-131">Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

