---
title: O (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Combina dos condiciones. Devuelve TRUE si cualquiera de las dos condiciones es true.
ms.openlocfilehash: ffa605d2403c5aa8396d89f78d0bb7dd11343540
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308074"
---
# <a name="or-access-custom-web-app"></a><span data-ttu-id="090fe-104">O (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="090fe-104">OR (Access custom web app)</span></span>

<span data-ttu-id="090fe-105">Combina dos condiciones.</span><span class="sxs-lookup"><span data-stu-id="090fe-105">Combines two conditions.</span></span> <span data-ttu-id="090fe-106">Devuelve TRUE si cualquiera de las dos condiciones es true.</span><span class="sxs-lookup"><span data-stu-id="090fe-106">Returns TRUE when either of the two conditions is true.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="090fe-p103">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="090fe-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="090fe-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="090fe-109">Syntax</span></span>

 <span data-ttu-id="090fe-110">*Expresiónbooleana* **O bien** *Expresiónbooleana*</span><span class="sxs-lookup"><span data-stu-id="090fe-110">*BooleanExpression* **Or** *BooleanExpression*</span></span> 
  
<span data-ttu-id="090fe-111">El operador **or** utiliza el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="090fe-111">The **Or** operator uses the following argument.</span></span> 
  
|<span data-ttu-id="090fe-112">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="090fe-112">**Argument name**</span></span>|<span data-ttu-id="090fe-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="090fe-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="090fe-114">*Expresiónbooleana*</span><span class="sxs-lookup"><span data-stu-id="090fe-114">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="090fe-115">Cualquier expresión válida que devuelva TRUE o FALSE.</span><span class="sxs-lookup"><span data-stu-id="090fe-115">Any valid expression that returns TRUE or FALSE.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="090fe-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="090fe-116">Remarks</span></span>

<span data-ttu-id="090fe-117">Cuando se usa más de un operador lógico en una instrucción, los operadores **or** se evalúan después de los operadores **and** .</span><span class="sxs-lookup"><span data-stu-id="090fe-117">When more than one logical operator is used in a statement, **Or** operators are evaluated after **And** operators.</span></span> <span data-ttu-id="090fe-118">Sin embargo, puede cambiar el orden de evaluación mediante paréntesis.</span><span class="sxs-lookup"><span data-stu-id="090fe-118">However, you can change the order of evaluation by using parentheses.</span></span> 
  
<span data-ttu-id="090fe-119">En la siguiente tabla se muestra el resultado del operador **or** .</span><span class="sxs-lookup"><span data-stu-id="090fe-119">The following table shows the result of the **Or** operator.</span></span> 
  
||<span data-ttu-id="090fe-120">**CASO**</span><span class="sxs-lookup"><span data-stu-id="090fe-120">**TRUE**</span></span>|<span data-ttu-id="090fe-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="090fe-121">**FALSE**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="090fe-122">**CASO**</span><span class="sxs-lookup"><span data-stu-id="090fe-122">**TRUE**</span></span> <br/> |<span data-ttu-id="090fe-123">TRUE</span><span class="sxs-lookup"><span data-stu-id="090fe-123">TRUE</span></span>  <br/> |<span data-ttu-id="090fe-124">TRUE</span><span class="sxs-lookup"><span data-stu-id="090fe-124">TRUE</span></span>  <br/> |
|<span data-ttu-id="090fe-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="090fe-125">**FALSE**</span></span> <br/> |<span data-ttu-id="090fe-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="090fe-126">TRUE</span></span>  <br/> |<span data-ttu-id="090fe-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="090fe-127">FALSE</span></span>  <br/> |
   

