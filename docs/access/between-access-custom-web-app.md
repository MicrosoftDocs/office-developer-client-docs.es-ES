---
title: BETWEEN (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Especifica un intervalo que se va a probar.
ms.openlocfilehash: fd67d1163f6a39779e0202b5ca1ba998ba8650a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429302"
---
# <a name="between-access-custom-web-app"></a><span data-ttu-id="7cc99-103">BETWEEN (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="7cc99-103">BETWEEN (Access custom web app)</span></span>

<span data-ttu-id="7cc99-104">Especifica un intervalo que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="7cc99-104">Specifies a range to test.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="7cc99-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="7cc99-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7cc99-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7cc99-107">Syntax</span></span>

 <span data-ttu-id="7cc99-108">*test_expression*  [ NO] **ENTRE** *begin_expression* **Y** *end_expression*</span><span class="sxs-lookup"><span data-stu-id="7cc99-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span></span> 
  
<span data-ttu-id="7cc99-109">El **operador Between** contiene los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="7cc99-109">The **Between** operator contains the following arguments.</span></span> 
  
|<span data-ttu-id="7cc99-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="7cc99-110">**Argument**</span></span>|<span data-ttu-id="7cc99-111">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="7cc99-111">**Required**</span></span>|<span data-ttu-id="7cc99-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7cc99-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="7cc99-113">*test_expression*</span><span class="sxs-lookup"><span data-stu-id="7cc99-113">*test_expression*</span></span>  <br/> |<span data-ttu-id="7cc99-114">Sí</span><span class="sxs-lookup"><span data-stu-id="7cc99-114">Yes</span></span>  <br/> |<span data-ttu-id="7cc99-115">Expresión que se va a probar en el intervalo definido por  *begin_expression*  y  *end_expression*  .</span><span class="sxs-lookup"><span data-stu-id="7cc99-115">The expression to test for in the range defined by  *begin_expression*  and  *end_expression*  .</span></span> <span data-ttu-id="7cc99-116">Debe ser el mismo tipo de datos que  *begin_expression*  y  *end_expression*  .</span><span class="sxs-lookup"><span data-stu-id="7cc99-116">Must be the same data type as both  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="7cc99-117">*NOT*</span><span class="sxs-lookup"><span data-stu-id="7cc99-117">*NOT*</span></span>  <br/> |<span data-ttu-id="7cc99-118">No</span><span class="sxs-lookup"><span data-stu-id="7cc99-118">No</span></span>  <br/> |<span data-ttu-id="7cc99-119">Especifica que se nega el resultado del predicado.</span><span class="sxs-lookup"><span data-stu-id="7cc99-119">Specifies that the result of the predicate be negated.</span></span>  <br/> |
| <span data-ttu-id="7cc99-120">*begin_expression*</span><span class="sxs-lookup"><span data-stu-id="7cc99-120">*begin_expression*</span></span>  <br/> |<span data-ttu-id="7cc99-121">Sí</span><span class="sxs-lookup"><span data-stu-id="7cc99-121">Yes</span></span>  <br/> |<span data-ttu-id="7cc99-122">Expresión válida.</span><span class="sxs-lookup"><span data-stu-id="7cc99-122">A valid expression.</span></span> <span data-ttu-id="7cc99-123">Debe ser el mismo tipo de datos que  *test_expression*  y  *end_expression*  .</span><span class="sxs-lookup"><span data-stu-id="7cc99-123">Must be the same data type as both  *test_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="7cc99-124">*end_expression*</span><span class="sxs-lookup"><span data-stu-id="7cc99-124">*end_expression*</span></span>  <br/> |<span data-ttu-id="7cc99-125">Sí</span><span class="sxs-lookup"><span data-stu-id="7cc99-125">Yes</span></span>  <br/> |<span data-ttu-id="7cc99-126">Expresión válida.</span><span class="sxs-lookup"><span data-stu-id="7cc99-126">A valid expression.</span></span> <span data-ttu-id="7cc99-127">Debe ser el mismo tipo de datos que  *test_expression*  y  *begin_expression*  .</span><span class="sxs-lookup"><span data-stu-id="7cc99-127">Must be the same data type as both  *test_expression*  and  *begin_expression*  .</span></span>  <br/> |
| <span data-ttu-id="7cc99-128">*AND*</span><span class="sxs-lookup"><span data-stu-id="7cc99-128">*AND*</span></span>  <br/> |<span data-ttu-id="7cc99-129">Sí</span><span class="sxs-lookup"><span data-stu-id="7cc99-129">Yes</span></span>  <br/> |<span data-ttu-id="7cc99-130">Indica que  *test_expression*  debe estar dentro del intervalo indicado por  *begin_expression*  y  *end_expression*  .</span><span class="sxs-lookup"><span data-stu-id="7cc99-130">Indicates  *test_expression*  should be within the range indicated by  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
   
## <a name="result-type"></a><span data-ttu-id="7cc99-131">Tipo de resultado</span><span class="sxs-lookup"><span data-stu-id="7cc99-131">Result Type</span></span>

 <span data-ttu-id="7cc99-132">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7cc99-132">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7cc99-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7cc99-133">Remarks</span></span>

 <span data-ttu-id="7cc99-134">**BETWEEN** devuelve **TRUE** si el valor de  *test_expression*  es mayor o igual que el valor de  *begin_expression*  y menor o igual que el valor de  *end_expression*  .</span><span class="sxs-lookup"><span data-stu-id="7cc99-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span></span> 
  
 <span data-ttu-id="7cc99-135">**NOT BETWEEN** devuelve **TRUE** si el valor de  *test_expression*  es menor que el valor de  *begin_expression*  o mayor que el valor de  *end_expression*  .</span><span class="sxs-lookup"><span data-stu-id="7cc99-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span></span> 
  
<span data-ttu-id="7cc99-136">Para especificar un intervalo exclusivo, use los operadores mayor que ( ) y \> menor que ( \< ).</span><span class="sxs-lookup"><span data-stu-id="7cc99-136">To specify an exclusive range, use the greater than (\>) and less than operators (\<).</span></span>
  

