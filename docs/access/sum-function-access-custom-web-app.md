---
title: Función SUM (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Devuelve la suma de todos los valores de la expresión.
ms.openlocfilehash: 98531a0487505c24ed62034b7c283b9765a3e7a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815504"
---
# <a name="sum-function-access-custom-web-app"></a><span data-ttu-id="48ee3-103">Función SUM (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="48ee3-103">Sum Function (Access custom web app)</span></span>

<span data-ttu-id="48ee3-104">Devuelve la suma de todos los valores de la expresión.</span><span class="sxs-lookup"><span data-stu-id="48ee3-104">Returns the sum of all the values in the expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="48ee3-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="48ee3-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="48ee3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48ee3-107">Syntax</span></span>

 <span data-ttu-id="48ee3-108">**Suma** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="48ee3-108">**Sum** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="48ee3-109">La función **Sum** contiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="48ee3-109">The **Sum** function contains the following argument.</span></span> 
  
|<span data-ttu-id="48ee3-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="48ee3-110">**Argument name**</span></span>|<span data-ttu-id="48ee3-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="48ee3-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="48ee3-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="48ee3-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="48ee3-113">Una expresión que identifica el campo que contiene los datos numéricos que desea agregar o una expresión que realiza un cálculo utilizando los datos de ese campo.</span><span class="sxs-lookup"><span data-stu-id="48ee3-113">An expression identifying the field that contains the numeric data you want to add or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="48ee3-114">Los operandos de *NumericExpression* pueden incluir el nombre de un campo de tabla, una constante o una función (que puede ser intrínseca o definida por el usuario, pero no una de las otras funciones de agregado de SQL).</span><span class="sxs-lookup"><span data-stu-id="48ee3-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48ee3-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48ee3-115">Remarks</span></span>

<span data-ttu-id="48ee3-116">La función **Sum** omite los registros que contienen valores nulos.</span><span class="sxs-lookup"><span data-stu-id="48ee3-116">The **Sum** function ignores records that contain Null values.</span></span> 
  
<span data-ttu-id="48ee3-117">La función **Sum** sólo puede utilizarse con columnas numéricas.</span><span class="sxs-lookup"><span data-stu-id="48ee3-117">The **Sum** function can only be used with numeric columns.</span></span> 
  

