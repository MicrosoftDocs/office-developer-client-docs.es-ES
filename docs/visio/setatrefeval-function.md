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
description: Se usa en el parámetro expresión_conjunto de la función SETATREF para indicar que expresión_conjunto debe evaluarse antes de asignarse al parámetro de referencia en SETATREF.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326162"
---
# <a name="setatrefeval-function"></a><span data-ttu-id="bd975-103">Función SETATREFEVAL</span><span class="sxs-lookup"><span data-stu-id="bd975-103">SETATREFEVAL Function</span></span>

<span data-ttu-id="bd975-104">Se usa en el parámetro _expresión_conjunto_ de la función SETATREF para indicar que _expresión_conjunto_ debe evaluarse antes de asignarse al parámetro de _referencia_ en SETATREF.</span><span class="sxs-lookup"><span data-stu-id="bd975-104">Used in the  _set_expression_ parameter of the SETATREF function to indicate that  _set_expression_ should be evaluated before assigning to the  _reference_ parameter in SETATREF.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bd975-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd975-105">Syntax</span></span>

<span data-ttu-id="bd975-106">SETATREFEVAL (\* \* *expr* \* \*)</span><span class="sxs-lookup"><span data-stu-id="bd975-106">SETATREFEVAL(\*\* *expr* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bd975-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd975-107">Parameters</span></span>

|<span data-ttu-id="bd975-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="bd975-108">**Name**</span></span>|<span data-ttu-id="bd975-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="bd975-109">**Required/Optional**</span></span>|<span data-ttu-id="bd975-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="bd975-110">**Data Type**</span></span>|<span data-ttu-id="bd975-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bd975-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bd975-112">_expr_</span><span class="sxs-lookup"><span data-stu-id="bd975-112">_expr_</span></span> <br/> |<span data-ttu-id="bd975-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bd975-113">Required</span></span>  <br/> |<span data-ttu-id="bd975-114">**Diferencias**</span><span class="sxs-lookup"><span data-stu-id="bd975-114">**Varies**</span></span> <br/> | <span data-ttu-id="bd975-115">Expresión que se evalúa cuando la función SETATREF redirige _expresión_conjunto_ a otra celda.</span><span class="sxs-lookup"><span data-stu-id="bd975-115">An expression that is evaluated when the SETATREF function redirects  _set_expression_ to another cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd975-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bd975-116">Remarks</span></span>

<span data-ttu-id="bd975-117">Cuando se asigna el parámetro *expresión_conjunto* de la función SETATREF a una celda a la que se hace referencia, Microsoft Visio escribe *expresión_conjunto* en la celda como una expresión de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="bd975-117">When assigning the  *set_expression*  parameter of the SETATREF function to a referenced cell, Microsoft Visio writes  *set_expression*  to the cell as an expression by default.</span></span> <span data-ttu-id="bd975-118">Sin embargo, si alguna parte del parámetro *expresión_conjunto* está ajustada por la función Setatrefeval, Visio evalúa la expresión y reemplaza la función setatrefeval por el resultado antes de resolver la expresión SETATREF.</span><span class="sxs-lookup"><span data-stu-id="bd975-118">However, if any portion of the  *set_expression*  parameter is wrapped by the SETATREFEVAL function, Visio evaluates the expression and replaces the SETATREFEVAL function with its result prior to resolving the SETATREF expression.</span></span> 
  
## <a name="example"></a><span data-ttu-id="bd975-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bd975-119">Example</span></span>

<span data-ttu-id="bd975-120">Para conocer un ejemplo, vea el tema que trata la función [SETATREF](setatref-function.md).</span><span class="sxs-lookup"><span data-stu-id="bd975-120">For an example, see the [SETATREF](setatref-function.md) function.</span></span> 
  

