---
title: Es igual a (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Compara la igualdad de dos expresiones.
ms.openlocfilehash: efdd06a1735190d63c13c4df8230e1d29d71c1dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815347"
---
# <a name="equals-access-custom-web-app"></a><span data-ttu-id="61dd9-103">Es igual a (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="61dd9-103">Equals (Access custom web app)</span></span>

<span data-ttu-id="61dd9-104">Compara la igualdad de dos expresiones.</span><span class="sxs-lookup"><span data-stu-id="61dd9-104">Compares the equality of two expressions.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="61dd9-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="61dd9-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="61dd9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61dd9-107">Syntax</span></span>

`= (Equals)`

<span data-ttu-id="61dd9-108">*expresión*  =  *expresión*</span><span class="sxs-lookup"><span data-stu-id="61dd9-108">*expression*  =  *expression*</span></span> 
  
<span data-ttu-id="61dd9-109">*expresión*  Es cualquier expresión válida.</span><span class="sxs-lookup"><span data-stu-id="61dd9-109">*expression*  Is any valid expression.</span></span> <span data-ttu-id="61dd9-110">Si las expresiones no son del mismo tipo de datos, el tipo de datos para una expresión debe ser implícitamente convertible al tipo de datos de la otra.</span><span class="sxs-lookup"><span data-stu-id="61dd9-110">If the expressions are not of the same data type, the data type for one expression must be implicitly convertible to the data type of the other.</span></span> <span data-ttu-id="61dd9-111">La conversión depende de las reglas de precedencia de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="61dd9-111">The conversion depends on the rules of data type precedence.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="61dd9-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61dd9-112">Return Type</span></span>

<span data-ttu-id="61dd9-113">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="61dd9-113">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="61dd9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="61dd9-114">Remarks</span></span>

<span data-ttu-id="61dd9-115">Cuando se comparan dos expresiones NULL, el resultado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="61dd9-115">When you compare two NULL expressions, the result is TRUE.</span></span>
  
<span data-ttu-id="61dd9-116">Comparación de NULL en un valor no nulo siempre da como resultado FALSE.</span><span class="sxs-lookup"><span data-stu-id="61dd9-116">Comparing NULL to a non-NULL value always results in FALSE.</span></span>
  

