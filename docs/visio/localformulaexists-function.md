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
description: Indica si la celda referida contiene una fórmula local.
ms.openlocfilehash: 1b749011de8554cb5b777fe92b20a6bcdb2fcb19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822499"
---
# <a name="localformulaexists-function"></a><span data-ttu-id="9f46b-103">Función LOCALFORMULAEXISTS</span><span class="sxs-lookup"><span data-stu-id="9f46b-103">LOCALFORMULAEXISTS Function</span></span>

<span data-ttu-id="9f46b-104">Indica si la celda referida contiene una fórmula local.</span><span class="sxs-lookup"><span data-stu-id="9f46b-104">Indicates whether the referenced cell contains a local formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9f46b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f46b-105">Syntax</span></span>

<span data-ttu-id="9f46b-106">LOCALFORMULAEXISTS (** *cellref* **)</span><span class="sxs-lookup"><span data-stu-id="9f46b-106">LOCALFORMULAEXISTS (** *cellref* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9f46b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f46b-107">Parameters</span></span>

|<span data-ttu-id="9f46b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="9f46b-108">**Name**</span></span>|<span data-ttu-id="9f46b-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="9f46b-109">**Required/Optional**</span></span>|<span data-ttu-id="9f46b-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="9f46b-110">**Data Type**</span></span>|<span data-ttu-id="9f46b-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9f46b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9f46b-112">_CellRef_</span><span class="sxs-lookup"><span data-stu-id="9f46b-112">_cellref_</span></span> <br/> |<span data-ttu-id="9f46b-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9f46b-113">Required</span></span>  <br/> |<span data-ttu-id="9f46b-114">**String**</span><span class="sxs-lookup"><span data-stu-id="9f46b-114">**String**</span></span> <br/> | <span data-ttu-id="9f46b-115">La celda en la que se debe comprobar si existe una fórmula.</span><span class="sxs-lookup"><span data-stu-id="9f46b-115">The cell that you want to check for the presence of a formula.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9f46b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f46b-116">Return value</span></span>

<span data-ttu-id="9f46b-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="9f46b-117">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9f46b-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f46b-118">Remarks</span></span>

<span data-ttu-id="9f46b-119">La función LOCALFORMULAEXISTS devuelve 1 si la celda contiene una fórmula local; si no es así o la fórmula es heredada, devuelve cero (0).</span><span class="sxs-lookup"><span data-stu-id="9f46b-119">The LOCALFORMULAEXISTS function returns 1 if the cell contains a local formula; if there is no formula, or if the formula is inherited, it returns 0 (zero).</span></span> 
  

