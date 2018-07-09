---
title: Función de subcadena (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Devuelve la parte de una expresión de texto.
ms.openlocfilehash: 49d9afefe4b25d91738e518e0ddb2b902067c038
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815506"
---
# <a name="substring-function-access-custom-web-app"></a><span data-ttu-id="5d204-103">Función de subcadena (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="5d204-103">SubString Function (Access custom web app)</span></span>

<span data-ttu-id="5d204-104">Devuelve la parte de una expresión de texto.</span><span class="sxs-lookup"><span data-stu-id="5d204-104">Returns part of a text expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="5d204-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="5d204-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5d204-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d204-107">Syntax</span></span>

 <span data-ttu-id="5d204-108">**Subcadena** (*TextExpression*, *Inicio*, *longitud*)</span><span class="sxs-lookup"><span data-stu-id="5d204-108">**SubString** (*TextExpression*, *Start*, *Length*)</span></span> 
  
<span data-ttu-id="5d204-109">La función de **subcadena** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="5d204-109">The **SubString** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="5d204-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="5d204-110">**Argument name**</span></span>|<span data-ttu-id="5d204-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d204-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5d204-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="5d204-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="5d204-113">Una expresión de texto.</span><span class="sxs-lookup"><span data-stu-id="5d204-113">A text expression.</span></span>  <br/> |
| <span data-ttu-id="5d204-114">*Start*</span><span class="sxs-lookup"><span data-stu-id="5d204-114">*Start*</span></span>  <br/> |<span data-ttu-id="5d204-115">Una expresión de número entero que especifica dónde empezar los caracteres devueltos.</span><span class="sxs-lookup"><span data-stu-id="5d204-115">An integer expression that specifies where the returned characters start.</span></span> <span data-ttu-id="5d204-116">Si start es menor que 1, se iniciará la expresión devuelta en el primer carácter que se especifica en la expresión.</span><span class="sxs-lookup"><span data-stu-id="5d204-116">If start is less than 1, the returned expression will begin at the first character that is specified in expression.</span></span> <span data-ttu-id="5d204-117">En este caso, el número de caracteres que se devuelven es el valor mayor de puede ser la suma de inicio + longitud-1 o 0.</span><span class="sxs-lookup"><span data-stu-id="5d204-117">In this case, the number of characters that are returned is the largest value of either the sum of start + length- 1 or 0.</span></span> <span data-ttu-id="5d204-118">Si start es mayor que el número de caracteres de la expresión de valor, se devuelve una expresión de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="5d204-118">If start is greater than the number of characters in the value expression, a zero-length expression is returned.</span></span>  <br/> |
| <span data-ttu-id="5d204-119">*Length*</span><span class="sxs-lookup"><span data-stu-id="5d204-119">*Length*</span></span>  <br/> |<span data-ttu-id="5d204-120">Una expresión de número entero positivo que especifica cuántos caracteres de la expresión se devolverán.</span><span class="sxs-lookup"><span data-stu-id="5d204-120">A positive integer expression that specifies how many characters of the expression will be returned.</span></span> <span data-ttu-id="5d204-121">Si length es negativo, se genera un error y se termina la instrucción.</span><span class="sxs-lookup"><span data-stu-id="5d204-121">If length is negative, an error is generated and the statement is terminated.</span></span> <span data-ttu-id="5d204-122">Si la suma de start y length es mayor que el número de caracteres en expresión, se devuelve el principio de la expresión de valor todo en Inicio.</span><span class="sxs-lookup"><span data-stu-id="5d204-122">If the sum of start and length is greater than the number of characters in expression, the whole value expression beginning at start is returned.</span></span>  <br/> |
   

