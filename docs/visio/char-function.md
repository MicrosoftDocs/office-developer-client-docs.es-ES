---
title: CHAR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
localization_priority: Normal
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: Devuelve el carácter ANSI de un número.
ms.openlocfilehash: 6f1c459892331ec30ad93bbc860fcd038e8f4732
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418193"
---
# <a name="char-function"></a><span data-ttu-id="db75d-103">Función CHAR</span><span class="sxs-lookup"><span data-stu-id="db75d-103">CHAR Function</span></span>

<span data-ttu-id="db75d-104">Devuelve el carácter ANSI de un número.</span><span class="sxs-lookup"><span data-stu-id="db75d-104">Returns the ANSI character for a number.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="db75d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db75d-105">Syntax</span></span>

<span data-ttu-id="db75d-106">CHAR(\*\* *number* \*\* )</span><span class="sxs-lookup"><span data-stu-id="db75d-106">CHAR(\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="db75d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db75d-107">Parameters</span></span>

|<span data-ttu-id="db75d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="db75d-108">**Name**</span></span>|<span data-ttu-id="db75d-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="db75d-109">**Required/Optional**</span></span>|<span data-ttu-id="db75d-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="db75d-110">**Data Type**</span></span>|<span data-ttu-id="db75d-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="db75d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="db75d-112">_number_</span><span class="sxs-lookup"><span data-stu-id="db75d-112">_number_</span></span> <br/> |<span data-ttu-id="db75d-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="db75d-113">Required</span></span>  <br/> |<span data-ttu-id="db75d-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="db75d-114">**Number**</span></span> <br/> |<span data-ttu-id="db75d-115">El número cuyo carácter ANSI desea obtener.</span><span class="sxs-lookup"><span data-stu-id="db75d-115">The number whose ANSI character you want to get.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db75d-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db75d-116">Remarks</span></span>

<span data-ttu-id="db75d-117">La cadena resultante tiene un carácter de longitud.</span><span class="sxs-lookup"><span data-stu-id="db75d-117">The resulting string is one character in length.</span></span> <span data-ttu-id="db75d-118">El  _parámetro number_ debe ser un entero entre 1 y 255 (ambos inclusive) o la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="db75d-118">The  _number_ parameter must be an integer between 1 and 255 (inclusive), or the function returns an error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="db75d-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="db75d-119">Example</span></span>

<span data-ttu-id="db75d-120">CHAR(9)</span><span class="sxs-lookup"><span data-stu-id="db75d-120">CHAR(9)</span></span> 
  
<span data-ttu-id="db75d-121">Devuelve el carácter de tabulador.</span><span class="sxs-lookup"><span data-stu-id="db75d-121">Returns the tab character.</span></span> 
  

