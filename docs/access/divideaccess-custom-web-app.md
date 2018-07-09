---
title: / (Dividir) (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: Divide un número por otro.
ms.openlocfilehash: fd5ce0f26d6ea03f14103cd76779a95ca8a34b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815350"
---
# <a name="-divide-access-custom-web-app"></a><span data-ttu-id="75ef1-103">/ (Dividir) (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="75ef1-103">/ (Divide) (Access custom web app)</span></span>

<span data-ttu-id="75ef1-104">Divide un número por otro.</span><span class="sxs-lookup"><span data-stu-id="75ef1-104">Divides one number by another.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="75ef1-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="75ef1-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="75ef1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="75ef1-107">Syntax</span></span>

 <span data-ttu-id="75ef1-108">*cheques*  /  *divisor*</span><span class="sxs-lookup"><span data-stu-id="75ef1-108">*dividend*  /  *divisor*</span></span> 
  
 <span data-ttu-id="75ef1-109">*cheques*  Es la expresión numérica que dividir.</span><span class="sxs-lookup"><span data-stu-id="75ef1-109">*dividend*  Is the numeric expression to divide.</span></span> <span data-ttu-id="75ef1-110">Puede ser cualquier expresión válida de cualquier uno de los tipos de datos de la categoría de tipo de datos numéricos, excepto el tipo de datos datetime.</span><span class="sxs-lookup"><span data-stu-id="75ef1-110">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
 <span data-ttu-id="75ef1-111">*Divisor*  Es la expresión numérica por la que se va a dividir el dividendo.</span><span class="sxs-lookup"><span data-stu-id="75ef1-111">*Divisor*  Is the numeric expression by which to divide the dividend.</span></span> <span data-ttu-id="75ef1-112">Puede ser cualquier expresión válida de cualquier uno de los tipos de datos de la categoría de tipo de datos numéricos, excepto el tipo de datos datetime.</span><span class="sxs-lookup"><span data-stu-id="75ef1-112">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="75ef1-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75ef1-113">Return Type</span></span>

<span data-ttu-id="75ef1-114">Devuelve el tipo de datos del argumento con la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="75ef1-114">Returns the data type of the argument with the higher precedence.</span></span> 
  
<span data-ttu-id="75ef1-115">Si un número entero *cheques* se dividen por un *divisor* de tipo entero, el resultado es un entero que tiene cualquier parte fraccionaria del resultado truncado.</span><span class="sxs-lookup"><span data-stu-id="75ef1-115">If an integer  *dividend*  is divided by an integer  *divisor*  , the result is an integer that has any fractional part of the result truncated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="75ef1-116">Notas</span><span class="sxs-lookup"><span data-stu-id="75ef1-116">Remarks</span></span>

<span data-ttu-id="75ef1-117">El valor real devuelto por el operador / es el cociente de la primera expresión, dividida por la segunda expresión.</span><span class="sxs-lookup"><span data-stu-id="75ef1-117">The actual value returned by the / operator is the quotient of the first expression divided by the second expression.</span></span>
  

