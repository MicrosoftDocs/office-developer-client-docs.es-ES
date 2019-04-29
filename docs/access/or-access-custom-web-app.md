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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414763"
---
# <a name="or-access-custom-web-app"></a><span data-ttu-id="bf27d-104">O (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="bf27d-104">OR (Access custom web app)</span></span>

<span data-ttu-id="bf27d-105">Combina dos condiciones.</span><span class="sxs-lookup"><span data-stu-id="bf27d-105">Combines two conditions.</span></span> <span data-ttu-id="bf27d-106">Devuelve TRUE si cualquiera de las dos condiciones es true.</span><span class="sxs-lookup"><span data-stu-id="bf27d-106">Returns TRUE when either of the two conditions is true.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="bf27d-p103">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="bf27d-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bf27d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf27d-109">Syntax</span></span>

 <span data-ttu-id="bf27d-110">*Expresiónbooleana* **O bien** *Expresiónbooleana*</span><span class="sxs-lookup"><span data-stu-id="bf27d-110">*BooleanExpression* **Or** *BooleanExpression*</span></span> 
  
<span data-ttu-id="bf27d-111">El operador **or** utiliza el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="bf27d-111">The **Or** operator uses the following argument.</span></span> 
  
|<span data-ttu-id="bf27d-112">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="bf27d-112">**Argument name**</span></span>|<span data-ttu-id="bf27d-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bf27d-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bf27d-114">*Expresiónbooleana*</span><span class="sxs-lookup"><span data-stu-id="bf27d-114">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="bf27d-115">Cualquier expresión válida que devuelva TRUE o FALSE.</span><span class="sxs-lookup"><span data-stu-id="bf27d-115">Any valid expression that returns TRUE or FALSE.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf27d-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf27d-116">Remarks</span></span>

<span data-ttu-id="bf27d-117">Cuando se usa más de un operador lógico en una instrucción, los operadores **or** se evalúan después de los operadores **and** .</span><span class="sxs-lookup"><span data-stu-id="bf27d-117">When more than one logical operator is used in a statement, **Or** operators are evaluated after **And** operators.</span></span> <span data-ttu-id="bf27d-118">Sin embargo, puede cambiar el orden de evaluación mediante paréntesis.</span><span class="sxs-lookup"><span data-stu-id="bf27d-118">However, you can change the order of evaluation by using parentheses.</span></span> 
  
<span data-ttu-id="bf27d-119">En la siguiente tabla se muestra el resultado del operador **or** .</span><span class="sxs-lookup"><span data-stu-id="bf27d-119">The following table shows the result of the **Or** operator.</span></span> 
  
||<span data-ttu-id="bf27d-120">**CASO**</span><span class="sxs-lookup"><span data-stu-id="bf27d-120">**TRUE**</span></span>|<span data-ttu-id="bf27d-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="bf27d-121">**FALSE**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bf27d-122">**CASO**</span><span class="sxs-lookup"><span data-stu-id="bf27d-122">**TRUE**</span></span> <br/> |<span data-ttu-id="bf27d-123">TRUE</span><span class="sxs-lookup"><span data-stu-id="bf27d-123">TRUE</span></span>  <br/> |<span data-ttu-id="bf27d-124">TRUE</span><span class="sxs-lookup"><span data-stu-id="bf27d-124">TRUE</span></span>  <br/> |
|<span data-ttu-id="bf27d-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="bf27d-125">**FALSE**</span></span> <br/> |<span data-ttu-id="bf27d-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="bf27d-126">TRUE</span></span>  <br/> |<span data-ttu-id="bf27d-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="bf27d-127">FALSE</span></span>  <br/> |
   

