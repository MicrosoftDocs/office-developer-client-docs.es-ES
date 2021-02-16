---
title: Función CharIndex (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Busca otra expresión de texto en una expresión de texto y devuelve su posición inicial si se encuentra.
ms.openlocfilehash: dc6906f70bc5bb17e12855d69946281909962988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423135"
---
# <a name="charindex-function-access-custom-web-app"></a><span data-ttu-id="149f1-103">Función CharIndex (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="149f1-103">CharIndex function (Access custom web app)</span></span>

<span data-ttu-id="149f1-104">Busca otra expresión de texto en una expresión de texto y devuelve su posición inicial si se encuentra.</span><span class="sxs-lookup"><span data-stu-id="149f1-104">Searches a text expression for another text expression and returns its starting position if found.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="149f1-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="149f1-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="149f1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="149f1-107">Syntax</span></span>

<span data-ttu-id="149f1-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span><span class="sxs-lookup"><span data-stu-id="149f1-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span></span> 
  
|<span data-ttu-id="149f1-109">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="149f1-109">**Argument Name**</span></span>|<span data-ttu-id="149f1-110">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="149f1-110">**Required**</span></span>|<span data-ttu-id="149f1-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="149f1-111">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="149f1-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="149f1-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="149f1-113">Sí</span><span class="sxs-lookup"><span data-stu-id="149f1-113">Yes</span></span>  <br/> |<span data-ttu-id="149f1-114">Expresión de texto que contiene el texto que se va a encontrar.</span><span class="sxs-lookup"><span data-stu-id="149f1-114">A text expression that contains the text to be found.</span></span>  <br/> |
| <span data-ttu-id="149f1-115">*WithinText*</span><span class="sxs-lookup"><span data-stu-id="149f1-115">*WithinText*</span></span>  <br/> |<span data-ttu-id="149f1-116">Sí</span><span class="sxs-lookup"><span data-stu-id="149f1-116">Yes</span></span>  <br/> |<span data-ttu-id="149f1-117">Expresión de texto en la que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="149f1-117">The text expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="149f1-118">*Start*</span><span class="sxs-lookup"><span data-stu-id="149f1-118">*Start*</span></span>  <br/> |<span data-ttu-id="149f1-119">No</span><span class="sxs-lookup"><span data-stu-id="149f1-119">No</span></span>  <br/> |<span data-ttu-id="149f1-120">Entero que especifica la ubicación en  *WithinText*  para iniciar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="149f1-120">An integer that specifies the location in  *WithinText*  to begin the search.</span></span> <span data-ttu-id="149f1-121">Si  *no*  se especifica Start, es un número negativo o es 0, la búsqueda comienza al principio de  *WithinText*  .</span><span class="sxs-lookup"><span data-stu-id="149f1-121">If  *Start*  is not specified, is a negative number, or is 0, the search starts at the beginning of  *WithinText*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="149f1-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="149f1-122">Remarks</span></span>

<span data-ttu-id="149f1-123">Si  *TextExpression o*  *WithinText*  es NULL,  *CharIndex*  devuelve NULL.</span><span class="sxs-lookup"><span data-stu-id="149f1-123">If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL.</span></span> 
  
<span data-ttu-id="149f1-124">Si  *TextExpression*  no se encuentra en  *WithinText*,  *CharIndex*  devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="149f1-124">If  *TextExpression*  is not found within  *WithinText*,  *CharIndex*  returns 0.</span></span> 
  
<span data-ttu-id="149f1-125">La posición inicial devuelta está basada en 1, no en 0.</span><span class="sxs-lookup"><span data-stu-id="149f1-125">The starting position returned is 1-based, not 0-based.</span></span>
  

