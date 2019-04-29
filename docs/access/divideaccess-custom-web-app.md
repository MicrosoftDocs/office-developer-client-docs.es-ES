---
title: /(Dividir) (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: Divide un número por otro.
ms.openlocfilehash: 48d43b224743949f86c5d206d9919a9e2d6fbcae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435190"
---
# <a name="-divide-access-custom-web-app"></a><span data-ttu-id="2a002-103">/(Dividir) (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="2a002-103">/ (Divide) (Access custom web app)</span></span>

<span data-ttu-id="2a002-104">Divide un número por otro.</span><span class="sxs-lookup"><span data-stu-id="2a002-104">Divides one number by another.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="2a002-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="2a002-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2a002-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a002-107">Syntax</span></span>

 <span data-ttu-id="2a002-108">\*\*  /  *divisor* del dividendo</span><span class="sxs-lookup"><span data-stu-id="2a002-108">*dividend*  /  *divisor*</span></span> 
  
 <span data-ttu-id="2a002-109">*dividendos*  Es la expresión numérica que se va a dividir.</span><span class="sxs-lookup"><span data-stu-id="2a002-109">*dividend*  Is the numeric expression to divide.</span></span> <span data-ttu-id="2a002-110">Puede ser cualquier expresión válida de cualquiera de los tipos de datos de la categoría de tipo de datos numéricos, excepto el tipo de datos DateTime.</span><span class="sxs-lookup"><span data-stu-id="2a002-110">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
 <span data-ttu-id="2a002-111">*Núm_divisor*  Es la expresión numérica por la que se va a dividir el dividendo.</span><span class="sxs-lookup"><span data-stu-id="2a002-111">*Divisor*  Is the numeric expression by which to divide the dividend.</span></span> <span data-ttu-id="2a002-112">Puede ser cualquier expresión válida de cualquiera de los tipos de datos de la categoría de tipo de datos numéricos, excepto el tipo de datos DateTime.</span><span class="sxs-lookup"><span data-stu-id="2a002-112">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="2a002-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a002-113">Return Type</span></span>

<span data-ttu-id="2a002-114">Devuelve el tipo de datos del argumento con la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="2a002-114">Returns the data type of the argument with the higher precedence.</span></span> 
  
<span data-ttu-id="2a002-115">Si un didivider de enteros se divide por un *divisor* de enteros, el resultado es un entero que tiene truncado cualquier parte fraccional del resultado. \*\*</span><span class="sxs-lookup"><span data-stu-id="2a002-115">If an integer  *dividend*  is divided by an integer  *divisor*  , the result is an integer that has any fractional part of the result truncated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2a002-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2a002-116">Remarks</span></span>

<span data-ttu-id="2a002-117">El valor real devuelto por el operador/es el cociente de la primera expresión dividida por la segunda expresión.</span><span class="sxs-lookup"><span data-stu-id="2a002-117">The actual value returned by the / operator is the quotient of the first expression divided by the second expression.</span></span>
  

