---
title: Función Count (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Devuelve el número de registros de una consulta o una tabla.
ms.openlocfilehash: 98dbed393bf2f6dc401119f6c5dc7ab6b5ff7864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419145"
---
# <a name="count-function-access-custom-web-app"></a><span data-ttu-id="b58dd-103">Función Count (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="b58dd-103">Count function (Access custom web app)</span></span>

<span data-ttu-id="b58dd-104">Devuelve el número de registros de una consulta o una tabla.</span><span class="sxs-lookup"><span data-stu-id="b58dd-104">Returns the number of records in a query or table.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b58dd-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="b58dd-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b58dd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b58dd-107">Syntax</span></span>

<span data-ttu-id="b58dd-108">**Número** de (*Expresión*)</span><span class="sxs-lookup"><span data-stu-id="b58dd-108">**Count** (*Expression*)</span></span> 
  
<span data-ttu-id="b58dd-109">La función **Count** contiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="b58dd-109">The **Count** function contains the following argument.</span></span> 
  
|<span data-ttu-id="b58dd-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="b58dd-110">**Argument name**</span></span>|<span data-ttu-id="b58dd-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b58dd-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b58dd-112">*Expresión*</span><span class="sxs-lookup"><span data-stu-id="b58dd-112">*Expression*</span></span>  <br/> |<span data-ttu-id="b58dd-113">Una expresión de cadena que identifica el campo que contiene los datos que desea contar o una expresión que realiza un cálculo con los datos del campo.</span><span class="sxs-lookup"><span data-stu-id="b58dd-113">A string expression identifying the field that contains the data you want to count or an expression that performs a calculation using the data in the field.</span></span> <span data-ttu-id="b58dd-114">Los operandos de la *expresión* pueden incluir el nombre de un campo de tabla o una función (que puede ser intrínseca o definida por el usuario, pero no puede ser ninguna de las otras funciones de agregado de SQL).</span><span class="sxs-lookup"><span data-stu-id="b58dd-114">Operands in  *Expression*  can include the name of a table field or function (which can be either intrinsic or user-defined but not other SQL aggregate functions).</span></span> <span data-ttu-id="b58dd-115">Se pueden contar todo tipo de datos, incluido texto.</span><span class="sxs-lookup"><span data-stu-id="b58dd-115">You can count any kind of data, including text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b58dd-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b58dd-116">Remarks</span></span>

<span data-ttu-id="b58dd-117">Puede usar Count para contar el número de registros de una consulta base.</span><span class="sxs-lookup"><span data-stu-id="b58dd-117">You can use Count to count the number of records in an underlying query.</span></span> <span data-ttu-id="b58dd-118">Por ejemplo, puede usar Count para contar el número de pedidos enviados a una región o país determinado.</span><span class="sxs-lookup"><span data-stu-id="b58dd-118">For example, you could use Count to count the number of orders shipped to a particular country or region.</span></span>
  
<span data-ttu-id="b58dd-119">**Número** de (\*) devuelve el número de elementos en un grupo.</span><span class="sxs-lookup"><span data-stu-id="b58dd-119">**Count** (\*) returns the number of items in a group.</span></span> <span data-ttu-id="b58dd-120">Esto incluye valores NULOs y duplicados.</span><span class="sxs-lookup"><span data-stu-id="b58dd-120">This includes NULL values and duplicates.</span></span> 
  

