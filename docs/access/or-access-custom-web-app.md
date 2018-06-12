---
title: O (tener acceso a la aplicación web personalizados)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Combina dos condiciones. Devuelve TRUE cuando alguna de las dos condiciones sea verdadera.
ms.openlocfilehash: 8ccf4a12644f45e80756f72013d42310fece07fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815461"
---
# <a name="or-access-custom-web-app"></a><span data-ttu-id="e409b-104">O (tener acceso a la aplicación web personalizados)</span><span class="sxs-lookup"><span data-stu-id="e409b-104">OR (Access custom web app)</span></span>

<span data-ttu-id="e409b-105">Combina dos condiciones.</span><span class="sxs-lookup"><span data-stu-id="e409b-105">Combines two conditions.</span></span> <span data-ttu-id="e409b-106">Devuelve TRUE cuando alguna de las dos condiciones sea verdadera.</span><span class="sxs-lookup"><span data-stu-id="e409b-106">Returns TRUE when either of the two conditions is true.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e409b-p103">[!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="e409b-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e409b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e409b-109">Syntax</span></span>

 <span data-ttu-id="e409b-110">*Expresiónbooleana* **O** *Expresiónbooleana*</span><span class="sxs-lookup"><span data-stu-id="e409b-110">*BooleanExpression* **Or** *BooleanExpression*</span></span> 
  
<span data-ttu-id="e409b-111">El operador **o** utiliza el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="e409b-111">The **Or** operator uses the following argument.</span></span> 
  
|<span data-ttu-id="e409b-112">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="e409b-112">**Argument name**</span></span>|<span data-ttu-id="e409b-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e409b-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e409b-114">*Expresiónbooleana*</span><span class="sxs-lookup"><span data-stu-id="e409b-114">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="e409b-115">Cualquier expresión válida que devuelve TRUE o FALSE.</span><span class="sxs-lookup"><span data-stu-id="e409b-115">Any valid expression that returns TRUE or FALSE.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e409b-116">Notas</span><span class="sxs-lookup"><span data-stu-id="e409b-116">Remarks</span></span>

<span data-ttu-id="e409b-117">Cuando se utiliza más de un operador lógico en una instrucción, se evalúan los operadores **o** después de los operadores **y** .</span><span class="sxs-lookup"><span data-stu-id="e409b-117">When more than one logical operator is used in a statement, **Or** operators are evaluated after **And** operators.</span></span> <span data-ttu-id="e409b-118">Sin embargo, puede cambiar el orden de evaluación mediante el uso de paréntesis.</span><span class="sxs-lookup"><span data-stu-id="e409b-118">However, you can change the order of evaluation by using parentheses.</span></span> 
  
<span data-ttu-id="e409b-119">En la siguiente tabla se muestra el resultado del operador **o** .</span><span class="sxs-lookup"><span data-stu-id="e409b-119">The following table shows the result of the **Or** operator.</span></span> 
  
||<span data-ttu-id="e409b-120">**ES TRUE**</span><span class="sxs-lookup"><span data-stu-id="e409b-120">**TRUE**</span></span>|<span data-ttu-id="e409b-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="e409b-121">**FALSE**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e409b-122">**ES TRUE**</span><span class="sxs-lookup"><span data-stu-id="e409b-122">**TRUE**</span></span> <br/> |<span data-ttu-id="e409b-123">TRUE</span><span class="sxs-lookup"><span data-stu-id="e409b-123">TRUE</span></span>  <br/> |<span data-ttu-id="e409b-124">TRUE</span><span class="sxs-lookup"><span data-stu-id="e409b-124">TRUE</span></span>  <br/> |
|<span data-ttu-id="e409b-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="e409b-125">**FALSE**</span></span> <br/> |<span data-ttu-id="e409b-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="e409b-126">TRUE</span></span>  <br/> |<span data-ttu-id="e409b-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="e409b-127">FALSE</span></span>  <br/> |
   

