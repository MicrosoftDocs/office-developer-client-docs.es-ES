---
title: Función SubString (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Devuelve parte de una expresión de texto.
ms.openlocfilehash: af93620905af366f41bcc50ab6102114acd3db9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433475"
---
# <a name="substring-function-access-custom-web-app"></a><span data-ttu-id="b6e0e-103">Función SubString (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-103">SubString Function (Access custom web app)</span></span>

<span data-ttu-id="b6e0e-104">Devuelve parte de una expresión de texto.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-104">Returns part of a text expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b6e0e-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b6e0e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6e0e-107">Syntax</span></span>

 <span data-ttu-id="b6e0e-108">**SubString** (*TextExpression*, *Start*, *Length*)</span><span class="sxs-lookup"><span data-stu-id="b6e0e-108">**SubString** (*TextExpression*, *Start*, *Length*)</span></span> 
  
<span data-ttu-id="b6e0e-109">La **función SubString** contiene los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-109">The **SubString** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="b6e0e-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-110">**Argument name**</span></span>|<span data-ttu-id="b6e0e-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b6e0e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b6e0e-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="b6e0e-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="b6e0e-113">Expresión de texto.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-113">A text expression.</span></span>  <br/> |
| <span data-ttu-id="b6e0e-114">*Start*</span><span class="sxs-lookup"><span data-stu-id="b6e0e-114">*Start*</span></span>  <br/> |<span data-ttu-id="b6e0e-115">Expresión de entero que especifica dónde comienzan los caracteres devueltos.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-115">An integer expression that specifies where the returned characters start.</span></span> <span data-ttu-id="b6e0e-116">Si start es menor que 1, la expresión devuelta empezará en el primer carácter especificado en expresión.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-116">If start is less than 1, the returned expression will begin at the first character that is specified in expression.</span></span> <span data-ttu-id="b6e0e-117">En este caso, el número de caracteres devueltos es el valor más grande de la suma de start + length- 1 o 0.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-117">In this case, the number of characters that are returned is the largest value of either the sum of start + length- 1 or 0.</span></span> <span data-ttu-id="b6e0e-118">Si start es mayor que el número de caracteres de la expresión de valor, se devuelve una expresión de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-118">If start is greater than the number of characters in the value expression, a zero-length expression is returned.</span></span>  <br/> |
| <span data-ttu-id="b6e0e-119">*Length*</span><span class="sxs-lookup"><span data-stu-id="b6e0e-119">*Length*</span></span>  <br/> |<span data-ttu-id="b6e0e-120">Expresión de entero positivo que especifica cuántos caracteres de la expresión se devolverán.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-120">A positive integer expression that specifies how many characters of the expression will be returned.</span></span> <span data-ttu-id="b6e0e-121">Si la longitud es negativa, se genera un error y se termina la instrucción.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-121">If length is negative, an error is generated and the statement is terminated.</span></span> <span data-ttu-id="b6e0e-122">Si la suma de inicio y longitud es mayor que el número de caracteres de expresión, se devuelve toda la expresión de valor que comienza al principio.</span><span class="sxs-lookup"><span data-stu-id="b6e0e-122">If the sum of start and length is greater than the number of characters in expression, the whole value expression beginning at start is returned.</span></span>  <br/> |
   

