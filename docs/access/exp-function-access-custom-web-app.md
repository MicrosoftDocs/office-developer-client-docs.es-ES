---
title: Función EXP (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09385b75-ec0e-4dde-b9c3-9ade4a7a2b74
description: Devuelve el valor exponencial de la expresión especificada.
ms.openlocfilehash: 9c4929a25da6a8eec5984f9e9a1a6695a049614d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815312"
---
# <a name="exp-function-access-custom-web-app"></a><span data-ttu-id="6790c-103">Función EXP (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="6790c-103">Exp Function (Access custom web app)</span></span>

<span data-ttu-id="6790c-104">Devuelve el valor exponencial de la expresión especificada.</span><span class="sxs-lookup"><span data-stu-id="6790c-104">Returns the exponential value of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6790c-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="6790c-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6790c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6790c-107">Syntax</span></span>

 <span data-ttu-id="6790c-108">**Exp** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="6790c-108">**Exp** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="6790c-109">La función **Exp** contiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="6790c-109">The **Exp** function contains the following argument.</span></span> 
  
|<span data-ttu-id="6790c-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="6790c-110">**Argument name**</span></span>|<span data-ttu-id="6790c-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6790c-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6790c-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="6790c-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="6790c-113">Una expresión de tipo Double o de un tipo que puede convertirse implícitamente a Double.</span><span class="sxs-lookup"><span data-stu-id="6790c-113">An expression of type Double or of a type that can be implicitly converted to Double.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6790c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6790c-114">Remarks</span></span>

<span data-ttu-id="6790c-115">La constante **e** (2.718281...), es la base de los logaritmos naturales.</span><span class="sxs-lookup"><span data-stu-id="6790c-115">The constant **e** (2.718281…), is the base of natural logarithms.</span></span> 
  
<span data-ttu-id="6790c-116">El exponente de un número es la constante **e** elevado a la potencia del número.</span><span class="sxs-lookup"><span data-stu-id="6790c-116">The exponent of a number is the constant **e** raised to the power of the number.</span></span> <span data-ttu-id="6790c-117">Por ejemplo **Exp** (1,0) = e ^ 1.0 = 2,71828182845905 y **Exp** (10) = e ^ 10 = 22026,4657948067.</span><span class="sxs-lookup"><span data-stu-id="6790c-117">For example **Exp** (1.0) = e^1.0 = 2.71828182845905 and **Exp** (10) = e^10 = 22026.4657948067.</span></span> 
  
<span data-ttu-id="6790c-118">La función exponencial del logaritmo natural de un número es el número propio: **Exp** (LOG (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="6790c-118">The exponential of the natural logarithm of a number is the number itself: **Exp** (LOG (n)) = n.</span></span> <span data-ttu-id="6790c-119">Y el logaritmo natural de la función exponencial de un número es el número propio: LOG (**Exp** (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="6790c-119">And the natural logarithm of the exponential of a number is the number itself: LOG (**Exp** (n)) = n.</span></span> 
  

