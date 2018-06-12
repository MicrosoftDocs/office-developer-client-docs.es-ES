---
title: BITOR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251400
localization_priority: Normal
ms.assetid: 1d0954c5-b2cb-6c5d-62b3-a68011cf0c85
description: Devuelve un número binario de 16 bits en el que cada bit está establecido en 1 si el bit correspondiente en número binario 1 o número binario 2 es 1. El bit se establece en 0 solo si el bit correspondiente es 0 en número binario 1 o número binario 2.
ms.openlocfilehash: db9808f16b32776149abbddf882310c02268cec3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821619"
---
# <a name="bitor-function"></a><span data-ttu-id="b77b4-104">BITOR (función)</span><span class="sxs-lookup"><span data-stu-id="b77b4-104">BITOR Function</span></span>

<span data-ttu-id="b77b4-105">Devuelve un número binario de 16 bits en el que cada bit está establecido en 1 si el bit correspondiente en *número binario 1* o *número binario 2* es 1.</span><span class="sxs-lookup"><span data-stu-id="b77b4-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either  *binary number1*  or  *binary number2*  is 1.</span></span> <span data-ttu-id="b77b4-106">El bit se establece en 0 solo si el bit correspondiente es 0 en *número binario 1* o *número binario 2* .</span><span class="sxs-lookup"><span data-stu-id="b77b4-106">The bit is set to 0 only if the corresponding bit is 0 in both  *binary number1*  and  *binary number2*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b77b4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b77b4-107">Syntax</span></span>

<span data-ttu-id="b77b4-108">BITOR (** *número binario 1* **, ** *número binario 2* **)</span><span class="sxs-lookup"><span data-stu-id="b77b4-108">BITOR(** *binary number1* **, ** *binary number2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b77b4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b77b4-109">Parameters</span></span>

|<span data-ttu-id="b77b4-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="b77b4-110">**Name**</span></span>|<span data-ttu-id="b77b4-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="b77b4-111">**Required/Optional**</span></span>|<span data-ttu-id="b77b4-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="b77b4-112">**Data Type**</span></span>|<span data-ttu-id="b77b4-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b77b4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b77b4-114">_número binario 1_</span><span class="sxs-lookup"><span data-stu-id="b77b4-114">_binary number1_</span></span> <br/> |<span data-ttu-id="b77b4-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b77b4-115">Required</span></span>  <br/> |<span data-ttu-id="b77b4-116">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="b77b4-116">**Numeric**</span></span> <br/> |<span data-ttu-id="b77b4-117">El primer número binario de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b77b4-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="b77b4-118">_número binario 2_</span><span class="sxs-lookup"><span data-stu-id="b77b4-118">_binary number2_</span></span> <br/> |<span data-ttu-id="b77b4-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b77b4-119">Required</span></span>  <br/> |<span data-ttu-id="b77b4-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="b77b4-120">**Numeric**</span></span> <br/> |<span data-ttu-id="b77b4-121">El segundo número binario de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b77b4-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b77b4-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b77b4-122">Return value</span></span>

<span data-ttu-id="b77b4-123">Binario de 16 bits</span><span class="sxs-lookup"><span data-stu-id="b77b4-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="b77b4-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b77b4-124">Example</span></span>

<span data-ttu-id="b77b4-125">BITOR(12;6)</span><span class="sxs-lookup"><span data-stu-id="b77b4-125">BITOR(12,6)</span></span>
  
<span data-ttu-id="b77b4-p103">Devuelve 14. El 12 = 0...01100. El 6 = 0...00110. Por lo tanto, BITOR(12;6) = 0...01110.</span><span class="sxs-lookup"><span data-stu-id="b77b4-p103">Returns 14. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITOR(12,6) = 0...01110.</span></span>
  

