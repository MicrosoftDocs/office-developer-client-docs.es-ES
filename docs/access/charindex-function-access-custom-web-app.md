---
title: Función CharIndex (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Las búsquedas que se encuentra una expresión de texto para otra expresión de texto y devuelve su inicio posición si.
ms.openlocfilehash: 86a46f57c64028530217326127eece887127c4c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815345"
---
# <a name="charindex-function-access-custom-web-app"></a><span data-ttu-id="3760a-103">Función CharIndex (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="3760a-103">CharIndex function (Access custom web app)</span></span>

<span data-ttu-id="3760a-104">Las búsquedas que se encuentra una expresión de texto para otra expresión de texto y devuelve su inicio posición si.</span><span class="sxs-lookup"><span data-stu-id="3760a-104">Searches a text expression for another text expression and returns its starting position if found.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="3760a-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="3760a-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3760a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3760a-107">Syntax</span></span>

<span data-ttu-id="3760a-108">**CharIndex** (*TextExpression*, *WithinText*, [*Iniciar*])</span><span class="sxs-lookup"><span data-stu-id="3760a-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span></span> 
  
|<span data-ttu-id="3760a-109">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="3760a-109">**Argument Name**</span></span>|<span data-ttu-id="3760a-110">**Necesario**</span><span class="sxs-lookup"><span data-stu-id="3760a-110">**Required**</span></span>|<span data-ttu-id="3760a-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3760a-111">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="3760a-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="3760a-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="3760a-113">Sí</span><span class="sxs-lookup"><span data-stu-id="3760a-113">Yes</span></span>  <br/> |<span data-ttu-id="3760a-114">Una expresión de texto que contiene el texto que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="3760a-114">A text expression that contains the text to be found.</span></span>  <br/> |
| <span data-ttu-id="3760a-115">*WithinText*</span><span class="sxs-lookup"><span data-stu-id="3760a-115">*WithinText*</span></span>  <br/> |<span data-ttu-id="3760a-116">Sí</span><span class="sxs-lookup"><span data-stu-id="3760a-116">Yes</span></span>  <br/> |<span data-ttu-id="3760a-117">La expresión de texto que se desea buscar.</span><span class="sxs-lookup"><span data-stu-id="3760a-117">The text expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="3760a-118">*Start*</span><span class="sxs-lookup"><span data-stu-id="3760a-118">*Start*</span></span>  <br/> |<span data-ttu-id="3760a-119">No</span><span class="sxs-lookup"><span data-stu-id="3760a-119">No</span></span>  <br/> |<span data-ttu-id="3760a-120">Un entero que especifica la ubicación en *WithinText* para iniciar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3760a-120">An integer that specifies the location in  *WithinText*  to begin the search.</span></span> <span data-ttu-id="3760a-121">Si *Iniciar* no se especifica, es un número negativo o es 0, la búsqueda comienza al principio de *WithinText* .</span><span class="sxs-lookup"><span data-stu-id="3760a-121">If  *Start*  is not specified, is a negative number, or is 0, the search starts at the beginning of  *WithinText*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3760a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3760a-122">Remarks</span></span>

<span data-ttu-id="3760a-123">Si *TextExpression* o *WithinText* es NULL, *CharIndex* devuelve NULL.</span><span class="sxs-lookup"><span data-stu-id="3760a-123">If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL.</span></span> 
  
<span data-ttu-id="3760a-124">Si no se encuentra *TextExpression* dentro de *WithinText*, *CharIndex* devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="3760a-124">If  *TextExpression*  is not found within  *WithinText*,  *CharIndex*  returns 0.</span></span> 
  
<span data-ttu-id="3760a-125">La posición inicial devuelta está basado en 1, no en 0.</span><span class="sxs-lookup"><span data-stu-id="3760a-125">The starting position returned is 1-based, not 0-based.</span></span>
  

