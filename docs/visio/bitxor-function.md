---
title: BITXOR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251401
localization_priority: Normal
ms.assetid: 672eacaf-a374-c7e2-b39b-8d42d2371aee
description: Devuelve un número binario de 16 bits en el que cada bit se establece en 1 si el bit correspondiente en cualquiera de los dos, pero no el número binario1 y el número binario2 es 1. De lo contrario, el bit se establece en 0.
ms.openlocfilehash: ab8ff46fe98512d963ef4ecd5c37127353827725
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439236"
---
# <a name="bitxor-function"></a><span data-ttu-id="28739-104">Función BITXOR</span><span class="sxs-lookup"><span data-stu-id="28739-104">BITXOR Function</span></span>

<span data-ttu-id="28739-105">Devuelve un número binario de 16 bits en el que cada bit se establece en 1 si el bit correspondiente en cualquiera de los dos, pero no el número binario1 y el número binario2 es 1.</span><span class="sxs-lookup"><span data-stu-id="28739-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either but not both binary number1 and binary number2 is 1.</span></span> <span data-ttu-id="28739-106">De lo contrario, el bit se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="28739-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="28739-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28739-107">Syntax</span></span>

<span data-ttu-id="28739-108">BITXOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span><span class="sxs-lookup"><span data-stu-id="28739-108">BITXOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="28739-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28739-109">Parameters</span></span>

|<span data-ttu-id="28739-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="28739-110">**Name**</span></span>|<span data-ttu-id="28739-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="28739-111">**Required/Optional**</span></span>|<span data-ttu-id="28739-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="28739-112">**Data Type**</span></span>|<span data-ttu-id="28739-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28739-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="28739-114">_binary number1_</span><span class="sxs-lookup"><span data-stu-id="28739-114">_binary number1_</span></span> <br/> |<span data-ttu-id="28739-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="28739-115">Required</span></span>  <br/> |<span data-ttu-id="28739-116">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="28739-116">**Numeric**</span></span> <br/> |<span data-ttu-id="28739-117">El primer número binario de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="28739-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="28739-118">_binary number2_</span><span class="sxs-lookup"><span data-stu-id="28739-118">_binary number2_</span></span> <br/> |<span data-ttu-id="28739-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="28739-119">Required</span></span>  <br/> |<span data-ttu-id="28739-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="28739-120">**Numeric**</span></span> <br/> |<span data-ttu-id="28739-121">El segundo número binario de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="28739-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="28739-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28739-122">Return value</span></span>

<span data-ttu-id="28739-123">Binario de 16 bits</span><span class="sxs-lookup"><span data-stu-id="28739-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="28739-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="28739-124">Example</span></span>

<span data-ttu-id="28739-125">BITXOR(12,6)</span><span class="sxs-lookup"><span data-stu-id="28739-125">BITXOR(12,6)</span></span>
  
<span data-ttu-id="28739-p103">Devuelve 10. El 12 = 0...01100. El 6 = 0...00110. Por lo tanto, BITXOR(12,6) = 0...01010.</span><span class="sxs-lookup"><span data-stu-id="28739-p103">Returns 10. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITXOR(12,6) = 0...01010.</span></span>
  

