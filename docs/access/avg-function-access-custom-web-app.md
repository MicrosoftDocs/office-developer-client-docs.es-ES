---
title: Función AVG (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Calcula la media aritmética de un conjunto de valores contenidos en un campo especificado.
ms.openlocfilehash: afe832a51fc9cd3b224087a0b06fe539f6a7004b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815323"
---
# <a name="avg-function-access-custom-web-app"></a><span data-ttu-id="0254d-103">Función AVG (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="0254d-103">Avg Function (Access custom web app)</span></span>

<span data-ttu-id="0254d-104">Calcula la media aritmética de un conjunto de valores contenidos en un campo especificado.</span><span class="sxs-lookup"><span data-stu-id="0254d-104">Calculates the arithmetic mean of a set of values contained in a specified field.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="0254d-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="0254d-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0254d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0254d-107">Syntax</span></span>

 <span data-ttu-id="0254d-108">**Avg** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="0254d-108">**Avg** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="0254d-109">La función **Avg** contiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="0254d-109">The **Avg** function contains the following argument.</span></span> 
  
|<span data-ttu-id="0254d-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="0254d-110">**Argument**</span></span>|<span data-ttu-id="0254d-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0254d-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0254d-112">NumericExpression</span><span class="sxs-lookup"><span data-stu-id="0254d-112">NumericExpression</span></span>  <br/> |<span data-ttu-id="0254d-113">Una expresión de cadena que identifica el campo que contiene los datos numéricos que desea promedio o una expresión que realiza un cálculo utilizando los datos de ese campo.</span><span class="sxs-lookup"><span data-stu-id="0254d-113">A string expression identifying the field that contains the numeric data you want to average or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="0254d-114">Los operandos de *NumericExpression* pueden incluir el nombre de un campo de tabla, una variable o una función (que puede ser intrínseca o definida por el usuario, pero no una de las otras funciones de agregado de SQL).</span><span class="sxs-lookup"><span data-stu-id="0254d-114">Operands in  *NumericExpression*  can include the name of a table field, a variable, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0254d-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0254d-115">Remarks</span></span>

<span data-ttu-id="0254d-p103">El promedio calculado por **Avg** es la media aritmética (la suma de los valores dividida entre el número de valores). **Avg** de puede usar, por ejemplo, para calcular el promedio del costo de transporte.</span><span class="sxs-lookup"><span data-stu-id="0254d-p103">The average calculated by **Avg** is the arithmetic mean (the sum of the values divided by the number of values). You could use **Avg**, for example, to calculate average freight cost.</span></span> 
  
<span data-ttu-id="0254d-118">La función **Avg** no incluye cualquiera de los valores **Null** en el cálculo.</span><span class="sxs-lookup"><span data-stu-id="0254d-118">The **Avg** function does not include any **Null** values in the calculation.</span></span> 
  
