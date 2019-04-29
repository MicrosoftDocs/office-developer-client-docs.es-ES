---
title: Función Var (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Devuelve la varianza estadística de una muestra de llenado representada como un conjunto de valores contenidos en un campo especificado de una consulta.
ms.openlocfilehash: 80cea512b0386d9b0461c927675ae51be3e0dcda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437759"
---
# <a name="var-function-access-custom-web-app"></a><span data-ttu-id="8a5e1-103">Función Var (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="8a5e1-103">Var Function (Access custom web app)</span></span>

<span data-ttu-id="8a5e1-104">Devuelve la varianza estadística de una muestra de llenado representada como un conjunto de valores contenidos en un campo especificado de una consulta.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-104">Returns the statistical variance for a population sample represented as a set of values contained in a specified field in a query.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="8a5e1-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8a5e1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a5e1-107">Syntax</span></span>

 <span data-ttu-id="8a5e1-108">**Var** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="8a5e1-108">**Var** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="8a5e1-109">La función **var** contiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-109">The **Var** function contains the following argument.</span></span> 
  
|<span data-ttu-id="8a5e1-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-110">**Argument name**</span></span>|<span data-ttu-id="8a5e1-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8a5e1-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="8a5e1-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="8a5e1-113">Una expresión de texto que identifica el campo que contiene los datos numéricos que desea evaluar o una expresión que realiza un cálculo con los datos de ese campo.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-113">A text expression identifying the field that contains the numeric data you want to evaluate or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="8a5e1-114">Los operandos de *NumericExpression* pueden incluir el nombre de un campo de tabla, una constante o una función (que puede ser intrínseca o definida por el usuario, pero no una de las otras funciones de agregado de SQL).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a5e1-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8a5e1-115">Remarks</span></span>

 <span data-ttu-id="8a5e1-116">**Var** solo se puede usar con columnas numéricas.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-116">**Var** can be used with numeric columns only.</span></span> <span data-ttu-id="8a5e1-117">Se omiten los valores NULL.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-117">Null values are ignored.</span></span> 
  

