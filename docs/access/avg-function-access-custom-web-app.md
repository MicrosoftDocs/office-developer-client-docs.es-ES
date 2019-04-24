---
title: Función AVG (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Calcula la media aritmética de un conjunto de valores contenidos en un campo especificado.
ms.openlocfilehash: e67cde12e66f943d3b25fe9cb2fee4fe4aea760f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282337"
---
# <a name="avg-function-access-custom-web-app"></a><span data-ttu-id="78779-103">Función AVG (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="78779-103">Avg Function (Access custom web app)</span></span>

<span data-ttu-id="78779-104">Calcula la media aritmética de un conjunto de valores contenidos en un campo especificado.</span><span class="sxs-lookup"><span data-stu-id="78779-104">Calculates the arithmetic mean of a set of values contained in a specified field.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="78779-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="78779-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="78779-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78779-107">Syntax</span></span>

 <span data-ttu-id="78779-108">**PROM** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="78779-108">**Avg** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="78779-109">La función **AVG** contiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="78779-109">The **Avg** function contains the following argument.</span></span> 
  
|<span data-ttu-id="78779-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="78779-110">**Argument**</span></span>|<span data-ttu-id="78779-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="78779-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="78779-112">NumericExpression</span><span class="sxs-lookup"><span data-stu-id="78779-112">NumericExpression</span></span>  <br/> |<span data-ttu-id="78779-113">Una expresión de cadena que identifica el campo que contiene los datos numéricos que desea calcular como promedio o una expresión que realiza un cálculo con los datos de ese campo.</span><span class="sxs-lookup"><span data-stu-id="78779-113">A string expression identifying the field that contains the numeric data you want to average or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="78779-114">Los operandos de *NumericExpression* pueden incluir el nombre de un campo de tabla, una variable o una función (que puede ser intrínseca o definida por el usuario, pero no una de las otras funciones de agregado de SQL).</span><span class="sxs-lookup"><span data-stu-id="78779-114">Operands in  *NumericExpression*  can include the name of a table field, a variable, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78779-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="78779-115">Remarks</span></span>

<span data-ttu-id="78779-p103">El promedio calculado por **Avg** es la media aritmética (la suma de los valores dividida entre el número de valores). **Avg** de puede usar, por ejemplo, para calcular el promedio del costo de transporte.</span><span class="sxs-lookup"><span data-stu-id="78779-p103">The average calculated by **Avg** is the arithmetic mean (the sum of the values divided by the number of values). You could use **Avg**, for example, to calculate average freight cost.</span></span> 
  
<span data-ttu-id="78779-118">La función **AVG** no incluye ningún valor **null** en el cálculo.</span><span class="sxs-lookup"><span data-stu-id="78779-118">The **Avg** function does not include any **Null** values in the calculation.</span></span> 
  

