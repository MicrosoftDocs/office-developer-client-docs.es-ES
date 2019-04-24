---
title: Función Rand (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6390b325-025e-4546-bb19-1cd1c45ceb5a
description: Devuelve un número seudo aleatorio entre 0 y 1.
ms.openlocfilehash: 02d914de9d74083a6ebf76f6d0e556fe51954a24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307997"
---
# <a name="rand-function-access-custom-web-app"></a><span data-ttu-id="6023e-103">Función Rand (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="6023e-103">Rand Function (Access custom web app)</span></span>

<span data-ttu-id="6023e-104">Devuelve un número seudo aleatorio entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="6023e-104">Returns a pseudo-random number between 0 and 1.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6023e-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="6023e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6023e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6023e-107">Syntax</span></span>

 <span data-ttu-id="6023e-108">**Aleatorio** ([ *SEED* ])</span><span class="sxs-lookup"><span data-stu-id="6023e-108">**Rand** ( [  *Seed*  ])</span></span> 
  
<span data-ttu-id="6023e-109">La función **Rand** contiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="6023e-109">The **Rand** function contains the following argument.</span></span> 
  
|<span data-ttu-id="6023e-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="6023e-110">**Argument name**</span></span>|<span data-ttu-id="6023e-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6023e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6023e-112">*Seed*</span><span class="sxs-lookup"><span data-stu-id="6023e-112">*Seed*</span></span>  <br/> |<span data-ttu-id="6023e-113">Expresión de entero que da el valor de inicialización.</span><span class="sxs-lookup"><span data-stu-id="6023e-113">An integer expression that gives the seed value.</span></span> <span data-ttu-id="6023e-114">Si \*\* no se especifica el valor de inicialización, se asigna un valor de inicialización de forma aleatoria.</span><span class="sxs-lookup"><span data-stu-id="6023e-114">If  *Seed*  is not specified, a seed value is assigned at random.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6023e-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6023e-115">Remarks</span></span>

<span data-ttu-id="6023e-116">Las llamadas repetitivas de la función **Rand** con los mismos valores de inicialización devuelven los mismos resultados.</span><span class="sxs-lookup"><span data-stu-id="6023e-116">Repetitive calls of the **Rand** function with the same seed return the same results.</span></span> 
  

