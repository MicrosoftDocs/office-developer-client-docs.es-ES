---
title: Es igual a (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Compara la igualdad de dos expresiones.
ms.openlocfilehash: 8c551e3dbc057433b49bc2558e08feba5ee3d04f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308228"
---
# <a name="equals-access-custom-web-app"></a><span data-ttu-id="2a588-103">Es igual a (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="2a588-103">Equals (Access custom web app)</span></span>

<span data-ttu-id="2a588-104">Compara la igualdad de dos expresiones.</span><span class="sxs-lookup"><span data-stu-id="2a588-104">Compares the equality of two expressions.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="2a588-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="2a588-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2a588-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a588-107">Syntax</span></span>

`= (Equals)`

<span data-ttu-id="2a588-108">\*\*  =  *expresión* de expresión</span><span class="sxs-lookup"><span data-stu-id="2a588-108">*expression*  =  *expression*</span></span> 
  
<span data-ttu-id="2a588-109">*expresión*  Es cualquier expresión válida.</span><span class="sxs-lookup"><span data-stu-id="2a588-109">*expression*  Is any valid expression.</span></span> <span data-ttu-id="2a588-110">Si las expresiones no son del mismo tipo de datos, el tipo de datos de una expresión debe ser implícitamente convertible al tipo de datos del otro.</span><span class="sxs-lookup"><span data-stu-id="2a588-110">If the expressions are not of the same data type, the data type for one expression must be implicitly convertible to the data type of the other.</span></span> <span data-ttu-id="2a588-111">La conversión depende de las reglas de prioridad del tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2a588-111">The conversion depends on the rules of data type precedence.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="2a588-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a588-112">Return Type</span></span>

<span data-ttu-id="2a588-113">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2a588-113">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2a588-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a588-114">Remarks</span></span>

<span data-ttu-id="2a588-115">Cuando se comparan dos expresiones NULL, el resultado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="2a588-115">When you compare two NULL expressions, the result is TRUE.</span></span>
  
<span data-ttu-id="2a588-116">La comparación de NULL con un valor no nulo siempre da como resultado FALSE.</span><span class="sxs-lookup"><span data-stu-id="2a588-116">Comparing NULL to a non-NULL value always results in FALSE.</span></span>
  

