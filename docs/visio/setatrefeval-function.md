---
title: SETATREFEVAL (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1042150
localization_priority: Normal
ms.assetid: b3f3a0a0-7b14-0b71-d247-ada81b93b66b
description: Se usa en el parámetro expresión_definida de la función SETATREF para indicar que expresión_definida debe evaluarse antes de asignar al parámetro referencia en SETATREF.
ms.openlocfilehash: 0826ef9ca91e180576c0b2611452758b238736a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823120"
---
# <a name="setatrefeval-function"></a><span data-ttu-id="39d64-103">Función SETATREFEVAL</span><span class="sxs-lookup"><span data-stu-id="39d64-103">SETATREFEVAL Function</span></span>

<span data-ttu-id="39d64-104">Se usa en el parámetro _expresión_definida_ de la función SETATREF para indicar que _expresión_conjunto_ debe evaluarse antes de asignar al parámetro _referencia_ en SETATREF.</span><span class="sxs-lookup"><span data-stu-id="39d64-104">Used in the  _set_expression_ parameter of the SETATREF function to indicate that  _set_expression_ should be evaluated before assigning to the  _reference_ parameter in SETATREF.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="39d64-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39d64-105">Syntax</span></span>

<span data-ttu-id="39d64-106">SETATREFEVAL (** *expr* **)</span><span class="sxs-lookup"><span data-stu-id="39d64-106">SETATREFEVAL(** *expr* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="39d64-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39d64-107">Parameters</span></span>

|<span data-ttu-id="39d64-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="39d64-108">**Name**</span></span>|<span data-ttu-id="39d64-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="39d64-109">**Required/Optional**</span></span>|<span data-ttu-id="39d64-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="39d64-110">**Data Type**</span></span>|<span data-ttu-id="39d64-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="39d64-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="39d64-112">_expr_</span><span class="sxs-lookup"><span data-stu-id="39d64-112">_expr_</span></span> <br/> |<span data-ttu-id="39d64-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="39d64-113">Required</span></span>  <br/> |<span data-ttu-id="39d64-114">**Varían**</span><span class="sxs-lookup"><span data-stu-id="39d64-114">**Varies**</span></span> <br/> | <span data-ttu-id="39d64-115">Una expresión que se evalúa cuando la función SETATREF redirige _expresión_definida_ a otra celda.</span><span class="sxs-lookup"><span data-stu-id="39d64-115">An expression that is evaluated when the SETATREF function redirects  _set_expression_ to another cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39d64-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="39d64-116">Remarks</span></span>

<span data-ttu-id="39d64-117">Cuando se asigna el parámetro *expresión_definida* de la función SETATREF a una celda que se hace referencia, Microsoft Visio escribe *expresión_definida* en la celda como expresión de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="39d64-117">When assigning the  *set_expression*  parameter of the SETATREF function to a referenced cell, Microsoft Visio writes  *set_expression*  to the cell as an expression by default.</span></span> <span data-ttu-id="39d64-118">Sin embargo, si cualquier parte del parámetro *expresión_conjunto* se ajusta mediante la función SETATREFEVAL, Visio evalúa la expresión y reemplaza la función SETATREFEVAL con el resultado anterior a la resolución de la expresión SETATREF.</span><span class="sxs-lookup"><span data-stu-id="39d64-118">However, if any portion of the  *set_expression*  parameter is wrapped by the SETATREFEVAL function, Visio evaluates the expression and replaces the SETATREFEVAL function with its result prior to resolving the SETATREF expression.</span></span> 
  
## <a name="example"></a><span data-ttu-id="39d64-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39d64-119">Example</span></span>

<span data-ttu-id="39d64-120">Para conocer un ejemplo, vea el tema que trata la función [SETATREF](setatref-function.md).</span><span class="sxs-lookup"><span data-stu-id="39d64-120">For an example, see the [SETATREF](setatref-function.md) function.</span></span> 
  

