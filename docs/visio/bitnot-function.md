---
title: BITNOT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
localization_priority: Normal
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: Devuelve un número binario de 16 bits en el que cada bit está establecido en 1 solo si el bit correspondiente en número binario es 0. De lo contrario, el bit se establece en 0.
ms.openlocfilehash: 0806e7c52cab659a09d27a60efb9c09aa436fb92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821602"
---
# <a name="bitnot-function"></a><span data-ttu-id="f66e8-104">BITNOT (función)</span><span class="sxs-lookup"><span data-stu-id="f66e8-104">BITNOT Function</span></span>

<span data-ttu-id="f66e8-105">Devuelve un número binario de 16 bits en el que cada bit está establecido en 1 solo si el bit correspondiente en número binario es 0.</span><span class="sxs-lookup"><span data-stu-id="f66e8-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in binary number is 0.</span></span> <span data-ttu-id="f66e8-106">De lo contrario, el bit se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="f66e8-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f66e8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f66e8-107">Syntax</span></span>

<span data-ttu-id="f66e8-108">BITNOT (** *número binario* **)</span><span class="sxs-lookup"><span data-stu-id="f66e8-108">BITNOT(** *binary number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f66e8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f66e8-109">Parameters</span></span>

|<span data-ttu-id="f66e8-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="f66e8-110">**Name**</span></span>|<span data-ttu-id="f66e8-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="f66e8-111">**Required/Optional**</span></span>|<span data-ttu-id="f66e8-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="f66e8-112">**Data Type**</span></span>|<span data-ttu-id="f66e8-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f66e8-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f66e8-114">_número binario_</span><span class="sxs-lookup"><span data-stu-id="f66e8-114">_binary number_</span></span> <br/> |<span data-ttu-id="f66e8-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f66e8-115">Required</span></span>  <br/> |<span data-ttu-id="f66e8-116">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="f66e8-116">**Numeric**</span></span> <br/> |<span data-ttu-id="f66e8-117">Un número binario de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f66e8-117">A 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f66e8-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f66e8-118">Return value</span></span>

<span data-ttu-id="f66e8-119">Binario de 16 bits</span><span class="sxs-lookup"><span data-stu-id="f66e8-119">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="f66e8-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f66e8-120">Example</span></span>

<span data-ttu-id="f66e8-121">BITNOT(6)</span><span class="sxs-lookup"><span data-stu-id="f66e8-121">BITNOT(6)</span></span>
  
<span data-ttu-id="f66e8-p103">Devuelve 65529. El 6 = 0...00110. Por lo tanto, BITNOT(6) = 1...11001.</span><span class="sxs-lookup"><span data-stu-id="f66e8-p103">Returns 65529. The 6 = 0...00110. Therefore, BITNOT(6) = 1...11001.</span></span>
  

