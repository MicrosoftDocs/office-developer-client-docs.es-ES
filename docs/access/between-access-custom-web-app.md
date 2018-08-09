---
title: ENTRE (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Especifica un intervalo para probar.
ms.openlocfilehash: 0ef3384d6a29826968220f8d6cfc0d2f85e1131c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815334"
---
# <a name="between-access-custom-web-app"></a><span data-ttu-id="9fbc5-103">ENTRE (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="9fbc5-103">BETWEEN (Access custom web app)</span></span>

<span data-ttu-id="9fbc5-104">Especifica un intervalo para probar.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-104">Specifies a range to test.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9fbc5-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9fbc5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fbc5-107">Syntax</span></span>

 <span data-ttu-id="9fbc5-108">*test_expression*  [NOT] **BETWEEN** *begin_expression* **AND** *end_expression*</span><span class="sxs-lookup"><span data-stu-id="9fbc5-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span></span> 
  
<span data-ttu-id="9fbc5-109">El operador **entre** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-109">The **Between** operator contains the following arguments.</span></span> 
  
|<span data-ttu-id="9fbc5-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="9fbc5-110">**Argument**</span></span>|<span data-ttu-id="9fbc5-111">**Necesario**</span><span class="sxs-lookup"><span data-stu-id="9fbc5-111">**Required**</span></span>|<span data-ttu-id="9fbc5-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9fbc5-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9fbc5-113">*test_expression*</span><span class="sxs-lookup"><span data-stu-id="9fbc5-113">*test_expression*</span></span>  <br/> |<span data-ttu-id="9fbc5-114">Sí</span><span class="sxs-lookup"><span data-stu-id="9fbc5-114">Yes</span></span>  <br/> |<span data-ttu-id="9fbc5-115">La expresión para la prueba en el intervalo definido mediante *begin_expression* y *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="9fbc5-115">The expression to test for in the range defined by  *begin_expression*  and  *end_expression*  .</span></span> <span data-ttu-id="9fbc5-116">Debe ser del mismo tipo de datos como *begin_expression* y *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="9fbc5-116">Must be the same data type as both  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="9fbc5-117">*NOT*</span><span class="sxs-lookup"><span data-stu-id="9fbc5-117">*NOT*</span></span>  <br/> |<span data-ttu-id="9fbc5-118">No</span><span class="sxs-lookup"><span data-stu-id="9fbc5-118">No</span></span>  <br/> |<span data-ttu-id="9fbc5-119">Especifica que se niega el resultado del predicado.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-119">Specifies that the result of the predicate be negated.</span></span>  <br/> |
| <span data-ttu-id="9fbc5-120">*begin_expression*</span><span class="sxs-lookup"><span data-stu-id="9fbc5-120">*begin_expression*</span></span>  <br/> |<span data-ttu-id="9fbc5-121">Sí</span><span class="sxs-lookup"><span data-stu-id="9fbc5-121">Yes</span></span>  <br/> |<span data-ttu-id="9fbc5-122">Una expresión válida.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-122">A valid expression.</span></span> <span data-ttu-id="9fbc5-123">Debe ser del mismo tipo de datos que *test_expression* y *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="9fbc5-123">Must be the same data type as both  *test_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="9fbc5-124">*end_expression*</span><span class="sxs-lookup"><span data-stu-id="9fbc5-124">*end_expression*</span></span>  <br/> |<span data-ttu-id="9fbc5-125">Sí</span><span class="sxs-lookup"><span data-stu-id="9fbc5-125">Yes</span></span>  <br/> |<span data-ttu-id="9fbc5-126">Una expresión válida.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-126">A valid expression.</span></span> <span data-ttu-id="9fbc5-127">Debe ser del mismo tipo de datos que *test_expression* y *begin_expression* .</span><span class="sxs-lookup"><span data-stu-id="9fbc5-127">Must be the same data type as both  *test_expression*  and  *begin_expression*  .</span></span>  <br/> |
| <span data-ttu-id="9fbc5-128">*AND*</span><span class="sxs-lookup"><span data-stu-id="9fbc5-128">*AND*</span></span>  <br/> |<span data-ttu-id="9fbc5-129">Sí</span><span class="sxs-lookup"><span data-stu-id="9fbc5-129">Yes</span></span>  <br/> |<span data-ttu-id="9fbc5-130">Indica que *test_expression* debe estar dentro del intervalo indicado por *begin_expression* y *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="9fbc5-130">Indicates  *test_expression*  should be within the range indicated by  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
   
## <a name="result-type"></a><span data-ttu-id="9fbc5-131">Tipo de resultado</span><span class="sxs-lookup"><span data-stu-id="9fbc5-131">Result Type</span></span>

 <span data-ttu-id="9fbc5-132">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9fbc5-132">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9fbc5-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9fbc5-133">Remarks</span></span>

 <span data-ttu-id="9fbc5-134">**BETWEEN** devuelve **TRUE** si el valor de *test_expression* es mayor o igual que el valor de *begin_expression* y menor o igual que el valor de *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="9fbc5-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span></span> 
  
 <span data-ttu-id="9fbc5-135">**NOT BETWEEN** devuelve **TRUE** si el valor de *test_expression* es menor que el valor de *begin_expression* o mayor que el valor de *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="9fbc5-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span></span> 
  
<span data-ttu-id="9fbc5-136">Para especificar un intervalo exclusivo, use el mayor que (\>) operadores y menor que (\<).</span><span class="sxs-lookup"><span data-stu-id="9fbc5-136">To specify an exclusive range, use the greater than (\>) and less than operators (\<).</span></span>
  

