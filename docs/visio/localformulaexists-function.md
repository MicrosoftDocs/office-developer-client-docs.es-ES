---
title: LOCALFORMULAEXISTS (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60105
localization_priority: Normal
ms.assetid: 2b757c8d-7732-0f9b-c836-ef755dd1c673
description: Indica si la celda a la que se hace referencia contiene una fórmula local.
ms.openlocfilehash: bd0a5dafecf1bd8dca1567392d880ecaaa3e0374
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344467"
---
# <a name="localformulaexists-function"></a><span data-ttu-id="088f2-103">Función LOCALFORMULAEXISTS</span><span class="sxs-lookup"><span data-stu-id="088f2-103">LOCALFORMULAEXISTS Function</span></span>

<span data-ttu-id="088f2-104">Indica si la celda a la que se hace referencia contiene una fórmula local.</span><span class="sxs-lookup"><span data-stu-id="088f2-104">Indicates whether the referenced cell contains a local formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="088f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="088f2-105">Syntax</span></span>

<span data-ttu-id="088f2-106">LOCALFORMULAEXISTS (\* \* *referenciaDeCelda* \* \*)</span><span class="sxs-lookup"><span data-stu-id="088f2-106">LOCALFORMULAEXISTS (\*\* *cellref* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="088f2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="088f2-107">Parameters</span></span>

|<span data-ttu-id="088f2-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="088f2-108">**Name**</span></span>|<span data-ttu-id="088f2-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="088f2-109">**Required/Optional**</span></span>|<span data-ttu-id="088f2-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="088f2-110">**Data Type**</span></span>|<span data-ttu-id="088f2-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="088f2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="088f2-112">_referenciaDeCelda_</span><span class="sxs-lookup"><span data-stu-id="088f2-112">_cellref_</span></span> <br/> |<span data-ttu-id="088f2-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="088f2-113">Required</span></span>  <br/> |<span data-ttu-id="088f2-114">**String**</span><span class="sxs-lookup"><span data-stu-id="088f2-114">**String**</span></span> <br/> | <span data-ttu-id="088f2-115">La celda en la que se debe comprobar si existe una fórmula.</span><span class="sxs-lookup"><span data-stu-id="088f2-115">The cell that you want to check for the presence of a formula.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="088f2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="088f2-116">Return value</span></span>

<span data-ttu-id="088f2-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="088f2-117">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="088f2-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="088f2-118">Remarks</span></span>

<span data-ttu-id="088f2-119">La función LOCALFORMULAEXISTS devuelve 1 si la celda contiene una fórmula local; si no es así o la fórmula es heredada, devuelve cero (0).</span><span class="sxs-lookup"><span data-stu-id="088f2-119">The LOCALFORMULAEXISTS function returns 1 if the cell contains a local formula; if there is no formula, or if the formula is inherited, it returns 0 (zero).</span></span> 
  

