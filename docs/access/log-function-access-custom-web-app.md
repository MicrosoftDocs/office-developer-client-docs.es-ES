---
title: Función log (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a897e812-08dc-49c9-954b-e8908a0daab3
description: Devuelve el logaritmo natural (neperiano), o bien el logaritmo de base determinada, de la expresión especificada.
ms.openlocfilehash: 5004b2b32e89a9d68364d271e8b94d72b012a62c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815308"
---
# <a name="log-function-access-custom-web-app"></a><span data-ttu-id="004c3-103">Función log (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="004c3-103">Log Function (Access custom web app)</span></span>

<span data-ttu-id="004c3-104">Devuelve el logaritmo natural (neperiano), o bien el logaritmo de base determinada, de la expresión especificada.</span><span class="sxs-lookup"><span data-stu-id="004c3-104">Returns the natural logarithm, or the logarithm of the given base, of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="004c3-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="004c3-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="004c3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="004c3-107">Syntax</span></span>

 <span data-ttu-id="004c3-108">**Registro** (*NumericExpression* , [ *Base* ])</span><span class="sxs-lookup"><span data-stu-id="004c3-108">**Log** (*NumericExpression*  , [  *Base*  ])</span></span> 
  
<span data-ttu-id="004c3-109">La función de **registro** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="004c3-109">The **Log** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="004c3-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="004c3-110">**Argument name**</span></span>|<span data-ttu-id="004c3-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="004c3-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="004c3-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="004c3-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="004c3-113">El número positivo cuyo logaritmo se desea.</span><span class="sxs-lookup"><span data-stu-id="004c3-113">The positive number for which you want the logarithm.</span></span>  <br/> |
| <span data-ttu-id="004c3-114">*Base*</span><span class="sxs-lookup"><span data-stu-id="004c3-114">*Base*</span></span>  <br/> |<span data-ttu-id="004c3-115">La base del logaritmo.</span><span class="sxs-lookup"><span data-stu-id="004c3-115">The base of the logarithm.</span></span> <span data-ttu-id="004c3-116">Si se omite, la función **Log** devuelve el logaritmo natural (neperiano).</span><span class="sxs-lookup"><span data-stu-id="004c3-116">If omitted, the **Log** function returns the natural logarithm.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="004c3-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="004c3-117">Remarks</span></span>

<span data-ttu-id="004c3-118">La función **Log10** es similar, pero siempre devuelve el logaritmo común, lo que significa el logaritmo de la base 10.</span><span class="sxs-lookup"><span data-stu-id="004c3-118">The function **Log10** is similar, but always returns the common logarithm, meaning the logarithm for the base 10.</span></span> 
  
<span data-ttu-id="004c3-119">El logaritmo natural es el logaritmo en base e, donde e es una constante irrational aproximadamente igual a 2.718281828.</span><span class="sxs-lookup"><span data-stu-id="004c3-119">The natural logarithm is the logarithm to the base e, where e is an irrational constant approximately equal to 2.718281828.</span></span>
  

