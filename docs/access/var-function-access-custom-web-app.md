---
title: Función Var (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Devuelve la varianza estadística para una muestra de llenado representada como un conjunto de valores contenidos en un campo especificado en una consulta.
ms.openlocfilehash: 9937f1985c0a7df5eb06977333ab889947891380
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815516"
---
# <a name="var-function-access-custom-web-app"></a><span data-ttu-id="6ad5d-103">Función Var (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="6ad5d-103">Var Function (Access custom web app)</span></span>

<span data-ttu-id="6ad5d-104">Devuelve la varianza estadística para una muestra de llenado representada como un conjunto de valores contenidos en un campo especificado en una consulta.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-104">Returns the statistical variance for a population sample represented as a set of values contained in a specified field in a query.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6ad5d-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6ad5d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ad5d-107">Syntax</span></span>

 <span data-ttu-id="6ad5d-108">**Var** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="6ad5d-108">**Var** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="6ad5d-109">La función **Var** contiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-109">The **Var** function contains the following argument.</span></span> 
  
|<span data-ttu-id="6ad5d-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="6ad5d-110">**Argument name**</span></span>|<span data-ttu-id="6ad5d-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ad5d-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6ad5d-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="6ad5d-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="6ad5d-113">Una expresión de texto que identifica el campo que contiene los datos numéricos que desea evaluar o una expresión que realiza un cálculo utilizando los datos de ese campo.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-113">A text expression identifying the field that contains the numeric data you want to evaluate or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="6ad5d-114">Los operandos de *NumericExpression* pueden incluir el nombre de un campo de tabla, una constante o una función (que puede ser intrínseca o definida por el usuario, pero no una de las otras funciones de agregado de SQL).</span><span class="sxs-lookup"><span data-stu-id="6ad5d-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ad5d-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ad5d-115">Remarks</span></span>

 <span data-ttu-id="6ad5d-116">**Var** pueden usarse con sólo columnas numéricas.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-116">**Var** can be used with numeric columns only.</span></span> <span data-ttu-id="6ad5d-117">Se omiten los valores nulos.</span><span class="sxs-lookup"><span data-stu-id="6ad5d-117">Null values are ignored.</span></span> 
  

