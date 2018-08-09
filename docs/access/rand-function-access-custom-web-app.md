---
title: Función RAND (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6390b325-025e-4546-bb19-1cd1c45ceb5a
description: Devuelve un número pseudoaleatorio entre 0 y 1.
ms.openlocfilehash: ed0f9991b2b1d9553d6d45524d6b1e4e5321ea7e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815472"
---
# <a name="rand-function-access-custom-web-app"></a><span data-ttu-id="8670c-103">Función RAND (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="8670c-103">Rand Function (Access custom web app)</span></span>

<span data-ttu-id="8670c-104">Devuelve un número pseudoaleatorio entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="8670c-104">Returns a pseudo-random number between 0 and 1.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="8670c-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="8670c-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8670c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8670c-107">Syntax</span></span>

 <span data-ttu-id="8670c-108">**RAND** ([ *Inicialización* ])</span><span class="sxs-lookup"><span data-stu-id="8670c-108">**Rand** ( [  *Seed*  ])</span></span> 
  
<span data-ttu-id="8670c-109">La función **aleatorio** contiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="8670c-109">The **Rand** function contains the following argument.</span></span> 
  
|<span data-ttu-id="8670c-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="8670c-110">**Argument name**</span></span>|<span data-ttu-id="8670c-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8670c-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8670c-112">*Seed*</span><span class="sxs-lookup"><span data-stu-id="8670c-112">*Seed*</span></span>  <br/> |<span data-ttu-id="8670c-113">Una expresión de número entero que da como resultado el valor de inicialización.</span><span class="sxs-lookup"><span data-stu-id="8670c-113">An integer expression that gives the seed value.</span></span> <span data-ttu-id="8670c-114">Si no se especifica el *valor de inicialización* , se asigna un valor de inicialización de forma aleatoria.</span><span class="sxs-lookup"><span data-stu-id="8670c-114">If  *Seed*  is not specified, a seed value is assigned at random.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8670c-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8670c-115">Remarks</span></span>

<span data-ttu-id="8670c-116">Las llamadas repetitivas de la función **aleatorio** con el mismo valor de inicialización devuelven los resultados de la misma.</span><span class="sxs-lookup"><span data-stu-id="8670c-116">Repetitive calls of the **Rand** function with the same seed return the same results.</span></span> 
  

