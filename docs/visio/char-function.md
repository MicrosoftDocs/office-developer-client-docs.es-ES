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
description: Devuelve el carácter ANSI para un número.
ms.openlocfilehash: 209614d20dd663ed2f7ca030c25500d43f925c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821741"
---
# <a name="char-function"></a><span data-ttu-id="d744a-103">Función CHAR</span><span class="sxs-lookup"><span data-stu-id="d744a-103">CHAR Function</span></span>

<span data-ttu-id="d744a-104">Devuelve el carácter ANSI para un número.</span><span class="sxs-lookup"><span data-stu-id="d744a-104">Returns the ANSI character for a number.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d744a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d744a-105">Syntax</span></span>

<span data-ttu-id="d744a-106">CHAR (** *número* **)</span><span class="sxs-lookup"><span data-stu-id="d744a-106">CHAR(** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d744a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d744a-107">Parameters</span></span>

|<span data-ttu-id="d744a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d744a-108">**Name**</span></span>|<span data-ttu-id="d744a-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="d744a-109">**Required/Optional**</span></span>|<span data-ttu-id="d744a-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="d744a-110">**Data Type**</span></span>|<span data-ttu-id="d744a-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d744a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d744a-112">_number_</span><span class="sxs-lookup"><span data-stu-id="d744a-112">_number_</span></span> <br/> |<span data-ttu-id="d744a-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d744a-113">Required</span></span>  <br/> |<span data-ttu-id="d744a-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="d744a-114">**Number**</span></span> <br/> |<span data-ttu-id="d744a-115">El número cuyo carácter ANSI desea obtener.</span><span class="sxs-lookup"><span data-stu-id="d744a-115">The number whose ANSI character you want to get.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d744a-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d744a-116">Remarks</span></span>

<span data-ttu-id="d744a-117">La cadena resultante tiene un carácter de longitud.</span><span class="sxs-lookup"><span data-stu-id="d744a-117">The resulting string is one character in length.</span></span> <span data-ttu-id="d744a-118">El parámetro de _número_ debe ser un entero entre 1 y 255 (ambos inclusive), o la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="d744a-118">The  _number_ parameter must be an integer between 1 and 255 (inclusive), or the function returns an error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d744a-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d744a-119">Example</span></span>

<span data-ttu-id="d744a-120">CHAR(9)</span><span class="sxs-lookup"><span data-stu-id="d744a-120">CHAR(9)</span></span> 
  
<span data-ttu-id="d744a-121">Devuelve el carácter de tabulador.</span><span class="sxs-lookup"><span data-stu-id="d744a-121">Returns the tab character.</span></span> 
  

