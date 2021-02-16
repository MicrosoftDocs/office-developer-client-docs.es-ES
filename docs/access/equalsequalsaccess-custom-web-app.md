---
title: Igual a(Aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Compara la igualdad de dos expresiones.
ms.openlocfilehash: 8c551e3dbc057433b49bc2558e08feba5ee3d04f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408932"
---
# <a name="equals-access-custom-web-app"></a><span data-ttu-id="f17c0-103">Es igual a (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="f17c0-103">Equals (Access custom web app)</span></span>

<span data-ttu-id="f17c0-104">Compara la igualdad de dos expresiones.</span><span class="sxs-lookup"><span data-stu-id="f17c0-104">Compares the equality of two expressions.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="f17c0-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="f17c0-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f17c0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f17c0-107">Syntax</span></span>

`= (Equals)`

<span data-ttu-id="f17c0-108">*expresión*   =   *expresión*</span><span class="sxs-lookup"><span data-stu-id="f17c0-108">*expression*  =  *expression*</span></span> 
  
<span data-ttu-id="f17c0-109">*expresión*  Es cualquier expresión válida.</span><span class="sxs-lookup"><span data-stu-id="f17c0-109">*expression*  Is any valid expression.</span></span> <span data-ttu-id="f17c0-110">Si las expresiones no son del mismo tipo de datos, el tipo de datos de una expresión debe ser implícitamente convertible al tipo de datos de la otra.</span><span class="sxs-lookup"><span data-stu-id="f17c0-110">If the expressions are not of the same data type, the data type for one expression must be implicitly convertible to the data type of the other.</span></span> <span data-ttu-id="f17c0-111">La conversión depende de las reglas de prioridad del tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f17c0-111">The conversion depends on the rules of data type precedence.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="f17c0-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f17c0-112">Return Type</span></span>

<span data-ttu-id="f17c0-113">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f17c0-113">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f17c0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f17c0-114">Remarks</span></span>

<span data-ttu-id="f17c0-115">Cuando se comparan dos expresiones NULL, el resultado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="f17c0-115">When you compare two NULL expressions, the result is TRUE.</span></span>
  
<span data-ttu-id="f17c0-116">La comparación de NULL con un valor que no es NULL siempre da como resultado FALSE.</span><span class="sxs-lookup"><span data-stu-id="f17c0-116">Comparing NULL to a non-NULL value always results in FALSE.</span></span>
  

