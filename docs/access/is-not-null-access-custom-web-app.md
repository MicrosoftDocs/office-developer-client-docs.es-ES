---
title: IS [NOT] NULL (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Determina si una expresión especificada es NULL.
localization_priority: Priority
ms.openlocfilehash: fe6a0fe4f182a1385304b783e7cfaaf515f732d4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699320"
---
# <a name="is-not-null-access-custom-web-app"></a><span data-ttu-id="c382b-103">IS [NOT] NULL (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="c382b-103">IS [NOT] NULL (Access custom web app)</span></span>

<span data-ttu-id="c382b-104">Determina si una expresión especificada es NULL.</span><span class="sxs-lookup"><span data-stu-id="c382b-104">Determines whether a specified expression is NULL.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c382b-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="c382b-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c382b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c382b-107">Syntax</span></span>

 <span data-ttu-id="c382b-108">*expression* **IS** [  *NOT*  ] **NULL**</span><span class="sxs-lookup"><span data-stu-id="c382b-108">*expression* **IS** [  *NOT*  ] **NULL**</span></span>
  
<span data-ttu-id="c382b-109">El predicado **IS [NOT] NULL** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="c382b-109">The **IS [NOT] NULL** predicate contains the following arguments.</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c382b-110">*expression*</span><span class="sxs-lookup"><span data-stu-id="c382b-110">*expression*</span></span>  <br/> |<span data-ttu-id="c382b-111">Cualquier expresión válida.</span><span class="sxs-lookup"><span data-stu-id="c382b-111">Any valid expression.</span></span>  <br/> |
| <span data-ttu-id="c382b-112">*NOT*</span><span class="sxs-lookup"><span data-stu-id="c382b-112">*NOT*</span></span>  <br/> |<span data-ttu-id="c382b-p102">Especifica que se niega el resultado Boolean. El predicado invierte los valores devueltos, devolviendo TRUE si el valor no es NULL y FALSE si el valor es NULL.</span><span class="sxs-lookup"><span data-stu-id="c382b-p102">Specifies that the Boolean result be negated. The predicate reverses its return values, returning TRUE if the value is not NULL, and FALSE if the value is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c382b-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c382b-115">Remarks</span></span>

<span data-ttu-id="c382b-116">Si el valor de  *expresión*  es NULL, IS NULL devuelve TRUE; de lo contrario, devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="c382b-116">If the value of  *expression*  is NULL, IS NULL returns TRUE; otherwise, it returns FALSE.</span></span> 
  
<span data-ttu-id="c382b-117">Si el valor de la expresión es NULL, IS NOT NULL devuelve FALSE; de lo contrario, devuelve TRUE.</span><span class="sxs-lookup"><span data-stu-id="c382b-117">If the value of expression is NULL, IS NOT NULL returns FALSE; otherwise, it returns TRUE.</span></span>
  

