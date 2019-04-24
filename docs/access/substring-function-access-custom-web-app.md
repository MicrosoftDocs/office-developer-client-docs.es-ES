---
title: Función substring (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Devuelve parte de una expresión de texto.
ms.openlocfilehash: af93620905af366f41bcc50ab6102114acd3db9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301697"
---
# <a name="substring-function-access-custom-web-app"></a><span data-ttu-id="82b52-103">Función substring (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="82b52-103">SubString Function (Access custom web app)</span></span>

<span data-ttu-id="82b52-104">Devuelve parte de una expresión de texto.</span><span class="sxs-lookup"><span data-stu-id="82b52-104">Returns part of a text expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="82b52-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="82b52-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="82b52-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82b52-107">Syntax</span></span>

 <span data-ttu-id="82b52-108">**Subcadena** (*TextExpression*, *Inicio*, *longitud*)</span><span class="sxs-lookup"><span data-stu-id="82b52-108">**SubString** (*TextExpression*, *Start*, *Length*)</span></span> 
  
<span data-ttu-id="82b52-109">La \*\*\*\* función Substring contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="82b52-109">The **SubString** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="82b52-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="82b52-110">**Argument name**</span></span>|<span data-ttu-id="82b52-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="82b52-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="82b52-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="82b52-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="82b52-113">Una expresión de texto.</span><span class="sxs-lookup"><span data-stu-id="82b52-113">A text expression.</span></span>  <br/> |
| <span data-ttu-id="82b52-114">*Start*</span><span class="sxs-lookup"><span data-stu-id="82b52-114">*Start*</span></span>  <br/> |<span data-ttu-id="82b52-115">Expresión de tipo Integer que especifica dónde se inician los caracteres devueltos.</span><span class="sxs-lookup"><span data-stu-id="82b52-115">An integer expression that specifies where the returned characters start.</span></span> <span data-ttu-id="82b52-116">Si Start es menor que 1, la expresión que se devuelve comenzará en el primer carácter que se especifique en la expresión.</span><span class="sxs-lookup"><span data-stu-id="82b52-116">If start is less than 1, the returned expression will begin at the first character that is specified in expression.</span></span> <span data-ttu-id="82b52-117">En este caso, el número de caracteres que se devuelven es el mayor valor de la suma de Start + length-1 o 0.</span><span class="sxs-lookup"><span data-stu-id="82b52-117">In this case, the number of characters that are returned is the largest value of either the sum of start + length- 1 or 0.</span></span> <span data-ttu-id="82b52-118">Si Start es mayor que el número de caracteres de la expresión de valor, se devuelve una expresión de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="82b52-118">If start is greater than the number of characters in the value expression, a zero-length expression is returned.</span></span>  <br/> |
| <span data-ttu-id="82b52-119">*Length*</span><span class="sxs-lookup"><span data-stu-id="82b52-119">*Length*</span></span>  <br/> |<span data-ttu-id="82b52-120">Expresión de número entero positivo que especifica cuántos caracteres de la expresión se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="82b52-120">A positive integer expression that specifies how many characters of the expression will be returned.</span></span> <span data-ttu-id="82b52-121">Si length es negativo, se genera un error y se termina la instrucción.</span><span class="sxs-lookup"><span data-stu-id="82b52-121">If length is negative, an error is generated and the statement is terminated.</span></span> <span data-ttu-id="82b52-122">Si la suma de Start y length es mayor que el número de caracteres en la expresión, se devuelve la expresión de valor completa que comienza en Start.</span><span class="sxs-lookup"><span data-stu-id="82b52-122">If the sum of start and length is greater than the number of characters in expression, the whole value expression beginning at start is returned.</span></span>  <br/> |
   

