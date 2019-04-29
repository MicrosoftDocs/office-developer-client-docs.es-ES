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
description: Devuelve un número binario de 16 bits en el que cada bit está establecido en 1 si el bit correspondiente en el número binario número1 o el número binario 2 es 1. El bit se establece en 0 sólo si el bit correspondiente es 0 en el argumento número1 binario y el número binario 2.
ms.openlocfilehash: 13bda2c6c65557b1f8372432cf919b2aaf2d75de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408085"
---
# <a name="bitor-function"></a><span data-ttu-id="cd2f1-104">Función BITOR</span><span class="sxs-lookup"><span data-stu-id="cd2f1-104">BITOR Function</span></span>

<span data-ttu-id="cd2f1-105">Devuelve un número binario de 16 bits en el que cada bit está establecido en 1 si el bit correspondiente en el *número binario número1* o el número *binario 2* es 1.</span><span class="sxs-lookup"><span data-stu-id="cd2f1-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either  *binary number1*  or  *binary number2*  is 1.</span></span> <span data-ttu-id="cd2f1-106">El bit se establece en 0 sólo si el bit correspondiente es 0 en el argumento *número1 binario* y el número binario *2* .</span><span class="sxs-lookup"><span data-stu-id="cd2f1-106">The bit is set to 0 only if the corresponding bit is 0 in both  *binary number1*  and  *binary number2*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cd2f1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd2f1-107">Syntax</span></span>

<span data-ttu-id="cd2f1-108">BITOR (\* \* *número binario* 1 \* \*, \* \* número *binario 2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="cd2f1-108">BITOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cd2f1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd2f1-109">Parameters</span></span>

|<span data-ttu-id="cd2f1-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="cd2f1-110">**Name**</span></span>|<span data-ttu-id="cd2f1-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="cd2f1-111">**Required/Optional**</span></span>|<span data-ttu-id="cd2f1-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="cd2f1-112">**Data Type**</span></span>|<span data-ttu-id="cd2f1-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd2f1-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cd2f1-114">_número binario_</span><span class="sxs-lookup"><span data-stu-id="cd2f1-114">_binary number1_</span></span> <br/> |<span data-ttu-id="cd2f1-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="cd2f1-115">Required</span></span>  <br/> |<span data-ttu-id="cd2f1-116">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="cd2f1-116">**Numeric**</span></span> <br/> |<span data-ttu-id="cd2f1-117">El primer número binario de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="cd2f1-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="cd2f1-118">_número2 binario_</span><span class="sxs-lookup"><span data-stu-id="cd2f1-118">_binary number2_</span></span> <br/> |<span data-ttu-id="cd2f1-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="cd2f1-119">Required</span></span>  <br/> |<span data-ttu-id="cd2f1-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="cd2f1-120">**Numeric**</span></span> <br/> |<span data-ttu-id="cd2f1-121">El segundo número binario de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="cd2f1-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="cd2f1-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd2f1-122">Return value</span></span>

<span data-ttu-id="cd2f1-123">Binario de 16 bits</span><span class="sxs-lookup"><span data-stu-id="cd2f1-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="cd2f1-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd2f1-124">Example</span></span>

<span data-ttu-id="cd2f1-125">BITOR (12, 6)</span><span class="sxs-lookup"><span data-stu-id="cd2f1-125">BITOR(12,6)</span></span>
  
<span data-ttu-id="cd2f1-p103">Devuelve 14. El 12 = 0...01100. El 6 = 0...00110. Por lo tanto, BITOR(12;6) = 0...01110.</span><span class="sxs-lookup"><span data-stu-id="cd2f1-p103">Returns 14. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITOR(12,6) = 0...01110.</span></span>
  

