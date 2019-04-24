---
title: BETWEEN (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Especifica el intervalo que se va a probar.
ms.openlocfilehash: fd67d1163f6a39779e0202b5ca1ba998ba8650a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280746"
---
# <a name="between-access-custom-web-app"></a><span data-ttu-id="12dc9-103">BETWEEN (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="12dc9-103">BETWEEN (Access custom web app)</span></span>

<span data-ttu-id="12dc9-104">Especifica el intervalo que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="12dc9-104">Specifies a range to test.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="12dc9-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="12dc9-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="12dc9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12dc9-107">Syntax</span></span>

 <span data-ttu-id="12dc9-108">*test_expression*  NO **Entre** *begin_expression* **Y** *end_expression*</span><span class="sxs-lookup"><span data-stu-id="12dc9-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span></span> 
  
<span data-ttu-id="12dc9-109">El operador **between** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="12dc9-109">The **Between** operator contains the following arguments.</span></span> 
  
|<span data-ttu-id="12dc9-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="12dc9-110">**Argument**</span></span>|<span data-ttu-id="12dc9-111">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="12dc9-111">**Required**</span></span>|<span data-ttu-id="12dc9-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="12dc9-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="12dc9-113">*argumentos*</span><span class="sxs-lookup"><span data-stu-id="12dc9-113">*test_expression*</span></span>  <br/> |<span data-ttu-id="12dc9-114">Sí</span><span class="sxs-lookup"><span data-stu-id="12dc9-114">Yes</span></span>  <br/> |<span data-ttu-id="12dc9-115">Expresión que se va a probar en el rango definido por *begin_expression* y *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="12dc9-115">The expression to test for in the range defined by  *begin_expression*  and  *end_expression*  .</span></span> <span data-ttu-id="12dc9-116">Debe ser del mismo tipo de datos que los *argumentos begin_expression* y *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="12dc9-116">Must be the same data type as both  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="12dc9-117">*NOT*</span><span class="sxs-lookup"><span data-stu-id="12dc9-117">*NOT*</span></span>  <br/> |<span data-ttu-id="12dc9-118">No</span><span class="sxs-lookup"><span data-stu-id="12dc9-118">No</span></span>  <br/> |<span data-ttu-id="12dc9-119">Especifica que se niega el resultado del predicado.</span><span class="sxs-lookup"><span data-stu-id="12dc9-119">Specifies that the result of the predicate be negated.</span></span>  <br/> |
| <span data-ttu-id="12dc9-120">*begin_expression*</span><span class="sxs-lookup"><span data-stu-id="12dc9-120">*begin_expression*</span></span>  <br/> |<span data-ttu-id="12dc9-121">Sí</span><span class="sxs-lookup"><span data-stu-id="12dc9-121">Yes</span></span>  <br/> |<span data-ttu-id="12dc9-122">Una expresión válida.</span><span class="sxs-lookup"><span data-stu-id="12dc9-122">A valid expression.</span></span> <span data-ttu-id="12dc9-123">Debe ser del mismo tipo de datos que los *argumentos test_expression* y *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="12dc9-123">Must be the same data type as both  *test_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="12dc9-124">*end_expression*</span><span class="sxs-lookup"><span data-stu-id="12dc9-124">*end_expression*</span></span>  <br/> |<span data-ttu-id="12dc9-125">Sí</span><span class="sxs-lookup"><span data-stu-id="12dc9-125">Yes</span></span>  <br/> |<span data-ttu-id="12dc9-126">Una expresión válida.</span><span class="sxs-lookup"><span data-stu-id="12dc9-126">A valid expression.</span></span> <span data-ttu-id="12dc9-127">Debe ser del mismo tipo de datos que los *argumentos test_expression* y *begin_expression* .</span><span class="sxs-lookup"><span data-stu-id="12dc9-127">Must be the same data type as both  *test_expression*  and  *begin_expression*  .</span></span>  <br/> |
| <span data-ttu-id="12dc9-128">*AND*</span><span class="sxs-lookup"><span data-stu-id="12dc9-128">*AND*</span></span>  <br/> |<span data-ttu-id="12dc9-129">Sí</span><span class="sxs-lookup"><span data-stu-id="12dc9-129">Yes</span></span>  <br/> |<span data-ttu-id="12dc9-130">Indica que *test_expression* debe estar dentro del intervalo indicado por *begin_expression* y *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="12dc9-130">Indicates  *test_expression*  should be within the range indicated by  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
   
## <a name="result-type"></a><span data-ttu-id="12dc9-131">Tipo de resultado</span><span class="sxs-lookup"><span data-stu-id="12dc9-131">Result Type</span></span>

 <span data-ttu-id="12dc9-132">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="12dc9-132">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="12dc9-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12dc9-133">Remarks</span></span>

 <span data-ttu-id="12dc9-134">**Between** devuelve **true** si el valor de *test_expression* es mayor o igual que el valor de *begin_expression* y menor o igual que el valor de *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="12dc9-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span></span> 
  
 <span data-ttu-id="12dc9-135">**Not between** devuelve **true** si el valor de *test_expression* es menor que el valor de *begin_expression* o mayor que el valor de *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="12dc9-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span></span> 
  
<span data-ttu-id="12dc9-136">Para especificar un intervalo exclusivo, use el operador mayor que\>() y menor que (\<).</span><span class="sxs-lookup"><span data-stu-id="12dc9-136">To specify an exclusive range, use the greater than (\>) and less than operators (\<).</span></span>
  

