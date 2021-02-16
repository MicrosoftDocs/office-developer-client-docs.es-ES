---
title: BITAND (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251398
localization_priority: Normal
ms.assetid: c437de23-d2e0-469d-62e6-8eb8b8cfea5c
description: Devuelve un número binario de 16 bits en el que cada bit se establece en 1 solo si el bit correspondiente en binarynumber1 y binarynumber2 es 1. De lo contrario, el bit se establece en 0.
ms.openlocfilehash: a3c76a9122d0f02d5ab61460cf3457bb15da4d7b
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293495"
---
# <a name="bitand-function"></a><span data-ttu-id="90a91-104">Función BITAND</span><span class="sxs-lookup"><span data-stu-id="90a91-104">BITAND Function</span></span>

<span data-ttu-id="90a91-105">Devuelve un número binario de 16 bits en el que cada bit se establece en 1 solo si el bit correspondiente en binarynumber1 y binarynumber2 es 1.</span><span class="sxs-lookup"><span data-stu-id="90a91-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in both binarynumber1 and binarynumber2 is 1.</span></span> <span data-ttu-id="90a91-106">De lo contrario, el bit se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="90a91-106">Otherwise, the bit is set to 0.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="90a91-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90a91-107">Syntax</span></span>

<span data-ttu-id="90a91-108">BITAND(***binarynumber1***, ***binarynumber2*** )</span><span class="sxs-lookup"><span data-stu-id="90a91-108">BITAND(***binarynumber1***, ***binarynumber2*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="90a91-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90a91-109">Parameters</span></span>

|<span data-ttu-id="90a91-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="90a91-110">**Name**</span></span>|<span data-ttu-id="90a91-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="90a91-111">**Required/Optional**</span></span>|<span data-ttu-id="90a91-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="90a91-112">**Data Type**</span></span>|<span data-ttu-id="90a91-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90a91-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="90a91-114">_binary number1_</span><span class="sxs-lookup"><span data-stu-id="90a91-114">_binary number1_</span></span> <br/> |<span data-ttu-id="90a91-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="90a91-115">Required</span></span>  <br/> |<span data-ttu-id="90a91-116">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="90a91-116">**Numeric**</span></span> <br/> |<span data-ttu-id="90a91-117">El primer número binario de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="90a91-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="90a91-118">_número binario2_</span><span class="sxs-lookup"><span data-stu-id="90a91-118">_binary number2_</span></span> <br/> |<span data-ttu-id="90a91-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="90a91-119">Required</span></span>  <br/> |<span data-ttu-id="90a91-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="90a91-120">**Numeric**</span></span> <br/> |<span data-ttu-id="90a91-121">El segundo número binario de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="90a91-121">The second 16-bit binary number.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90a91-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="90a91-122">Remarks</span></span>

<span data-ttu-id="90a91-123">Puede usar esta función para probar y cambiar las propiedades de una forma que se almacenan como máscaras de bits, por ejemplo, el formato de texto de la forma.</span><span class="sxs-lookup"><span data-stu-id="90a91-123">You can use this function to test and change properties of a shape that are stored as bitmasks, for example, the shape's text format.</span></span>
  
## <a name="example"></a><span data-ttu-id="90a91-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="90a91-124">Example</span></span>

<span data-ttu-id="90a91-125">BITAND(12,6)</span><span class="sxs-lookup"><span data-stu-id="90a91-125">BITAND(12,6)</span></span>
  
<span data-ttu-id="90a91-p103">Devuelve 4. El 12 = 0...01100. El 6 = 0...00110. Por lo tanto, BITAND(12,6) = 0...00100.</span><span class="sxs-lookup"><span data-stu-id="90a91-p103">Returns 4. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITAND(12,6) = 0...00100.</span></span>
  

