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
description: Se usa en set_expression parámetro de la función SETATREF para indicar que set_expression debe evaluarse antes de asignar al parámetro de referencia en SETATREF.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432985"
---
# <a name="setatrefeval-function"></a><span data-ttu-id="b4571-103">Función SETATREFEVAL</span><span class="sxs-lookup"><span data-stu-id="b4571-103">SETATREFEVAL Function</span></span>

<span data-ttu-id="b4571-104">Se usa en _set_expression_ parámetro de la función SETATREF para indicar que set_expression debe  evaluarse antes de asignar al parámetro de referencia en SETATREF. </span><span class="sxs-lookup"><span data-stu-id="b4571-104">Used in the  _set_expression_ parameter of the SETATREF function to indicate that  _set_expression_ should be evaluated before assigning to the  _reference_ parameter in SETATREF.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b4571-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4571-105">Syntax</span></span>

<span data-ttu-id="b4571-106">SETATREFEVAL(\*\* *expr* \*\* )</span><span class="sxs-lookup"><span data-stu-id="b4571-106">SETATREFEVAL(\*\* *expr* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b4571-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4571-107">Parameters</span></span>

|<span data-ttu-id="b4571-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b4571-108">**Name**</span></span>|<span data-ttu-id="b4571-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="b4571-109">**Required/Optional**</span></span>|<span data-ttu-id="b4571-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="b4571-110">**Data Type**</span></span>|<span data-ttu-id="b4571-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b4571-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b4571-112">_expr_</span><span class="sxs-lookup"><span data-stu-id="b4571-112">_expr_</span></span> <br/> |<span data-ttu-id="b4571-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b4571-113">Required</span></span>  <br/> |<span data-ttu-id="b4571-114">**Varía**</span><span class="sxs-lookup"><span data-stu-id="b4571-114">**Varies**</span></span> <br/> | <span data-ttu-id="b4571-115">Expresión que se evalúa cuando la función SETATREF redirige set_expression  _a_ otra celda.</span><span class="sxs-lookup"><span data-stu-id="b4571-115">An expression that is evaluated when the SETATREF function redirects  _set_expression_ to another cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4571-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b4571-116">Remarks</span></span>

<span data-ttu-id="b4571-117">Al asignar el *parámetro set_expression* de la función SETATREF a una  celda a la que se hace referencia, Microsoft Visio escribe set_expression en la celda como expresión de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b4571-117">When assigning the  *set_expression*  parameter of the SETATREF function to a referenced cell, Microsoft Visio writes  *set_expression*  to the cell as an expression by default.</span></span> <span data-ttu-id="b4571-118">Sin embargo, si alguna parte del parámetro  *set_expression*  está ajustada por la función SETATREFEVAL, Visio evalúa la expresión y reemplaza la función SETATREFEVAL por su resultado antes de resolver la expresión SETATREF.</span><span class="sxs-lookup"><span data-stu-id="b4571-118">However, if any portion of the  *set_expression*  parameter is wrapped by the SETATREFEVAL function, Visio evaluates the expression and replaces the SETATREFEVAL function with its result prior to resolving the SETATREF expression.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b4571-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b4571-119">Example</span></span>

<span data-ttu-id="b4571-120">Para conocer un ejemplo, vea el tema que trata la función [SETATREF](setatref-function.md).</span><span class="sxs-lookup"><span data-stu-id="b4571-120">For an example, see the [SETATREF](setatref-function.md) function.</span></span> 
  

