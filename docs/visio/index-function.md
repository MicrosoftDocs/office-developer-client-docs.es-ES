---
title: INDEX (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251443
localization_priority: Normal
ms.assetid: cc46f91e-733f-e25a-17d2-19df8c8febd2
description: Devuelve la subcadena en el índice de ubicación de base cero en la lista delimitada por el delimitador. O bien, si el índice está fuera del intervalo, devuelve una cadena vacía o el token opcional proporcionado como el argumento valordeerror.
ms.openlocfilehash: 11362ed984a489682d57f007300e60de548ddf11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344733"
---
# <a name="index-function"></a><span data-ttu-id="95a81-104">Función INDEX</span><span class="sxs-lookup"><span data-stu-id="95a81-104">INDEX Function</span></span>

<span data-ttu-id="95a81-105">Devuelve la subcadena en el _Índice_ de ubicación de base cero en la _lista_ delimitada por el delimitador. __</span><span class="sxs-lookup"><span data-stu-id="95a81-105">Returns the substring at the zero-based location  _index_ in the  _list_ delimited by  _delimiter_.</span></span> <span data-ttu-id="95a81-106">O bien, si el índice está fuera del intervalo, devuelve una cadena vacía o el token opcional proporcionado como el argumento *valordeerror* .</span><span class="sxs-lookup"><span data-stu-id="95a81-106">Or, if the index is out of range, returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="95a81-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95a81-107">Syntax</span></span>

<span data-ttu-id="95a81-108">Índice (\* \* *Índice* \* *, "* \* *lista* \* *" [, [* \* \*\* delimitador \* *] [, [* \* *valordeerror* \* \*]]])</span><span class="sxs-lookup"><span data-stu-id="95a81-108">INDEX(\*\* *index* \*\*," \*\* *list* \*\* "[,[ \*\* *delimiter* \*\* ][,[ \*\* *errorvalue* \*\* ]]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="95a81-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95a81-109">Parameters</span></span>

|<span data-ttu-id="95a81-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="95a81-110">**Name**</span></span>|<span data-ttu-id="95a81-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="95a81-111">**Required/Optional**</span></span>|<span data-ttu-id="95a81-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="95a81-112">**Data Type**</span></span>|<span data-ttu-id="95a81-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95a81-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="95a81-114">_index_</span><span class="sxs-lookup"><span data-stu-id="95a81-114">_index_</span></span> <br/> |<span data-ttu-id="95a81-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="95a81-115">Required</span></span>  <br/> |<span data-ttu-id="95a81-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="95a81-116">**Number**</span></span> <br/> |<span data-ttu-id="95a81-117">Especifica la ubicación que desea buscar.</span><span class="sxs-lookup"><span data-stu-id="95a81-117">The location that you want to find.</span></span>  <br/> |
| <span data-ttu-id="95a81-118">_list_</span><span class="sxs-lookup"><span data-stu-id="95a81-118">_list_</span></span> <br/> |<span data-ttu-id="95a81-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="95a81-119">Required</span></span>  <br/> |<span data-ttu-id="95a81-120">**String**</span><span class="sxs-lookup"><span data-stu-id="95a81-120">**String**</span></span> <br/> |<span data-ttu-id="95a81-121">Lista en la que desea realizar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="95a81-121">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="95a81-122">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="95a81-122">_delimiter_</span></span> <br/> |<span data-ttu-id="95a81-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="95a81-123">Optional</span></span>  <br/> |<span data-ttu-id="95a81-124">**String**</span><span class="sxs-lookup"><span data-stu-id="95a81-124">**String**</span></span> <br/> | <span data-ttu-id="95a81-125">La cadena que se va a usar como delimitador de la _lista_.</span><span class="sxs-lookup"><span data-stu-id="95a81-125">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="95a81-126">Una __ cadena de delimitador puede tener más de un carácter de longitud e incluir caracteres de varios bytes.</span><span class="sxs-lookup"><span data-stu-id="95a81-126">A  _delimiter_ string can be more than one character in length and include multibyte characters.</span></span> <span data-ttu-id="95a81-127">El valor predeterminado es un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="95a81-127">The default is a semicolon.</span></span>  <br/> |
| <span data-ttu-id="95a81-128">_valordeerror_</span><span class="sxs-lookup"><span data-stu-id="95a81-128">_errorvalue_</span></span> <br/> |<span data-ttu-id="95a81-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="95a81-129">Optional</span></span>  <br/> |<span data-ttu-id="95a81-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="95a81-130">**Number**</span></span> <br/> | <span data-ttu-id="95a81-131">Valor especificado por el usuario que debe devolverse en el caso de que el índice no esté incluido en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="95a81-131">A user-specified value to return if the index is out of range.</span></span> <span data-ttu-id="95a81-132">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="95a81-132">The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95a81-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95a81-133">Remarks</span></span>

<span data-ttu-id="95a81-p105">Si la lista comienza o termina con un delimitador, se supone que existe una cadena nula antes o después de la misma. Dos delimitadores consecutivos indican que hay una cadena nula entre ellos.</span><span class="sxs-lookup"><span data-stu-id="95a81-p105">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="95a81-136">Si el índice está fuera del intervalo, Visio devuelve una cadena vacía o el token opcional proporcionado como el argumento *valordeerror* .</span><span class="sxs-lookup"><span data-stu-id="95a81-136">If the index is out of range, Visio returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="95a81-137">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="95a81-137">Example 1</span></span>

<span data-ttu-id="95a81-138">Índice (3, "gato; Rat;; caprino ")</span><span class="sxs-lookup"><span data-stu-id="95a81-138">INDEX(3,"cat;rat;;goat")</span></span>
  
<span data-ttu-id="95a81-139">Devuelve "cabra".</span><span class="sxs-lookup"><span data-stu-id="95a81-139">Returns "goat".</span></span>
  
## <a name="example-2"></a><span data-ttu-id="95a81-140">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="95a81-140">Example 2</span></span>

<span data-ttu-id="95a81-141">ÍNDICE (54, "; 1; 2; 3;";, "ERROR")</span><span class="sxs-lookup"><span data-stu-id="95a81-141">INDEX(54,";1;2;3;",,"ERROR")</span></span>
  
<span data-ttu-id="95a81-142">Devuelve "ERROR".</span><span class="sxs-lookup"><span data-stu-id="95a81-142">Returns "ERROR".</span></span>
  

