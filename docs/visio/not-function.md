---
title: NOT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Devuelve TRUE (1) si expresiónLógica es FALSE. De lo contrario, devuelve FALSE (0).
ms.openlocfilehash: e2359aaab18469cd4f272f71aca8d899a12b2120
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822681"
---
# <a name="not-function"></a><span data-ttu-id="36fe4-104">Función NOT</span><span class="sxs-lookup"><span data-stu-id="36fe4-104">NOT Function</span></span>

<span data-ttu-id="36fe4-105">Devuelve TRUE (1) si _expresiónLógica_ es FALSE.</span><span class="sxs-lookup"><span data-stu-id="36fe4-105">Returns TRUE (1) if  _logicalexpression_ is FALSE.</span></span> <span data-ttu-id="36fe4-106">De lo contrario, devuelve FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="36fe4-106">Otherwise, it returns FALSE (0).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="36fe4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36fe4-107">Syntax</span></span>

<span data-ttu-id="36fe4-108">NO (** *expresiónLógica* **)</span><span class="sxs-lookup"><span data-stu-id="36fe4-108">NOT(** *logicalexpression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="36fe4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36fe4-109">Parameters</span></span>

|<span data-ttu-id="36fe4-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="36fe4-110">**Name**</span></span>|<span data-ttu-id="36fe4-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="36fe4-111">**Required/Optional**</span></span>|<span data-ttu-id="36fe4-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="36fe4-112">**Data Type**</span></span>|<span data-ttu-id="36fe4-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="36fe4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="36fe4-114">_expresiónLógica_</span><span class="sxs-lookup"><span data-stu-id="36fe4-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="36fe4-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="36fe4-115">Required</span></span>  <br/> |<span data-ttu-id="36fe4-116">**String**</span><span class="sxs-lookup"><span data-stu-id="36fe4-116">**String**</span></span> <br/> |<span data-ttu-id="36fe4-117">La expresión lógica por evaluar.</span><span class="sxs-lookup"><span data-stu-id="36fe4-117">The logical expression to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="36fe4-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36fe4-118">Return value</span></span>

<span data-ttu-id="36fe4-119">Boolean</span><span class="sxs-lookup"><span data-stu-id="36fe4-119">Boolean</span></span>
  
## <a name="example"></a><span data-ttu-id="36fe4-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="36fe4-120">Example</span></span>

<span data-ttu-id="36fe4-121">NO (alto \> 0,75 pda)</span><span class="sxs-lookup"><span data-stu-id="36fe4-121">NOT(Height \> 0.75 in)</span></span> 
  
<span data-ttu-id="36fe4-p103">Devuelve 1 si Height es menor o igual que 0,75 pulgadas. Devuelve 0 si Height es mayor que 0,75 pulgadas.</span><span class="sxs-lookup"><span data-stu-id="36fe4-p103">Returns 1 if Height is less than or equal to 0.75 inches. Returns 0 if Height is greater than 0.75 inches.</span></span> 
  

