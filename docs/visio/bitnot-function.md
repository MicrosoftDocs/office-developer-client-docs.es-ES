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
description: Devuelve un número binario de 16 bits en el que cada bit se establece en 1 solo si el bit correspondiente en el número binario es 0. De lo contrario, el bit se establece en 0.
ms.openlocfilehash: 34ea6fd614feae8e3c8e97e34b7ff6c531f4c123
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438837"
---
# <a name="bitnot-function"></a><span data-ttu-id="e5783-104">Función BITNOT</span><span class="sxs-lookup"><span data-stu-id="e5783-104">BITNOT Function</span></span>

<span data-ttu-id="e5783-105">Devuelve un número binario de 16 bits en el que cada bit se establece en 1 solo si el bit correspondiente en el número binario es 0.</span><span class="sxs-lookup"><span data-stu-id="e5783-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in binary number is 0.</span></span> <span data-ttu-id="e5783-106">De lo contrario, el bit se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="e5783-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e5783-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5783-107">Syntax</span></span>

<span data-ttu-id="e5783-108">BITNOT(\*\* *binary number* \*\* )</span><span class="sxs-lookup"><span data-stu-id="e5783-108">BITNOT(\*\* *binary number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e5783-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5783-109">Parameters</span></span>

|<span data-ttu-id="e5783-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="e5783-110">**Name**</span></span>|<span data-ttu-id="e5783-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e5783-111">**Required/Optional**</span></span>|<span data-ttu-id="e5783-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="e5783-112">**Data Type**</span></span>|<span data-ttu-id="e5783-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e5783-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e5783-114">_número binario_</span><span class="sxs-lookup"><span data-stu-id="e5783-114">_binary number_</span></span> <br/> |<span data-ttu-id="e5783-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e5783-115">Required</span></span>  <br/> |<span data-ttu-id="e5783-116">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="e5783-116">**Numeric**</span></span> <br/> |<span data-ttu-id="e5783-117">Un número binario de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e5783-117">A 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e5783-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5783-118">Return value</span></span>

<span data-ttu-id="e5783-119">Binario de 16 bits</span><span class="sxs-lookup"><span data-stu-id="e5783-119">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="e5783-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e5783-120">Example</span></span>

<span data-ttu-id="e5783-121">BITNOT(6)</span><span class="sxs-lookup"><span data-stu-id="e5783-121">BITNOT(6)</span></span>
  
<span data-ttu-id="e5783-p103">Devuelve 65529. El 6 = 0...00110. Por lo tanto, BITNOT(6) = 1...11001.</span><span class="sxs-lookup"><span data-stu-id="e5783-p103">Returns 65529. The 6 = 0...00110. Therefore, BITNOT(6) = 1...11001.</span></span>
  

