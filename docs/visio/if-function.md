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
description: Devuelve valueiftrue si expresiónLógica es TRUE. De lo contrario, devuelve valueiffalse.
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344768"
---
# <a name="if-function"></a><span data-ttu-id="7c08c-104">Función IF</span><span class="sxs-lookup"><span data-stu-id="7c08c-104">IF Function</span></span>

<span data-ttu-id="7c08c-105">Devuelve _valueiftrue_ si _expresiónLógica_ es true.</span><span class="sxs-lookup"><span data-stu-id="7c08c-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="7c08c-106">De lo contrario, devuelve _valueiffalse_.</span><span class="sxs-lookup"><span data-stu-id="7c08c-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="7c08c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c08c-107">Syntax</span></span>

<span data-ttu-id="7c08c-108">IF (\* \* *expresiónLógica* \* \*, \* \* *valueiftrue* \* \*, \* \* *valueiffalse* \* \*)</span><span class="sxs-lookup"><span data-stu-id="7c08c-108">IF(\*\* *logicalexpression* \*\*, \*\* *valueiftrue* \*\*, \*\* *valueiffalse* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7c08c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c08c-109">Parameters</span></span>

|<span data-ttu-id="7c08c-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="7c08c-110">**Name**</span></span>|<span data-ttu-id="7c08c-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="7c08c-111">**Required/Optional**</span></span>|<span data-ttu-id="7c08c-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="7c08c-112">**Data Type**</span></span>|<span data-ttu-id="7c08c-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7c08c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7c08c-114">_expresiónLógica_</span><span class="sxs-lookup"><span data-stu-id="7c08c-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="7c08c-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7c08c-115">Required</span></span>  <br/> |<span data-ttu-id="7c08c-116">**String**</span><span class="sxs-lookup"><span data-stu-id="7c08c-116">**String**</span></span> <br/> |<span data-ttu-id="7c08c-117">Expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="7c08c-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="7c08c-118">_valueiftrue_</span><span class="sxs-lookup"><span data-stu-id="7c08c-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="7c08c-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7c08c-119">Required</span></span>  <br/> |<span data-ttu-id="7c08c-120">**Diferencias**</span><span class="sxs-lookup"><span data-stu-id="7c08c-120">**Varies**</span></span> <br/> |<span data-ttu-id="7c08c-121">Valor que se va a devolver si _expresiónLógica_ es true.</span><span class="sxs-lookup"><span data-stu-id="7c08c-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="7c08c-122">_valueiffalse_</span><span class="sxs-lookup"><span data-stu-id="7c08c-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="7c08c-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7c08c-123">Required</span></span>  <br/> |<span data-ttu-id="7c08c-124">**Diferencias**</span><span class="sxs-lookup"><span data-stu-id="7c08c-124">**Varies**</span></span> <br/> | <span data-ttu-id="7c08c-125">Valor que se va a devolver si _expresiónLógica_ es false.</span><span class="sxs-lookup"><span data-stu-id="7c08c-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7c08c-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c08c-126">Return value</span></span>

<span data-ttu-id="7c08c-127">Varía</span><span class="sxs-lookup"><span data-stu-id="7c08c-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="7c08c-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7c08c-128">Example</span></span>

<span data-ttu-id="7c08c-129">IF (height \> 1,25 en,5, 7)</span><span class="sxs-lookup"><span data-stu-id="7c08c-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="7c08c-130">Devuelve 5 si el alto de la forma es mayor de 1,25 pulgadas.</span><span class="sxs-lookup"><span data-stu-id="7c08c-130">Returns 5 if the shape's height is greater than 1.25 inches.</span></span> <span data-ttu-id="7c08c-131">Devuelve 7 si el alto de la forma es menor o igual que 1,25 pulgadas.</span><span class="sxs-lookup"><span data-stu-id="7c08c-131">Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

